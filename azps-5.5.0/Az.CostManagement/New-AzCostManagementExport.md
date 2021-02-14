---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115887"
---
# <span data-ttu-id="775c9-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="775c9-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="775c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="775c9-102">SYNOPSIS</span></span>
<span data-ttu-id="775c9-103">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="775c9-103">The operation to create or update a export.</span></span>
<span data-ttu-id="775c9-104">A operação de atualização requer que o eTag mais recente seja definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="775c9-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="775c9-105">Você pode obter o eTag mais recente executando uma operação de get.</span><span class="sxs-lookup"><span data-stu-id="775c9-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="775c9-106">A operação de criação não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="775c9-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="775c9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="775c9-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="775c9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="775c9-108">DESCRIPTION</span></span>
<span data-ttu-id="775c9-109">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="775c9-109">The operation to create or update a export.</span></span>
<span data-ttu-id="775c9-110">A operação de atualização requer que o eTag mais recente seja definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="775c9-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="775c9-111">Você pode obter o eTag mais recente executando uma operação de get.</span><span class="sxs-lookup"><span data-stu-id="775c9-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="775c9-112">A operação de criação não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="775c9-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="775c9-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="775c9-113">EXAMPLES</span></span>

### <span data-ttu-id="775c9-114">Exemplo 1: Criar um AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="775c9-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="775c9-115">Criar um AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="775c9-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="775c9-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="775c9-116">PARAMETERS</span></span>

### <span data-ttu-id="775c9-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="775c9-117">-ConfigurationColumn</span></span>
<span data-ttu-id="775c9-118">Matriz de nomes de coluna a serem incluídos na exportação.</span><span class="sxs-lookup"><span data-stu-id="775c9-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="775c9-119">Se não for fornecida, a exportação incluirá todas as colunas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="775c9-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="775c9-120">As colunas disponíveis podem variar de acordo com o canal do cliente (veja exemplos).</span><span class="sxs-lookup"><span data-stu-id="775c9-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="775c9-121">-DataSetArularity</span><span class="sxs-lookup"><span data-stu-id="775c9-121">-DataSetGranularity</span></span>
<span data-ttu-id="775c9-122">A granularidade das linhas na exportação.</span><span class="sxs-lookup"><span data-stu-id="775c9-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="775c9-123">Atualmente, só há suporte para "Diário".</span><span class="sxs-lookup"><span data-stu-id="775c9-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="775c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775c9-124">-DefaultProfile</span></span>
<span data-ttu-id="775c9-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="775c9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="775c9-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="775c9-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="775c9-127">O período de tempo para a coleta de dados para a exportação.</span><span class="sxs-lookup"><span data-stu-id="775c9-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="775c9-128">Se personalizado, um período de tempo específico deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="775c9-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="775c9-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="775c9-129">-DefinitionType</span></span>
<span data-ttu-id="775c9-130">O tipo de exportação.</span><span class="sxs-lookup"><span data-stu-id="775c9-130">The type of the export.</span></span>
<span data-ttu-id="775c9-131">Observe que "Uso" é equivalente a "RealCost" e é aplicável às exportações que ainda não fornecem dados para encargos ou depreciação para reservas de serviço.</span><span class="sxs-lookup"><span data-stu-id="775c9-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="775c9-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="775c9-132">-DestinationContainer</span></span>
<span data-ttu-id="775c9-133">O nome do contêiner onde as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="775c9-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="775c9-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="775c9-134">-DestinationResourceId</span></span>
<span data-ttu-id="775c9-135">A ID do recurso da conta de armazenamento onde as exportações serão entregues.</span><span class="sxs-lookup"><span data-stu-id="775c9-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="775c9-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="775c9-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="775c9-137">O nome do diretório onde as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="775c9-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="775c9-138">-Formatar</span><span class="sxs-lookup"><span data-stu-id="775c9-138">-Format</span></span>
<span data-ttu-id="775c9-139">O formato da exportação que está sendo entregue.</span><span class="sxs-lookup"><span data-stu-id="775c9-139">The format of the export being delivered.</span></span>
<span data-ttu-id="775c9-140">Atualmente, somente 'Csv' é suportado.</span><span class="sxs-lookup"><span data-stu-id="775c9-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="775c9-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="775c9-141">-Name</span></span>
<span data-ttu-id="775c9-142">Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="775c9-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775c9-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="775c9-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="775c9-144">A data de início da recorrência.</span><span class="sxs-lookup"><span data-stu-id="775c9-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="775c9-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="775c9-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="775c9-146">A data de término da recorrência.</span><span class="sxs-lookup"><span data-stu-id="775c9-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="775c9-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="775c9-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="775c9-148">A recorrência do cronograma.</span><span class="sxs-lookup"><span data-stu-id="775c9-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="775c9-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="775c9-149">-ScheduleStatus</span></span>
<span data-ttu-id="775c9-150">O status do cronograma da exportação.</span><span class="sxs-lookup"><span data-stu-id="775c9-150">The status of the export's schedule.</span></span>
<span data-ttu-id="775c9-151">Se 'Inativo', o cronograma da exportação será pausado.</span><span class="sxs-lookup"><span data-stu-id="775c9-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="775c9-152">-Escopo</span><span class="sxs-lookup"><span data-stu-id="775c9-152">-Scope</span></span>
<span data-ttu-id="775c9-153">Este parâmetro define o escopo de gerenciamento de custos de perspectivas diferentes "Assinatura", "Grupo de Recursos" e "Fornecer Serviço".</span><span class="sxs-lookup"><span data-stu-id="775c9-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="775c9-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="775c9-154">-TimePeriodFrom</span></span>
<span data-ttu-id="775c9-155">A data de início para exportar dados.</span><span class="sxs-lookup"><span data-stu-id="775c9-155">The start date for export data.</span></span>

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

### <span data-ttu-id="775c9-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="775c9-156">-TimePeriodTo</span></span>
<span data-ttu-id="775c9-157">A data de término dos dados de exportação.</span><span class="sxs-lookup"><span data-stu-id="775c9-157">The end date for export data.</span></span>

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

### <span data-ttu-id="775c9-158">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="775c9-158">-Confirm</span></span>
<span data-ttu-id="775c9-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="775c9-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="775c9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="775c9-160">-WhatIf</span></span>
<span data-ttu-id="775c9-161">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="775c9-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="775c9-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="775c9-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="775c9-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775c9-163">CommonParameters</span></span>
<span data-ttu-id="775c9-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="775c9-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775c9-165">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="775c9-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775c9-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="775c9-166">INPUTS</span></span>

## <span data-ttu-id="775c9-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="775c9-167">OUTPUTS</span></span>

### <span data-ttu-id="775c9-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="775c9-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="775c9-169">Notas</span><span class="sxs-lookup"><span data-stu-id="775c9-169">NOTES</span></span>

<span data-ttu-id="775c9-170">Aliases</span><span class="sxs-lookup"><span data-stu-id="775c9-170">ALIASES</span></span>

## <span data-ttu-id="775c9-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="775c9-171">RELATED LINKS</span></span>

