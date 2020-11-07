---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: d060119b4bdf04d5021eb1334c0b4c2e2d3567a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943494"
---
# <span data-ttu-id="ab299-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ab299-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="ab299-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab299-102">SYNOPSIS</span></span>
<span data-ttu-id="ab299-103">Atribui a função RBAC especificada à entidade de segurança especificada, no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="ab299-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="ab299-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab299-104">SYNTAX</span></span>

### <span data-ttu-id="ab299-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab299-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab299-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab299-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab299-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab299-115">DESCRIPTION</span></span>
<span data-ttu-id="ab299-116">Use o comando New-AzRoleAssignment para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="ab299-116">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="ab299-117">O Access é concedido atribuindo a função RBAC apropriada a ele no escopo certo.</span><span class="sxs-lookup"><span data-stu-id="ab299-117">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="ab299-118">Para conceder acesso à assinatura inteira, atribua uma função no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ab299-118">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="ab299-119">Para conceder acesso a um grupo de recursos específico em uma assinatura, atribua uma função no escopo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ab299-119">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="ab299-120">O assunto da tarefa deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="ab299-120">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="ab299-121">Para especificar um usuário, use SignInName ou os parâmetros do ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ab299-121">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="ab299-122">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ab299-122">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="ab299-123">E para especificar um aplicativo do Azure AD, use parâmetros ApplicationId ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="ab299-123">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="ab299-124">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="ab299-124">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="ab299-125">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="ab299-125">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="ab299-126">O padrão é a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="ab299-126">It defaults to the selected subscription.</span></span> <span data-ttu-id="ab299-127">O escopo da atribuição pode ser especificado usando-se uma das combinações de parâmetro a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab299-127">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="ab299-128">Scope-este é o escopo totalmente qualificado começando com/subscriptions/ \< SubscriptionId \> b.</span><span class="sxs-lookup"><span data-stu-id="ab299-128">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="ab299-129">ResourceGroupName-para conceder acesso ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ab299-129">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="ab299-130">partição.</span><span class="sxs-lookup"><span data-stu-id="ab299-130">c.</span></span>
<span data-ttu-id="ab299-131">ResourceFile, ResourceType, ResourceGroupName e (opcionalmente) ParentResource-para especificar um determinado recurso dentro de um grupo de recursos para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="ab299-131">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="ab299-132">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab299-132">EXAMPLES</span></span>

### <span data-ttu-id="ab299-133">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab299-133">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="ab299-134">Conceder acesso à função de leitor a um usuário em um escopo de grupo de recursos com a atribuição de função disponível para delegação</span><span class="sxs-lookup"><span data-stu-id="ab299-134">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="ab299-135">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ab299-135">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="ab299-136">Conceder acesso a um grupo de segurança</span><span class="sxs-lookup"><span data-stu-id="ab299-136">Grant access to a security group</span></span>

### <span data-ttu-id="ab299-137">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ab299-137">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="ab299-138">Conceder acesso a um usuário em um recurso (website)</span><span class="sxs-lookup"><span data-stu-id="ab299-138">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="ab299-139">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ab299-139">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="ab299-140">Conceder acesso a um grupo em um recurso aninhado (sub-rede)</span><span class="sxs-lookup"><span data-stu-id="ab299-140">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="ab299-141">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="ab299-141">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="ab299-142">Conceder acesso de leitor a uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="ab299-142">Grant reader access to a service principal</span></span>

## <span data-ttu-id="ab299-143">OS</span><span class="sxs-lookup"><span data-stu-id="ab299-143">PARAMETERS</span></span>

### <span data-ttu-id="ab299-144">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="ab299-144">-AllowDelegation</span></span>
<span data-ttu-id="ab299-145">O sinalizador de delegação ao criar uma atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="ab299-145">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="ab299-146">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ab299-146">-ApplicationId</span></span>
<span data-ttu-id="ab299-147">A ID do aplicativo do servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ab299-147">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="ab299-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab299-148">-DefaultProfile</span></span>
<span data-ttu-id="ab299-149">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ab299-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab299-150">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ab299-150">-ObjectId</span></span>
<span data-ttu-id="ab299-151">ObjectID do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ab299-151">Azure AD Objectid of the user, group or service principal.</span></span>

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

