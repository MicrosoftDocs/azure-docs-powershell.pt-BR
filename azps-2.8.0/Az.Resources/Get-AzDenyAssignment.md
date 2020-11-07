---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 745df057c7c111bdca7cc30ac0864e15905ffd6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772604"
---
# <span data-ttu-id="0dc4d-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="0dc4d-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="0dc4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc4d-103">Lista as atribuições de negação do Azure RBAC no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="0dc4d-104">Por padrão, ele lista todas as atribuições de negação na assinatura do Azure selecionada.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="0dc4d-105">Use os parâmetros respectivos para listar as atribuições para um usuário específico ou para listar as atribuições em um recurso ou grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="0dc4d-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dc4d-106">SYNTAX</span></span>

### <span data-ttu-id="0dc4d-107">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0dc4d-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-108">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-108">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-109">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-109">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment -DenyAssignmentName <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-110">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-110">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-111">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-111">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-112">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-112">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-113">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-113">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-114">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-114">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-115">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-115">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-116">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-116">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-117">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-117">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-118">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-118">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-119">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-119">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-120">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-120">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-121">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-121">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-122">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-122">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-123">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-123">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4d-124">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc4d-124">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dc4d-125">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dc4d-125">DESCRIPTION</span></span>
<span data-ttu-id="0dc4d-126">Use o comando Get-AzDenyAssignment para listar todas as atribuições de negação que são efetivas em um escopo.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="0dc4d-127">Sem parâmetros, esse comando retorna todas as atribuições Deny feitas sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="0dc4d-128">Essa lista pode ser filtrada usando parâmetros de filtragem para a entidade de segurança, negar o nome e o escopo da atribuição.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="0dc4d-129">Para especificar um usuário, use SignInName ou os parâmetros do ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="0dc4d-130">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="0dc4d-131">E para especificar um aplicativo do Azure AD, use os parâmetros servicePrincipalName ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="0dc4d-132">O escopo no qual o acesso é negado pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="0dc4d-133">O padrão é a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="0dc4d-134">O escopo da atribuição Deny pode ser especificado usando-se uma das combinações de parâmetro a seguir.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="0dc4d-135">Scope-este é o escopo totalmente qualificado começando com/subscriptions/ \< SubscriptionId \> .</span><span class="sxs-lookup"><span data-stu-id="0dc4d-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="0dc4d-136">Isso filtrará as atribuições de negação que são efetivas nesse escopo específico, ou seja, todas as atribuições de negação nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="0dc4d-137">b.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-137">b.</span></span>
<span data-ttu-id="0dc4d-138">ResourceGroupName-nome de qualquer grupo de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="0dc4d-139">Isso filtrará as tarefas de forma eficaz no grupo de recursos especificado, ou seja, todas as atribuições de negação nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="0dc4d-140">partição.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-140">c.</span></span>
<span data-ttu-id="0dc4d-141">ResourceFile, ResourceType, ResourceGroupName e (opcionalmente) ParentResource-identifica um recurso específico na assinatura e filtra as atribuições de negação efetivas nesse escopo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="0dc4d-142">Para determinar o que o acesso é negado para um usuário específico na assinatura, use a opção ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="0dc4d-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="0dc4d-143">Isso listará todas as atribuições de negação atribuídas ao usuário e os grupos dos quais o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="0dc4d-144">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dc4d-144">EXAMPLES</span></span>

### <span data-ttu-id="0dc4d-145">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0dc4d-145">Example 1</span></span>

<span data-ttu-id="0dc4d-146">Listar todas as atribuições negadas na assinatura</span><span class="sxs-lookup"><span data-stu-id="0dc4d-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="0dc4d-147">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0dc4d-147">Example 2</span></span>

<span data-ttu-id="0dc4d-148">Obtém todas as atribuições Deny feitas ao usuário john.doe@contoso.com no escopo testRG e versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="0dc4d-149">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0dc4d-149">Example 3</span></span>

<span data-ttu-id="0dc4d-150">Obtém todas as atribuições de negação da entidade de serviço especificada</span><span class="sxs-lookup"><span data-stu-id="0dc4d-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="0dc4d-151">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="0dc4d-151">Example 4</span></span>

