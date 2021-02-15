---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112006"
---
# <span data-ttu-id="d1c67-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d1c67-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="d1c67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1c67-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c67-103">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-103">The operation to create or update a export.</span></span>
<span data-ttu-id="d1c67-104">A operação de atualização requer que o eTag mais recente seja definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d1c67-105">Você pode obter o eTag mais recente executando uma operação de get.</span><span class="sxs-lookup"><span data-stu-id="d1c67-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d1c67-106">A operação de criação não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="d1c67-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d1c67-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1c67-107">SYNTAX</span></span>

### <span data-ttu-id="d1c67-108">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d1c67-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1c67-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1c67-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1c67-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1c67-110">DESCRIPTION</span></span>
<span data-ttu-id="d1c67-111">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-111">The operation to create or update a export.</span></span>
<span data-ttu-id="d1c67-112">A operação de atualização requer que o eTag mais recente seja definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d1c67-113">Você pode obter o eTag mais recente executando uma operação de get.</span><span class="sxs-lookup"><span data-stu-id="d1c67-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d1c67-114">A operação de criação não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="d1c67-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d1c67-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1c67-115">EXAMPLES</span></span>

### <span data-ttu-id="d1c67-116">Exemplo 1: Atualizar a AzCostManagementExport por escopo e nome</span><span class="sxs-lookup"><span data-stu-id="d1c67-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="d1c67-117">Atualizar a AzCostManagementExport por Escopo e nome</span><span class="sxs-lookup"><span data-stu-id="d1c67-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="d1c67-118">Exemplo 2: Atualizar AzCostManagementExport por InputObject</span><span class="sxs-lookup"><span data-stu-id="d1c67-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="d1c67-119">Atualizar AzCostManagementExport por InputObject</span><span class="sxs-lookup"><span data-stu-id="d1c67-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="d1c67-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1c67-120">PARAMETERS</span></span>

### <span data-ttu-id="d1c67-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="d1c67-121">-ConfigurationColumn</span></span>
<span data-ttu-id="d1c67-122">Matriz de nomes de coluna a serem incluídos na exportação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="d1c67-123">Se não for fornecida, a exportação incluirá todas as colunas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d1c67-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="d1c67-124">As colunas disponíveis podem variar de acordo com o canal do cliente (veja exemplos).</span><span class="sxs-lookup"><span data-stu-id="d1c67-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="d1c67-125">-DataSetArularity</span><span class="sxs-lookup"><span data-stu-id="d1c67-125">-DataSetGranularity</span></span>
<span data-ttu-id="d1c67-126">A granularidade das linhas na exportação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="d1c67-127">Atualmente, só há suporte para "Diário".</span><span class="sxs-lookup"><span data-stu-id="d1c67-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="d1c67-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c67-128">-DefaultProfile</span></span>
<span data-ttu-id="d1c67-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1c67-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1c67-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="d1c67-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="d1c67-131">O período de tempo para a coleta de dados para a exportação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="d1c67-132">Se personalizado, um período de tempo específico deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1c67-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="d1c67-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="d1c67-133">-DefinitionType</span></span>
<span data-ttu-id="d1c67-134">O tipo de exportação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-134">The type of the export.</span></span>
<span data-ttu-id="d1c67-135">Observe que "Uso" é equivalente a "RealCost" e é aplicável às exportações que ainda não fornecem dados para encargos ou depreciação para reservas de serviço.</span><span class="sxs-lookup"><span data-stu-id="d1c67-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="d1c67-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="d1c67-136">-DestinationContainer</span></span>
<span data-ttu-id="d1c67-137">O nome do contêiner onde as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="d1c67-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d1c67-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d1c67-138">-DestinationResourceId</span></span>
<span data-ttu-id="d1c67-139">A ID do recurso da conta de armazenamento onde as exportações serão entregues.</span><span class="sxs-lookup"><span data-stu-id="d1c67-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="d1c67-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="d1c67-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="d1c67-141">O nome do diretório onde as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="d1c67-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d1c67-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="d1c67-142">-ETag</span></span>
<span data-ttu-id="d1c67-143">eTag do recurso.</span><span class="sxs-lookup"><span data-stu-id="d1c67-143">eTag of the resource.</span></span>
<span data-ttu-id="d1c67-144">Para lidar com o cenário de atualização simultânea, esse campo será usado para determinar se o usuário está atualizando ou não a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="d1c67-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="d1c67-145">-Formatar</span><span class="sxs-lookup"><span data-stu-id="d1c67-145">-Format</span></span>
<span data-ttu-id="d1c67-146">O formato da exportação que está sendo entregue.</span><span class="sxs-lookup"><span data-stu-id="d1c67-146">The format of the export being delivered.</span></span>
<span data-ttu-id="d1c67-147">Atualmente, somente 'Csv' é suportado.</span><span class="sxs-lookup"><span data-stu-id="d1c67-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="d1c67-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1c67-148">-InputObject</span></span>
<span data-ttu-id="d1c67-149">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="d1c67-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1c67-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1c67-150">-Name</span></span>
<span data-ttu-id="d1c67-151">Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="d1c67-151">Export Name.</span></span>

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

