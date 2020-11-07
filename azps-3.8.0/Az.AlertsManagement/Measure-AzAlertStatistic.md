---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941201"
---
# <span data-ttu-id="c9cbc-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="c9cbc-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="c9cbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="c9cbc-103">Obtém informações de resumo do alerta</span><span class="sxs-lookup"><span data-stu-id="c9cbc-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="c9cbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9cbc-104">SYNTAX</span></span>

### <span data-ttu-id="c9cbc-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="c9cbc-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9cbc-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="c9cbc-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9cbc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9cbc-107">DESCRIPTION</span></span>
<span data-ttu-id="c9cbc-108">O cmdlet **Measure-AzAlertStatistic** Obtém detalhes do resumo do alerta.</span><span class="sxs-lookup"><span data-stu-id="c9cbc-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="c9cbc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9cbc-109">EXAMPLES</span></span>

### <span data-ttu-id="c9cbc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9cbc-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="c9cbc-111">Resumir a contagem de alertas agrupada por severidade e estado filtrado pelo estado ativo.</span><span class="sxs-lookup"><span data-stu-id="c9cbc-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="c9cbc-112">OS</span><span class="sxs-lookup"><span data-stu-id="c9cbc-112">PARAMETERS</span></span>

### <span data-ttu-id="c9cbc-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c9cbc-113">-AlertRuleId</span></span>
<span data-ttu-id="c9cbc-114">Filtrar por ID de regra de alerta</span><span class="sxs-lookup"><span data-stu-id="c9cbc-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="c9cbc-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="c9cbc-115">-CustomTimeRange</span></span>
<span data-ttu-id="c9cbc-116">Formato com suporte-horário de início-horário de \< início \> / \< \> no qual o tempo está no formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="c9cbc-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="c9cbc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9cbc-117">-DefaultProfile</span></span>
<span data-ttu-id="c9cbc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9cbc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9cbc-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="c9cbc-119">-GroupBy</span></span>
<span data-ttu-id="c9cbc-120">Resumir por Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9cbc-120">Summarize by property</span></span>

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

### <span data-ttu-id="c9cbc-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="c9cbc-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="c9cbc-122">Incluir contagem de SmartGroups</span><span class="sxs-lookup"><span data-stu-id="c9cbc-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="c9cbc-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="c9cbc-123">-MonitorCondition</span></span>
<span data-ttu-id="c9cbc-124">Filtrar por condição de monitor</span><span class="sxs-lookup"><span data-stu-id="c9cbc-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="c9cbc-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="c9cbc-125">-MonitorService</span></span>
<span data-ttu-id="c9cbc-126">Filtrar no serviço moniter</span><span class="sxs-lookup"><span data-stu-id="c9cbc-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="c9cbc-127">-Severidade</span><span class="sxs-lookup"><span data-stu-id="c9cbc-127">-Severity</span></span>
<span data-ttu-id="c9cbc-128">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="c9cbc-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="c9cbc-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="c9cbc-129">-State</span></span>
<span data-ttu-id="c9cbc-130">Filtrar no estado de alerta</span><span class="sxs-lookup"><span data-stu-id="c9cbc-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="c9cbc-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c9cbc-131">-TargetResourceGroup</span></span>
<span data-ttu-id="c9cbc-132">Filtrar no grupo de recursos nome do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="c9cbc-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="c9cbc-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c9cbc-133">-TargetResourceId</span></span>
<span data-ttu-id="c9cbc-134">Filtre a ID do recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="c9cbc-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="c9cbc-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="c9cbc-135">-TargetResourceType</span></span>
<span data-ttu-id="c9cbc-136">Filtrar tipo de recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="c9cbc-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="c9cbc-137">-Intervalo de</span><span class="sxs-lookup"><span data-stu-id="c9cbc-137">-TimeRange</span></span>
<span data-ttu-id="c9cbc-138">Valores de intervalo de tempo com suporte-1h, 1D, 7D, 30D (o padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="c9cbc-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="c9cbc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9cbc-139">CommonParameters</span></span>
<span data-ttu-id="c9cbc-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9cbc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9cbc-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9cbc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9cbc-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9cbc-142">INPUTS</span></span>

### <span data-ttu-id="c9cbc-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c9cbc-143">None</span></span>

## <span data-ttu-id="c9cbc-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9cbc-144">OUTPUTS</span></span>

### <span data-ttu-id="c9cbc-145">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="c9cbc-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="c9cbc-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9cbc-146">NOTES</span></span>

## <span data-ttu-id="c9cbc-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9cbc-147">RELATED LINKS</span></span>
