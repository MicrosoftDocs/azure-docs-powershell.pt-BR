---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: aeb86609e06417147f5ef4600c430665f28da454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890103"
---
# <span data-ttu-id="9f2cc-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="9f2cc-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="9f2cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2cc-103">Cria e inicia uma correção de política para uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="9f2cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9f2cc-104">SYNTAX</span></span>

### <span data-ttu-id="9f2cc-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f2cc-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2cc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2cc-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f2cc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9f2cc-107">DESCRIPTION</span></span>
<span data-ttu-id="9f2cc-108">O cmdlet **Start-AzPolicyRemediation** cria uma correção de política para uma atribuição de política específica.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="9f2cc-109">Todos os recursos não compatíveis em ou abaixo do escopo da correção serão remediados.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="9f2cc-110">A correção só é suportada para políticas com o efeito "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="9f2cc-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="9f2cc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f2cc-111">EXAMPLES</span></span>

### <span data-ttu-id="9f2cc-112">Exemplo 1: Iniciar uma correção no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="9f2cc-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="9f2cc-113">Este comando cria uma nova correção de política na assinatura "Minha Assinatura" para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="9f2cc-114">Exemplo 2: Iniciar uma correção no escopo do grupo de gerenciamento com filtros opcionais</span><span class="sxs-lookup"><span data-stu-id="9f2cc-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="9f2cc-115">Este comando cria uma nova correção de política no grupo de gerenciamento 'mg1' para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="9f2cc-116">Somente recursos nos locais 'westus' ou 'eastus' serão remediados.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="9f2cc-117">Exemplo 3: Iniciar uma correção no escopo do grupo de recursos para uma atribuição de definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="9f2cc-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="9f2cc-118">Este comando cria uma nova correção de política no grupo de recursos "myRG" para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="9f2cc-119">A atribuição de política atribui uma definição de conjunto de políticas (também conhecida como uma iniciativa).</span><span class="sxs-lookup"><span data-stu-id="9f2cc-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="9f2cc-120">A ID de referência de definição de política indica qual política dentro da iniciativa deve ser remediada.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="9f2cc-121">Exemplo 4: Iniciar uma correção e aguardar que ela seja concluída em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9f2cc-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="9f2cc-122">Este comando inicia uma nova correção de política na assinatura "Minha Assinatura" para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="9f2cc-123">Ele aguardará a conclusão da correção antes de retornar o status final de correção.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="9f2cc-124">Exemplo 5: Inicie uma correção que descobrirá recursos não compatíveis antes de remediar</span><span class="sxs-lookup"><span data-stu-id="9f2cc-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="9f2cc-125">Este comando cria uma nova correção de política na assinatura "Minha Assinatura" para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="9f2cc-126">O estado de conformidade dos recursos na assinatura será reavaliado em relação à atribuição de política e os recursos não compatíveis serão remediados.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="9f2cc-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9f2cc-127">PARAMETERS</span></span>

### <span data-ttu-id="9f2cc-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f2cc-128">-AsJob</span></span>
<span data-ttu-id="9f2cc-129">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9f2cc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2cc-130">-DefaultProfile</span></span>
<span data-ttu-id="9f2cc-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f2cc-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="9f2cc-132">-LocationFilter</span></span>
<span data-ttu-id="9f2cc-133">Os locais de recursos que devem ser incluídos na correção.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="9f2cc-134">Os recursos que não residem nesses locais não serão remediados.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-134">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2cc-135">-ManagementGroupName</span></span>
<span data-ttu-id="9f2cc-136">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-136">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-137">-Name</span><span class="sxs-lookup"><span data-stu-id="9f2cc-137">-Name</span></span>
<span data-ttu-id="9f2cc-138">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-138">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="9f2cc-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="9f2cc-140">ID da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-140">Policy assignment ID.</span></span>
<span data-ttu-id="9f2cc-141">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="9f2cc-141">E.g.</span></span>
<span data-ttu-id="9f2cc-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="9f2cc-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="9f2cc-144">Obtém a ID de referência de definição de política da definição individual que está sendo remediada.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="9f2cc-145">Obrigatório quando a atribuição de política atribui uma definição de conjunto de política.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-145">Required when the policy assignment assigns a policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="9f2cc-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="9f2cc-147">Descreve como a tarefa de correção descobrirá recursos que precisam ser remediados.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="9f2cc-148">ReEvaluateCompliance não é suportado ao remediar escopos de grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2cc-149">-ResourceGroupName</span></span>
<span data-ttu-id="9f2cc-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-150">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2cc-151">-ResourceId</span></span>
<span data-ttu-id="9f2cc-152">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-152">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="9f2cc-153">-Scope</span></span>
<span data-ttu-id="9f2cc-154">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-154">Scope of the resource.</span></span>
<span data-ttu-id="9f2cc-155">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="9f2cc-155">E.g.</span></span>
<span data-ttu-id="9f2cc-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2cc-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f2cc-157">-Confirm</span></span>
<span data-ttu-id="9f2cc-158">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f2cc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f2cc-159">-WhatIf</span></span>
<span data-ttu-id="9f2cc-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f2cc-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f2cc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2cc-162">CommonParameters</span></span>
<span data-ttu-id="9f2cc-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2cc-164">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f2cc-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2cc-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f2cc-165">INPUTS</span></span>

### <span data-ttu-id="9f2cc-166">System.String</span><span class="sxs-lookup"><span data-stu-id="9f2cc-166">System.String</span></span>

### <span data-ttu-id="9f2cc-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9f2cc-167">System.String[]</span></span>

## <span data-ttu-id="9f2cc-168">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9f2cc-168">OUTPUTS</span></span>

### <span data-ttu-id="9f2cc-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="9f2cc-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="9f2cc-170">NOTES</span><span class="sxs-lookup"><span data-stu-id="9f2cc-170">NOTES</span></span>

## <span data-ttu-id="9f2cc-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f2cc-171">RELATED LINKS</span></span>
