---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: dd59b49ad4002d38cd9a49506cb1723b5ac1e426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891288"
---
# <span data-ttu-id="e80b8-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e80b8-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="e80b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e80b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e80b8-103">Lista as atribuições de função do Azure RBAC no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="e80b8-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="e80b8-104">Por padrão, ele lista todas as atribuições de função na assinatura selecionada do Azure.</span><span class="sxs-lookup"><span data-stu-id="e80b8-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="e80b8-105">Use os parâmetros respectivos para listar atribuições para um usuário específico ou para listar atribuições em um grupo de recursos ou recurso específico.</span><span class="sxs-lookup"><span data-stu-id="e80b8-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="e80b8-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e80b8-106">SYNTAX</span></span>

### <span data-ttu-id="e80b8-107">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e80b8-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e80b8-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e80b8-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e80b8-124">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e80b8-124">DESCRIPTION</span></span>
<span data-ttu-id="e80b8-125">Use o Get-AzRoleAssignment para listar todas as atribuições de função que são efetivas em um escopo.</span><span class="sxs-lookup"><span data-stu-id="e80b8-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="e80b8-126">Sem parâmetros, este comando retorna todas as atribuições de função feitas sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e80b8-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="e80b8-127">Essa lista pode ser filtrada usando parâmetros de filtragem para principal, função e escopo.</span><span class="sxs-lookup"><span data-stu-id="e80b8-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="e80b8-128">O assunto da atribuição deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e80b8-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="e80b8-129">Para especificar um usuário, use os parâmetros SignInName ou ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e80b8-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="e80b8-130">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e80b8-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="e80b8-131">E para especificar um aplicativo do Azure AD, use parâmetros ServicePrincipalName ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e80b8-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="e80b8-132">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="e80b8-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="e80b8-133">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e80b8-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="e80b8-134">Ele é padrão para a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="e80b8-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="e80b8-135">O escopo da atribuição pode ser especificado usando uma das seguintes combinações de parâmetros a.</span><span class="sxs-lookup"><span data-stu-id="e80b8-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="e80b8-136">Escopo - Este é o escopo totalmente qualificado começando com /subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="e80b8-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="e80b8-137">Isso filtrará as atribuições que são efetivas nesse escopo específico, ou seja, todas as atribuições nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="e80b8-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="e80b8-138">b.</span><span class="sxs-lookup"><span data-stu-id="e80b8-138">b.</span></span>
<span data-ttu-id="e80b8-139">ResourceGroupName - Nome de qualquer grupo de recursos sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e80b8-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="e80b8-140">Isso filtrará as atribuições efetivas no grupo de recursos especificado c.</span><span class="sxs-lookup"><span data-stu-id="e80b8-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="e80b8-141">ResourceName, ResourceType, ResourceGroupName e (opcionalmente) ParentResource - Identifica um determinado recurso sob a assinatura e filtrará atribuições efetivas nesse escopo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e80b8-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="e80b8-142">Para determinar o acesso que um determinado usuário tem na assinatura, use a opção ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="e80b8-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="e80b8-143">Isso lista todas as funções atribuídas ao usuário e aos grupos dos quais o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="e80b8-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="e80b8-144">Use a opção IncludeClassicAdministrators para também exibir os administradores e co-administradores de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e80b8-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="e80b8-145">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e80b8-145">EXAMPLES</span></span>

### <span data-ttu-id="e80b8-146">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e80b8-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="e80b8-147">Listar todas as atribuições de função na assinatura</span><span class="sxs-lookup"><span data-stu-id="e80b8-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="e80b8-148">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e80b8-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="e80b8-149">Obtém todas as atribuições de função feitas ao usuário e aos grupos dos quais ele é membro, no escopo john.doe@contoso.com testRG ou acima.</span><span class="sxs-lookup"><span data-stu-id="e80b8-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="e80b8-150">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e80b8-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="e80b8-151">Obtém todas as atribuições de função da entidade de serviço especificada</span><span class="sxs-lookup"><span data-stu-id="e80b8-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="e80b8-152">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e80b8-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="e80b8-153">Obtém atribuições de função no escopo do site 'site1'.</span><span class="sxs-lookup"><span data-stu-id="e80b8-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="e80b8-154">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e80b8-154">PARAMETERS</span></span>

