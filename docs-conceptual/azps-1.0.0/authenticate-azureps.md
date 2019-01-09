---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786672"
---
# <a name="sign-in-with-azure-powershell"></a>Entrar com o Azure PowerShell

O Azure PowerShell dá suporte a vários métodos de autenticação. É a maneira mais simples para entrar interativamente na linha de comando.

## <a name="sign-in-interactively"></a>Entrar no modo interativo

Para entrar no modo interativo, use o cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

Quando executado, esse cmdlet apresentará uma cadeia de caracteres de token. Para fazer logon, copie essa cadeia de caracteres e cole-a na https://microsoft.com/devicelogin em um navegador. Sua sessão do PowerShell, em seguida, será autenticada para se conectar ao Azure. Essa autenticação dura o tempo da sessão atual do PowerShell.

> [!IMPORTANT]
>
> Suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado.
> Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Entrar com uma entidade de serviço

Entidades de serviço são contas do Azure não interativas. Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory. Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.

Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).

Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzAccount`. Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço. Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Esse cmdlet apresentará um prompt para a ID de usuário e a senha da entidade de serviço.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Entre usando uma Identidade de Serviço Gerenciada do Azure

Identidades gerenciadas para recursos do Azure é um recurso do Azure Active Directory. Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos. As identidades gerenciadas só estão disponíveis em máquinas virtuais em execução em uma nuvem do Azure.

Para saber mais informações sobre identidades gerenciadas para recursos do Azure, consulte [Como usar identidades gerenciadas para recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Entrar como um Provedor de Soluções na Nuvem (CSP)

Entrar no [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) requer o uso de `-TenantId`. Normalmente, esse parâmetro pode ser fornecido como uma ID de locatário ou nome de domínio. No entanto, para entrar no CSP, deve ser fornecido uma **ID de locatário**.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Entre em outra Nuvem

Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com os regulamentos de manipulação de dados regionais.
Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.
Por exemplo, se sua conta estiver em uma nuvem da China:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

O seguinte comando obtém uma lista de ambientes disponíveis:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Saiba mais sobre como gerenciar o acesso baseado em função do Azure

Para obter mais informações sobre o gerenciamento de autenticação e assinatura no Azure, consulte [Gerenciar contas, assinaturas e funções administrativas](/azure/active-directory/role-based-access-control-configure) (a página pode estar em inglês).

Cmdlets do Azure PowerShell para gerenciamento de função:

* [Get-AzRoleAssignment](/powershell/module/az.Resources/Get-azRoleAssignment)
* [Get-AzRoleDefinition](/powershell/module/az.Resources/Get-azRoleDefinition)
* [New-AzRoleAssignment](/powershell/module/az.Resources/New-azRoleAssignment)
* [New-AzRoleDefinition](/powershell/module/az.Resources/New-azRoleDefinition)
* [Remove-AzRoleAssignment](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [Remove-AzRoleDefinition](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.Resources/Set-azRoleDefinition)
