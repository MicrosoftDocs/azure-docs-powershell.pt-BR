---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256754"
---
# <span data-ttu-id="720a5-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="720a5-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="720a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="720a5-102">SYNOPSIS</span></span>
<span data-ttu-id="720a5-103">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="720a5-103">The operation to create or update a export.</span></span>
<span data-ttu-id="720a5-104">A operação de atualização requer que o eTag mais recente seja definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="720a5-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="720a5-105">Você pode obter a eTag mais recente executando uma operação obter.</span><span class="sxs-lookup"><span data-stu-id="720a5-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="720a5-106">A operação Create não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="720a5-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="720a5-107">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="720a5-107">SYNTAX</span></span>

### <span data-ttu-id="720a5-108">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="720a5-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="720a5-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="720a5-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="720a5-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="720a5-110">DESCRIPTION</span></span>
<span data-ttu-id="720a5-111">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="720a5-111">The operation to create or update a export.</span></span>
<span data-ttu-id="720a5-112">A operação de atualização requer que o eTag mais recente seja definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="720a5-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="720a5-113">Você pode obter a eTag mais recente executando uma operação obter.</span><span class="sxs-lookup"><span data-stu-id="720a5-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="720a5-114">A operação Create não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="720a5-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="720a5-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="720a5-115">EXAMPLES</span></span>

### <span data-ttu-id="720a5-116">Exemplo 1: atualizar AzCostManagementExport por escopo e nome</span><span class="sxs-lookup"><span data-stu-id="720a5-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="720a5-117">Atualizar AzCostManagementExport pelo escopo e nome</span><span class="sxs-lookup"><span data-stu-id="720a5-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="720a5-118">Exemplo 2: atualizar AzCostManagementExport por InputObject</span><span class="sxs-lookup"><span data-stu-id="720a5-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="720a5-119">Atualizar o AzCostManagementExport por InputObject</span><span class="sxs-lookup"><span data-stu-id="720a5-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="720a5-120">OS</span><span class="sxs-lookup"><span data-stu-id="720a5-120">PARAMETERS</span></span>

### <span data-ttu-id="720a5-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="720a5-121">-ConfigurationColumn</span></span>
<span data-ttu-id="720a5-122">Matriz de nomes de coluna a serem incluídos na exportação.</span><span class="sxs-lookup"><span data-stu-id="720a5-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="720a5-123">Se não for fornecido, a exportação incluirá todas as colunas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="720a5-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="720a5-124">As colunas disponíveis podem variar de acordo com o canal do cliente (consulte exemplos).</span><span class="sxs-lookup"><span data-stu-id="720a5-124">The available columns can vary by customer channel (see examples).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="720a5-125">-DataSetGranularity</span></span>
<span data-ttu-id="720a5-126">A granularidade das linhas na exportação.</span><span class="sxs-lookup"><span data-stu-id="720a5-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="720a5-127">Atualmente apenas "diário" tem suporte.</span><span class="sxs-lookup"><span data-stu-id="720a5-127">Currently only 'Daily' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720a5-128">-DefaultProfile</span></span>
<span data-ttu-id="720a5-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="720a5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="720a5-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="720a5-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="720a5-131">O intervalo de tempo para a recepção de dados para a exportação.</span><span class="sxs-lookup"><span data-stu-id="720a5-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="720a5-132">Se for personalizado, um período de tempo específico deverá ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="720a5-132">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-133">-Definitiontype</span><span class="sxs-lookup"><span data-stu-id="720a5-133">-DefinitionType</span></span>
<span data-ttu-id="720a5-134">O tipo da exportação.</span><span class="sxs-lookup"><span data-stu-id="720a5-134">The type of the export.</span></span>
<span data-ttu-id="720a5-135">Observe que ' Usage ' é equivalente a ' ActualCost ' e se aplica a exportações que ainda não fornecem dados para cobranças ou amortização para reservas de serviço.</span><span class="sxs-lookup"><span data-stu-id="720a5-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="720a5-136">-DestinationContainer</span></span>
<span data-ttu-id="720a5-137">O nome do contêiner em que as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="720a5-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="720a5-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="720a5-138">-DestinationResourceId</span></span>
<span data-ttu-id="720a5-139">A ID do recurso da conta de armazenamento na qual as exportações serão entregues.</span><span class="sxs-lookup"><span data-stu-id="720a5-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="720a5-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="720a5-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="720a5-141">O nome do diretório em que as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="720a5-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="720a5-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="720a5-142">-ETag</span></span>
<span data-ttu-id="720a5-143">eTag do recurso.</span><span class="sxs-lookup"><span data-stu-id="720a5-143">eTag of the resource.</span></span>
<span data-ttu-id="720a5-144">Para manipular o cenário de atualização simultânea, este campo será usado para determinar se o usuário está atualizando a versão mais recente ou não.</span><span class="sxs-lookup"><span data-stu-id="720a5-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="720a5-145">-Format</span><span class="sxs-lookup"><span data-stu-id="720a5-145">-Format</span></span>
<span data-ttu-id="720a5-146">O formato da exportação que está sendo entregue.</span><span class="sxs-lookup"><span data-stu-id="720a5-146">The format of the export being delivered.</span></span>
<span data-ttu-id="720a5-147">Atualmente só há suporte para "CSV".</span><span class="sxs-lookup"><span data-stu-id="720a5-147">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="720a5-148">-InputObject</span></span>
<span data-ttu-id="720a5-149">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="720a5-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="720a5-150">-Name</span></span>
<span data-ttu-id="720a5-151">Nome para exportação.</span><span class="sxs-lookup"><span data-stu-id="720a5-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="720a5-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="720a5-153">A data de início da recorrência.</span><span class="sxs-lookup"><span data-stu-id="720a5-153">The start date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="720a5-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="720a5-155">A data de término da recorrência.</span><span class="sxs-lookup"><span data-stu-id="720a5-155">The end date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="720a5-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="720a5-157">A recorrência do cronograma.</span><span class="sxs-lookup"><span data-stu-id="720a5-157">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="720a5-158">-ScheduleStatus</span></span>
<span data-ttu-id="720a5-159">O status do cronograma da exportação.</span><span class="sxs-lookup"><span data-stu-id="720a5-159">The status of the export's schedule.</span></span>
<span data-ttu-id="720a5-160">Se ' inativo ', o cronograma da exportação será pausado.</span><span class="sxs-lookup"><span data-stu-id="720a5-160">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-161">-Escopo</span><span class="sxs-lookup"><span data-stu-id="720a5-161">-Scope</span></span>
<span data-ttu-id="720a5-162">Esse parâmetro define o escopo de costmanagement de uma "assinatura", "Resource" e "fornecer serviço" de perspectivas diferentes.</span><span class="sxs-lookup"><span data-stu-id="720a5-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="720a5-163">-TimePeriodFrom</span></span>
<span data-ttu-id="720a5-164">A data de início para exportar dados.</span><span class="sxs-lookup"><span data-stu-id="720a5-164">The start date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-165">-Timeperiodto</span><span class="sxs-lookup"><span data-stu-id="720a5-165">-TimePeriodTo</span></span>
<span data-ttu-id="720a5-166">A data de término da exportação de dados.</span><span class="sxs-lookup"><span data-stu-id="720a5-166">The end date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a5-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="720a5-167">-Confirm</span></span>
<span data-ttu-id="720a5-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="720a5-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="720a5-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="720a5-169">-WhatIf</span></span>
<span data-ttu-id="720a5-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="720a5-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="720a5-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="720a5-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="720a5-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720a5-172">CommonParameters</span></span>
<span data-ttu-id="720a5-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="720a5-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720a5-174">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="720a5-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720a5-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="720a5-175">INPUTS</span></span>

