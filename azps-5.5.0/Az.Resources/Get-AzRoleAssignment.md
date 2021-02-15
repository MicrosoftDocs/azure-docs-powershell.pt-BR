---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118761"
---
# <span data-ttu-id="081e0-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="081e0-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="081e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="081e0-102">SYNOPSIS</span></span>
<span data-ttu-id="081e0-103">Lista as atribuições de função RBAC do Azure no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="081e0-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="081e0-104">Por padrão, ele lista todas as atribuições de função na assinatura do Azure selecionada.</span><span class="sxs-lookup"><span data-stu-id="081e0-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="081e0-105">Use parâmetros respectivos para listar atribuições a um usuário específico ou para listar atribuições em um grupo ou recurso de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="081e0-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="081e0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="081e0-106">SYNTAX</span></span>

### <span data-ttu-id="081e0-107">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="081e0-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081e0-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="081e0-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="081e0-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="081e0-124">DESCRIPTION</span></span>
<span data-ttu-id="081e0-125">Use o comando Get-AzRoleAssignment para listar todas as atribuições de função que são eficazes em um escopo.</span><span class="sxs-lookup"><span data-stu-id="081e0-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="081e0-126">Sem parâmetros, esse comando retorna todas as atribuições de função feitas sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="081e0-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="081e0-127">Essa lista pode ser filtrada usando parâmetros de filtragem para principal, função e escopo.</span><span class="sxs-lookup"><span data-stu-id="081e0-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="081e0-128">O assunto da tarefa deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="081e0-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="081e0-129">Para especificar um usuário, use os parâmetros SignInName ou Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="081e0-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="081e0-130">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="081e0-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="081e0-131">E para especificar um aplicativo Azure AD, use parâmetros ServicePrincipalName ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="081e0-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="081e0-132">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="081e0-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="081e0-133">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="081e0-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="081e0-134">Ele é padrão para a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="081e0-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="081e0-135">O escopo da atribuição pode ser especificado usando uma das seguintes combinações de parâmetros a.</span><span class="sxs-lookup"><span data-stu-id="081e0-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="081e0-136">Escopo – este é o escopo totalmente qualificado, começando com /subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="081e0-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="081e0-137">Isso filtrará as atribuições que são eficazes nesse escopo específico, ou seja, todas as atribuições nesse escopo e acima.</span><span class="sxs-lookup"><span data-stu-id="081e0-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="081e0-138">B.</span><span class="sxs-lookup"><span data-stu-id="081e0-138">b.</span></span>
<span data-ttu-id="081e0-139">ResourceGroupName - Nome de qualquer grupo de recursos sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="081e0-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="081e0-140">Isso filtrará as atribuições em vigor no grupo de recursos especificado c.</span><span class="sxs-lookup"><span data-stu-id="081e0-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="081e0-141">ResourceName, ResourceType, ResourceGroupName e (opcionalmente) ParentResource – identifica um determinado recurso sob a assinatura e filtrará as atribuições efetivas nesse escopo de recurso.</span><span class="sxs-lookup"><span data-stu-id="081e0-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="081e0-142">Para determinar qual acesso um determinado usuário tem na assinatura, use a opção ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="081e0-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="081e0-143">Isso lista todas as funções atribuídas ao usuário e aos grupos dos quais o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="081e0-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="081e0-144">Use a opção IncludeClassicAdministrators para também exibir os administradores e co-administradores da assinatura.</span><span class="sxs-lookup"><span data-stu-id="081e0-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="081e0-145">Exemplos</span><span class="sxs-lookup"><span data-stu-id="081e0-145">EXAMPLES</span></span>

### <span data-ttu-id="081e0-146">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="081e0-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="081e0-147">Listar todas as atribuições de função na assinatura</span><span class="sxs-lookup"><span data-stu-id="081e0-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="081e0-148">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="081e0-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="081e0-149">Obtém todas as atribuições de função feitas ao usuário e aos grupos dos quais ele é membro, no escopo john.doe@contoso.com de testRG ou acima.</span><span class="sxs-lookup"><span data-stu-id="081e0-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="081e0-150">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="081e0-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="081e0-151">Obtém todas as atribuições de função da entidade de serviço especificada</span><span class="sxs-lookup"><span data-stu-id="081e0-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="081e0-152">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="081e0-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="081e0-153">Obtém atribuições de função no escopo do site "site1".</span><span class="sxs-lookup"><span data-stu-id="081e0-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="081e0-154">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="081e0-154">PARAMETERS</span></span>

