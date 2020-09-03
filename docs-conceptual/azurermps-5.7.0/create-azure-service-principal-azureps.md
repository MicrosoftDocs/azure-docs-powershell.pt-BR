---
title: Criar uma entidade de serviço do Azure com o Azure PowerShell
description: Saiba como criar uma entidade de serviço para seu aplicativo ou serviço com o Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 38b12e70a8a1edcd18d278e95bef880be0400b4b
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243796"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Criar uma entidade de serviço do Azure com o Azure PowerShell

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Se você planeja gerenciar seu aplicativo ou serviço com o Azure PowerShell, execute-o em uma entidade de serviço do Azure Active Directory (AAD), em vez de suas próprias credenciais. Este tópico orienta você pela criação de uma entidade de segurança com o Azure PowerShell.

> [!NOTE]
> Você também pode criar uma entidade de serviço por meio do Portal do Azure. Leia [Usar o portal para criar um aplicativo e entidade de serviço do Active Directory que pode acessar recursos](/azure/azure-resource-manager/resource-group-create-service-principal-portal) para obter mais detalhes.

## <a name="what-is-a-service-principal"></a>O que é uma ‘entidade de serviço’?

Uma entidade de serviço do Azure é uma identidade de segurança usada por aplicativos criados pelo usuário, serviços e ferramentas de automação para acessar recursos específicos do Azure. Pense nela como uma “identidade de usuário” (nome de usuário e senha ou certificado) com uma função específica e permissões rigidamente controladas. Ela só precisa ser capaz de fazer coisas específicas, ao contrário de uma identidade de usuário geral. A segurança aumenta se você só conceder a ela o nível mínimo de permissões necessárias para realizar suas tarefas de gerenciamento.

## <a name="verify-your-own-permission-level"></a>Verificar seu próprio nível de permissão

Primeiro, você deve ter permissões suficientes no Azure Active Directory e em sua assinatura do Azure. Especificamente, você deve ser capaz de criar um aplicativo no Active Directory e atribuir uma função à entidade de serviço.

A maneira mais fácil de verificar se a sua conta tem as permissões adequadas é por meio do portal. Consulte [Verificar permissão necessária no portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Criar uma entidade de serviço para seu aplicativo

Depois de fazer logon em sua conta do Azure, é possível criar a entidade de serviço. Você deve ter uma das maneiras a seguir para identificar seu aplicativo implantado:

* O nome exclusivo do seu aplicativo implantado, como "MyDemoWebApp" nos exemplos a seguir ou
* A ID do Aplicativo, o GUID exclusivo associado ao seu aplicativo, serviço ou objeto implantado

### <a name="get-information-about-your-application"></a>Obter informações sobre seu aplicativo

O cmdlet `Get-AzureRmADApplication` pode ser usado para descobrir informações sobre seu aplicativo.

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Criar uma entidade de serviço para seu aplicativo

O cmdlet `New-AzureRmADServicePrincipal` é usado para criar a entidade de serviço.

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>Obter informações sobre a entidade de serviço

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>Entrar usando a entidade de serviço

Agora você pode entrar como a nova entidade de serviço para seu aplicativo usando a *appId* e a *senha* fornecidas. Você precisa fornecer a Id do Locatário para sua conta. Sua Id do Locatário é exibida quando você entra no Azure com suas credenciais pessoais.

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Execute este comando de uma nova sessão do PowerShell. Após uma entrada bem-sucedida, você verá uma saída semelhante a esta:

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Parabéns! Você pode usar essas credenciais para executar seu aplicativo. Em seguida, será necessário ajustar as permissões da entidade de serviço.

## <a name="managing-roles"></a>Gerenciamento de funções

> [!NOTE]
> O RBAC (Controle de Acesso do Azure Baseado em Função) é um modelo para definir e gerenciar funções para entidades de usuário e de serviço. As funções têm conjuntos de permissões associados a elas, que determinam os recursos que uma entidade pode ler, acessar, gravar ou gerenciar. Para saber mais sobre RBAC e funções, veja [RBAC: funções internas](/azure/active-directory/role-based-access-built-in-roles).

O Azure PowerShell fornece os seguintes cmdlets para gerenciar atribuições de função:

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

A função padrão para uma entidade de serviço é **Colaborador**. Pode não ser a melhor opção, dependendo do escopo das interações do seu aplicativo com os serviços do Azure, dadas suas permissões amplas.
A função **Leitor** é mais restritiva e pode ser uma boa opção para aplicativos somente leitura. Você pode exibir detalhes sobre as permissões específicas de função ou criar conectores personalizados por meio do portal do Azure.

Neste exemplo, adicionamos a função **Leitor** ao nosso exemplo anterior e excluímos a função **Colaborador**:

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Para exibir as funções atuais atribuídas:

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Outros cmdlets do Azure PowerShell para gerenciamento de funções:

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Alterar as credenciais da entidade de segurança

É uma boa prática de segurança examinar as permissões e atualizar a senha regularmente. Talvez você queira gerenciar e modificar as credenciais de segurança à medida que seu aplicativo muda. Por exemplo, podemos alterar a senha da entidade de serviço criando uma nova senha e removendo a antiga.

### <a name="add-a-new-password-for-the-service-principal"></a>Adicionar uma nova senha para a entidade de serviço

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Obter uma lista de credenciais para a entidade de serviço

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Remover a senha antiga da entidade de serviço

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Verificar a lista de credenciais para a entidade de serviço

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
