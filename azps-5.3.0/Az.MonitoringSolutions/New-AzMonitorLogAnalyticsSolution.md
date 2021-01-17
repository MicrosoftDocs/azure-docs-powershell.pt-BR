---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427099"
---
# <span data-ttu-id="47ef5-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="47ef5-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="47ef5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="47ef5-103">Cria uma solução de análise de logs.</span><span class="sxs-lookup"><span data-stu-id="47ef5-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="47ef5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47ef5-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47ef5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47ef5-105">DESCRIPTION</span></span>
<span data-ttu-id="47ef5-106">Cria uma solução de análise de logs.</span><span class="sxs-lookup"><span data-stu-id="47ef5-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="47ef5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47ef5-107">EXAMPLES</span></span>

### <span data-ttu-id="47ef5-108">Exemplo 1: criar uma solução de análise de logs de monitor para o espaço de trabalho de análise de logs</span><span class="sxs-lookup"><span data-stu-id="47ef5-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="47ef5-109">Esse comando cria uma solução de análise de logs de monitor para o espaço de trabalho de análise de logs.</span><span class="sxs-lookup"><span data-stu-id="47ef5-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="47ef5-110">Os tipos comumente usados são:</span><span class="sxs-lookup"><span data-stu-id="47ef5-110">Commonly used types are:</span></span>

| <span data-ttu-id="47ef5-111">Digite</span><span class="sxs-lookup"><span data-stu-id="47ef5-111">Type</span></span> | <span data-ttu-id="47ef5-112">Descritivo</span><span class="sxs-lookup"><span data-stu-id="47ef5-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="47ef5-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="47ef5-113">SecurityCenterFree</span></span> |  <span data-ttu-id="47ef5-114">Central de segurança do Azure – edição gratuita</span><span class="sxs-lookup"><span data-stu-id="47ef5-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="47ef5-115">Segurança</span><span class="sxs-lookup"><span data-stu-id="47ef5-115">Security</span></span> | <span data-ttu-id="47ef5-116">Central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="47ef5-116">Azure Security Center</span></span> |
| <span data-ttu-id="47ef5-117">Actualiza</span><span class="sxs-lookup"><span data-stu-id="47ef5-117">Updates</span></span> | <span data-ttu-id="47ef5-118">Gerenciamento de atualizações</span><span class="sxs-lookup"><span data-stu-id="47ef5-118">Update Management</span></span> |
| <span data-ttu-id="47ef5-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="47ef5-119">ContainerInsights</span></span> | <span data-ttu-id="47ef5-120">Monitor do Azure para contêineres</span><span class="sxs-lookup"><span data-stu-id="47ef5-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="47ef5-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="47ef5-121">ServiceMap</span></span> | <span data-ttu-id="47ef5-122">Mapa de serviço</span><span class="sxs-lookup"><span data-stu-id="47ef5-122">Service Map</span></span> |
| <span data-ttu-id="47ef5-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="47ef5-123">AzureActivity</span></span> | <span data-ttu-id="47ef5-124">Análise de logs de atividades</span><span class="sxs-lookup"><span data-stu-id="47ef5-124">Activity log analytics</span></span> |
| <span data-ttu-id="47ef5-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="47ef5-125">ChangeTracking</span></span> | <span data-ttu-id="47ef5-126">Alterar o controle e o inventário</span><span class="sxs-lookup"><span data-stu-id="47ef5-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="47ef5-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="47ef5-127">VMInsights</span></span> | <span data-ttu-id="47ef5-128">Monitor do Azure para VMs</span><span class="sxs-lookup"><span data-stu-id="47ef5-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="47ef5-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="47ef5-129">SecurityInsights</span></span> | <span data-ttu-id="47ef5-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="47ef5-130">Azure Sentinel</span></span> |
| <span data-ttu-id="47ef5-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="47ef5-131">NetworkMonitoring</span></span> | <span data-ttu-id="47ef5-132">Monitor de desempenho de rede</span><span class="sxs-lookup"><span data-stu-id="47ef5-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="47ef5-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="47ef5-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="47ef5-134">Avaliação de vulnerabilidade do SQL</span><span class="sxs-lookup"><span data-stu-id="47ef5-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="47ef5-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="47ef5-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="47ef5-136">Proteção avançada contra ameaças do SQL</span><span class="sxs-lookup"><span data-stu-id="47ef5-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="47ef5-137">AntiMalware</span><span class="sxs-lookup"><span data-stu-id="47ef5-137">AntiMalware</span></span> | <span data-ttu-id="47ef5-138">Avaliação Antimalware</span><span class="sxs-lookup"><span data-stu-id="47ef5-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="47ef5-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="47ef5-139">AzureAutomation</span></span> | <span data-ttu-id="47ef5-140">Trabalhador híbrido de automação</span><span class="sxs-lookup"><span data-stu-id="47ef5-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="47ef5-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="47ef5-141">LogicAppsManagement</span></span> | <span data-ttu-id="47ef5-142">Gerenciamento de aplicativos lógicos</span><span class="sxs-lookup"><span data-stu-id="47ef5-142">Logic Apps Management</span></span> |
| <span data-ttu-id="47ef5-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="47ef5-143">SQLDataClassification</span></span> | <span data-ttu-id="47ef5-144">Classificação & do SQL Data Discovery</span><span class="sxs-lookup"><span data-stu-id="47ef5-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="47ef5-145">OS</span><span class="sxs-lookup"><span data-stu-id="47ef5-145">PARAMETERS</span></span>

