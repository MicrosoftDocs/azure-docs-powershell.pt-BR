---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: c3988727e8afd54dddea9719c348222c41f47503
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430665"
---
# <span data-ttu-id="cecd1-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cecd1-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="cecd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cecd1-102">SYNOPSIS</span></span>
<span data-ttu-id="cecd1-103">Atribui a função RBAC especificada à entidade de segurança especificada, no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="cecd1-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cecd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cecd1-104">SYNTAX</span></span>

### <span data-ttu-id="cecd1-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cecd1-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecd1-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cecd1-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cecd1-116">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cecd1-116">DESCRIPTION</span></span>
<span data-ttu-id="cecd1-117">Use o comando New-AzureRMRoleAssignment para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="cecd1-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="cecd1-118">O Access é concedido atribuindo a função RBAC apropriada a ele no escopo certo.</span><span class="sxs-lookup"><span data-stu-id="cecd1-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="cecd1-119">Para conceder acesso à assinatura inteira, atribua uma função no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="cecd1-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="cecd1-120">Para conceder acesso a um grupo de recursos específico em uma assinatura, atribua uma função no escopo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cecd1-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>

<span data-ttu-id="cecd1-121">O assunto da tarefa deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="cecd1-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="cecd1-122">Para especificar um usuário, use SignInName ou os parâmetros do ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cecd1-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="cecd1-123">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cecd1-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="cecd1-124">E para especificar um aplicativo do Azure AD, use os parâmetros servicePrincipalName ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="cecd1-124">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="cecd1-125">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="cecd1-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="cecd1-126">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="cecd1-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="cecd1-127">O padrão é a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="cecd1-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="cecd1-128">O escopo da atribuição pode ser especificado usando-se uma das combinações de parâmetro a seguir.</span><span class="sxs-lookup"><span data-stu-id="cecd1-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="cecd1-129">Scope-este é o escopo totalmente qualificado começando com/subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="cecd1-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="cecd1-130">ResourceGroupName-para conceder acesso ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="cecd1-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="cecd1-131">partição.</span><span class="sxs-lookup"><span data-stu-id="cecd1-131">c.</span></span>
<span data-ttu-id="cecd1-132">ResourceFile, ResourceType, ResourceGroupName e (opcionalmente) ParentResource-para especificar um determinado recurso dentro de um grupo de recursos para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="cecd1-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="cecd1-133">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cecd1-133">EXAMPLES</span></span>