### <span data-ttu-id="d1c67-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d1c67-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="d1c67-153">A data de início da recorrência.</span><span class="sxs-lookup"><span data-stu-id="d1c67-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="d1c67-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d1c67-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="d1c67-155">A data de término da recorrência.</span><span class="sxs-lookup"><span data-stu-id="d1c67-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="d1c67-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="d1c67-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="d1c67-157">A recorrência do cronograma.</span><span class="sxs-lookup"><span data-stu-id="d1c67-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="d1c67-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="d1c67-158">-ScheduleStatus</span></span>
<span data-ttu-id="d1c67-159">O status do cronograma da exportação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-159">The status of the export's schedule.</span></span>
<span data-ttu-id="d1c67-160">Se 'Inativo', o cronograma da exportação será pausado.</span><span class="sxs-lookup"><span data-stu-id="d1c67-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="d1c67-161">-Escopo</span><span class="sxs-lookup"><span data-stu-id="d1c67-161">-Scope</span></span>
<span data-ttu-id="d1c67-162">Este parâmetro define o escopo de gerenciamento de custos de perspectivas diferentes "Assinatura", "Grupo de Recursos" e "Fornecer Serviço".</span><span class="sxs-lookup"><span data-stu-id="d1c67-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="d1c67-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d1c67-163">-TimePeriodFrom</span></span>
<span data-ttu-id="d1c67-164">A data de início para exportar dados.</span><span class="sxs-lookup"><span data-stu-id="d1c67-164">The start date for export data.</span></span>

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

### <span data-ttu-id="d1c67-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d1c67-165">-TimePeriodTo</span></span>
<span data-ttu-id="d1c67-166">A data de término dos dados de exportação.</span><span class="sxs-lookup"><span data-stu-id="d1c67-166">The end date for export data.</span></span>

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

### <span data-ttu-id="d1c67-167">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d1c67-167">-Confirm</span></span>
<span data-ttu-id="d1c67-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1c67-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1c67-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1c67-169">-WhatIf</span></span>
<span data-ttu-id="d1c67-170">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d1c67-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1c67-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1c67-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1c67-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c67-172">CommonParameters</span></span>
<span data-ttu-id="d1c67-173">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c67-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c67-174">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1c67-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c67-175">Entradas</span><span class="sxs-lookup"><span data-stu-id="d1c67-175">INPUTS</span></span>

### <span data-ttu-id="d1c67-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="d1c67-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="d1c67-177">Saídas</span><span class="sxs-lookup"><span data-stu-id="d1c67-177">OUTPUTS</span></span>

### <span data-ttu-id="d1c67-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="d1c67-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="d1c67-179">Notas</span><span class="sxs-lookup"><span data-stu-id="d1c67-179">NOTES</span></span>

<span data-ttu-id="d1c67-180">Aliases</span><span class="sxs-lookup"><span data-stu-id="d1c67-180">ALIASES</span></span>

<span data-ttu-id="d1c67-181">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="d1c67-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1c67-182">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d1c67-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1c67-183">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1c67-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1c67-184">INPUTOBJECT: <ICostManagementIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="d1c67-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1c67-185">`[AlertId <String>]`: ID de alerta</span><span class="sxs-lookup"><span data-stu-id="d1c67-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="d1c67-186">`[ExportName <String>]`: Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="d1c67-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="d1c67-187">`[ExternalCloudProviderId <String>]`: pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para contas consolidadas usadas com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="d1c67-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="d1c67-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: o tipo de provedor de nuvem externo associado às operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="d1c67-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="d1c67-189">Isso inclui "externalSubscriptions" para conta vinculada e "externalBillingAccounts" para conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="d1c67-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="d1c67-190">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d1c67-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1c67-191">`[Scope <String>]`: o escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="d1c67-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="d1c67-192">Isso inclui "assinaturas/{subscriptionId}" para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}' para escopo de Conta de Cobrança, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' para escopo do Departamento, 'provedores/Microsoft.Billing/billingAccounts/{billingAccounts}/enrollmentAccounts/{enrollmentAccountId}' para o escopo de EnrollmentAccounts, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' para escopo invoiceSection, 'provedores/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.</span><span class="sxs-lookup"><span data-stu-id="d1c67-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="d1c67-193">`[ViewName <String>]`: Nome da exibição</span><span class="sxs-lookup"><span data-stu-id="d1c67-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="d1c67-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1c67-194">RELATED LINKS</span></span>

