---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
ms.openlocfilehash: 5cbf4f46d102188ff1db3becf66d3edffe426fae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432573"
---
# <span data-ttu-id="d1a54-101">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d1a54-101">Get-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="d1a54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1a54-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a54-103">Lista as atribuições de função RBAC do Azure no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a54-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="d1a54-104">Por padrão, ele lista todas as atribuições de função na assinatura do Azure selecionada.</span><span class="sxs-lookup"><span data-stu-id="d1a54-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="d1a54-105">Use os parâmetros respectivos para listar as atribuições para um usuário específico ou para listar as atribuições em um recurso ou grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="d1a54-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1a54-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1a54-106">SYNTAX</span></span>

### <span data-ttu-id="d1a54-107">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1a54-107">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-116">SignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1a54-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-120">SPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-121">ResourceGroupParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-122">ResourceParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a54-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a54-123">ScopeParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1a54-124">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1a54-124">DESCRIPTION</span></span>
<span data-ttu-id="d1a54-125">Use o comando Get-AzureRMRoleAssignment para listar todas as atribuições de função que são efetivas em um escopo.</span><span class="sxs-lookup"><span data-stu-id="d1a54-125">Use the Get-AzureRMRoleAssignment command to list all role assignments that are effective on a scope.</span></span>

<span data-ttu-id="d1a54-126">Sem parâmetros, esse comando retorna todas as atribuições de função feitas sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="d1a54-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="d1a54-127">Essa lista pode ser filtrada usando parâmetros de filtragem para principal, função e escopo.</span><span class="sxs-lookup"><span data-stu-id="d1a54-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>

<span data-ttu-id="d1a54-128">O assunto da tarefa deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a54-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="d1a54-129">Para especificar um usuário, use SignInName ou os parâmetros do ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d1a54-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="d1a54-130">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d1a54-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="d1a54-131">E para especificar um aplicativo do Azure AD, use os parâmetros servicePrincipalName ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="d1a54-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="d1a54-132">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="d1a54-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="d1a54-133">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a54-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="d1a54-134">O padrão é a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="d1a54-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="d1a54-135">O escopo da atribuição pode ser especificado usando-se uma das combinações de parâmetro a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1a54-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="d1a54-136">Scope-este é o escopo totalmente qualificado que começa com/subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="d1a54-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="d1a54-137">Isso filtrará as tarefas que são efetivas nesse escopo específico, ou seja, todas as tarefas nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="d1a54-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="d1a54-138">b.</span><span class="sxs-lookup"><span data-stu-id="d1a54-138">b.</span></span>
<span data-ttu-id="d1a54-139">ResourceGroupName-nome de qualquer grupo de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d1a54-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="d1a54-140">Isso filtrará as atribuições de forma eficaz no grupo de recursos c especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a54-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="d1a54-141">ResourceFile, ResourceType, ResourceGroupName e (opcionalmente) ParentResource-identifica um recurso específico na assinatura e filtrará as atribuições em vigor nesse escopo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1a54-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>

<span data-ttu-id="d1a54-142">Para determinar qual acesso um usuário específico tem na assinatura, use a opção ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="d1a54-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="d1a54-143">Isso listará todas as funções atribuídas ao usuário e os grupos dos quais o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="d1a54-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>

<span data-ttu-id="d1a54-144">Use a opção IncludeClassicAdministrators para exibir também os administradores de assinaturas e administradores de coadministrador.</span><span class="sxs-lookup"><span data-stu-id="d1a54-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="d1a54-145">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1a54-145">EXAMPLES</span></span>

### <span data-ttu-id="d1a54-146">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d1a54-146">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment
```

<span data-ttu-id="d1a54-147">Listar todas as atribuições de função na assinatura</span><span class="sxs-lookup"><span data-stu-id="d1a54-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="d1a54-148">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d1a54-148">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com -ExpandPrincipalGroups
```

<span data-ttu-id="d1a54-149">Obtém todas as atribuições de função feitas ao usuário john.doe@contoso.com e os grupos dos quais ele é membro, no escopo testRG ou superior.</span><span class="sxs-lookup"><span data-stu-id="d1a54-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="d1a54-150">--------------------------Exemplo 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="d1a54-150">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="d1a54-151">Obtém todas as atribuições de função da entidade de serviço especificada</span><span class="sxs-lookup"><span data-stu-id="d1a54-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="d1a54-152">--------------------------Exemplo 4--------------------------</span><span class="sxs-lookup"><span data-stu-id="d1a54-152">--------------------------  Example 4  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="d1a54-153">Obtém as atribuições de função no escopo do site "site1".</span><span class="sxs-lookup"><span data-stu-id="d1a54-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="d1a54-154">OS</span><span class="sxs-lookup"><span data-stu-id="d1a54-154">PARAMETERS</span></span>

