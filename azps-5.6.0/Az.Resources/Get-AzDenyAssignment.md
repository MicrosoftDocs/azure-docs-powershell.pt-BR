---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: d54d6ff9ed26b76d3c36ab47cf04024dcdf11281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885967"
---
# <span data-ttu-id="e906e-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="e906e-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="e906e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e906e-102">SYNOPSIS</span></span>
<span data-ttu-id="e906e-103">Listas O Azure RBAC nega atribuições no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="e906e-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="e906e-104">Por padrão, lista todas as atribuições de negação na assinatura selecionada do Azure.</span><span class="sxs-lookup"><span data-stu-id="e906e-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="e906e-105">Use os parâmetros respectivos para listar atribuições de negação a um usuário específico ou listar atribuições de negação em um grupo de recursos ou recurso específico.</span><span class="sxs-lookup"><span data-stu-id="e906e-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="e906e-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e906e-106">SYNTAX</span></span>

### <span data-ttu-id="e906e-107">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e906e-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e906e-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e906e-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e906e-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e906e-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e906e-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e906e-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e906e-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e906e-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e906e-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e906e-125">DESCRIPTION</span></span>
<span data-ttu-id="e906e-126">Use o Get-AzDenyAssignment para listar todas as atribuições de negação que são efetivas em um escopo.</span><span class="sxs-lookup"><span data-stu-id="e906e-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="e906e-127">Sem parâmetros, esse comando retorna todas as atribuições de negação feitas sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e906e-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="e906e-128">Essa lista pode ser filtrada usando parâmetros de filtragem para entidade principal, negar nome e escopo de atribuição.</span><span class="sxs-lookup"><span data-stu-id="e906e-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="e906e-129">Para especificar um usuário, use os parâmetros SignInName ou ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e906e-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="e906e-130">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e906e-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="e906e-131">E para especificar um aplicativo do Azure AD, use parâmetros ServicePrincipalName ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e906e-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="e906e-132">O escopo no qual o acesso está sendo negado pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e906e-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="e906e-133">Ele é padrão para a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="e906e-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="e906e-134">O escopo da atribuição de negação pode ser especificado usando uma das seguintes combinações de parâmetros a.</span><span class="sxs-lookup"><span data-stu-id="e906e-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="e906e-135">Escopo - Este é o escopo totalmente qualificado começando com /subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="e906e-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="e906e-136">Isso filtrará as atribuições de negação que são efetivas nesse escopo específico, ou seja, todas negam atribuições nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="e906e-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="e906e-137">b.</span><span class="sxs-lookup"><span data-stu-id="e906e-137">b.</span></span>
<span data-ttu-id="e906e-138">ResourceGroupName - Nome de qualquer grupo de recursos sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e906e-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="e906e-139">Isso filtrará as atribuições efetivas no grupo de recursos especificado, ou seja, todas negam atribuições nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="e906e-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="e906e-140">c.</span><span class="sxs-lookup"><span data-stu-id="e906e-140">c.</span></span>
<span data-ttu-id="e906e-141">ResourceName, ResourceType, ResourceGroupName e (opcionalmente) ParentResource - Identifica um determinado recurso sob a assinatura e filtrará as atribuições de negação efetivas nesse escopo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e906e-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="e906e-142">Para determinar qual acesso é negado para um determinado usuário na assinatura, use a opção ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="e906e-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="e906e-143">Isso lista todas as atribuições de negação atribuídas ao usuário e aos grupos dos que o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="e906e-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="e906e-144">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e906e-144">EXAMPLES</span></span>

### <span data-ttu-id="e906e-145">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e906e-145">Example 1</span></span>

<span data-ttu-id="e906e-146">Listar todas as atribuições de negação na assinatura</span><span class="sxs-lookup"><span data-stu-id="e906e-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="e906e-147">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e906e-147">Example 2</span></span>

<span data-ttu-id="e906e-148">Obtém todas as atribuições de negação feitas ao john.doe@contoso.com usuário no testRG de escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="e906e-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="e906e-149">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e906e-149">Example 3</span></span>

<span data-ttu-id="e906e-150">Obtém todas as atribuições de negação da entidade de serviço especificada</span><span class="sxs-lookup"><span data-stu-id="e906e-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="e906e-151">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e906e-151">Example 4</span></span>

<span data-ttu-id="e906e-152">Obtém atribuições de negação no escopo do site 'site1'.</span><span class="sxs-lookup"><span data-stu-id="e906e-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="e906e-153">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e906e-153">PARAMETERS</span></span>

