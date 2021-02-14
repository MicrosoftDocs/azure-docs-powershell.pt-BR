---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116669"
---
# <span data-ttu-id="18a71-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="18a71-101">Get-AzAlert</span></span>

## <span data-ttu-id="18a71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18a71-102">SYNOPSIS</span></span>
<span data-ttu-id="18a71-103">Obter informações de alertas</span><span class="sxs-lookup"><span data-stu-id="18a71-103">Get Alerts Information</span></span>

## <span data-ttu-id="18a71-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18a71-104">SYNTAX</span></span>

### <span data-ttu-id="18a71-105">AlertsListByFilter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18a71-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18a71-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="18a71-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18a71-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="18a71-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18a71-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="18a71-108">DESCRIPTION</span></span>
<span data-ttu-id="18a71-109">**O cmdlet Get-AzAlert** recebe instâncias de alerta disparadas.</span><span class="sxs-lookup"><span data-stu-id="18a71-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="18a71-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18a71-110">EXAMPLES</span></span>

### <span data-ttu-id="18a71-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18a71-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="18a71-112">Liste todos os alertas com a gravidade de Sev2 e a condição do monitor Desv2.</span><span class="sxs-lookup"><span data-stu-id="18a71-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="18a71-113">Configurando IncludeContext como true, inclua uma carga de alerta personalizada.</span><span class="sxs-lookup"><span data-stu-id="18a71-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="18a71-114">Use Format-List para obter os detalhes completos de cada alerta na lista.</span><span class="sxs-lookup"><span data-stu-id="18a71-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="18a71-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="18a71-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="18a71-116">Obter detalhes do Alerta por ID (GUID) ou ID do Recurso (ID de ARM completa)</span><span class="sxs-lookup"><span data-stu-id="18a71-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="18a71-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="18a71-117">Example 3</span></span>

<span data-ttu-id="18a71-118">Obter informações de alertas.</span><span class="sxs-lookup"><span data-stu-id="18a71-118">Get Alerts Information.</span></span> <span data-ttu-id="18a71-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="18a71-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="18a71-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18a71-120">PARAMETERS</span></span>

### <span data-ttu-id="18a71-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="18a71-121">-AlertId</span></span>
<span data-ttu-id="18a71-122">Identificador exclusivo de alerta/ResourceId de alerta.</span><span class="sxs-lookup"><span data-stu-id="18a71-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="18a71-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="18a71-123">-AlertRuleId</span></span>
<span data-ttu-id="18a71-124">Filtrar na ID da Regra de Alerta</span><span class="sxs-lookup"><span data-stu-id="18a71-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="18a71-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="18a71-125">-CustomTimeRange</span></span>
<span data-ttu-id="18a71-126">Formato com suporte - \<start-time\> / \<end-time\> onde o tempo está no formato ISO-8601</span><span class="sxs-lookup"><span data-stu-id="18a71-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="18a71-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a71-127">-DefaultProfile</span></span>
<span data-ttu-id="18a71-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18a71-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a71-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="18a71-129">-IncludeContext</span></span>
<span data-ttu-id="18a71-130">Incluir contexto (carga personalizada) de alerta</span><span class="sxs-lookup"><span data-stu-id="18a71-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="18a71-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="18a71-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="18a71-132">Incluir EgressConfig</span><span class="sxs-lookup"><span data-stu-id="18a71-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="18a71-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="18a71-133">-MonitorCondition</span></span>
<span data-ttu-id="18a71-134">Filtrar na Condição de Monitor</span><span class="sxs-lookup"><span data-stu-id="18a71-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="18a71-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="18a71-135">-MonitorService</span></span>
<span data-ttu-id="18a71-136">Filtrar no Serviço de Moniter</span><span class="sxs-lookup"><span data-stu-id="18a71-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="18a71-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="18a71-137">-PageCount</span></span>
<span data-ttu-id="18a71-138">Número de alertas a serem buscados em uma página.</span><span class="sxs-lookup"><span data-stu-id="18a71-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="18a71-139">-Selecionar</span><span class="sxs-lookup"><span data-stu-id="18a71-139">-Select</span></span>
<span data-ttu-id="18a71-140">Projetar os campos necessários fora do essencial.</span><span class="sxs-lookup"><span data-stu-id="18a71-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="18a71-141">A entrada esperada é separada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="18a71-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="18a71-142">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="18a71-142">-Severity</span></span>
<span data-ttu-id="18a71-143">Filtrar na Gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="18a71-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="18a71-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="18a71-144">-SmartGroupId</span></span>
<span data-ttu-id="18a71-145">Filtrar todos os alertas com a ID do Grupo Inteligente</span><span class="sxs-lookup"><span data-stu-id="18a71-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="18a71-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="18a71-146">-SortBy</span></span>
<span data-ttu-id="18a71-147">Propriedade de alerta a ser usada durante a classificação</span><span class="sxs-lookup"><span data-stu-id="18a71-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="18a71-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="18a71-148">-SortOrder</span></span>
<span data-ttu-id="18a71-149">Ordem de Classificação</span><span class="sxs-lookup"><span data-stu-id="18a71-149">Sort Order</span></span>

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

### <span data-ttu-id="18a71-150">-Estado</span><span class="sxs-lookup"><span data-stu-id="18a71-150">-State</span></span>
<span data-ttu-id="18a71-151">Filtrar no Estado de alerta</span><span class="sxs-lookup"><span data-stu-id="18a71-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="18a71-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18a71-152">-TargetResourceGroup</span></span>
<span data-ttu-id="18a71-153">Filtre o nome do grupo Recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="18a71-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="18a71-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="18a71-154">-TargetResourceId</span></span>
<span data-ttu-id="18a71-155">Filtrar a ID do Recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="18a71-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="18a71-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="18a71-156">-TargetResourceType</span></span>
<span data-ttu-id="18a71-157">Filtrar o tipo de recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="18a71-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="18a71-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="18a71-158">-TimeRange</span></span>
<span data-ttu-id="18a71-159">Valores de intervalo de tempo suportados - 1h, 1d, 7d, 30d (Padrão é 1d)</span><span class="sxs-lookup"><span data-stu-id="18a71-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="18a71-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a71-160">CommonParameters</span></span>
<span data-ttu-id="18a71-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a71-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a71-162">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18a71-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a71-163">Entradas</span><span class="sxs-lookup"><span data-stu-id="18a71-163">INPUTS</span></span>

### <span data-ttu-id="18a71-164">Nenhum</span><span class="sxs-lookup"><span data-stu-id="18a71-164">None</span></span>

## <span data-ttu-id="18a71-165">Saídas</span><span class="sxs-lookup"><span data-stu-id="18a71-165">OUTPUTS</span></span>

### <span data-ttu-id="18a71-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="18a71-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="18a71-167">Notas</span><span class="sxs-lookup"><span data-stu-id="18a71-167">NOTES</span></span>

## <span data-ttu-id="18a71-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18a71-168">RELATED LINKS</span></span>
