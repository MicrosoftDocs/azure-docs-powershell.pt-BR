---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271656"
---
# <span data-ttu-id="0892e-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="0892e-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="0892e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0892e-102">SYNOPSIS</span></span>
<span data-ttu-id="0892e-103">Cria e inicia uma correção de política para uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="0892e-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="0892e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0892e-104">SYNTAX</span></span>

### <span data-ttu-id="0892e-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0892e-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0892e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0892e-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0892e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0892e-107">DESCRIPTION</span></span>
<span data-ttu-id="0892e-108">O cmdlet **Start-AzPolicyRemediation** cria uma correção de política para uma determinada atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="0892e-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="0892e-109">Todos os recursos não compatíveis no escopo da correção serão corrigidos ou abaixo.</span><span class="sxs-lookup"><span data-stu-id="0892e-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="0892e-110">A correção só tem suporte para políticas com o efeito ' deployIfNotExists '.</span><span class="sxs-lookup"><span data-stu-id="0892e-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="0892e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0892e-111">EXAMPLES</span></span>

### <span data-ttu-id="0892e-112">Exemplo 1: iniciar uma correção em escopo de assinatura</span><span class="sxs-lookup"><span data-stu-id="0892e-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="0892e-113">Esse comando cria uma nova correção de política na "minha assinatura" da assinatura para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="0892e-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="0892e-114">Exemplo 2: iniciar uma correção no escopo do grupo de gerenciamento com filtros opcionais</span><span class="sxs-lookup"><span data-stu-id="0892e-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="0892e-115">Esse comando cria uma nova correção de política no grupo de gerenciamento ' MG1 ' para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="0892e-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="0892e-116">Somente os recursos nos locais "oesteus" ou "eastus" serão corrigidos.</span><span class="sxs-lookup"><span data-stu-id="0892e-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="0892e-117">Exemplo 3: iniciar uma correção em escopo de grupo de recursos para uma atribuição de definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="0892e-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="0892e-118">Esse comando cria uma nova correção de política no grupo de recursos "myRG" para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="0892e-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="0892e-119">A atribuição de política atribui uma definição de conjunto de políticas (também conhecida como uma iniciativa).</span><span class="sxs-lookup"><span data-stu-id="0892e-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="0892e-120">A ID de referência de definição de política indica qual política na iniciativa deve ser corrigida.</span><span class="sxs-lookup"><span data-stu-id="0892e-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="0892e-121">Exemplo 4: iniciar uma correção e aguardar para que ela seja concluída em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0892e-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="0892e-122">Esse comando inicia uma nova correção de política na "minha assinatura" da assinatura para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="0892e-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="0892e-123">Ele aguardará a remediação ser concluída antes de retornar o status de correção final.</span><span class="sxs-lookup"><span data-stu-id="0892e-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="0892e-124">Exemplo 5: iniciar uma correção que descobrirá recursos não compatíveis antes de remediar</span><span class="sxs-lookup"><span data-stu-id="0892e-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="0892e-125">Esse comando cria uma nova correção de política na "minha assinatura" da assinatura para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="0892e-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="0892e-126">O estado de conformidade dos recursos na assinatura será reavaliado em relação à atribuição de política e os recursos não compatíveis serão corrigidos.</span><span class="sxs-lookup"><span data-stu-id="0892e-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="0892e-127">OS</span><span class="sxs-lookup"><span data-stu-id="0892e-127">PARAMETERS</span></span>

### <span data-ttu-id="0892e-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0892e-128">-AsJob</span></span>
<span data-ttu-id="0892e-129">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0892e-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0892e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0892e-130">-DefaultProfile</span></span>
<span data-ttu-id="0892e-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0892e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0892e-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="0892e-132">-LocationFilter</span></span>
<span data-ttu-id="0892e-133">Os locais de recursos que devem ser incluídos na correção.</span><span class="sxs-lookup"><span data-stu-id="0892e-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="0892e-134">Os recursos que não residem nesses locais não serão corrigidos.</span><span class="sxs-lookup"><span data-stu-id="0892e-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="0892e-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0892e-135">-ManagementGroupName</span></span>
<span data-ttu-id="0892e-136">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="0892e-136">Management group ID.</span></span>

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

### <span data-ttu-id="0892e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="0892e-137">-Name</span></span>
<span data-ttu-id="0892e-138">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0892e-138">Resource name.</span></span>

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

### <span data-ttu-id="0892e-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="0892e-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="0892e-140">ID da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="0892e-140">Policy assignment ID.</span></span>
<span data-ttu-id="0892e-141">:.</span><span class="sxs-lookup"><span data-stu-id="0892e-141">E.g.</span></span>
<span data-ttu-id="0892e-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="0892e-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="0892e-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="0892e-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="0892e-144">Obtém a ID de referência da definição de política da definição individual que está sendo remediada.</span><span class="sxs-lookup"><span data-stu-id="0892e-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="0892e-145">Obrigatório quando a atribuição de política atribui uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="0892e-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="0892e-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="0892e-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="0892e-147">Descreve como a tarefa de correção irá descobrir recursos que precisam ser corrigidos.</span><span class="sxs-lookup"><span data-stu-id="0892e-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="0892e-148">Não há suporte para ReEvaluateCompliance ao corrigir escopos do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="0892e-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="0892e-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0892e-149">-ResourceGroupName</span></span>
<span data-ttu-id="0892e-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0892e-150">Resource group name.</span></span>

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

### <span data-ttu-id="0892e-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0892e-151">-ResourceId</span></span>
<span data-ttu-id="0892e-152">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0892e-152">Resource ID.</span></span>

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

### <span data-ttu-id="0892e-153">-Escopo</span><span class="sxs-lookup"><span data-stu-id="0892e-153">-Scope</span></span>
<span data-ttu-id="0892e-154">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="0892e-154">Scope of the resource.</span></span>
<span data-ttu-id="0892e-155">:.</span><span class="sxs-lookup"><span data-stu-id="0892e-155">E.g.</span></span>
<span data-ttu-id="0892e-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="0892e-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="0892e-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0892e-157">-Confirm</span></span>
<span data-ttu-id="0892e-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0892e-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0892e-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0892e-159">-WhatIf</span></span>
<span data-ttu-id="0892e-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0892e-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0892e-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0892e-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0892e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0892e-162">CommonParameters</span></span>
<span data-ttu-id="0892e-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0892e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0892e-164">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0892e-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0892e-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0892e-165">INPUTS</span></span>

### <span data-ttu-id="0892e-166">System. String</span><span class="sxs-lookup"><span data-stu-id="0892e-166">System.String</span></span>

### <span data-ttu-id="0892e-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="0892e-167">System.String[]</span></span>

## <span data-ttu-id="0892e-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0892e-168">OUTPUTS</span></span>

### <span data-ttu-id="0892e-169">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="0892e-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="0892e-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0892e-170">NOTES</span></span>

## <span data-ttu-id="0892e-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0892e-171">RELATED LINKS</span></span>