### <span data-ttu-id="cecd1-134">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cecd1-134">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader
```

<span data-ttu-id="cecd1-135">Conceder acesso à função de leitor a um usuário em um escopo de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cecd1-135">Grant Reader role access to a user at a resource group scope</span></span>

### <span data-ttu-id="cecd1-136">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cecd1-136">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           ObjectId
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="cecd1-137">Conceder acesso a um grupo de segurança</span><span class="sxs-lookup"><span data-stu-id="cecd1-137">Grant access to a security group</span></span>

### <span data-ttu-id="cecd1-138">--------------------------Exemplo 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="cecd1-138">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="cecd1-139">Conceder acesso a um usuário em um recurso (website)</span><span class="sxs-lookup"><span data-stu-id="cecd1-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="cecd1-140">--------------------------Exemplo 4--------------------------</span><span class="sxs-lookup"><span data-stu-id="cecd1-140">--------------------------  Example 4  --------------------------</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="cecd1-141">Conceder acesso a um grupo em um recurso aninhado (sub-rede)</span><span class="sxs-lookup"><span data-stu-id="cecd1-141">Grant access to a group at a nested resource (subnet)</span></span>

## <span data-ttu-id="cecd1-142">OS</span><span class="sxs-lookup"><span data-stu-id="cecd1-142">PARAMETERS</span></span>

### <span data-ttu-id="cecd1-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cecd1-143">-ObjectId</span></span>
<span data-ttu-id="cecd1-144">ObjectID do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="cecd1-144">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecd1-145">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="cecd1-145">-ParentResource</span></span>
<span data-ttu-id="cecd1-146">O recurso pai na hierarquia (do recurso especificado usando o parâmetro ResourceManager).</span><span class="sxs-lookup"><span data-stu-id="cecd1-146">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="cecd1-147">Só deve ser usado em conjunto com parâmetros ResourceGroupName, ResourceType e resourceName para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="cecd1-147">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="cecd1-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cecd1-148">-ResourceGroupName</span></span>
<span data-ttu-id="cecd1-149">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cecd1-149">The resource group name.</span></span>
<span data-ttu-id="cecd1-150">Cria uma tarefa que é eficaz no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="cecd1-150">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="cecd1-151">Quando usado em conjunto com os parâmetros ResourceFile, ResourceType e (opcionalmente) ParentResource, o comando constrói um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="cecd1-151">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="cecd1-152">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cecd1-152">-ResourceName</span></span>
<span data-ttu-id="cecd1-153">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cecd1-153">The resource name.</span></span>
<span data-ttu-id="cecd1-154">Por exemplo, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="cecd1-154">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="cecd1-155">Só deve ser usado em conjunto com ResourceGroupName, ResourceType e (opcionalmente) ParentResource parâmetros para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="cecd1-155">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="cecd1-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cecd1-156">-ResourceType</span></span>
<span data-ttu-id="cecd1-157">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="cecd1-157">The resource type.</span></span>
<span data-ttu-id="cecd1-158">Por exemplo, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="cecd1-158">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="cecd1-159">Só deve ser usado em conjunto com ResourceGroupName, ResourceManager e (opcionalmente) ParentResource parâmetros para construir um escopo hierárquico na forma de um URI relativo que identifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="cecd1-159">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="cecd1-160">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="cecd1-160">-RoleDefinitionId</span></span>
<span data-ttu-id="cecd1-161">ID da função RBAC que precisa ser atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="cecd1-161">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="cecd1-162">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="cecd1-162">-RoleDefinitionName</span></span>
<span data-ttu-id="cecd1-163">Nome da função RBAC que precisa ser atribuída à entidade de segurança, ou seja, leitor, colaborador, administrador de rede virtual etc.</span><span class="sxs-lookup"><span data-stu-id="cecd1-163">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecd1-164">-Escopo</span><span class="sxs-lookup"><span data-stu-id="cecd1-164">-Scope</span></span>
<span data-ttu-id="cecd1-165">O escopo da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="cecd1-165">The Scope of the role assignment.</span></span>
<span data-ttu-id="cecd1-166">No formato de URI relativo.</span><span class="sxs-lookup"><span data-stu-id="cecd1-166">In the format of relative URI.</span></span>
<span data-ttu-id="cecd1-167">Por exemplo, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="cecd1-167">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="cecd1-168">Se não for especificado, criará a atribuição de função no nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cecd1-168">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="cecd1-169">Se especificado, ele deve começar com "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="cecd1-169">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecd1-170">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="cecd1-170">-ServicePrincipalName</span></span>
<span data-ttu-id="cecd1-171">O servicePrincipalName do aplicativo Azure AD</span><span class="sxs-lookup"><span data-stu-id="cecd1-171">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecd1-172">-SignInName</span><span class="sxs-lookup"><span data-stu-id="cecd1-172">-SignInName</span></span>
<span data-ttu-id="cecd1-173">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="cecd1-173">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="cecd1-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cecd1-174">-DefaultProfile</span></span>
<span data-ttu-id="cecd1-175">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cecd1-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cecd1-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cecd1-176">CommonParameters</span></span>
<span data-ttu-id="cecd1-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cecd1-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cecd1-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cecd1-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cecd1-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cecd1-179">INPUTS</span></span>

## <span data-ttu-id="cecd1-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cecd1-180">OUTPUTS</span></span>

### <span data-ttu-id="cecd1-181">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cecd1-181">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="cecd1-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cecd1-182">NOTES</span></span>
<span data-ttu-id="cecd1-183">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="cecd1-183">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="cecd1-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cecd1-184">RELATED LINKS</span></span>

[<span data-ttu-id="cecd1-185">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cecd1-185">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="cecd1-186">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cecd1-186">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="cecd1-187">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cecd1-187">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
