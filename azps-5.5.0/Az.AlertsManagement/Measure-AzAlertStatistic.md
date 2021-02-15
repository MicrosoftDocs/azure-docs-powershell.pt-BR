---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118108"
---
# <span data-ttu-id="469c2-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="469c2-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="469c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="469c2-102">SYNOPSIS</span></span>
<span data-ttu-id="469c2-103">Obtém informações de resumo de alerta</span><span class="sxs-lookup"><span data-stu-id="469c2-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="469c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="469c2-104">SYNTAX</span></span>

### <span data-ttu-id="469c2-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="469c2-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="469c2-106">Filtro de Resumo</span><span class="sxs-lookup"><span data-stu-id="469c2-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="469c2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="469c2-107">DESCRIPTION</span></span>
<span data-ttu-id="469c2-108">**O cmdlet Measure-AzAlertStatistic** obtém detalhes de resumo de alerta.</span><span class="sxs-lookup"><span data-stu-id="469c2-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="469c2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="469c2-109">EXAMPLES</span></span>

### <span data-ttu-id="469c2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="469c2-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="469c2-111">Resumir a contagem de alertas agrupada por gravidade e estado filtrado pelo estado Ativo.</span><span class="sxs-lookup"><span data-stu-id="469c2-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="469c2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="469c2-112">PARAMETERS</span></span>

### <span data-ttu-id="469c2-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="469c2-113">-AlertRuleId</span></span>
<span data-ttu-id="469c2-114">Filtrar na ID da Regra de Alerta</span><span class="sxs-lookup"><span data-stu-id="469c2-114">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="469c2-115">-CustomTimeRange</span></span>
<span data-ttu-id="469c2-116">Formato com suporte - \<start-time\> / \<end-time\> onde o tempo está no formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="469c2-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469c2-117">-DefaultProfile</span></span>
<span data-ttu-id="469c2-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="469c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="469c2-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="469c2-119">-GroupBy</span></span>
<span data-ttu-id="469c2-120">Resumir por propriedade</span><span class="sxs-lookup"><span data-stu-id="469c2-120">Summarize by property</span></span>

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

### <span data-ttu-id="469c2-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="469c2-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="469c2-122">Incluir Contagem de Grupos Inteligentes</span><span class="sxs-lookup"><span data-stu-id="469c2-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="469c2-123">-MonitorCondition</span></span>
<span data-ttu-id="469c2-124">Filtrar na Condição de Monitor</span><span class="sxs-lookup"><span data-stu-id="469c2-124">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="469c2-125">-MonitorService</span></span>
<span data-ttu-id="469c2-126">Filtrar no Serviço de Moniter</span><span class="sxs-lookup"><span data-stu-id="469c2-126">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-127">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="469c2-127">-Severity</span></span>
<span data-ttu-id="469c2-128">Filtrar na Gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="469c2-128">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="469c2-129">-State</span></span>
<span data-ttu-id="469c2-130">Filtrar no Estado de alerta</span><span class="sxs-lookup"><span data-stu-id="469c2-130">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="469c2-131">-TargetResourceGroup</span></span>
<span data-ttu-id="469c2-132">Filtre o nome do grupo Recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="469c2-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="469c2-133">-TargetResourceId</span></span>
<span data-ttu-id="469c2-134">Filtrar a ID do Recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="469c2-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="469c2-135">-TargetResourceType</span></span>
<span data-ttu-id="469c2-136">Filtrar o tipo de recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="469c2-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="469c2-137">-TimeRange</span></span>
<span data-ttu-id="469c2-138">Valores de intervalo de tempo com suporte - 1h, 1d, 7d, 30d (Padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="469c2-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469c2-139">CommonParameters</span></span>
<span data-ttu-id="469c2-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469c2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469c2-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="469c2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469c2-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="469c2-142">INPUTS</span></span>

### <span data-ttu-id="469c2-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="469c2-143">None</span></span>

## <span data-ttu-id="469c2-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="469c2-144">OUTPUTS</span></span>

### <span data-ttu-id="469c2-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="469c2-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="469c2-146">Notas</span><span class="sxs-lookup"><span data-stu-id="469c2-146">NOTES</span></span>

## <span data-ttu-id="469c2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="469c2-147">RELATED LINKS</span></span>
