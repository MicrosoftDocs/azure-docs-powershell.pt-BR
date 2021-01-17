---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429008"
---
# <span data-ttu-id="0bcf8-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="0bcf8-101">Get-AzAlert</span></span>

## <span data-ttu-id="0bcf8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bcf8-102">SYNOPSIS</span></span>
<span data-ttu-id="0bcf8-103">Obter informações de alertas</span><span class="sxs-lookup"><span data-stu-id="0bcf8-103">Get Alerts Information</span></span>

## <span data-ttu-id="0bcf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bcf8-104">SYNTAX</span></span>

### <span data-ttu-id="0bcf8-105">AlertsListByFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="0bcf8-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bcf8-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="0bcf8-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bcf8-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="0bcf8-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bcf8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bcf8-108">DESCRIPTION</span></span>
<span data-ttu-id="0bcf8-109">O cmdlet **Get-AzAlert** é acionado com instâncias de alerta.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="0bcf8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bcf8-110">EXAMPLES</span></span>

### <span data-ttu-id="0bcf8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0bcf8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="0bcf8-112">Listar todos os alertas com severidade Sev2 e condição de monitor disparada.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="0bcf8-113">Definir IncludeContext como verdadeiro, incluir a carga personalizada do alerta.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="0bcf8-114">Use Format-List para obter os detalhes completos de cada alerta na lista.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="0bcf8-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0bcf8-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="0bcf8-116">Obter detalhes do alerta por ID (GUID) ou ID do recurso (ID do braço completo)</span><span class="sxs-lookup"><span data-stu-id="0bcf8-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="0bcf8-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0bcf8-117">Example 3</span></span>

<span data-ttu-id="0bcf8-118">Obter informações de alertas.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-118">Get Alerts Information.</span></span> <span data-ttu-id="0bcf8-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="0bcf8-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="0bcf8-120">OS</span><span class="sxs-lookup"><span data-stu-id="0bcf8-120">PARAMETERS</span></span>

### <span data-ttu-id="0bcf8-121">-Alertid</span><span class="sxs-lookup"><span data-stu-id="0bcf8-121">-AlertId</span></span>
<span data-ttu-id="0bcf8-122">Identificador exclusivo do alerta/ResourceId do alerta.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="0bcf8-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0bcf8-123">-AlertRuleId</span></span>
<span data-ttu-id="0bcf8-124">Filtrar por ID de regra de alerta</span><span class="sxs-lookup"><span data-stu-id="0bcf8-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="0bcf8-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="0bcf8-125">-CustomTimeRange</span></span>
<span data-ttu-id="0bcf8-126">Formato com suporte- \<start-time\> / \<end-time\> onde o tempo está no formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="0bcf8-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="0bcf8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bcf8-127">-DefaultProfile</span></span>
<span data-ttu-id="0bcf8-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bcf8-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="0bcf8-129">-IncludeContext</span></span>
<span data-ttu-id="0bcf8-130">Incluir contexto (carga personalizada) do alerta</span><span class="sxs-lookup"><span data-stu-id="0bcf8-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="0bcf8-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="0bcf8-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="0bcf8-132">Incluir EgressConfig</span><span class="sxs-lookup"><span data-stu-id="0bcf8-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="0bcf8-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="0bcf8-133">-MonitorCondition</span></span>
<span data-ttu-id="0bcf8-134">Filtrar por condição de monitor</span><span class="sxs-lookup"><span data-stu-id="0bcf8-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="0bcf8-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="0bcf8-135">-MonitorService</span></span>
<span data-ttu-id="0bcf8-136">Filtrar no serviço moniter</span><span class="sxs-lookup"><span data-stu-id="0bcf8-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="0bcf8-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="0bcf8-137">-PageCount</span></span>
<span data-ttu-id="0bcf8-138">Número de alertas a serem buscados em uma página.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="0bcf8-139">-Selecione</span><span class="sxs-lookup"><span data-stu-id="0bcf8-139">-Select</span></span>
<span data-ttu-id="0bcf8-140">Projetar os campos obrigatórios fora do Essentials.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="0bcf8-141">A entrada esperada é separada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="0bcf8-142">-Severidade</span><span class="sxs-lookup"><span data-stu-id="0bcf8-142">-Severity</span></span>
<span data-ttu-id="0bcf8-143">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="0bcf8-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="0bcf8-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="0bcf8-144">-SmartGroupId</span></span>
<span data-ttu-id="0bcf8-145">Filtrar todos os alertas com a ID do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="0bcf8-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="0bcf8-146">-ClassificarPor</span><span class="sxs-lookup"><span data-stu-id="0bcf8-146">-SortBy</span></span>
<span data-ttu-id="0bcf8-147">Propriedade de alerta a ser usada durante a classificação</span><span class="sxs-lookup"><span data-stu-id="0bcf8-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="0bcf8-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="0bcf8-148">-SortOrder</span></span>
<span data-ttu-id="0bcf8-149">Ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="0bcf8-149">Sort Order</span></span>

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

### <span data-ttu-id="0bcf8-150">-Estado</span><span class="sxs-lookup"><span data-stu-id="0bcf8-150">-State</span></span>
<span data-ttu-id="0bcf8-151">Filtrar no estado de alerta</span><span class="sxs-lookup"><span data-stu-id="0bcf8-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="0bcf8-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0bcf8-152">-TargetResourceGroup</span></span>
<span data-ttu-id="0bcf8-153">Filtrar no grupo de recursos nome do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="0bcf8-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0bcf8-154">-TargetResourceId</span></span>
<span data-ttu-id="0bcf8-155">Filtre a ID do recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="0bcf8-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="0bcf8-156">-TargetResourceType</span></span>
<span data-ttu-id="0bcf8-157">Filtrar tipo de recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="0bcf8-158">-Intervalo de</span><span class="sxs-lookup"><span data-stu-id="0bcf8-158">-TimeRange</span></span>
<span data-ttu-id="0bcf8-159">Valores de intervalo de tempo com suporte-1h, 1D, 7D, 30D (o padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="0bcf8-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="0bcf8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bcf8-160">CommonParameters</span></span>
<span data-ttu-id="0bcf8-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bcf8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bcf8-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bcf8-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bcf8-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bcf8-163">INPUTS</span></span>

### <span data-ttu-id="0bcf8-164">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0bcf8-164">None</span></span>

## <span data-ttu-id="0bcf8-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bcf8-165">OUTPUTS</span></span>

### <span data-ttu-id="0bcf8-166">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="0bcf8-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="0bcf8-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bcf8-167">NOTES</span></span>

## <span data-ttu-id="0bcf8-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bcf8-168">RELATED LINKS</span></span>
