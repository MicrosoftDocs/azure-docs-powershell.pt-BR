---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 46e5e84b6718cc7a700ef2df4e82647e8cb60941
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856059"
---
# <a name="sign-in-with-azure-powershell"></a>Entrar com o Azure PowerShell

O Azure PowerShell dá suporte a vários métodos de autenticação. A maneira mais fácil de começar é com o [Azure Cloud Shell](/azure/cloud-shell/overview) que conecta você automaticamente. Em uma instalação local, você pode entrar interativamente com seu navegador. Ao escrever scripts para automação, a abordagem recomendada é usar uma [entidade de serviço](create-azure-service-principal-azureps.md) com as permissões necessárias. Ao restringir as permissões de logon o máximo possível para seu caso de uso, você ajuda a proteger os recursos do Azure.

Inicialmente, você está conectado à primeira assinatura que o Azure retorna se você tem acesso a mais de uma assinatura. Por padrão, os comandos são executados para essa assinatura. Para mudar sua assinatura ativa para uma sessão, use o cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext). Para alterar sua assinatura ativa e fazer com que ela persista entre as sessões no mesmo sistema, use o cmdlet [Select-AzContext](/powershell/module/az.accounts/select-azcontext).

> [!IMPORTANT]
> Suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado.
> Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).

## <a name="sign-in-interactively"></a>Entrar no modo interativo

Para entrar no modo interativo, use o cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

Do módulo do Az PowerShell versão 5.0.0 em diante, esse cmdlet apresenta um prompt de logon interativo baseado em navegador por padrão. Você pode especificar o parâmetro `UseDeviceAuthentication` para receber uma cadeia de caracteres de token que anteriormente era o padrão para o PowerShell versão 6 e superior.

> [!IMPORTANT]
> A autorização da credencial de nome de usuário/senha foi removida no Azure PowerShell devido a alterações nas implementações de autorização do Active Directory e questões de segurança. Caso você use autorização de credenciais para fins de automação, em vez disso, [crie uma entidade de serviço](create-azure-service-principal-azureps.md).

Use o cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext) para armazenar a sua ID de locatário em uma variável a ser usada nas próximas duas seções deste artigo.

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a>Entrar com uma entidade de serviço <a name="sp-signin"/>

Entidades de serviço são contas do Azure não interativas. Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory. Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.

Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).

Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzAccount`. Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço. A forma como você entra com uma entidade de serviço depende de se ela está configurada para autenticação baseada em certificado ou em senha.

### <a name="password-based-authentication"></a>Autenticação baseada em senha

Crie uma entidade de serviço a ser usada nos exemplos nesta seção. Para obter mais informações sobre como criar as entidades de serviço, confira [Criar uma entidade de serviço do Azure com o Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Esse cmdlet apresenta um prompt para um nome de usuário e uma senha. Use o `applicationID` da entidade de serviço para o nome de usuário e converta o `secret` em texto sem formatação para a senha.

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Para cenários de automação, você precisa criar as credenciais de `applicationId` e `secret` de uma entidade de serviço:

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Verifique se que você está usando boas práticas de armazenamento de senha ao automatizar as conexões de entidade de serviço.

### <a name="certificate-based-authentication"></a>Autenticação baseada em certificado

A autenticação baseada em certificado exige que o Azure PowerShell possa recuperar informações de um repositório de certificados local com base em uma impressão digital do certificado.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

Ao usar uma entidade de serviço em vez de um aplicativo registrado, adicione o argumento `-ServicePrincipal` e forneça a ID do aplicativo da entidade de serviço como o valor do parâmetro `-ApplicationId`.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

No PowerShell 5.1, o repositório de certificados pode ser gerenciado e inspecionado com o módulo [PKI](/powershell/module/pkiclient). Para o PowerShell Core 6.x e posterior, o processo é mais complicado. Os scripts a seguir mostram como importar um certificado existente no repositório de certificados acessível pelo PowerShell.

#### <a name="import-a-certificate-in-powershell-51"></a>Importar um certificado no PowerShell 5.1

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>Importar um certificado no PowerShell Core 6.x e posterior

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>Entrar usando uma identidade gerenciada

As identidades gerenciadas são um recurso do Azure Active Directory. Elas são entidades de serviço atribuídas aos recursos executados no Azure. Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos. As identidades gerenciadas só estão disponíveis nos recursos executados em uma nuvem do Azure.

Esse exemplo se conecta usando a identidade gerenciada do ambiente de host. Por exemplo, se executado em uma VirtualMachine com uma Identidade de Serviço Gerenciada atribuída, isso permitirá que o código entre usando essa identidade atribuída.

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Entrar com um locatário diferente do padrão ou como um Provedor de Soluções na Nuvem (CSP)

Se a sua conta está associada a mais de um locatário, é preciso que o parâmetro `-Tenant` seja especificado na conexão para entrar. Esse parâmetro funciona com qualquer método de conexão. Ao fazer logon, esse valor de parâmetro pode ser a ID de objeto do Azure do locatário (ID do Locatário) ou o nome de domínio totalmente qualificado do locatário.

Se você for um [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), o valor `-Tenant`**deverá** ser uma ID de locatário.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Entre em outra Nuvem

Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com as leis de manipulação de dados regionais. Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`. Esse parâmetro funciona com qualquer método de conexão. Por exemplo, se sua conta estiver em uma nuvem da China:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

O seguinte comando obtém uma lista de ambientes disponíveis:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
