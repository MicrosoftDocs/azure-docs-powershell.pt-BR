---
title: Fazer logon com o Azure PowerShell
description: Fazer logon com o Azure PowerShell
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 1af5aeffb8e87e916df3e2440a84805935136c0f
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
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

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a>Faça logon usando uma identidade de serviço gerenciado do Azure VM

A Identidade do Serviço Gerenciado (MSI) é a versão prévia de um recurso para o Azure Active Directory. Você pode usar uma entidade de serviço do MSI para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.

Para obter mais informações sobre o MSI, consulte [Como usar uma Identidade de Serviço Gerenciado (MSI) da VM do Azure para conexão e aquisição de token](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="log-in-to-another-cloud"></a>Faça logon em outra Nuvem

Os Serviços de Nuvem do Azure oferecem ambientes diferentes que estão de acordo com as regulamentações de manipulação de dados de diversos governos. Caso sua conta do Azure esteja em uma das nuvens de governo, será necessário especificar o ambiente ao se conectar. Por exemplo, se sua conta está na nuvem da China, faça logon usando o seguinte comando:

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Use o seguinte comando para obter uma lista de ambientes disponíveis:

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
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