### <span data-ttu-id="e80b8-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80b8-155">-DefaultProfile</span></span>
<span data-ttu-id="e80b8-156">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e80b8-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e80b8-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="e80b8-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="e80b8-158">Se especificado, retorna funções atribuídas diretamente ao usuário e aos grupos dos quais o usuário é membro (transitivamente).</span><span class="sxs-lookup"><span data-stu-id="e80b8-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="e80b8-159">Suportado apenas para uma entidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="e80b8-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="e80b8-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="e80b8-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="e80b8-161">Se especificado, também lista as atribuições de função de administradores clássicos de assinatura (co-administradores, administradores de serviço, etc.).</span><span class="sxs-lookup"><span data-stu-id="e80b8-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="e80b8-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e80b8-162">-ObjectId</span></span>
<span data-ttu-id="e80b8-163">ObjectId do Azure AD da Entidade de Usuário, Grupo ou Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="e80b8-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="e80b8-164">Filtra todas as atribuições feitas à entidade especificada.</span><span class="sxs-lookup"><span data-stu-id="e80b8-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80b8-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="e80b8-165">-ParentResource</span></span>
<span data-ttu-id="e80b8-166">O recurso pai na hierarquia do recurso especificado usando o parâmetro ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e80b8-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="e80b8-167">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e80b8-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="e80b8-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e80b8-168">-ResourceGroupName</span></span>
<span data-ttu-id="e80b8-169">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e80b8-169">The resource group name.</span></span>
<span data-ttu-id="e80b8-170">Lista atribuições de função que são efetivas no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e80b8-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="e80b8-171">Quando usado em conjunto com parâmetros ResourceName, ResourceType e ParentResource, o comando lista atribuições efetivas em recursos dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e80b8-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="e80b8-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e80b8-172">-ResourceName</span></span>
<span data-ttu-id="e80b8-173">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e80b8-173">The resource name.</span></span>
<span data-ttu-id="e80b8-174">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="e80b8-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="e80b8-175">Deve ser usado em conjunto com os parâmetros ResourceGroupName, ResourceType e (opcionalmente)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="e80b8-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e80b8-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e80b8-176">-ResourceType</span></span>
<span data-ttu-id="e80b8-177">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e80b8-177">The resource type.</span></span>
<span data-ttu-id="e80b8-178">Por exemplo, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="e80b8-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="e80b8-179">Deve ser usado em conjunto com os parâmetros ResourceGroupName, ResourceName e (opcionalmente)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="e80b8-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e80b8-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e80b8-180">-RoleDefinitionId</span></span>
<span data-ttu-id="e80b8-181">ID da função atribuída à entidade principal.</span><span class="sxs-lookup"><span data-stu-id="e80b8-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="e80b8-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e80b8-182">-RoleDefinitionName</span></span>
<span data-ttu-id="e80b8-183">Função atribuída à entidade principal, isto é, Leitor, Colaborador, Administrador de Rede Virtual, etc.</span><span class="sxs-lookup"><span data-stu-id="e80b8-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="e80b8-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="e80b8-184">-Scope</span></span>
<span data-ttu-id="e80b8-185">O Escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="e80b8-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="e80b8-186">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="e80b8-186">In the format of relative URI.</span></span>
<span data-ttu-id="e80b8-187">Por exemplo, /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="e80b8-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="e80b8-188">Ele deve começar com "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="e80b8-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="e80b8-189">O comando filtra todas as atribuições que são efetivas nesse escopo.</span><span class="sxs-lookup"><span data-stu-id="e80b8-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="e80b8-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e80b8-190">-ServicePrincipalName</span></span>
<span data-ttu-id="e80b8-191">ServicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e80b8-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="e80b8-192">Filtra todas as atribuições feitas ao aplicativo Azure AD especificado.</span><span class="sxs-lookup"><span data-stu-id="e80b8-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="e80b8-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e80b8-193">-SignInName</span></span>
<span data-ttu-id="e80b8-194">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="e80b8-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="e80b8-195">Filtra todas as atribuições feitas ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="e80b8-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="e80b8-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80b8-196">CommonParameters</span></span>
<span data-ttu-id="e80b8-197">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e80b8-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80b8-198">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e80b8-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80b8-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e80b8-199">INPUTS</span></span>

### <span data-ttu-id="e80b8-200">System.String</span><span class="sxs-lookup"><span data-stu-id="e80b8-200">System.String</span></span>

### <span data-ttu-id="e80b8-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e80b8-201">System.Guid</span></span>

## <span data-ttu-id="e80b8-202">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e80b8-202">OUTPUTS</span></span>

### <span data-ttu-id="e80b8-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e80b8-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="e80b8-204">NOTES</span><span class="sxs-lookup"><span data-stu-id="e80b8-204">NOTES</span></span>
<span data-ttu-id="e80b8-205">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="e80b8-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e80b8-206">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e80b8-206">RELATED LINKS</span></span>

[<span data-ttu-id="e80b8-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e80b8-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="e80b8-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e80b8-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="e80b8-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e80b8-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

