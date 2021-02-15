---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111429"
---
# <span data-ttu-id="e2b42-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="e2b42-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="e2b42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2b42-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b42-103">Listas em que o Azure RBAC nega atribuições no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="e2b42-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="e2b42-104">Por padrão, lista todas as atribuições de negação na assinatura selecionada do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2b42-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="e2b42-105">Use os parâmetros respectivos para listar negar atribuições a um usuário específico ou para listar negar atribuições em um grupo ou recurso de recursos específicos.</span><span class="sxs-lookup"><span data-stu-id="e2b42-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="e2b42-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2b42-106">SYNTAX</span></span>

### <span data-ttu-id="e2b42-107">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e2b42-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b42-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b42-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b42-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b42-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b42-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b42-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b42-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b42-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2b42-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2b42-125">DESCRIPTION</span></span>
<span data-ttu-id="e2b42-126">Use o comando Get-AzDenyAssignment para listar todas as atribuições negadas que são eficazes em um escopo.</span><span class="sxs-lookup"><span data-stu-id="e2b42-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="e2b42-127">Sem parâmetros, esse comando retorna todas as atribuições de negação feitas sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b42-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="e2b42-128">Essa lista pode ser filtrada usando parâmetros de filtragem de entidade, negar nome e escopo da atribuição.</span><span class="sxs-lookup"><span data-stu-id="e2b42-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="e2b42-129">Para especificar um usuário, use os parâmetros SignInName ou Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e2b42-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="e2b42-130">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e2b42-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="e2b42-131">E para especificar um aplicativo Azure AD, use parâmetros ServicePrincipalName ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e2b42-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="e2b42-132">O escopo no qual o acesso está sendo negado pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e2b42-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="e2b42-133">Ele é padrão para a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="e2b42-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="e2b42-134">O escopo da atribuição de negação pode ser especificado usando uma das seguintes combinações de parâmetros a.</span><span class="sxs-lookup"><span data-stu-id="e2b42-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="e2b42-135">Escopo – este é o escopo totalmente qualificado, começando com /subscriptions/. \<subscriptionId\></span><span class="sxs-lookup"><span data-stu-id="e2b42-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="e2b42-136">Isso filtrará as atribuições que são efetivas nesse escopo específico, ou seja, todas negarão atribuições nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="e2b42-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="e2b42-137">B.</span><span class="sxs-lookup"><span data-stu-id="e2b42-137">b.</span></span>
<span data-ttu-id="e2b42-138">ResourceGroupName – Nome de qualquer grupo de recursos sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b42-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="e2b42-139">Isso filtrará as atribuições efetivas no grupo de recursos especificado, ou seja, todas negarão atribuições nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="e2b42-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="e2b42-140">C.</span><span class="sxs-lookup"><span data-stu-id="e2b42-140">c.</span></span>
<span data-ttu-id="e2b42-141">ResourceName, ResourceType, ResourceGroupName e (opcionalmente) ParentResource – identifica um determinado recurso sob a assinatura e filtrará as atribuições negadas efetivas nesse escopo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e2b42-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="e2b42-142">Para determinar qual acesso foi negado a um determinado usuário na assinatura, use a opção ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="e2b42-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="e2b42-143">Isso lista todas as atribuições de negação atribuídas ao usuário e aos grupos dos que o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="e2b42-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="e2b42-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e2b42-144">EXAMPLES</span></span>

### <span data-ttu-id="e2b42-145">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2b42-145">Example 1</span></span>

<span data-ttu-id="e2b42-146">Listar todas as atribuições negadas na assinatura</span><span class="sxs-lookup"><span data-stu-id="e2b42-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="e2b42-147">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e2b42-147">Example 2</span></span>

<span data-ttu-id="e2b42-148">Obtém todas as atribuições negadas feitas ao john.doe@contoso.com usuário no teste de escopoRG e acima.</span><span class="sxs-lookup"><span data-stu-id="e2b42-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="e2b42-149">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e2b42-149">Example 3</span></span>

<span data-ttu-id="e2b42-150">Obtém todas as atribuições de negação da entidade de serviço especificada</span><span class="sxs-lookup"><span data-stu-id="e2b42-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="e2b42-151">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e2b42-151">Example 4</span></span>

<span data-ttu-id="e2b42-152">Obtém atribuições negadas no escopo do site "site1".</span><span class="sxs-lookup"><span data-stu-id="e2b42-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="e2b42-153">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2b42-153">PARAMETERS</span></span>

### <span data-ttu-id="e2b42-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b42-154">-DefaultProfile</span></span>
<span data-ttu-id="e2b42-155">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e2b42-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2b42-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e2b42-156">-DenyAssignmentName</span></span>
<span data-ttu-id="e2b42-157">Nome da atribuição de negação.</span><span class="sxs-lookup"><span data-stu-id="e2b42-157">Name of the deny assignment.</span></span>

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

