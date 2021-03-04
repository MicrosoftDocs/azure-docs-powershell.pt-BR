---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: ff9a54852d84d7c1183e81cb8b597279f357ebe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887103"
---
# <span data-ttu-id="000cd-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="000cd-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="000cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="000cd-102">SYNOPSIS</span></span>
<span data-ttu-id="000cd-103">Cria uma solução de análise de log.</span><span class="sxs-lookup"><span data-stu-id="000cd-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="000cd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="000cd-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="000cd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="000cd-105">DESCRIPTION</span></span>
<span data-ttu-id="000cd-106">Cria uma solução de análise de log.</span><span class="sxs-lookup"><span data-stu-id="000cd-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="000cd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="000cd-107">EXAMPLES</span></span>

### <span data-ttu-id="000cd-108">Exemplo 1: Criar uma solução de análise de log de monitoramento para o espaço de trabalho de análise de log</span><span class="sxs-lookup"><span data-stu-id="000cd-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="000cd-109">Este comando cria uma solução de análise de log de monitoramento para o espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="000cd-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="000cd-110">Os tipos mais usados são:</span><span class="sxs-lookup"><span data-stu-id="000cd-110">Commonly used types are:</span></span>

| <span data-ttu-id="000cd-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="000cd-111">Type</span></span> | <span data-ttu-id="000cd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="000cd-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="000cd-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="000cd-113">SecurityCenterFree</span></span> |  <span data-ttu-id="000cd-114">Centro de Segurança do Azure – Edição Gratuita</span><span class="sxs-lookup"><span data-stu-id="000cd-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="000cd-115">Segurança</span><span class="sxs-lookup"><span data-stu-id="000cd-115">Security</span></span> | <span data-ttu-id="000cd-116">Centro de Segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="000cd-116">Azure Security Center</span></span> |
| <span data-ttu-id="000cd-117">Atualizações</span><span class="sxs-lookup"><span data-stu-id="000cd-117">Updates</span></span> | <span data-ttu-id="000cd-118">Gerenciamento de atualizações</span><span class="sxs-lookup"><span data-stu-id="000cd-118">Update Management</span></span> |
| <span data-ttu-id="000cd-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="000cd-119">ContainerInsights</span></span> | <span data-ttu-id="000cd-120">Monitor do Azure para Contêineres</span><span class="sxs-lookup"><span data-stu-id="000cd-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="000cd-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="000cd-121">ServiceMap</span></span> | <span data-ttu-id="000cd-122">Mapa de Serviço</span><span class="sxs-lookup"><span data-stu-id="000cd-122">Service Map</span></span> |
| <span data-ttu-id="000cd-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="000cd-123">AzureActivity</span></span> | <span data-ttu-id="000cd-124">Análise de log de atividades</span><span class="sxs-lookup"><span data-stu-id="000cd-124">Activity log analytics</span></span> |
| <span data-ttu-id="000cd-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="000cd-125">ChangeTracking</span></span> | <span data-ttu-id="000cd-126">Controle e inventário de alterações</span><span class="sxs-lookup"><span data-stu-id="000cd-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="000cd-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="000cd-127">VMInsights</span></span> | <span data-ttu-id="000cd-128">Monitor do Azure para VMs</span><span class="sxs-lookup"><span data-stu-id="000cd-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="000cd-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="000cd-129">SecurityInsights</span></span> | <span data-ttu-id="000cd-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="000cd-130">Azure Sentinel</span></span> |
| <span data-ttu-id="000cd-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="000cd-131">NetworkMonitoring</span></span> | <span data-ttu-id="000cd-132">Monitor de Desempenho de Rede</span><span class="sxs-lookup"><span data-stu-id="000cd-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="000cd-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="000cd-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="000cd-134">SQL Avaliação de Vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="000cd-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="000cd-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="000cd-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="000cd-136">SQL Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="000cd-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="000cd-137">AntiMalware</span><span class="sxs-lookup"><span data-stu-id="000cd-137">AntiMalware</span></span> | <span data-ttu-id="000cd-138">Avaliação antimalware</span><span class="sxs-lookup"><span data-stu-id="000cd-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="000cd-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="000cd-139">AzureAutomation</span></span> | <span data-ttu-id="000cd-140">Trabalhador Híbrido de Automação</span><span class="sxs-lookup"><span data-stu-id="000cd-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="000cd-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="000cd-141">LogicAppsManagement</span></span> | <span data-ttu-id="000cd-142">Gerenciamento de Aplicativos Lógicos</span><span class="sxs-lookup"><span data-stu-id="000cd-142">Logic Apps Management</span></span> |
| <span data-ttu-id="000cd-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="000cd-143">SQLDataClassification</span></span> | <span data-ttu-id="000cd-144">SQL De descoberta de dados & Classificação</span><span class="sxs-lookup"><span data-stu-id="000cd-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="000cd-145">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="000cd-145">PARAMETERS</span></span>

### <span data-ttu-id="000cd-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000cd-146">-DefaultProfile</span></span>
<span data-ttu-id="000cd-147">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="000cd-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000cd-148">-Location</span><span class="sxs-lookup"><span data-stu-id="000cd-148">-Location</span></span>
<span data-ttu-id="000cd-149">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="000cd-149">Resource location.</span></span>
<span data-ttu-id="000cd-150">Deve ser igual ao espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="000cd-150">Must be the same as the log analytic workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000cd-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="000cd-151">-ResourceGroupName</span></span>
<span data-ttu-id="000cd-152">O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="000cd-152">The name of the resource group to get.</span></span>
<span data-ttu-id="000cd-153">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="000cd-153">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000cd-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="000cd-154">-SubscriptionId</span></span>
<span data-ttu-id="000cd-155">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="000cd-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="000cd-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="000cd-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000cd-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="000cd-157">-Tag</span></span>
<span data-ttu-id="000cd-158">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="000cd-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000cd-159">-Type</span><span class="sxs-lookup"><span data-stu-id="000cd-159">-Type</span></span>
<span data-ttu-id="000cd-160">Tipo da solução a ser criada.</span><span class="sxs-lookup"><span data-stu-id="000cd-160">Type of the solution to be created.</span></span>
<span data-ttu-id="000cd-161">Por exemplo, "Contêiner".</span><span class="sxs-lookup"><span data-stu-id="000cd-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000cd-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="000cd-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="000cd-163">A ID de recurso do Azure para o espaço de trabalho onde a solução será implantada/habilitada.</span><span class="sxs-lookup"><span data-stu-id="000cd-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000cd-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="000cd-164">-Confirm</span></span>
<span data-ttu-id="000cd-165">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="000cd-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="000cd-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="000cd-166">-WhatIf</span></span>
<span data-ttu-id="000cd-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="000cd-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="000cd-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="000cd-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="000cd-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000cd-169">CommonParameters</span></span>
<span data-ttu-id="000cd-170">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="000cd-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000cd-171">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="000cd-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000cd-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="000cd-172">INPUTS</span></span>

## <span data-ttu-id="000cd-173">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="000cd-173">OUTPUTS</span></span>

### <span data-ttu-id="000cd-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="000cd-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="000cd-175">NOTES</span><span class="sxs-lookup"><span data-stu-id="000cd-175">NOTES</span></span>

<span data-ttu-id="000cd-176">ALIASES</span><span class="sxs-lookup"><span data-stu-id="000cd-176">ALIASES</span></span>

## <span data-ttu-id="000cd-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="000cd-177">RELATED LINKS</span></span>



[<span data-ttu-id="000cd-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="000cd-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

