---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: dc2fd6492e611e84ef3db5aba57bec204985c203
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886515"
---
# <span data-ttu-id="7e366-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="7e366-101">Get-AzAlert</span></span>

## <span data-ttu-id="7e366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e366-102">SYNOPSIS</span></span>
<span data-ttu-id="7e366-103">Obter informações sobre alertas</span><span class="sxs-lookup"><span data-stu-id="7e366-103">Get Alerts Information</span></span>

## <span data-ttu-id="7e366-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7e366-104">SYNTAX</span></span>

### <span data-ttu-id="7e366-105">AlertsListByFilter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7e366-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e366-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="7e366-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e366-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="7e366-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e366-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7e366-108">DESCRIPTION</span></span>
<span data-ttu-id="7e366-109">O cmdlet **Get-AzAlert** recebe instâncias de alerta disparadas.</span><span class="sxs-lookup"><span data-stu-id="7e366-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="7e366-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e366-110">EXAMPLES</span></span>

### <span data-ttu-id="7e366-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e366-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="7e366-112">Listar todos os alertas com gravidade de Sev2 e condição de monitor acionado.</span><span class="sxs-lookup"><span data-stu-id="7e366-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="7e366-113">Definindo IncludeContext como true, inclua carga personalizada de alerta.</span><span class="sxs-lookup"><span data-stu-id="7e366-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="7e366-114">Use Format-List para obter os detalhes completos de cada alerta na lista.</span><span class="sxs-lookup"><span data-stu-id="7e366-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="7e366-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7e366-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="7e366-116">Obter detalhes do alerta por ID (GUID) ou ID de Recurso (ID ARM ID completa)</span><span class="sxs-lookup"><span data-stu-id="7e366-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="7e366-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7e366-117">Example 3</span></span>

<span data-ttu-id="7e366-118">Obter informações de alertas.</span><span class="sxs-lookup"><span data-stu-id="7e366-118">Get Alerts Information.</span></span> <span data-ttu-id="7e366-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="7e366-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="7e366-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7e366-120">PARAMETERS</span></span>

### <span data-ttu-id="7e366-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="7e366-121">-AlertId</span></span>
<span data-ttu-id="7e366-122">Identificador exclusivo de Alerta/ResourceId de alerta.</span><span class="sxs-lookup"><span data-stu-id="7e366-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="7e366-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="7e366-123">-AlertRuleId</span></span>
<span data-ttu-id="7e366-124">Filtrar na ID da Regra de Alerta</span><span class="sxs-lookup"><span data-stu-id="7e366-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="7e366-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="7e366-125">-CustomTimeRange</span></span>
<span data-ttu-id="7e366-126">Formato com suporte - \<start-time\> / \<end-time\> onde o tempo está no formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="7e366-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="7e366-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e366-127">-DefaultProfile</span></span>
<span data-ttu-id="7e366-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e366-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e366-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="7e366-129">-IncludeContext</span></span>
<span data-ttu-id="7e366-130">Incluir contexto (carga personalizada) de alerta</span><span class="sxs-lookup"><span data-stu-id="7e366-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="7e366-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="7e366-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="7e366-132">Incluir EgressConfig</span><span class="sxs-lookup"><span data-stu-id="7e366-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="7e366-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="7e366-133">-MonitorCondition</span></span>
<span data-ttu-id="7e366-134">Filtrar na condição de monitor</span><span class="sxs-lookup"><span data-stu-id="7e366-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="7e366-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="7e366-135">-MonitorService</span></span>
<span data-ttu-id="7e366-136">Filtrar no serviço Moniter</span><span class="sxs-lookup"><span data-stu-id="7e366-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="7e366-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="7e366-137">-PageCount</span></span>
<span data-ttu-id="7e366-138">Número de alertas a serem buscados em uma página.</span><span class="sxs-lookup"><span data-stu-id="7e366-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="7e366-139">-Select</span><span class="sxs-lookup"><span data-stu-id="7e366-139">-Select</span></span>
<span data-ttu-id="7e366-140">Projeia os campos necessários fora do essencial.</span><span class="sxs-lookup"><span data-stu-id="7e366-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="7e366-141">A entrada esperada é separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7e366-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="7e366-142">-Severity</span><span class="sxs-lookup"><span data-stu-id="7e366-142">-Severity</span></span>
<span data-ttu-id="7e366-143">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="7e366-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="7e366-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="7e366-144">-SmartGroupId</span></span>
<span data-ttu-id="7e366-145">Filtrar todos os alertas com a ID do Grupo Inteligente</span><span class="sxs-lookup"><span data-stu-id="7e366-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="7e366-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="7e366-146">-SortBy</span></span>
<span data-ttu-id="7e366-147">Propriedade Alert a ser usada durante a classificação</span><span class="sxs-lookup"><span data-stu-id="7e366-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="7e366-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="7e366-148">-SortOrder</span></span>
<span data-ttu-id="7e366-149">Ordem de Classificação</span><span class="sxs-lookup"><span data-stu-id="7e366-149">Sort Order</span></span>

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

### <span data-ttu-id="7e366-150">-State</span><span class="sxs-lookup"><span data-stu-id="7e366-150">-State</span></span>
<span data-ttu-id="7e366-151">Filtrar em estado de alerta</span><span class="sxs-lookup"><span data-stu-id="7e366-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="7e366-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e366-152">-TargetResourceGroup</span></span>
<span data-ttu-id="7e366-153">Filtrar o nome do grupo de recursos do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="7e366-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="7e366-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7e366-154">-TargetResourceId</span></span>
<span data-ttu-id="7e366-155">Filtrar na ID de Recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="7e366-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="7e366-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="7e366-156">-TargetResourceType</span></span>
<span data-ttu-id="7e366-157">Filtrar o tipo de recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="7e366-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="7e366-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="7e366-158">-TimeRange</span></span>
<span data-ttu-id="7e366-159">Valores de intervalo de tempo suportados - 1h, 1d, 7d, 30d (Padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="7e366-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="7e366-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e366-160">CommonParameters</span></span>
<span data-ttu-id="7e366-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e366-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e366-162">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e366-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e366-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e366-163">INPUTS</span></span>

### <span data-ttu-id="7e366-164">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7e366-164">None</span></span>

## <span data-ttu-id="7e366-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7e366-165">OUTPUTS</span></span>

### <span data-ttu-id="7e366-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="7e366-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="7e366-167">NOTES</span><span class="sxs-lookup"><span data-stu-id="7e366-167">NOTES</span></span>

## <span data-ttu-id="7e366-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e366-168">RELATED LINKS</span></span>
