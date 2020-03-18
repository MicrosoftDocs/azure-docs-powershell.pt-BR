---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.openlocfilehash: 0de487cc34593ceac05aa2077358d692470dc23e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402741"
---
# <a name="sign-in-with-azure-powershell"></a>Entrar com o Azure PowerShell

O Azure PowerShell dá suporte a vários métodos de autenticação. A maneira mais fácil de começar é com o [Azure Cloud Shell](/azure/cloud-shell/overview) que conecta você automaticamente. Em uma instalação local, você pode entrar interativamente com seu navegador. Ao escrever scripts para automação, a abordagem recomendada é usar uma [entidade de serviço](create-azure-service-principal-azureps.md) com as permissões necessárias. Ao restringir as permissões de logon o máximo possível para seu caso de uso, você ajuda a proteger os recursos do Azure.

Após a conexão, os comandos são executados em sua assinatura padrão. Para mudar sua assinatura ativa para uma sessão, use o cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext). Para mudar a assinatura padrão usada ao fazer logon no Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).

> [!IMPORTANT]
>
> Suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado.
> Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).

## <a name="sign-in-interactively"></a>Entrar no modo interativo

Para entrar no modo interativo, use o cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

Quando executado, esse cmdlet apresentará uma cadeia de caracteres de token. Para fazer logon, copie essa cadeia de caracteres e cole-a em https://microsoft.com/devicelogin no navegador. Sua sessão do PowerShell será autenticada para conectar o Azure.

> [!IMPORTANT]
>
> A autorização da credencial de nome de usuário/senha foi removida no Azure PowerShell devido a alterações nas implementações de autorização do Active Directory e questões de segurança.
> Caso você use autorização de credenciais para fins de automação, em vez disso, [crie uma entidade de serviço](create-azure-service-principal-azureps.md).

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a>Entrar com uma entidade de serviço <a name="sp-signin"/>

Entidades de serviço são contas do Azure não interativas. Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory. Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.

Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).

Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzAccount`. Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço. A forma como você entra com uma entidade de serviço dependerá de se ela está configurada para autenticação baseada em certificado ou em senha.

### <a name="password-based-authentication"></a>Autenticação baseada em senha

Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Esse cmdlet apresentará um prompt para nome de usuário e senha. Use a ID da entidade de serviço para o nome de usuário.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Para cenários de automação, você precisa criar as credenciais usando um nome de usuário e uma cadeia de caracteres segura:

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
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

Esse comando se conecta usando a identidade gerenciada do ambiente de host. Por exemplo, se executado em uma VirtualMachine com uma Identidade de Serviço Gerenciada atribuída, isso permitirá que o código entre usando essa identidade atribuída.

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Entrar com um locatário diferente do padrão ou como um Provedor de Soluções na Nuvem (CSP)

Se sua conta estiver associada a mais de um locatário, entrar requer o uso do parâmetro `-Tenant` na conexão. Esse parâmetro funcionará com qualquer método de entrada. Ao fazer logon, esse valor de parâmetro pode ser a ID de objeto do Azure do locatário (ID do Locatário) ou o nome de domínio totalmente qualificado do locatário.

Se você for um [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), o valor `-Tenant`**deverá** ser uma ID de locatário.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Entre em outra Nuvem

Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com as leis de manipulação de dados regionais.
Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.
Esse parâmetro funcionará com qualquer método de entrada. Por exemplo, se sua conta estiver em uma nuvem da China:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

O seguinte comando obtém uma lista de ambientes disponíveis:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
