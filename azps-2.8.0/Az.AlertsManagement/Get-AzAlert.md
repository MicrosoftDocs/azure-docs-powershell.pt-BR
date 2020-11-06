---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: e3a5cbe95bf524a70194cfce7e0b8bb80b701dec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598190"
---
# <span data-ttu-id="925bb-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="925bb-101">Get-AzAlert</span></span>

## <span data-ttu-id="925bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="925bb-102">SYNOPSIS</span></span>
<span data-ttu-id="925bb-103">Obter informações de alertas</span><span class="sxs-lookup"><span data-stu-id="925bb-103">Get Alerts Information</span></span>

## <span data-ttu-id="925bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="925bb-104">SYNTAX</span></span>

### <span data-ttu-id="925bb-105">AlertsListByFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="925bb-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="925bb-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="925bb-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="925bb-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="925bb-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="925bb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="925bb-108">DESCRIPTION</span></span>
<span data-ttu-id="925bb-109">O cmdlet **Get-AzAlert** é acionado com instâncias de alerta.</span><span class="sxs-lookup"><span data-stu-id="925bb-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="925bb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="925bb-110">EXAMPLES</span></span>

### <span data-ttu-id="925bb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="925bb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="925bb-112">Listar todos os alertas com severidade Sev2 e condição de monitor disparada.</span><span class="sxs-lookup"><span data-stu-id="925bb-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="925bb-113">Definir IncludeContext como verdadeiro, incluir a carga personalizada do alerta.</span><span class="sxs-lookup"><span data-stu-id="925bb-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="925bb-114">Use Format-List para obter os detalhes completos de cada alerta na lista.</span><span class="sxs-lookup"><span data-stu-id="925bb-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="925bb-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="925bb-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="925bb-116">Obter detalhes do alerta por ID (GUID) ou ID do recurso (ID do braço completo)</span><span class="sxs-lookup"><span data-stu-id="925bb-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="925bb-117">OS</span><span class="sxs-lookup"><span data-stu-id="925bb-117">PARAMETERS</span></span>

### <span data-ttu-id="925bb-118">-Alertid</span><span class="sxs-lookup"><span data-stu-id="925bb-118">-AlertId</span></span>
<span data-ttu-id="925bb-119">Identificador exclusivo do alerta/ResourceId do alerta.</span><span class="sxs-lookup"><span data-stu-id="925bb-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="925bb-120">-AlertRuleId</span></span>
<span data-ttu-id="925bb-121">Filtrar por ID de regra de alerta</span><span class="sxs-lookup"><span data-stu-id="925bb-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="925bb-122">-CustomTimeRange</span></span>
<span data-ttu-id="925bb-123">Formato com suporte-horário de início-horário de \< início \> / \< \> no qual o tempo está no formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="925bb-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="925bb-124">-DefaultProfile</span></span>
<span data-ttu-id="925bb-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="925bb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="925bb-126">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="925bb-126">-IncludeContext</span></span>
<span data-ttu-id="925bb-127">Incluir contexto (carga personalizada) do alerta</span><span class="sxs-lookup"><span data-stu-id="925bb-127">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="925bb-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="925bb-129">Incluir EgressConfig</span><span class="sxs-lookup"><span data-stu-id="925bb-129">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="925bb-130">-MonitorCondition</span></span>
<span data-ttu-id="925bb-131">Filtrar por condição de monitor</span><span class="sxs-lookup"><span data-stu-id="925bb-131">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="925bb-132">-MonitorService</span></span>
<span data-ttu-id="925bb-133">Filtrar no serviço moniter</span><span class="sxs-lookup"><span data-stu-id="925bb-133">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="925bb-134">-PageCount</span></span>
<span data-ttu-id="925bb-135">Número de alertas a serem buscados em uma página.</span><span class="sxs-lookup"><span data-stu-id="925bb-135">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-136">-Selecione</span><span class="sxs-lookup"><span data-stu-id="925bb-136">-Select</span></span>
<span data-ttu-id="925bb-137">Projetar os campos obrigatórios fora do Essentials.</span><span class="sxs-lookup"><span data-stu-id="925bb-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="925bb-138">A entrada esperada é separada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="925bb-138">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-139">-Severidade</span><span class="sxs-lookup"><span data-stu-id="925bb-139">-Severity</span></span>
<span data-ttu-id="925bb-140">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="925bb-140">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="925bb-141">-SmartGroupId</span></span>
<span data-ttu-id="925bb-142">Filtrar todos os alertas com a ID do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="925bb-142">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-143">-ClassificarPor</span><span class="sxs-lookup"><span data-stu-id="925bb-143">-SortBy</span></span>
<span data-ttu-id="925bb-144">Propriedade de alerta a ser usada durante a classificação</span><span class="sxs-lookup"><span data-stu-id="925bb-144">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="925bb-145">-SortOrder</span></span>
<span data-ttu-id="925bb-146">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="925bb-146">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-147">-Estado</span><span class="sxs-lookup"><span data-stu-id="925bb-147">-State</span></span>
<span data-ttu-id="925bb-148">Filtrar no estado de alerta</span><span class="sxs-lookup"><span data-stu-id="925bb-148">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="925bb-149">-TargetResourceGroup</span></span>
<span data-ttu-id="925bb-150">Filtrar no grupo de recursos nome do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="925bb-150">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="925bb-151">-TargetResourceId</span></span>
<span data-ttu-id="925bb-152">Filtre a ID do recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="925bb-152">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="925bb-153">-TargetResourceType</span></span>
<span data-ttu-id="925bb-154">Filtrar tipo de recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="925bb-154">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-155">-Intervalo de</span><span class="sxs-lookup"><span data-stu-id="925bb-155">-TimeRange</span></span>
<span data-ttu-id="925bb-156">Valores de intervalo de tempo com suporte-1h, 1D, 7D, 30D (o padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="925bb-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="925bb-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="925bb-157">CommonParameters</span></span>
<span data-ttu-id="925bb-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="925bb-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="925bb-159">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="925bb-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="925bb-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="925bb-160">INPUTS</span></span>

### <span data-ttu-id="925bb-161">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="925bb-161">None</span></span>

## <span data-ttu-id="925bb-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="925bb-162">OUTPUTS</span></span>

### <span data-ttu-id="925bb-163">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="925bb-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="925bb-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="925bb-164">NOTES</span></span>

## <span data-ttu-id="925bb-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="925bb-165">RELATED LINKS</span></span>
