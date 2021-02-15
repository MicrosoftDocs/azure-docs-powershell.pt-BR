---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: fc954dcf2ce3b9a1c066b3986bbc0bbea302ea2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118734"
---
# <span data-ttu-id="24fea-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="24fea-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="24fea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24fea-102">SYNOPSIS</span></span>
<span data-ttu-id="24fea-103">Remove uma atribuição de função ao diretor especificado que está atribuído a uma determinada função em um escopo específico.</span><span class="sxs-lookup"><span data-stu-id="24fea-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="24fea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24fea-104">SYNTAX</span></span>

### <span data-ttu-id="24fea-105">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24fea-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fea-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fea-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24fea-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="24fea-117">DESCRIPTION</span></span>
<span data-ttu-id="24fea-118">Use o Remove-AzRoleAssignment para revogar o acesso a qualquer entidade em determinado escopo e função.</span><span class="sxs-lookup"><span data-stu-id="24fea-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="24fea-119">O objeto da atribuição, ou seja, o principal DEVE ser especificado.</span><span class="sxs-lookup"><span data-stu-id="24fea-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="24fea-120">O principal pode ser um usuário (use parâmetros SignInName ou ObjectId para identificar um usuário), grupo de segurança (usar parâmetro ObjectId para identificar um grupo) ou entidade de serviço (use parâmetros ServicePrincipalName ou ObjectId para identificar um ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="24fea-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="24fea-121">A função à que a entidade deve ser atribuída deve ser especificada usando o parâmetro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="24fea-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="24fea-122">O escopo da atribuição PODE ser especificado e, se não especificado, padrão para o escopo da assinatura, ou seja, ele tentará excluir uma tarefa para o principal especificado e a função no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="24fea-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="24fea-123">O escopo da atribuição pode ser especificado usando um dos parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="24fea-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="24fea-124">Um.</span><span class="sxs-lookup"><span data-stu-id="24fea-124">a.</span></span>
<span data-ttu-id="24fea-125">Escopo – este é o escopo totalmente qualificado, começando com \<subscriptionId\> /subscriptions/b.</span><span class="sxs-lookup"><span data-stu-id="24fea-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="24fea-126">ResourceGroupName – Nome de qualquer grupo de recursos sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="24fea-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="24fea-127">C.</span><span class="sxs-lookup"><span data-stu-id="24fea-127">c.</span></span>
<span data-ttu-id="24fea-128">ResourceName, ResourceType, ResourceGroupName e (opcionalmente) ParentResource – Identifica um determinado recurso sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="24fea-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="24fea-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24fea-129">EXAMPLES</span></span>

### <span data-ttu-id="24fea-130">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24fea-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="24fea-131">Remove uma atribuição de função para quem está atribuído à função Leitor no escopo do grupo de john.doe@contoso.com recursos rg1.</span><span class="sxs-lookup"><span data-stu-id="24fea-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="24fea-132">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="24fea-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="24fea-133">Remove a atribuição de função à entidade do grupo identificada pela ObjectId e atribuída à função Leitor.</span><span class="sxs-lookup"><span data-stu-id="24fea-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="24fea-134">O padrão é usar a assinatura atual como escopo para encontrar a tarefa a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="24fea-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="24fea-135">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="24fea-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="24fea-136">Remove o primeiro objeto de atribuição de função que é buscado do commandlet Get-AzRoleAssignment função.</span><span class="sxs-lookup"><span data-stu-id="24fea-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="24fea-137">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24fea-137">PARAMETERS</span></span>

### <span data-ttu-id="24fea-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24fea-138">-DefaultProfile</span></span>
<span data-ttu-id="24fea-139">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="24fea-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24fea-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24fea-140">-InputObject</span></span>
<span data-ttu-id="24fea-141">Objeto de Atribuição de Função.</span><span class="sxs-lookup"><span data-stu-id="24fea-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="24fea-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="24fea-142">-ObjectId</span></span>
<span data-ttu-id="24fea-143">ObjectId do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="24fea-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fea-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="24fea-144">-ParentResource</span></span>
<span data-ttu-id="24fea-145">O recurso pai na hierarquia(do recurso especificado usando o parâmetro ResourceName), se for o caso.</span><span class="sxs-lookup"><span data-stu-id="24fea-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="24fea-146">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e ResourceName para construir um escopo hierárquico na forma de um URI relativo que identifique o recurso.</span><span class="sxs-lookup"><span data-stu-id="24fea-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="24fea-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24fea-147">-PassThru</span></span>
<span data-ttu-id="24fea-148">Se especificado, exibirá a atribuição de função excluída</span><span class="sxs-lookup"><span data-stu-id="24fea-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="24fea-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24fea-149">-ResourceGroupName</span></span>
<span data-ttu-id="24fea-150">O nome do grupo de recursos ao que a função foi atribuída.</span><span class="sxs-lookup"><span data-stu-id="24fea-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="24fea-151">Tenta excluir uma atribuição no escopo do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="24fea-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="24fea-152">Quando usado em conjunto com parâmetros ResourceName, ResourceType e (opcionalmente)ParentResource, o comando construirá um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="24fea-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="24fea-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="24fea-153">-ResourceName</span></span>
<span data-ttu-id="24fea-154">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="24fea-154">The resource name.</span></span>
<span data-ttu-id="24fea-155">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="24fea-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="24fea-156">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e (opcionalmente)ParentResource, para construir um escopo hierárquico na forma de um URI relativo que identifique o recurso e exclua uma atribuição nesse escopo.</span><span class="sxs-lookup"><span data-stu-id="24fea-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="24fea-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="24fea-157">-ResourceType</span></span>
<span data-ttu-id="24fea-158">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="24fea-158">The resource type.</span></span>
<span data-ttu-id="24fea-159">Por exemplo, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="24fea-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="24fea-160">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceName e (opcionalmente)ParentResource para construir um escopo hierárquico na forma de um URI relativo que identifique o recurso e exclua uma atribuição nesse escopo de recurso.</span><span class="sxs-lookup"><span data-stu-id="24fea-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="24fea-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="24fea-161">-RoleDefinitionId</span></span>
<span data-ttu-id="24fea-162">ID da função RBAC para a qual a tarefa precisa ser excluída.</span><span class="sxs-lookup"><span data-stu-id="24fea-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="24fea-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="24fea-163">-RoleDefinitionName</span></span>
<span data-ttu-id="24fea-164">Nome da função RBAC para a qual a tarefa precisa ser excluída, ou seja, Leitor, Colaborador, Administrador de Rede Virtual etc.</span><span class="sxs-lookup"><span data-stu-id="24fea-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="24fea-165">-Escopo</span><span class="sxs-lookup"><span data-stu-id="24fea-165">-Scope</span></span>
<span data-ttu-id="24fea-166">O Escopo da atribuição de função a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="24fea-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="24fea-167">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="24fea-167">In the format of relative URI.</span></span>
<span data-ttu-id="24fea-168">Por exemplo, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="24fea-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="24fea-169">Se não especificado, tentará excluir a função no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="24fea-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="24fea-170">Se especificado, deve começar com "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="24fea-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="24fea-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="24fea-171">-ServicePrincipalName</span></span>
<span data-ttu-id="24fea-172">O ServicePrincipalName do aplicativo Azure AD</span><span class="sxs-lookup"><span data-stu-id="24fea-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="24fea-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="24fea-173">-SignInName</span></span>
<span data-ttu-id="24fea-174">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="24fea-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="24fea-175">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="24fea-175">-Confirm</span></span>
<span data-ttu-id="24fea-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24fea-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24fea-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24fea-177">-WhatIf</span></span>
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

### <span data-ttu-id="24fea-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24fea-178">CommonParameters</span></span>
<span data-ttu-id="24fea-179">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24fea-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24fea-180">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24fea-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24fea-181">Entradas</span><span class="sxs-lookup"><span data-stu-id="24fea-181">INPUTS</span></span>

### <span data-ttu-id="24fea-182">System.String</span><span class="sxs-lookup"><span data-stu-id="24fea-182">System.String</span></span>

### <span data-ttu-id="24fea-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="24fea-183">System.Guid</span></span>

### <span data-ttu-id="24fea-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="24fea-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="24fea-185">Saídas</span><span class="sxs-lookup"><span data-stu-id="24fea-185">OUTPUTS</span></span>

### <span data-ttu-id="24fea-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="24fea-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="24fea-187">Notas</span><span class="sxs-lookup"><span data-stu-id="24fea-187">NOTES</span></span>
<span data-ttu-id="24fea-188">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="24fea-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="24fea-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24fea-189">RELATED LINKS</span></span>

[<span data-ttu-id="24fea-190">Novo-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="24fea-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="24fea-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="24fea-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="24fea-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24fea-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