### <span data-ttu-id="081e0-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081e0-155">-DefaultProfile</span></span>
<span data-ttu-id="081e0-156">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="081e0-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="081e0-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="081e0-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="081e0-158">Se especificado, retornará funções atribuídas diretamente ao usuário e aos grupos dos quais o usuário é membro (transitamente).</span><span class="sxs-lookup"><span data-stu-id="081e0-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="081e0-159">Com suporte apenas para uma entidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="081e0-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="081e0-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="081e0-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="081e0-161">Se especificado, também lista atribuições de função de administradores de assinatura (co-administradores, administradores de serviço etc.).</span><span class="sxs-lookup"><span data-stu-id="081e0-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="081e0-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="081e0-162">-ObjectId</span></span>
<span data-ttu-id="081e0-163">O ObjectId do Azure AD do Usuário, Grupo ou Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="081e0-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="081e0-164">Filtra todas as atribuições que são feitas para o diretor especificado.</span><span class="sxs-lookup"><span data-stu-id="081e0-164">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="081e0-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="081e0-165">-ParentResource</span></span>
<span data-ttu-id="081e0-166">O recurso pai na hierarquia do recurso especificado usando o parâmetro ResourceName.</span><span class="sxs-lookup"><span data-stu-id="081e0-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="081e0-167">Deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="081e0-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="081e0-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="081e0-168">-ResourceGroupName</span></span>
<span data-ttu-id="081e0-169">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="081e0-169">The resource group name.</span></span>
<span data-ttu-id="081e0-170">Lista as atribuições de função que são eficazes no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="081e0-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="081e0-171">Quando usado em conjunto com parâmetros ResourceName, ResourceType e ParentResource, o comando lista atribuições efetivas em recursos dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="081e0-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="081e0-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="081e0-172">-ResourceName</span></span>
<span data-ttu-id="081e0-173">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="081e0-173">The resource name.</span></span>
<span data-ttu-id="081e0-174">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="081e0-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="081e0-175">Deve ser usado em conjunto com os parâmetros ResourceGroupName, ResourceType e (opcionalmente)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="081e0-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="081e0-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="081e0-176">-ResourceType</span></span>
<span data-ttu-id="081e0-177">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="081e0-177">The resource type.</span></span>
<span data-ttu-id="081e0-178">Por exemplo, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="081e0-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="081e0-179">Deve ser usado em conjunto com ResourceGroupName, ResourceName e (opcionalmente)Parâmetros ParentResource.</span><span class="sxs-lookup"><span data-stu-id="081e0-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="081e0-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="081e0-180">-RoleDefinitionId</span></span>
<span data-ttu-id="081e0-181">ID da Função atribuída ao diretor.</span><span class="sxs-lookup"><span data-stu-id="081e0-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="081e0-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="081e0-182">-RoleDefinitionName</span></span>
<span data-ttu-id="081e0-183">Função atribuída à entidade, ou seja, Leitor, Colaborador, Administrador de Rede Virtual, etc.</span><span class="sxs-lookup"><span data-stu-id="081e0-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="081e0-184">-Escopo</span><span class="sxs-lookup"><span data-stu-id="081e0-184">-Scope</span></span>
<span data-ttu-id="081e0-185">O Escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="081e0-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="081e0-186">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="081e0-186">In the format of relative URI.</span></span>
<span data-ttu-id="081e0-187">Por exemplo, /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="081e0-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="081e0-188">Ele deve começar com "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="081e0-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="081e0-189">O comando filtra todas as atribuições que são eficazes nesse escopo.</span><span class="sxs-lookup"><span data-stu-id="081e0-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="081e0-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="081e0-190">-ServicePrincipalName</span></span>
<span data-ttu-id="081e0-191">O ServicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="081e0-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="081e0-192">Filtra todas as atribuições que são feitas para o aplicativo Azure AD especificado.</span><span class="sxs-lookup"><span data-stu-id="081e0-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="081e0-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="081e0-193">-SignInName</span></span>
<span data-ttu-id="081e0-194">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="081e0-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="081e0-195">Filtra todas as atribuições feitas ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="081e0-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="081e0-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081e0-196">CommonParameters</span></span>
<span data-ttu-id="081e0-197">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081e0-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081e0-198">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="081e0-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081e0-199">Entradas</span><span class="sxs-lookup"><span data-stu-id="081e0-199">INPUTS</span></span>

### <span data-ttu-id="081e0-200">System.String</span><span class="sxs-lookup"><span data-stu-id="081e0-200">System.String</span></span>

### <span data-ttu-id="081e0-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="081e0-201">System.Guid</span></span>

## <span data-ttu-id="081e0-202">Saídas</span><span class="sxs-lookup"><span data-stu-id="081e0-202">OUTPUTS</span></span>

### <span data-ttu-id="081e0-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="081e0-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="081e0-204">Notas</span><span class="sxs-lookup"><span data-stu-id="081e0-204">NOTES</span></span>
<span data-ttu-id="081e0-205">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="081e0-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="081e0-206">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="081e0-206">RELATED LINKS</span></span>

[<span data-ttu-id="081e0-207">Novo-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="081e0-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="081e0-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="081e0-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="081e0-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="081e0-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