### <span data-ttu-id="47ef5-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ef5-146">-DefaultProfile</span></span>
<span data-ttu-id="47ef5-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47ef5-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47ef5-148">-Local</span><span class="sxs-lookup"><span data-stu-id="47ef5-148">-Location</span></span>
<span data-ttu-id="47ef5-149">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="47ef5-149">Resource location.</span></span>
<span data-ttu-id="47ef5-150">Deve ser igual ao espaço de trabalho analítico de logs.</span><span class="sxs-lookup"><span data-stu-id="47ef5-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="47ef5-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ef5-151">-ResourceGroupName</span></span>
<span data-ttu-id="47ef5-152">O nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="47ef5-152">The name of the resource group to get.</span></span>
<span data-ttu-id="47ef5-153">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="47ef5-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="47ef5-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47ef5-154">-SubscriptionId</span></span>
<span data-ttu-id="47ef5-155">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47ef5-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="47ef5-156">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="47ef5-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47ef5-157">-Marca</span><span class="sxs-lookup"><span data-stu-id="47ef5-157">-Tag</span></span>
<span data-ttu-id="47ef5-158">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="47ef5-158">Resource tags</span></span>

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

### <span data-ttu-id="47ef5-159">-Digite</span><span class="sxs-lookup"><span data-stu-id="47ef5-159">-Type</span></span>
<span data-ttu-id="47ef5-160">Tipo da solução a ser criada.</span><span class="sxs-lookup"><span data-stu-id="47ef5-160">Type of the solution to be created.</span></span>
<span data-ttu-id="47ef5-161">Por exemplo, "contêiner".</span><span class="sxs-lookup"><span data-stu-id="47ef5-161">For example "Container".</span></span>

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

### <span data-ttu-id="47ef5-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="47ef5-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="47ef5-163">A ID de recurso do Azure para o espaço de trabalho em que a solução será implantada/habilitada.</span><span class="sxs-lookup"><span data-stu-id="47ef5-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="47ef5-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47ef5-164">-Confirm</span></span>
<span data-ttu-id="47ef5-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47ef5-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ef5-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ef5-166">-WhatIf</span></span>
<span data-ttu-id="47ef5-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47ef5-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ef5-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47ef5-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ef5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ef5-169">CommonParameters</span></span>
<span data-ttu-id="47ef5-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ef5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ef5-171">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47ef5-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ef5-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47ef5-172">INPUTS</span></span>

## <span data-ttu-id="47ef5-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47ef5-173">OUTPUTS</span></span>

### <span data-ttu-id="47ef5-174">Microsoft. Azure. PowerShell. cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="47ef5-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="47ef5-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47ef5-175">NOTES</span></span>

<span data-ttu-id="47ef5-176">ALIASES</span><span class="sxs-lookup"><span data-stu-id="47ef5-176">ALIASES</span></span>

## <span data-ttu-id="47ef5-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47ef5-177">RELATED LINKS</span></span>



[<span data-ttu-id="47ef5-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="47ef5-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