### <span data-ttu-id="720a5-176">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="720a5-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="720a5-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="720a5-177">OUTPUTS</span></span>

### <span data-ttu-id="720a5-178">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="720a5-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="720a5-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="720a5-179">NOTES</span></span>

<span data-ttu-id="720a5-180">ALIASES</span><span class="sxs-lookup"><span data-stu-id="720a5-180">ALIASES</span></span>

<span data-ttu-id="720a5-181">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="720a5-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="720a5-182">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="720a5-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="720a5-183">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="720a5-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="720a5-184">INPUTobject <ICostManagementIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="720a5-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="720a5-185">`[AlertId <String>]`: ID do alerta</span><span class="sxs-lookup"><span data-stu-id="720a5-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="720a5-186">`[ExportName <String>]`: Exportar nome.</span><span class="sxs-lookup"><span data-stu-id="720a5-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="720a5-187">`[ExternalCloudProviderId <String>]`: Pode ser ' {externalSubscriptionId} ' para a conta vinculada ou ' {externalBillingAccountId} ' para a conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="720a5-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="720a5-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="720a5-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="720a5-189">Isso inclui "externalSubscriptions" para a conta vinculada e "externalBillingAccounts" para a conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="720a5-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="720a5-190">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="720a5-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="720a5-191">`[Scope <String>]`: O escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="720a5-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="720a5-192">Isso inclui ' assinaturas/{SubscriptionId} ' para o escopo da assinatura, ' assinaturas/{SubscriptionId}/resourceGroups/{resourceGroupName} ' para o escopo do subsource, ' provedores/Microsoft. billing/billingAccounts/{billingAccountId} ' para o escopo da conta de cobrança, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/departamentos/{DepartmentID} ' para escopo do departamento, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} ' para escopo EnrollmentAccount, ' Providers billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' para BillingProfile Scope, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' para InvoiceSection Scope, ' Providers/Microsoft. Management/managementGroups/{managementGroupId} ' para o escopo do grupo de gerenciamento, ' Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} ' para o escopo da conta de cobrança externa e os ' provedores/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} ' para o escopo de assinatura externa.</span><span class="sxs-lookup"><span data-stu-id="720a5-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="720a5-193">`[ViewName <String>]`: Nome do modo de exibição</span><span class="sxs-lookup"><span data-stu-id="720a5-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="720a5-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="720a5-194">RELATED LINKS</span></span>

