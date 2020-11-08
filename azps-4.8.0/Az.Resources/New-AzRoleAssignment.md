---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 2ec39bc66b3b027cb7b5ef9dda09734f8aaf457a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110966"
---
# <span data-ttu-id="303cf-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="303cf-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="303cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="303cf-102">SYNOPSIS</span></span>
<span data-ttu-id="303cf-103">Atribui a função RBAC especificada à entidade de segurança especificada, no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="303cf-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="303cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="303cf-104">SYNTAX</span></span>

### <span data-ttu-id="303cf-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="303cf-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="303cf-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="303cf-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="303cf-116">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="303cf-116">DESCRIPTION</span></span>
<span data-ttu-id="303cf-117">Use o comando New-AzRoleAssignment para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="303cf-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="303cf-118">O Access é concedido atribuindo a função RBAC apropriada a ele no escopo certo.</span><span class="sxs-lookup"><span data-stu-id="303cf-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="303cf-119">Para conceder acesso à assinatura inteira, atribua uma função no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="303cf-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="303cf-120">Para conceder acesso a um grupo de recursos específico em uma assinatura, atribua uma função no escopo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="303cf-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="303cf-121">O assunto da tarefa deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="303cf-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="303cf-122">Para especificar um usuário, use SignInName ou os parâmetros do ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="303cf-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="303cf-123">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="303cf-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="303cf-124">E para especificar um aplicativo do Azure AD, use parâmetros ApplicationId ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="303cf-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="303cf-125">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="303cf-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="303cf-126">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="303cf-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="303cf-127">O padrão é a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="303cf-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="303cf-128">O escopo da atribuição pode ser especificado usando-se uma das combinações de parâmetro a seguir.</span><span class="sxs-lookup"><span data-stu-id="303cf-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="303cf-129">Scope-este é o escopo totalmente qualificado começando com/subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="303cf-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="303cf-130">ResourceGroupName-para conceder acesso ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="303cf-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="303cf-131">partição.</span><span class="sxs-lookup"><span data-stu-id="303cf-131">c.</span></span>
<span data-ttu-id="303cf-132">ResourceFile, ResourceType, ResourceGroupName e (opcionalmente) ParentResource-para especificar um determinado recurso dentro de um grupo de recursos para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="303cf-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="303cf-133">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="303cf-133">EXAMPLES</span></span>

### <span data-ttu-id="303cf-134">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="303cf-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="303cf-135">Conceder acesso à função de leitor a um usuário em um escopo de grupo de recursos com a atribuição de função disponível para delegação</span><span class="sxs-lookup"><span data-stu-id="303cf-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="303cf-136">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="303cf-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="303cf-137">Conceder acesso a um grupo de segurança</span><span class="sxs-lookup"><span data-stu-id="303cf-137">Grant access to a security group</span></span>

### <span data-ttu-id="303cf-138">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="303cf-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="303cf-139">Conceder acesso a um usuário em um recurso (website)</span><span class="sxs-lookup"><span data-stu-id="303cf-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="303cf-140">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="303cf-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="303cf-141">Conceder acesso a um grupo em um recurso aninhado (sub-rede)</span><span class="sxs-lookup"><span data-stu-id="303cf-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="303cf-142">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="303cf-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="303cf-143">Conceder acesso de leitor a uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="303cf-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="303cf-144">OS</span><span class="sxs-lookup"><span data-stu-id="303cf-144">PARAMETERS</span></span>