<span data-ttu-id="0dc4d-152">Obtém as atribuições de negação no escopo do site "site1".</span><span class="sxs-lookup"><span data-stu-id="0dc4d-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

```

## <span data-ttu-id="0dc4d-153">OS</span><span class="sxs-lookup"><span data-stu-id="0dc4d-153">PARAMETERS</span></span>

### <span data-ttu-id="0dc4d-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc4d-154">-DefaultProfile</span></span>
<span data-ttu-id="0dc4d-155">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0dc4d-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-156">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="0dc4d-156">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="0dc4d-157">Se especificado, retorna a negação de atribuições diretamente atribuídas ao usuário e para os grupos dos quais o usuário é membro (transitivamente).</span><span class="sxs-lookup"><span data-stu-id="0dc4d-157">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="0dc4d-158">Com suporte somente para um usuário principal.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-158">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0dc4d-159">-ObjectId</span></span>
<span data-ttu-id="0dc4d-160">O ObjectId do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-160">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="0dc4d-161">Filtra todas as atribuições Deny feitas à entidade de segurança especificada.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-161">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-162">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="0dc4d-162">-ParentResource</span></span>
<span data-ttu-id="0dc4d-163">O recurso pai na hierarquia do recurso especificado usando o parâmetro ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-163">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="0dc4d-164">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e resourceName.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-164">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc4d-165">-ResourceGroupName</span></span>
<span data-ttu-id="0dc4d-166">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-166">The resource group name.</span></span>
<span data-ttu-id="0dc4d-167">Lista negar atribuições que sejam efetivas no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-167">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="0dc4d-168">Quando usado em conjunto com parâmetros ResourceFile, ResourceType e ParentResource, o comando lista negar atribuições efetivas em recursos dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-168">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-169">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0dc4d-169">-ResourceName</span></span>
<span data-ttu-id="0dc4d-170">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-170">The resource name.</span></span>
<span data-ttu-id="0dc4d-171">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-171">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="0dc4d-172">Deve ser usado em conjunto com ResourceGroupName, ResourceType e (opcionalmente) parâmetros ParentResource.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-172">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-173">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0dc4d-173">-ResourceType</span></span>
<span data-ttu-id="0dc4d-174">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-174">The resource type.</span></span>
<span data-ttu-id="0dc4d-175">Por exemplo, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-175">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="0dc4d-176">Deve ser usado em conjunto com ResourceGroupName, Resource Resources e (opcionalmente) parâmetros ParentResource.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-176">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-177">-Escopo</span><span class="sxs-lookup"><span data-stu-id="0dc4d-177">-Scope</span></span>
<span data-ttu-id="0dc4d-178">O escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-178">The Scope of the role assignment.</span></span>
<span data-ttu-id="0dc4d-179">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-179">In the format of relative URI.</span></span>
<span data-ttu-id="0dc4d-180">Por exemplo,/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-180">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="0dc4d-181">Ele deve começar com "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="0dc4d-181">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="0dc4d-182">O comando filtra todas as atribuições Deny que são efetivas nesse escopo.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-182">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-183">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="0dc4d-183">-ServicePrincipalName</span></span>
<span data-ttu-id="0dc4d-184">O servicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-184">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="0dc4d-185">Filtra todas as atribuições negadas feitas ao aplicativo do Azure AD especificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-185">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0dc4d-186">-SignInName</span></span>
<span data-ttu-id="0dc4d-187">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-187">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="0dc4d-188">Filtra todas as atribuições Deny feitas ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-188">Filters all deny assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc4d-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc4d-189">CommonParameters</span></span>
<span data-ttu-id="0dc4d-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc4d-191">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc4d-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc4d-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dc4d-192">INPUTS</span></span>

### <span data-ttu-id="0dc4d-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0dc4d-193">System.Guid</span></span>

### <span data-ttu-id="0dc4d-194">System. String</span><span class="sxs-lookup"><span data-stu-id="0dc4d-194">System.String</span></span>

## <span data-ttu-id="0dc4d-195">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dc4d-195">OUTPUTS</span></span>

### <span data-ttu-id="0dc4d-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="0dc4d-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="0dc4d-197">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dc4d-197">NOTES</span></span>
<span data-ttu-id="0dc4d-198">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="0dc4d-198">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>