### <span data-ttu-id="e906e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e906e-154">-DefaultProfile</span></span>
<span data-ttu-id="e906e-155">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e906e-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e906e-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e906e-156">-DenyAssignmentName</span></span>
<span data-ttu-id="e906e-157">Nome da atribuição de negação.</span><span class="sxs-lookup"><span data-stu-id="e906e-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e906e-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="e906e-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="e906e-159">Se especificado, retorna nega atribuições atribuídas diretamente ao usuário e aos grupos dos quais o usuário é membro (transitivamente).</span><span class="sxs-lookup"><span data-stu-id="e906e-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="e906e-160">Suportado apenas para uma entidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="e906e-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="e906e-161">-Id</span><span class="sxs-lookup"><span data-stu-id="e906e-161">-Id</span></span>
<span data-ttu-id="e906e-162">Negar id de atribuição.</span><span class="sxs-lookup"><span data-stu-id="e906e-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e906e-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e906e-163">-ObjectId</span></span>
<span data-ttu-id="e906e-164">ObjectId do Azure AD da Entidade de Usuário, Grupo ou Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="e906e-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="e906e-165">Filtra todas as atribuições negadas feitas à entidade especificada.</span><span class="sxs-lookup"><span data-stu-id="e906e-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e906e-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="e906e-166">-ParentResource</span></span>
<span data-ttu-id="e906e-167">O recurso pai na hierarquia do recurso especificado usando o parâmetro ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e906e-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="e906e-168">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e906e-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="e906e-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e906e-169">-ResourceGroupName</span></span>
<span data-ttu-id="e906e-170">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e906e-170">The resource group name.</span></span>
<span data-ttu-id="e906e-171">As listas negam atribuições que são efetivas no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e906e-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="e906e-172">Quando usado em conjunto com parâmetros ResourceName, ResourceType e ParentResource, as listas de comandos negam atribuições efetivas em recursos dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e906e-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="e906e-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e906e-173">-ResourceName</span></span>
<span data-ttu-id="e906e-174">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e906e-174">The resource name.</span></span>
<span data-ttu-id="e906e-175">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="e906e-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="e906e-176">Deve ser usado em conjunto com os parâmetros ResourceGroupName, ResourceType e (opcionalmente)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="e906e-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e906e-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e906e-177">-ResourceType</span></span>
<span data-ttu-id="e906e-178">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e906e-178">The resource type.</span></span>
<span data-ttu-id="e906e-179">Por exemplo, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="e906e-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="e906e-180">Deve ser usado em conjunto com os parâmetros ResourceGroupName, ResourceName e (opcionalmente)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="e906e-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e906e-181">-Scope</span><span class="sxs-lookup"><span data-stu-id="e906e-181">-Scope</span></span>
<span data-ttu-id="e906e-182">O Escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="e906e-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="e906e-183">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="e906e-183">In the format of relative URI.</span></span>
<span data-ttu-id="e906e-184">Por exemplo, /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="e906e-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="e906e-185">Ele deve começar com "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="e906e-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="e906e-186">O comando filtra todas as atribuições negadas que são efetivas nesse escopo.</span><span class="sxs-lookup"><span data-stu-id="e906e-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="e906e-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e906e-187">-ServicePrincipalName</span></span>
<span data-ttu-id="e906e-188">ServicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e906e-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="e906e-189">Filtra todas as atribuições negadas feitas ao aplicativo Azure AD especificado.</span><span class="sxs-lookup"><span data-stu-id="e906e-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="e906e-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e906e-190">-SignInName</span></span>
<span data-ttu-id="e906e-191">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="e906e-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="e906e-192">Filtra todas as atribuições negadas feitas ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="e906e-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="e906e-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e906e-193">CommonParameters</span></span>
<span data-ttu-id="e906e-194">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e906e-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e906e-195">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e906e-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e906e-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e906e-196">INPUTS</span></span>

### <span data-ttu-id="e906e-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e906e-197">System.Guid</span></span>

### <span data-ttu-id="e906e-198">System.String</span><span class="sxs-lookup"><span data-stu-id="e906e-198">System.String</span></span>

## <span data-ttu-id="e906e-199">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e906e-199">OUTPUTS</span></span>

### <span data-ttu-id="e906e-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="e906e-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="e906e-201">NOTES</span><span class="sxs-lookup"><span data-stu-id="e906e-201">NOTES</span></span>
<span data-ttu-id="e906e-202">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="e906e-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e906e-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e906e-203">RELATED LINKS</span></span>
