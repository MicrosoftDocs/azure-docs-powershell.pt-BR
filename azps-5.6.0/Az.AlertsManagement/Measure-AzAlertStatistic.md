---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 27fb22a5cded5e196a4bef0aa8b504771abef864
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891417"
---
# <span data-ttu-id="f0b17-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="f0b17-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="f0b17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b17-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b17-103">Obtém informações de resumo de alerta</span><span class="sxs-lookup"><span data-stu-id="f0b17-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="f0b17-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f0b17-104">SYNTAX</span></span>

### <span data-ttu-id="f0b17-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="f0b17-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0b17-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="f0b17-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0b17-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f0b17-107">DESCRIPTION</span></span>
<span data-ttu-id="f0b17-108">O cmdlet **Measure-AzAlertStatistic** obtém detalhes do resumo do alerta.</span><span class="sxs-lookup"><span data-stu-id="f0b17-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="f0b17-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0b17-109">EXAMPLES</span></span>

### <span data-ttu-id="f0b17-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0b17-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="f0b17-111">Resumir a contagem de alertas agrupados por gravidade e estado filtrado pelo estado Ativo.</span><span class="sxs-lookup"><span data-stu-id="f0b17-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="f0b17-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f0b17-112">PARAMETERS</span></span>

### <span data-ttu-id="f0b17-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="f0b17-113">-AlertRuleId</span></span>
<span data-ttu-id="f0b17-114">Filtrar na ID da Regra de Alerta</span><span class="sxs-lookup"><span data-stu-id="f0b17-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="f0b17-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="f0b17-115">-CustomTimeRange</span></span>
<span data-ttu-id="f0b17-116">Formato com suporte - \<start-time\> / \<end-time\> onde o tempo está no formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="f0b17-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="f0b17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b17-117">-DefaultProfile</span></span>
<span data-ttu-id="f0b17-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0b17-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="f0b17-119">-GroupBy</span></span>
<span data-ttu-id="f0b17-120">Resumir por propriedade</span><span class="sxs-lookup"><span data-stu-id="f0b17-120">Summarize by property</span></span>

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

### <span data-ttu-id="f0b17-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="f0b17-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="f0b17-122">Incluir Contagem smartGroups</span><span class="sxs-lookup"><span data-stu-id="f0b17-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="f0b17-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="f0b17-123">-MonitorCondition</span></span>
<span data-ttu-id="f0b17-124">Filtrar na condição de monitor</span><span class="sxs-lookup"><span data-stu-id="f0b17-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="f0b17-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="f0b17-125">-MonitorService</span></span>
<span data-ttu-id="f0b17-126">Filtrar no serviço Moniter</span><span class="sxs-lookup"><span data-stu-id="f0b17-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="f0b17-127">-Severity</span><span class="sxs-lookup"><span data-stu-id="f0b17-127">-Severity</span></span>
<span data-ttu-id="f0b17-128">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="f0b17-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="f0b17-129">-State</span><span class="sxs-lookup"><span data-stu-id="f0b17-129">-State</span></span>
<span data-ttu-id="f0b17-130">Filtrar em estado de alerta</span><span class="sxs-lookup"><span data-stu-id="f0b17-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="f0b17-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0b17-131">-TargetResourceGroup</span></span>
<span data-ttu-id="f0b17-132">Filtrar o nome do grupo de recursos do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="f0b17-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="f0b17-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b17-133">-TargetResourceId</span></span>
<span data-ttu-id="f0b17-134">Filtrar na ID de Recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="f0b17-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="f0b17-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="f0b17-135">-TargetResourceType</span></span>
<span data-ttu-id="f0b17-136">Filtrar o tipo de recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="f0b17-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="f0b17-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="f0b17-137">-TimeRange</span></span>
<span data-ttu-id="f0b17-138">Valores de intervalo de tempo suportados - 1h, 1d, 7d, 30d (Padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="f0b17-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="f0b17-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b17-139">CommonParameters</span></span>
<span data-ttu-id="f0b17-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b17-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b17-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0b17-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b17-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0b17-142">INPUTS</span></span>

### <span data-ttu-id="f0b17-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f0b17-143">None</span></span>

## <span data-ttu-id="f0b17-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f0b17-144">OUTPUTS</span></span>

### <span data-ttu-id="f0b17-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="f0b17-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="f0b17-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="f0b17-146">NOTES</span></span>

## <span data-ttu-id="f0b17-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0b17-147">RELATED LINKS</span></span>
