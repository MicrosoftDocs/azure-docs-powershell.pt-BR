---
title: Fazer logon com o Azure PowerShell
description: Fazer logon com o Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 71a2554052f5a25ea86fe44b6dcf5d9343c81f3e
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "47424676"
---
# <a name="log-in-with-azure-powershell"></a>Fazer logon com o Azure PowerShell

O Azure PowerShell oferece suporte a vários métodos de logon. É a maneira mais simples para começar a fazer logon interativamente na linha de comando.

## <a name="interactive-log-in"></a>Logon Interativo

1. Digite `Login-AzureRmAccount`. Será exibida a caixa de diálogo solicitando as credenciais do Azure.

2. Digite o endereço de e-mail e a senha associada à sua conta. O Azure autentica e salva as informações de credenciais e, em seguida, fecha a janela.

## <a name="log-in-with-a-service-principal"></a>Fazer logon com uma entidade de serviço

As entidades de serviço oferecem uma maneira de criar contas não interativas para manipular recursos. As entidades de serviço são como as contas de usuário às quais você pode aplicar regras usando o Azure Active Directory. Ao conceder as permissões mínimas necessárias para uma entidade de serviço, você pode garantir que seus scripts de automação fiquem ainda mais seguros.

1. Se você ainda não tiver uma entidade de serviço, [crie uma](create-azure-service-principal-azureps.md).

2. Faça logon com uma entidade de serviço.

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    Para obter a TenantId, faça logon interativamente e obtenha a TenantId da sua assinatura.

    ```powershell
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a>Entrar usando identidades gerenciadas para recursos do Azure

Identidades gerenciadas para recursos do Azure é um recurso do Azure Active Directory. Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.

Para saber mais informações sobre identidades gerenciadas para recursos do Azure, consulte [Como usar identidades gerenciadas para recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="log-in-to-another-cloud"></a>Faça logon em outra Nuvem

Os Serviços de Nuvem do Azure oferecem ambientes diferentes que estão de acordo com as regulamentações de manipulação de dados de diversos governos. Caso sua conta do Azure esteja em uma das nuvens de governo, será necessário especificar o ambiente ao se conectar. Por exemplo, se sua conta está na nuvem da China, faça logon usando o seguinte comando:

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Use o seguinte comando para obter uma lista de ambientes disponíveis:

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Saiba mais sobre como gerenciar o acesso baseado em função do Azure

Para obter mais informações sobre o gerenciamento de autenticação e assinatura no Azure, consulte [Gerenciar contas, assinaturas e funções administrativas](/azure/active-directory/role-based-access-control-configure) (a página pode estar em inglês).

Cmdlets do Azure PowerShell para gerenciamento de função

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