### <span data-ttu-id="d1a54-155">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="d1a54-155">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="d1a54-156">Se especificado, retorna as funções diretamente atribuídas ao usuário e para os grupos dos quais o usuário é membro (transitivamente).</span><span class="sxs-lookup"><span data-stu-id="d1a54-156">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="d1a54-157">Com suporte somente para um usuário principal.</span><span class="sxs-lookup"><span data-stu-id="d1a54-157">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="d1a54-158">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="d1a54-158">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="d1a54-159">Se especificado, também listará os administradores clássicos da assinatura (coadministradores, administradores de serviços, etc.) atribuições de função.</span><span class="sxs-lookup"><span data-stu-id="d1a54-159">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a54-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d1a54-160">-ObjectId</span></span>
<span data-ttu-id="d1a54-161">O ObjectId do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d1a54-161">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="d1a54-162">Filtra todas as atribuições feitas ao objeto de segurança especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a54-162">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="d1a54-163">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="d1a54-163">-ParentResource</span></span>
<span data-ttu-id="d1a54-164">O recurso pai na hierarquia do recurso especificado usando o parâmetro ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="d1a54-164">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="d1a54-165">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e resourceName.</span><span class="sxs-lookup"><span data-stu-id="d1a54-165">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="d1a54-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a54-166">-ResourceGroupName</span></span>
<span data-ttu-id="d1a54-167">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1a54-167">The resource group name.</span></span>
<span data-ttu-id="d1a54-168">Lista as atribuições de função que são eficientes no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a54-168">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="d1a54-169">Quando usado em conjunto com parâmetros ResourceFile, ResourceType e ParentResource, o comando lista as atribuições de efetivo em recursos dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1a54-169">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="d1a54-170">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d1a54-170">-ResourceName</span></span>
<span data-ttu-id="d1a54-171">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d1a54-171">The resource name.</span></span>
<span data-ttu-id="d1a54-172">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="d1a54-172">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="d1a54-173">Deve ser usado em conjunto com ResourceGroupName, ResourceType e (opcionalmente) parâmetros ParentResource.</span><span class="sxs-lookup"><span data-stu-id="d1a54-173">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="d1a54-174">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d1a54-174">-ResourceType</span></span>
<span data-ttu-id="d1a54-175">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d1a54-175">The resource type.</span></span>
<span data-ttu-id="d1a54-176">Por exemplo, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="d1a54-176">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="d1a54-177">Deve ser usado em conjunto com ResourceGroupName, Resource Resources e (opcionalmente) parâmetros ParentResource.</span><span class="sxs-lookup"><span data-stu-id="d1a54-177">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="d1a54-178">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d1a54-178">-RoleDefinitionId</span></span>
<span data-ttu-id="d1a54-179">ID da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="d1a54-179">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a54-180">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d1a54-180">-RoleDefinitionName</span></span>
<span data-ttu-id="d1a54-181">Função que é atribuída à entidade, ou seja, leitor, colaborador, administrador de rede virtual, etc.</span><span class="sxs-lookup"><span data-stu-id="d1a54-181">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a54-182">-Escopo</span><span class="sxs-lookup"><span data-stu-id="d1a54-182">-Scope</span></span>
<span data-ttu-id="d1a54-183">O escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="d1a54-183">The Scope of the role assignment.</span></span>
<span data-ttu-id="d1a54-184">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="d1a54-184">In the format of relative URI.</span></span>
<span data-ttu-id="d1a54-185">Por exemplo,/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="d1a54-185">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="d1a54-186">Ele deve começar com "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="d1a54-186">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="d1a54-187">O comando filtra todas as tarefas que são efetivas nesse escopo.</span><span class="sxs-lookup"><span data-stu-id="d1a54-187">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="d1a54-188">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="d1a54-188">-ServicePrincipalName</span></span>
<span data-ttu-id="d1a54-189">O servicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d1a54-189">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="d1a54-190">Filtra todas as atribuições feitas ao aplicativo do Azure AD especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a54-190">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="d1a54-191">-SignInName</span><span class="sxs-lookup"><span data-stu-id="d1a54-191">-SignInName</span></span>
<span data-ttu-id="d1a54-192">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="d1a54-192">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="d1a54-193">Filtra todas as atribuições feitas ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a54-193">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="d1a54-194">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a54-194">-DefaultProfile</span></span>
<span data-ttu-id="d1a54-195">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a54-195">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1a54-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a54-196">CommonParameters</span></span>
<span data-ttu-id="d1a54-197">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a54-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a54-198">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1a54-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a54-199">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1a54-199">INPUTS</span></span>

## <span data-ttu-id="d1a54-200">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1a54-200">OUTPUTS</span></span>

### <span data-ttu-id="d1a54-201">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleAssignment]</span><span class="sxs-lookup"><span data-stu-id="d1a54-201">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="d1a54-202">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1a54-202">NOTES</span></span>
<span data-ttu-id="d1a54-203">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="d1a54-203">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d1a54-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1a54-204">RELATED LINKS</span></span>

[<span data-ttu-id="d1a54-205">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d1a54-205">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="d1a54-206">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d1a54-206">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="d1a54-207">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d1a54-207">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

