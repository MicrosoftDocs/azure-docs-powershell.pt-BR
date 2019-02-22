---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56144049"
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

## <a name="sign-in-with-credentials"></a>Entrar com credenciais

Você também pode entrar com um objeto `PSCredential` autorizado para conectar-se ao Azure.
A maneira mais fácil de obter um objeto de credencial é com o cmdlet [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential). Quando executado, esse cmdlet solicitará um par de credenciais com o nome de usuário/senha.

> [!Note]
> Essa abordagem não funciona com contas da Microsoft ou contas que tenham a autenticação de dois fatores habilitada.

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a>Entrar com uma entidade de serviço

Entidades de serviço são contas do Azure não interativas. Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory. Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.

Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).

Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzAccount`. Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço. Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Esse cmdlet apresentará um prompt para a ID de usuário e a senha da entidade de serviço.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a>Entrar usando uma identidade gerenciada 

As identidades gerenciadas são um recurso do Azure Active Directory. Elas são entidades de serviço atribuídas aos recursos executados no Azure. Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos. As identidades gerenciadas só estão disponíveis nos recursos executados em uma nuvem do Azure.

Para saber mais sobre as identidades gerenciadas dos recursos do Azure, confira [Como usar identidades gerenciadas dos recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Entrar com um locatário diferente do padrão ou como um Provedor de Soluções na Nuvem (CSP)

Se sua conta estiver associada a mais de um locatário, entrar requer o uso do parâmetro `-TenantId` na conexão. Esse parâmetro funcionará com qualquer outro método de entrada. Ao fazer logon, esse valor de parâmetro pode ser a ID de objeto do Azure do locatário (ID do Locatário) ou o nome de domínio totalmente qualificado do locatário.

Se você for um [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), o valor `-TenantId` **deverá** ser uma ID de locatário.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Entre em outra Nuvem

Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com as leis de manipulação de dados regionais.
Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.
Por exemplo, se sua conta estiver em uma nuvem da China:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

O seguinte comando obtém uma lista de ambientes disponíveis:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```