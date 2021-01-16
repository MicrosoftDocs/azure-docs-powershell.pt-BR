---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258821"
---
# <span data-ttu-id="c5172-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="c5172-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="c5172-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5172-102">SYNOPSIS</span></span>
<span data-ttu-id="c5172-103">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="c5172-103">The operation to create or update a export.</span></span>
<span data-ttu-id="c5172-104">A operação de atualização requer que o eTag mais recente seja definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="c5172-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="c5172-105">Você pode obter a eTag mais recente executando uma operação obter.</span><span class="sxs-lookup"><span data-stu-id="c5172-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="c5172-106">A operação Create não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="c5172-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="c5172-107">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5172-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c5172-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5172-108">DESCRIPTION</span></span>
<span data-ttu-id="c5172-109">A operação para criar ou atualizar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="c5172-109">The operation to create or update a export.</span></span>
<span data-ttu-id="c5172-110">A operação de atualização requer que o eTag mais recente seja definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="c5172-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="c5172-111">Você pode obter a eTag mais recente executando uma operação obter.</span><span class="sxs-lookup"><span data-stu-id="c5172-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="c5172-112">A operação Create não requer eTag.</span><span class="sxs-lookup"><span data-stu-id="c5172-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="c5172-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5172-113">EXAMPLES</span></span>

### <span data-ttu-id="c5172-114">Exemplo 1: criar um AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="c5172-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="c5172-115">Criar uma AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="c5172-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="c5172-116">OS</span><span class="sxs-lookup"><span data-stu-id="c5172-116">PARAMETERS</span></span>

### <span data-ttu-id="c5172-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="c5172-117">-ConfigurationColumn</span></span>
<span data-ttu-id="c5172-118">Matriz de nomes de coluna a serem incluídos na exportação.</span><span class="sxs-lookup"><span data-stu-id="c5172-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="c5172-119">Se não for fornecido, a exportação incluirá todas as colunas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c5172-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="c5172-120">As colunas disponíveis podem variar de acordo com o canal do cliente (consulte exemplos).</span><span class="sxs-lookup"><span data-stu-id="c5172-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="c5172-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="c5172-121">-DataSetGranularity</span></span>
<span data-ttu-id="c5172-122">A granularidade das linhas na exportação.</span><span class="sxs-lookup"><span data-stu-id="c5172-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="c5172-123">Atualmente apenas "diário" tem suporte.</span><span class="sxs-lookup"><span data-stu-id="c5172-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="c5172-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5172-124">-DefaultProfile</span></span>
<span data-ttu-id="c5172-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5172-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5172-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="c5172-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="c5172-127">O intervalo de tempo para a recepção de dados para a exportação.</span><span class="sxs-lookup"><span data-stu-id="c5172-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="c5172-128">Se for personalizado, um período de tempo específico deverá ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="c5172-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="c5172-129">-Definitiontype</span><span class="sxs-lookup"><span data-stu-id="c5172-129">-DefinitionType</span></span>
<span data-ttu-id="c5172-130">O tipo da exportação.</span><span class="sxs-lookup"><span data-stu-id="c5172-130">The type of the export.</span></span>
<span data-ttu-id="c5172-131">Observe que ' Usage ' é equivalente a ' ActualCost ' e se aplica a exportações que ainda não fornecem dados para cobranças ou amortização para reservas de serviço.</span><span class="sxs-lookup"><span data-stu-id="c5172-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="c5172-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="c5172-132">-DestinationContainer</span></span>
<span data-ttu-id="c5172-133">O nome do contêiner em que as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="c5172-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="c5172-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="c5172-134">-DestinationResourceId</span></span>
<span data-ttu-id="c5172-135">A ID do recurso da conta de armazenamento na qual as exportações serão entregues.</span><span class="sxs-lookup"><span data-stu-id="c5172-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="c5172-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="c5172-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="c5172-137">O nome do diretório em que as exportações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="c5172-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="c5172-138">-Format</span><span class="sxs-lookup"><span data-stu-id="c5172-138">-Format</span></span>
<span data-ttu-id="c5172-139">O formato da exportação que está sendo entregue.</span><span class="sxs-lookup"><span data-stu-id="c5172-139">The format of the export being delivered.</span></span>
<span data-ttu-id="c5172-140">Atualmente só há suporte para "CSV".</span><span class="sxs-lookup"><span data-stu-id="c5172-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="c5172-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5172-141">-Name</span></span>
<span data-ttu-id="c5172-142">Nome para exportação.</span><span class="sxs-lookup"><span data-stu-id="c5172-142">Export Name.</span></span>

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

### <span data-ttu-id="c5172-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="c5172-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="c5172-144">A data de início da recorrência.</span><span class="sxs-lookup"><span data-stu-id="c5172-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="c5172-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="c5172-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="c5172-146">A data de término da recorrência.</span><span class="sxs-lookup"><span data-stu-id="c5172-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="c5172-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="c5172-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="c5172-148">A recorrência do cronograma.</span><span class="sxs-lookup"><span data-stu-id="c5172-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="c5172-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="c5172-149">-ScheduleStatus</span></span>
<span data-ttu-id="c5172-150">O status do cronograma da exportação.</span><span class="sxs-lookup"><span data-stu-id="c5172-150">The status of the export's schedule.</span></span>
<span data-ttu-id="c5172-151">Se ' inativo ', o cronograma da exportação será pausado.</span><span class="sxs-lookup"><span data-stu-id="c5172-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="c5172-152">-Escopo</span><span class="sxs-lookup"><span data-stu-id="c5172-152">-Scope</span></span>
<span data-ttu-id="c5172-153">Esse parâmetro define o escopo de costmanagement de uma "assinatura", "Resource" e "fornecer serviço" de perspectivas diferentes.</span><span class="sxs-lookup"><span data-stu-id="c5172-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="c5172-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="c5172-154">-TimePeriodFrom</span></span>
<span data-ttu-id="c5172-155">A data de início para exportar dados.</span><span class="sxs-lookup"><span data-stu-id="c5172-155">The start date for export data.</span></span>

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

### <span data-ttu-id="c5172-156">-Timeperiodto</span><span class="sxs-lookup"><span data-stu-id="c5172-156">-TimePeriodTo</span></span>
<span data-ttu-id="c5172-157">A data de término da exportação de dados.</span><span class="sxs-lookup"><span data-stu-id="c5172-157">The end date for export data.</span></span>

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

### <span data-ttu-id="c5172-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5172-158">-Confirm</span></span>
<span data-ttu-id="c5172-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5172-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5172-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5172-160">-WhatIf</span></span>
<span data-ttu-id="c5172-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5172-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5172-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5172-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5172-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5172-163">CommonParameters</span></span>
<span data-ttu-id="c5172-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5172-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5172-165">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5172-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5172-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5172-166">INPUTS</span></span>

## <span data-ttu-id="c5172-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5172-167">OUTPUTS</span></span>

### <span data-ttu-id="c5172-168">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="c5172-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="c5172-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5172-169">NOTES</span></span>

<span data-ttu-id="c5172-170">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c5172-170">ALIASES</span></span>

## <span data-ttu-id="c5172-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5172-171">RELATED LINKS</span></span>

