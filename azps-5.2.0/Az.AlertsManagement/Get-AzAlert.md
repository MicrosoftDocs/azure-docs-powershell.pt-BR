---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264304"
---
# <span data-ttu-id="250df-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="250df-101">Get-AzAlert</span></span>

## <span data-ttu-id="250df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="250df-102">SYNOPSIS</span></span>
<span data-ttu-id="250df-103">Obter informações de alertas</span><span class="sxs-lookup"><span data-stu-id="250df-103">Get Alerts Information</span></span>

## <span data-ttu-id="250df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="250df-104">SYNTAX</span></span>

### <span data-ttu-id="250df-105">AlertsListByFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="250df-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="250df-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="250df-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="250df-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="250df-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="250df-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="250df-108">DESCRIPTION</span></span>
<span data-ttu-id="250df-109">O cmdlet **Get-AzAlert** é acionado com instâncias de alerta.</span><span class="sxs-lookup"><span data-stu-id="250df-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="250df-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="250df-110">EXAMPLES</span></span>

### <span data-ttu-id="250df-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="250df-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="250df-112">Listar todos os alertas com severidade Sev2 e condição de monitor disparada.</span><span class="sxs-lookup"><span data-stu-id="250df-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="250df-113">Definir IncludeContext como verdadeiro, incluir a carga personalizada do alerta.</span><span class="sxs-lookup"><span data-stu-id="250df-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="250df-114">Use Format-List para obter os detalhes completos de cada alerta na lista.</span><span class="sxs-lookup"><span data-stu-id="250df-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="250df-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="250df-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="250df-116">Obter detalhes do alerta por ID (GUID) ou ID do recurso (ID do braço completo)</span><span class="sxs-lookup"><span data-stu-id="250df-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="250df-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="250df-117">Example 3</span></span>

<span data-ttu-id="250df-118">Obter informações de alertas.</span><span class="sxs-lookup"><span data-stu-id="250df-118">Get Alerts Information.</span></span> <span data-ttu-id="250df-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="250df-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="250df-120">OS</span><span class="sxs-lookup"><span data-stu-id="250df-120">PARAMETERS</span></span>

### <span data-ttu-id="250df-121">-Alertid</span><span class="sxs-lookup"><span data-stu-id="250df-121">-AlertId</span></span>
<span data-ttu-id="250df-122">Identificador exclusivo do alerta/ResourceId do alerta.</span><span class="sxs-lookup"><span data-stu-id="250df-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="250df-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="250df-123">-AlertRuleId</span></span>
<span data-ttu-id="250df-124">Filtrar por ID de regra de alerta</span><span class="sxs-lookup"><span data-stu-id="250df-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="250df-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="250df-125">-CustomTimeRange</span></span>
<span data-ttu-id="250df-126">Formato com suporte- \<start-time\> / \<end-time\> onde o tempo está no formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="250df-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="250df-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="250df-127">-DefaultProfile</span></span>
<span data-ttu-id="250df-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="250df-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="250df-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="250df-129">-IncludeContext</span></span>
<span data-ttu-id="250df-130">Incluir contexto (carga personalizada) do alerta</span><span class="sxs-lookup"><span data-stu-id="250df-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="250df-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="250df-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="250df-132">Incluir EgressConfig</span><span class="sxs-lookup"><span data-stu-id="250df-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="250df-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="250df-133">-MonitorCondition</span></span>
<span data-ttu-id="250df-134">Filtrar por condição de monitor</span><span class="sxs-lookup"><span data-stu-id="250df-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="250df-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="250df-135">-MonitorService</span></span>
<span data-ttu-id="250df-136">Filtrar no serviço moniter</span><span class="sxs-lookup"><span data-stu-id="250df-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="250df-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="250df-137">-PageCount</span></span>
<span data-ttu-id="250df-138">Número de alertas a serem buscados em uma página.</span><span class="sxs-lookup"><span data-stu-id="250df-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="250df-139">-Selecione</span><span class="sxs-lookup"><span data-stu-id="250df-139">-Select</span></span>
<span data-ttu-id="250df-140">Projetar os campos obrigatórios fora do Essentials.</span><span class="sxs-lookup"><span data-stu-id="250df-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="250df-141">A entrada esperada é separada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="250df-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="250df-142">-Severidade</span><span class="sxs-lookup"><span data-stu-id="250df-142">-Severity</span></span>
<span data-ttu-id="250df-143">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="250df-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="250df-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="250df-144">-SmartGroupId</span></span>
<span data-ttu-id="250df-145">Filtrar todos os alertas com a ID do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="250df-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="250df-146">-ClassificarPor</span><span class="sxs-lookup"><span data-stu-id="250df-146">-SortBy</span></span>
<span data-ttu-id="250df-147">Propriedade de alerta a ser usada durante a classificação</span><span class="sxs-lookup"><span data-stu-id="250df-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="250df-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="250df-148">-SortOrder</span></span>
<span data-ttu-id="250df-149">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="250df-149">Sort Order</span></span>

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

### <span data-ttu-id="250df-150">-Estado</span><span class="sxs-lookup"><span data-stu-id="250df-150">-State</span></span>
<span data-ttu-id="250df-151">Filtrar no estado de alerta</span><span class="sxs-lookup"><span data-stu-id="250df-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="250df-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="250df-152">-TargetResourceGroup</span></span>
<span data-ttu-id="250df-153">Filtrar no grupo de recursos nome do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="250df-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="250df-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="250df-154">-TargetResourceId</span></span>
<span data-ttu-id="250df-155">Filtre a ID do recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="250df-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="250df-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="250df-156">-TargetResourceType</span></span>
<span data-ttu-id="250df-157">Filtrar tipo de recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="250df-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="250df-158">-Intervalo de</span><span class="sxs-lookup"><span data-stu-id="250df-158">-TimeRange</span></span>
<span data-ttu-id="250df-159">Valores de intervalo de tempo com suporte-1h, 1D, 7D, 30D (o padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="250df-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="250df-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="250df-160">CommonParameters</span></span>
<span data-ttu-id="250df-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="250df-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="250df-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="250df-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="250df-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="250df-163">INPUTS</span></span>

### <span data-ttu-id="250df-164">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="250df-164">None</span></span>

## <span data-ttu-id="250df-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="250df-165">OUTPUTS</span></span>

### <span data-ttu-id="250df-166">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="250df-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="250df-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="250df-167">NOTES</span></span>

## <span data-ttu-id="250df-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="250df-168">RELATED LINKS</span></span>
