---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
ms.openlocfilehash: adf6147db102ee834f7e12e19409a95734fae7e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786371"
---
# <span data-ttu-id="c8a5c-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c8a5c-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="c8a5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a5c-103">Remove uma atribuição de função para a entidade de segurança especificada que é atribuída a uma função específica em um escopo específico.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8a5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8a5c-104">SYNTAX</span></span>

### <span data-ttu-id="c8a5c-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8a5c-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a5c-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a5c-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a5c-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8a5c-117">DESCRIPTION</span></span>
<span data-ttu-id="c8a5c-118">Use o Remove-AzureRmRoleAssignment commandlet para revogar o acesso a qualquer entidade em escopo específico e a função específica.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="c8a5c-119">O objeto da tarefa, ou seja, a principal deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="c8a5c-120">O principal pode ser um usuário (use parâmetros SignInName ou ObjectId para identificar um usuário), grupo de segurança (use o parâmetro ObjectId para identificar um grupo) ou entidade de serviço (use parâmetros servicePrincipalName ou ObjectId para identificar um servicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="c8a5c-121">A função à qual a entidade de segurança está atribuída deve ser especificada usando o parâmetro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="c8a5c-122">O escopo da atribuição pode ser especificado e, se não for especificado, o padrão será o escopo de assinatura, ou seja, ele tentará excluir uma atribuição para a entidade e função especificada no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="c8a5c-123">O escopo da atribuição pode ser especificado usando um dos parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="c8a5c-124">um.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-124">a.</span></span>
<span data-ttu-id="c8a5c-125">Scope-este é o escopo totalmente qualificado começando com/subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="c8a5c-126">ResourceGroupName-nome de qualquer grupo de recursos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="c8a5c-127">partição.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-127">c.</span></span>
<span data-ttu-id="c8a5c-128">ResourceFile, ResourceType, ResourceGroupName e (opcionalmente) ParentResource-identifica um recurso específico na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="c8a5c-129">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8a5c-129">EXAMPLES</span></span>

### <span data-ttu-id="c8a5c-130">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8a5c-130">Example 1</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="c8a5c-131">Remove uma atribuição de função para john.doe@contoso.com quem está atribuído à função de leitor no escopo do Rg1 Resource.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="c8a5c-132">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c8a5c-132">Example 2</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="c8a5c-133">Remove a atribuição de função para a entidade de segurança do grupo identificada pelo ObjectId e atribuída à função leitor.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="c8a5c-134">O padrão é usar a assinatura atual como escopo para localizar a atribuição a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="c8a5c-135">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c8a5c-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="c8a5c-136">Remove o primeiro objeto de atribuição de função que é buscado do Get-AzureRmRoleAssignment commandlet.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="c8a5c-137">OS</span><span class="sxs-lookup"><span data-stu-id="c8a5c-137">PARAMETERS</span></span>

### <span data-ttu-id="c8a5c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a5c-138">-DefaultProfile</span></span>
<span data-ttu-id="c8a5c-139">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c8a5c-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8a5c-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8a5c-140">-InputObject</span></span>
<span data-ttu-id="c8a5c-141">Objeto de atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-141">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c8a5c-142">-ObjectId</span></span>
<span data-ttu-id="c8a5c-143">ObjectId do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="c8a5c-144">-ParentResource</span></span>
<span data-ttu-id="c8a5c-145">O recurso pai na hierarquia (do recurso especificado usando o parâmetro ResourceManager), se houver.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="c8a5c-146">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e resourceName para construir um escopo hierárquico na forma de um URI relativo que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8a5c-147">-PassThru</span></span>
<span data-ttu-id="c8a5c-148">Se especificado, exibe a atribuição de função excluída</span><span class="sxs-lookup"><span data-stu-id="c8a5c-148">If specified, displays the deleted role assignment</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a5c-149">-ResourceGroupName</span></span>
<span data-ttu-id="c8a5c-150">O nome do grupo de recursos ao qual a função está atribuída.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="c8a5c-151">Tenta excluir uma tarefa no escopo do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="c8a5c-152">Quando usado em conjunto com os parâmetros ResourceFile, ResourceType e (opcionalmente) ParentResource, o comando constrói um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c8a5c-153">-ResourceName</span></span>
<span data-ttu-id="c8a5c-154">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-154">The resource name.</span></span>
<span data-ttu-id="c8a5c-155">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="c8a5c-156">Deve ser usado em conjunto com os parâmetros ResourceGroupName, ResourceType e (opcionalmente) ParentResource para construir um escopo hierárquico na forma de um URI relativo que identifique o recurso e exclua uma tarefa nesse escopo.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c8a5c-157">-ResourceType</span></span>
<span data-ttu-id="c8a5c-158">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-158">The resource type.</span></span>
<span data-ttu-id="c8a5c-159">Por exemplo, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="c8a5c-160">Deve ser usado em conjunto com ResourceGroupName, ResourceManager e (opcionalmente) ParentResource parâmetros para construir um escopo hierárquico na forma de um URI relativo que identifica o recurso e exclua uma tarefa nesse escopo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c8a5c-161">-RoleDefinitionId</span></span>
<span data-ttu-id="c8a5c-162">ID da função RBAC para a qual a atribuição precisa ser excluída.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="c8a5c-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="c8a5c-163">-RoleDefinitionName</span></span>
<span data-ttu-id="c8a5c-164">Nome da função RBAC para a qual a atribuição precisa ser excluída, ou seja, leitor, colaborador, administrador de rede virtual, etc.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-165">-Escopo</span><span class="sxs-lookup"><span data-stu-id="c8a5c-165">-Scope</span></span>
<span data-ttu-id="c8a5c-166">O escopo da atribuição de função a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="c8a5c-167">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-167">In the format of relative URI.</span></span>
<span data-ttu-id="c8a5c-168">Por exemplo, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="c8a5c-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="c8a5c-169">Se não for especificado, haverá uma tentativa de excluir a função no nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="c8a5c-170">Se especificado, ele deve começar com "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="c8a5c-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-171">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="c8a5c-171">-ServicePrincipalName</span></span>
<span data-ttu-id="c8a5c-172">O servicePrincipalName do aplicativo Azure AD</span><span class="sxs-lookup"><span data-stu-id="c8a5c-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="c8a5c-173">-SignInName</span></span>
<span data-ttu-id="c8a5c-174">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-175">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8a5c-175">-Confirm</span></span>
<span data-ttu-id="c8a5c-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a5c-177">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5c-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a5c-178">CommonParameters</span></span>
<span data-ttu-id="c8a5c-179">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a5c-180">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a5c-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a5c-181">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8a5c-181">INPUTS</span></span>

### <span data-ttu-id="c8a5c-182">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c8a5c-182">System.Guid</span></span>

### <span data-ttu-id="c8a5c-183">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a5c-183">System.String</span></span>

### <span data-ttu-id="c8a5c-184">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c8a5c-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>
<span data-ttu-id="c8a5c-185">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8a5c-185">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c8a5c-186">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8a5c-186">OUTPUTS</span></span>

### <span data-ttu-id="c8a5c-187">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c8a5c-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="c8a5c-188">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8a5c-188">NOTES</span></span>
<span data-ttu-id="c8a5c-189">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="c8a5c-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c8a5c-190">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8a5c-190">RELATED LINKS</span></span>

[<span data-ttu-id="c8a5c-191">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c8a5c-191">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="c8a5c-192">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c8a5c-192">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="c8a5c-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c8a5c-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

