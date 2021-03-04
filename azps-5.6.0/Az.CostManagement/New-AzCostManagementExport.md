---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: bc3ff9c6d27cba92cf29090dda988a27f9e8a50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892986"
---
# <span data-ttu-id="1d75f-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1d75f-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="1d75f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d75f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d75f-103">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-103">The operation to create or update a export.</span></span>
<span data-ttu-id="1d75f-104">A operação de atualização exige que a eTag mais recente seja definida na solicitação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="1d75f-105">Você pode obter a eTag mais recente executando uma operação get.</span><span class="sxs-lookup"><span data-stu-id="1d75f-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="1d75f-106">Criar operação não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="1d75f-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="1d75f-107">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1d75f-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1d75f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1d75f-108">DESCRIPTION</span></span>
<span data-ttu-id="1d75f-109">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-109">The operation to create or update a export.</span></span>
<span data-ttu-id="1d75f-110">A operação de atualização exige que a eTag mais recente seja definida na solicitação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="1d75f-111">Você pode obter a eTag mais recente executando uma operação get.</span><span class="sxs-lookup"><span data-stu-id="1d75f-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="1d75f-112">Criar operação não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="1d75f-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="1d75f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d75f-113">EXAMPLES</span></span>

### <span data-ttu-id="1d75f-114">Exemplo 1: Criar um AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1d75f-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="1d75f-115">Criar um AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1d75f-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="1d75f-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1d75f-116">PARAMETERS</span></span>

### <span data-ttu-id="1d75f-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="1d75f-117">-ConfigurationColumn</span></span>
<span data-ttu-id="1d75f-118">Matriz de nomes de coluna a serem incluídos na exportação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="1d75f-119">Se não for fornecida, a exportação incluirá todas as colunas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1d75f-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="1d75f-120">As colunas disponíveis podem variar de acordo com o canal do cliente (veja exemplos).</span><span class="sxs-lookup"><span data-stu-id="1d75f-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="1d75f-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="1d75f-121">-DataSetGranularity</span></span>
<span data-ttu-id="1d75f-122">A granularidade das linhas na exportação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="1d75f-123">Atualmente, apenas o 'Diário' é suportado.</span><span class="sxs-lookup"><span data-stu-id="1d75f-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="1d75f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d75f-124">-DefaultProfile</span></span>
<span data-ttu-id="1d75f-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d75f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d75f-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="1d75f-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="1d75f-127">O período de tempo para a retirada de dados para a exportação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="1d75f-128">Se personalizado, um período de tempo específico deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="1d75f-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="1d75f-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="1d75f-129">-DefinitionType</span></span>
<span data-ttu-id="1d75f-130">O tipo de exportação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-130">The type of the export.</span></span>
<span data-ttu-id="1d75f-131">Observe que 'Uso' é equivalente a 'ActualCost' e é aplicável às exportações que ainda não fornecem dados para encargos ou amortização para reservas de serviço.</span><span class="sxs-lookup"><span data-stu-id="1d75f-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="1d75f-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="1d75f-132">-DestinationContainer</span></span>
<span data-ttu-id="1d75f-133">O nome do contêiner onde as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="1d75f-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="1d75f-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="1d75f-134">-DestinationResourceId</span></span>
<span data-ttu-id="1d75f-135">A ID do recurso da conta de armazenamento onde as exportações serão entregues.</span><span class="sxs-lookup"><span data-stu-id="1d75f-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="1d75f-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="1d75f-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="1d75f-137">O nome do diretório onde as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="1d75f-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="1d75f-138">-Format</span><span class="sxs-lookup"><span data-stu-id="1d75f-138">-Format</span></span>
<span data-ttu-id="1d75f-139">O formato da exportação que está sendo entregue.</span><span class="sxs-lookup"><span data-stu-id="1d75f-139">The format of the export being delivered.</span></span>
<span data-ttu-id="1d75f-140">Atualmente, apenas 'Csv' é suportado.</span><span class="sxs-lookup"><span data-stu-id="1d75f-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="1d75f-141">-Name</span><span class="sxs-lookup"><span data-stu-id="1d75f-141">-Name</span></span>
<span data-ttu-id="1d75f-142">Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-142">Export Name.</span></span>

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

### <span data-ttu-id="1d75f-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="1d75f-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="1d75f-144">A data de início da recorrência.</span><span class="sxs-lookup"><span data-stu-id="1d75f-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="1d75f-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="1d75f-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="1d75f-146">A data de término da recorrência.</span><span class="sxs-lookup"><span data-stu-id="1d75f-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="1d75f-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="1d75f-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="1d75f-148">A recorrência de agendamento.</span><span class="sxs-lookup"><span data-stu-id="1d75f-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="1d75f-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="1d75f-149">-ScheduleStatus</span></span>
<span data-ttu-id="1d75f-150">O status da agenda da exportação.</span><span class="sxs-lookup"><span data-stu-id="1d75f-150">The status of the export's schedule.</span></span>
<span data-ttu-id="1d75f-151">Se 'Inativo', a agenda da exportação será pausada.</span><span class="sxs-lookup"><span data-stu-id="1d75f-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="1d75f-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="1d75f-152">-Scope</span></span>
<span data-ttu-id="1d75f-153">Este parâmetro define o escopo de gerenciamento de custos de diferentes perspectivas 'Subscription','ResourceGroup' e 'Provide Service'.</span><span class="sxs-lookup"><span data-stu-id="1d75f-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="1d75f-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="1d75f-154">-TimePeriodFrom</span></span>
<span data-ttu-id="1d75f-155">A data de início para exportar dados.</span><span class="sxs-lookup"><span data-stu-id="1d75f-155">The start date for export data.</span></span>

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

### <span data-ttu-id="1d75f-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="1d75f-156">-TimePeriodTo</span></span>
<span data-ttu-id="1d75f-157">A data de término para exportar dados.</span><span class="sxs-lookup"><span data-stu-id="1d75f-157">The end date for export data.</span></span>

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

### <span data-ttu-id="1d75f-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d75f-158">-Confirm</span></span>
<span data-ttu-id="1d75f-159">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d75f-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d75f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d75f-160">-WhatIf</span></span>
<span data-ttu-id="1d75f-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d75f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d75f-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d75f-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d75f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d75f-163">CommonParameters</span></span>
<span data-ttu-id="1d75f-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d75f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d75f-165">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d75f-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d75f-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d75f-166">INPUTS</span></span>

## <span data-ttu-id="1d75f-167">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1d75f-167">OUTPUTS</span></span>

### <span data-ttu-id="1d75f-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="1d75f-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="1d75f-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="1d75f-169">NOTES</span></span>

<span data-ttu-id="1d75f-170">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1d75f-170">ALIASES</span></span>

## <span data-ttu-id="1d75f-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d75f-171">RELATED LINKS</span></span>

