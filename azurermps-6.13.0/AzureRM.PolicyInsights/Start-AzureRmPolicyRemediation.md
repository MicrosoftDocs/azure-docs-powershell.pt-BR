---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/start-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
ms.openlocfilehash: d5a0d4cd14f86c782defd7b70a1edee209982d2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428418"
---
# <span data-ttu-id="3581e-101">Start-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="3581e-101">Start-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="3581e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3581e-102">SYNOPSIS</span></span>
<span data-ttu-id="3581e-103">Cria e inicia uma correção de política para uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="3581e-103">Creates and starts a policy remediation for a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3581e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3581e-104">SYNTAX</span></span>

### <span data-ttu-id="3581e-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3581e-105">ByName (Default)</span></span>
```
Start-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3581e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3581e-106">ByResourceId</span></span>
```
Start-AzureRmPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3581e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3581e-107">DESCRIPTION</span></span>
<span data-ttu-id="3581e-108">O cmdlet **Start-AzureRmPolicyRemediation** cria uma correção de política para uma determinada atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="3581e-108">The **Start-AzureRmPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="3581e-109">Todos os recursos não compatíveis no escopo da correção serão corrigidos ou abaixo.</span><span class="sxs-lookup"><span data-stu-id="3581e-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="3581e-110">A correção só tem suporte para políticas com o efeito ' deployIfNotExists '.</span><span class="sxs-lookup"><span data-stu-id="3581e-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="3581e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3581e-111">EXAMPLES</span></span>

### <span data-ttu-id="3581e-112">Exemplo 1: iniciar uma correção em escopo de assinatura</span><span class="sxs-lookup"><span data-stu-id="3581e-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="3581e-113">Esse comando cria uma nova correção de política na "minha assinatura" da assinatura para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="3581e-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="3581e-114">Exemplo 2: iniciar uma correção no escopo do grupo de gerenciamento com filtros opcionais</span><span class="sxs-lookup"><span data-stu-id="3581e-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzureRmPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="3581e-115">Esse comando cria uma nova correção de política no grupo de gerenciamento ' MG1 ' para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="3581e-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="3581e-116">Somente os recursos nos locais "oesteus" ou "eastus" serão corrigidos.</span><span class="sxs-lookup"><span data-stu-id="3581e-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="3581e-117">Exemplo 3: iniciar uma correção em escopo de grupo de recursos para uma atribuição de definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="3581e-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzureRmPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="3581e-118">Esse comando cria uma nova correção de política no grupo de recursos "myRG" para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="3581e-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="3581e-119">A atribuição de política atribui uma definição de conjunto de políticas (também conhecida como uma iniciativa).</span><span class="sxs-lookup"><span data-stu-id="3581e-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="3581e-120">A ID de referência de definição de política indica qual política na iniciativa deve ser corrigida.</span><span class="sxs-lookup"><span data-stu-id="3581e-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="3581e-121">Exemplo 4: iniciar uma correção e aguardar para que ela seja concluída em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3581e-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="3581e-122">Esse comando inicia uma nova correção de política na "minha assinatura" da assinatura para a atribuição de política determinada.</span><span class="sxs-lookup"><span data-stu-id="3581e-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="3581e-123">Ele aguardará a remediação ser concluída antes de retornar o status de correção final.</span><span class="sxs-lookup"><span data-stu-id="3581e-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="3581e-124">OS</span><span class="sxs-lookup"><span data-stu-id="3581e-124">PARAMETERS</span></span>

### <span data-ttu-id="3581e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3581e-125">-AsJob</span></span>
<span data-ttu-id="3581e-126">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="3581e-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3581e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3581e-127">-DefaultProfile</span></span>
<span data-ttu-id="3581e-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3581e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3581e-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="3581e-129">-LocationFilter</span></span>
<span data-ttu-id="3581e-130">Os locais de recursos que devem ser incluídos na correção.</span><span class="sxs-lookup"><span data-stu-id="3581e-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="3581e-131">Os recursos que não residem nesses locais não serão corrigidos.</span><span class="sxs-lookup"><span data-stu-id="3581e-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="3581e-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3581e-132">-ManagementGroupName</span></span>
<span data-ttu-id="3581e-133">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="3581e-133">Management group ID.</span></span>

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

### <span data-ttu-id="3581e-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="3581e-134">-Name</span></span>
<span data-ttu-id="3581e-135">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3581e-135">Resource name.</span></span>

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

### <span data-ttu-id="3581e-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="3581e-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="3581e-137">ID da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="3581e-137">Policy assignment ID.</span></span>
<span data-ttu-id="3581e-138">:.</span><span class="sxs-lookup"><span data-stu-id="3581e-138">E.g.</span></span>
<span data-ttu-id="3581e-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="3581e-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="3581e-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="3581e-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="3581e-141">Obtém a ID de referência da definição de política da definição individual que está sendo remediada.</span><span class="sxs-lookup"><span data-stu-id="3581e-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="3581e-142">Obrigatório quando a atribuição de política atribui uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="3581e-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="3581e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3581e-143">-ResourceGroupName</span></span>
<span data-ttu-id="3581e-144">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3581e-144">Resource group name.</span></span>

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

### <span data-ttu-id="3581e-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3581e-145">-ResourceId</span></span>
<span data-ttu-id="3581e-146">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3581e-146">Resource ID.</span></span>

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

### <span data-ttu-id="3581e-147">-Escopo</span><span class="sxs-lookup"><span data-stu-id="3581e-147">-Scope</span></span>
<span data-ttu-id="3581e-148">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="3581e-148">Scope of the resource.</span></span>
<span data-ttu-id="3581e-149">:.</span><span class="sxs-lookup"><span data-stu-id="3581e-149">E.g.</span></span>
<span data-ttu-id="3581e-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="3581e-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="3581e-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3581e-151">-Confirm</span></span>
<span data-ttu-id="3581e-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3581e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3581e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3581e-153">-WhatIf</span></span>
<span data-ttu-id="3581e-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3581e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3581e-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3581e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3581e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3581e-156">CommonParameters</span></span>
<span data-ttu-id="3581e-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3581e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3581e-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3581e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3581e-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3581e-159">INPUTS</span></span>

### <span data-ttu-id="3581e-160">System. String</span><span class="sxs-lookup"><span data-stu-id="3581e-160">System.String</span></span>

### <span data-ttu-id="3581e-161">System. String []</span><span class="sxs-lookup"><span data-stu-id="3581e-161">System.String[]</span></span>

## <span data-ttu-id="3581e-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3581e-162">OUTPUTS</span></span>

### <span data-ttu-id="3581e-163">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="3581e-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="3581e-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3581e-164">NOTES</span></span>

## <span data-ttu-id="3581e-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3581e-165">RELATED LINKS</span></span>