### <span data-ttu-id="303cf-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="303cf-145">-AllowDelegation</span></span>
<span data-ttu-id="303cf-146">O sinalizador de delegação ao criar uma atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="303cf-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="303cf-147">-ApplicationId</span></span>
<span data-ttu-id="303cf-148">A ID do aplicativo do servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="303cf-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-149">-Condition</span><span class="sxs-lookup"><span data-stu-id="303cf-149">-Condition</span></span>
<span data-ttu-id="303cf-150">Condição a ser aplicada ao RoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="303cf-150">Condition to be applied to the RoleAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="303cf-151">-ConditionVersion</span></span>
<span data-ttu-id="303cf-152">Versão da condição.</span><span class="sxs-lookup"><span data-stu-id="303cf-152">Version of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303cf-153">-DefaultProfile</span></span>
<span data-ttu-id="303cf-154">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="303cf-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="303cf-155">-Descrição</span><span class="sxs-lookup"><span data-stu-id="303cf-155">-Description</span></span>
<span data-ttu-id="303cf-156">Breve descrição da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="303cf-156">Brief description of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="303cf-157">-InputFile</span></span>
<span data-ttu-id="303cf-158">Caminho para a atribuição de função JSON</span><span class="sxs-lookup"><span data-stu-id="303cf-158">Path to role assignment json</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="303cf-159">-ObjectId</span></span>
<span data-ttu-id="303cf-160">ObjectID do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="303cf-160">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="303cf-161">-ParentResource</span></span>
<span data-ttu-id="303cf-162">O recurso pai na hierarquia (do recurso especificado usando o parâmetro ResourceManager).</span><span class="sxs-lookup"><span data-stu-id="303cf-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="303cf-163">Só deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e resourceName para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="303cf-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="303cf-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303cf-164">-ResourceGroupName</span></span>
<span data-ttu-id="303cf-165">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="303cf-165">The resource group name.</span></span>
<span data-ttu-id="303cf-166">Cria uma tarefa que é eficaz no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="303cf-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="303cf-167">Quando usado em conjunto com os parâmetros ResourceFile, ResourceType e (opcionalmente) ParentResource, o comando constrói um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="303cf-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="303cf-168">-ResourceName</span></span>
<span data-ttu-id="303cf-169">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="303cf-169">The resource name.</span></span>
<span data-ttu-id="303cf-170">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="303cf-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="303cf-171">Só deve ser usado em conjunto com ResourceGroupName, ResourceType e (opcionalmente) ParentResource parâmetros para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="303cf-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="303cf-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="303cf-172">-ResourceType</span></span>
<span data-ttu-id="303cf-173">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="303cf-173">The resource type.</span></span>
<span data-ttu-id="303cf-174">Por exemplo, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="303cf-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="303cf-175">Só deve ser usado em conjunto com ResourceGroupName, ResourceManager e (opcionalmente) ParentResource parâmetros para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="303cf-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="303cf-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="303cf-176">-RoleDefinitionId</span></span>
<span data-ttu-id="303cf-177">ID da função RBAC que precisa ser atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="303cf-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="303cf-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="303cf-178">-RoleDefinitionName</span></span>
<span data-ttu-id="303cf-179">Nome da função RBAC que precisa ser atribuída à entidade de segurança, ou seja, leitor, colaborador, administrador de rede virtual etc.</span><span class="sxs-lookup"><span data-stu-id="303cf-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-180">-Escopo</span><span class="sxs-lookup"><span data-stu-id="303cf-180">-Scope</span></span>
<span data-ttu-id="303cf-181">O escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="303cf-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="303cf-182">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="303cf-182">In the format of relative URI.</span></span>
<span data-ttu-id="303cf-183">Por exemplo, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="303cf-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="303cf-184">Se não for especificado, criará a atribuição de função no nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="303cf-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="303cf-185">Se especificado, ele deve começar com "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="303cf-185">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="303cf-186">-SignInName</span></span>
<span data-ttu-id="303cf-187">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="303cf-187">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303cf-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303cf-188">CommonParameters</span></span>
<span data-ttu-id="303cf-189">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303cf-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303cf-190">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="303cf-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303cf-191">SENSORES</span><span class="sxs-lookup"><span data-stu-id="303cf-191">INPUTS</span></span>

### <span data-ttu-id="303cf-192">System. String</span><span class="sxs-lookup"><span data-stu-id="303cf-192">System.String</span></span>

### <span data-ttu-id="303cf-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="303cf-193">System.Guid</span></span>

## <span data-ttu-id="303cf-194">EXIBE</span><span class="sxs-lookup"><span data-stu-id="303cf-194">OUTPUTS</span></span>

### <span data-ttu-id="303cf-195">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="303cf-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="303cf-196">INFORMA</span><span class="sxs-lookup"><span data-stu-id="303cf-196">NOTES</span></span>
<span data-ttu-id="303cf-197">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="303cf-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="303cf-198">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="303cf-198">RELATED LINKS</span></span>

[<span data-ttu-id="303cf-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="303cf-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="303cf-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="303cf-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="303cf-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="303cf-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