### <span data-ttu-id="e2b42-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="e2b42-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="e2b42-159">Se especificado, retornará as atribuições negadas diretamente atribuídas ao usuário e aos grupos dos quais o usuário é membro (transitamente).</span><span class="sxs-lookup"><span data-stu-id="e2b42-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="e2b42-160">Com suporte apenas para uma entidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="e2b42-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="e2b42-161">-ID</span><span class="sxs-lookup"><span data-stu-id="e2b42-161">-Id</span></span>
<span data-ttu-id="e2b42-162">Negar a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e2b42-162">Deny assignment id.</span></span>

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

### <span data-ttu-id="e2b42-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e2b42-163">-ObjectId</span></span>
<span data-ttu-id="e2b42-164">O ObjectId do Azure AD do Usuário, Grupo ou Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="e2b42-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="e2b42-165">Os filtros negam todas as atribuições feitas ao diretor especificado.</span><span class="sxs-lookup"><span data-stu-id="e2b42-165">Filters all deny assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="e2b42-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="e2b42-166">-ParentResource</span></span>
<span data-ttu-id="e2b42-167">O recurso pai na hierarquia do recurso especificado usando o parâmetro ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e2b42-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="e2b42-168">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e2b42-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="e2b42-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b42-169">-ResourceGroupName</span></span>
<span data-ttu-id="e2b42-170">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2b42-170">The resource group name.</span></span>
<span data-ttu-id="e2b42-171">As listas negam atribuições que são eficazes no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e2b42-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="e2b42-172">Quando usadas em conjunto com parâmetros ResourceName, ResourceType e ParentResource, as listas de comandos negam atribuições efetivas nos recursos dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2b42-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="e2b42-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e2b42-173">-ResourceName</span></span>
<span data-ttu-id="e2b42-174">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e2b42-174">The resource name.</span></span>
<span data-ttu-id="e2b42-175">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="e2b42-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="e2b42-176">Deve ser usado em conjunto com os parâmetros ResourceGroupName, ResourceType e (opcionalmente)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="e2b42-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e2b42-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e2b42-177">-ResourceType</span></span>
<span data-ttu-id="e2b42-178">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e2b42-178">The resource type.</span></span>
<span data-ttu-id="e2b42-179">Por exemplo, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="e2b42-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="e2b42-180">Deve ser usado em conjunto com ResourceGroupName, ResourceName e (opcionalmente)Parâmetros ParentResource.</span><span class="sxs-lookup"><span data-stu-id="e2b42-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e2b42-181">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e2b42-181">-Scope</span></span>
<span data-ttu-id="e2b42-182">O Escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="e2b42-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="e2b42-183">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="e2b42-183">In the format of relative URI.</span></span>
<span data-ttu-id="e2b42-184">Por exemplo, /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="e2b42-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="e2b42-185">Ele deve começar com "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="e2b42-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="e2b42-186">O comando filtra todas as atribuições negadas que são eficazes nesse escopo.</span><span class="sxs-lookup"><span data-stu-id="e2b42-186">The command filters all deny assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="e2b42-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e2b42-187">-ServicePrincipalName</span></span>
<span data-ttu-id="e2b42-188">O ServicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e2b42-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="e2b42-189">Os filtros negam todas as atribuições feitas ao aplicativo Azure AD especificado.</span><span class="sxs-lookup"><span data-stu-id="e2b42-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="e2b42-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e2b42-190">-SignInName</span></span>
<span data-ttu-id="e2b42-191">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2b42-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="e2b42-192">Os filtros negam todas as atribuições feitas ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="e2b42-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="e2b42-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b42-193">CommonParameters</span></span>
<span data-ttu-id="e2b42-194">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b42-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b42-195">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2b42-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b42-196">Entradas</span><span class="sxs-lookup"><span data-stu-id="e2b42-196">INPUTS</span></span>

### <span data-ttu-id="e2b42-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e2b42-197">System.Guid</span></span>

### <span data-ttu-id="e2b42-198">System.String</span><span class="sxs-lookup"><span data-stu-id="e2b42-198">System.String</span></span>

## <span data-ttu-id="e2b42-199">Saídas</span><span class="sxs-lookup"><span data-stu-id="e2b42-199">OUTPUTS</span></span>

### <span data-ttu-id="e2b42-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="e2b42-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="e2b42-201">Notas</span><span class="sxs-lookup"><span data-stu-id="e2b42-201">NOTES</span></span>
<span data-ttu-id="e2b42-202">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="e2b42-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e2b42-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2b42-203">RELATED LINKS</span></span>