### <span data-ttu-id="ab299-152">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="ab299-152">-ParentResource</span></span>
<span data-ttu-id="ab299-153">O recurso pai na hierarquia (do recurso especificado usando o parâmetro ResourceManager).</span><span class="sxs-lookup"><span data-stu-id="ab299-153">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="ab299-154">Só deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e resourceName para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="ab299-154">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ab299-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab299-155">-ResourceGroupName</span></span>
<span data-ttu-id="ab299-156">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ab299-156">The resource group name.</span></span>
<span data-ttu-id="ab299-157">Cria uma tarefa que é eficaz no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ab299-157">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="ab299-158">Quando usado em conjunto com os parâmetros ResourceFile, ResourceType e (opcionalmente) ParentResource, o comando constrói um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="ab299-158">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ab299-159">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ab299-159">-ResourceName</span></span>
<span data-ttu-id="ab299-160">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ab299-160">The resource name.</span></span>
<span data-ttu-id="ab299-161">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="ab299-161">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="ab299-162">Só deve ser usado em conjunto com ResourceGroupName, ResourceType e (opcionalmente) ParentResource parâmetros para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="ab299-162">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ab299-163">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ab299-163">-ResourceType</span></span>
<span data-ttu-id="ab299-164">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ab299-164">The resource type.</span></span>
<span data-ttu-id="ab299-165">Por exemplo, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="ab299-165">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="ab299-166">Só deve ser usado em conjunto com ResourceGroupName, ResourceManager e (opcionalmente) ParentResource parâmetros para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="ab299-166">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ab299-167">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ab299-167">-RoleDefinitionId</span></span>
<span data-ttu-id="ab299-168">ID da função RBAC que precisa ser atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="ab299-168">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="ab299-169">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ab299-169">-RoleDefinitionName</span></span>
<span data-ttu-id="ab299-170">Nome da função RBAC que precisa ser atribuída à entidade de segurança, ou seja, leitor, colaborador, administrador de rede virtual etc.</span><span class="sxs-lookup"><span data-stu-id="ab299-170">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="ab299-171">-Escopo</span><span class="sxs-lookup"><span data-stu-id="ab299-171">-Scope</span></span>
<span data-ttu-id="ab299-172">O escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="ab299-172">The Scope of the role assignment.</span></span>
<span data-ttu-id="ab299-173">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="ab299-173">In the format of relative URI.</span></span>
<span data-ttu-id="ab299-174">Por exemplo, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="ab299-174">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="ab299-175">Se não for especificado, criará a atribuição de função no nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ab299-175">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="ab299-176">Se especificado, ele deve começar com "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="ab299-176">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="ab299-177">-SignInName</span><span class="sxs-lookup"><span data-stu-id="ab299-177">-SignInName</span></span>
<span data-ttu-id="ab299-178">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="ab299-178">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="ab299-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab299-179">CommonParameters</span></span>
<span data-ttu-id="ab299-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab299-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab299-181">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab299-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab299-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab299-182">INPUTS</span></span>

### <span data-ttu-id="ab299-183">System. String</span><span class="sxs-lookup"><span data-stu-id="ab299-183">System.String</span></span>

### <span data-ttu-id="ab299-184">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ab299-184">System.Guid</span></span>

## <span data-ttu-id="ab299-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab299-185">OUTPUTS</span></span>

### <span data-ttu-id="ab299-186">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ab299-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="ab299-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab299-187">NOTES</span></span>
<span data-ttu-id="ab299-188">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="ab299-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ab299-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab299-189">RELATED LINKS</span></span>

[<span data-ttu-id="ab299-190">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ab299-190">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="ab299-191">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ab299-191">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="ab299-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ab299-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
