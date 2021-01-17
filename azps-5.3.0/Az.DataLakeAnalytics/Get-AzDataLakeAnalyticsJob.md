---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429836"
---
# <span data-ttu-id="09074-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="09074-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="09074-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09074-102">SYNOPSIS</span></span>
<span data-ttu-id="09074-103">Obtém um trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="09074-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="09074-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09074-104">SYNTAX</span></span>

### <span data-ttu-id="09074-105">GetAllInResourceGroupAndAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="09074-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09074-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="09074-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09074-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09074-107">DESCRIPTION</span></span>
<span data-ttu-id="09074-108">O cmdlet **Get-AzDataLakeAnalyticsJob** Obtém um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="09074-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="09074-109">Se você não especificar um trabalho, esse cmdlet receberá todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="09074-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="09074-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09074-110">EXAMPLES</span></span>

### <span data-ttu-id="09074-111">Exemplo 1: obter um trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="09074-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="09074-112">Este comando obtém o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="09074-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="09074-113">Exemplo 2: obter trabalhos enviados na semana passada</span><span class="sxs-lookup"><span data-stu-id="09074-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="09074-114">Este comando obtém os trabalhos enviados na última semana.</span><span class="sxs-lookup"><span data-stu-id="09074-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="09074-115">OS</span><span class="sxs-lookup"><span data-stu-id="09074-115">PARAMETERS</span></span>

### <span data-ttu-id="09074-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="09074-116">-Account</span></span>
<span data-ttu-id="09074-117">Especifica o nome de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="09074-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09074-118">-DefaultProfile</span></span>
<span data-ttu-id="09074-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="09074-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09074-120">-Include</span><span class="sxs-lookup"><span data-stu-id="09074-120">-Include</span></span>
<span data-ttu-id="09074-121">Especifica as opções que indicam o tipo de informação adicional a ser recuperada sobre o trabalho.</span><span class="sxs-lookup"><span data-stu-id="09074-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="09074-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="09074-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09074-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="09074-123">None</span></span>
- <span data-ttu-id="09074-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="09074-124">DebugInfo</span></span>
- <span data-ttu-id="09074-125">As</span><span class="sxs-lookup"><span data-stu-id="09074-125">Statistics</span></span>
- <span data-ttu-id="09074-126">Todo</span><span class="sxs-lookup"><span data-stu-id="09074-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="09074-127">-JobId</span></span>
<span data-ttu-id="09074-128">Especifica a ID do trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="09074-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="09074-129">-Name</span></span>
<span data-ttu-id="09074-130">Especifica um nome a ser usado para filtrar os resultados da lista de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="09074-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="09074-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="09074-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09074-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="09074-132">None</span></span>
- <span data-ttu-id="09074-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="09074-133">DebugInfo</span></span>
- <span data-ttu-id="09074-134">As</span><span class="sxs-lookup"><span data-stu-id="09074-134">Statistics</span></span>
- <span data-ttu-id="09074-135">Todo</span><span class="sxs-lookup"><span data-stu-id="09074-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-136">-Pipelineid</span><span class="sxs-lookup"><span data-stu-id="09074-136">-PipelineId</span></span>
<span data-ttu-id="09074-137">Uma ID opcional que indica apenas as tarefas que parte do pipeline especificado deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="09074-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-138">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="09074-138">-RecurrenceId</span></span>
<span data-ttu-id="09074-139">Uma ID opcional que indica apenas as tarefas que parte da recorrência especificada deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="09074-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-140">-Resultado</span><span class="sxs-lookup"><span data-stu-id="09074-140">-Result</span></span>
<span data-ttu-id="09074-141">Especifica um filtro de resultado para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="09074-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="09074-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="09074-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09074-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="09074-143">None</span></span>
- <span data-ttu-id="09074-144">Cela</span><span class="sxs-lookup"><span data-stu-id="09074-144">Cancelled</span></span>
- <span data-ttu-id="09074-145">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="09074-145">Failed</span></span>
- <span data-ttu-id="09074-146">Foi</span><span class="sxs-lookup"><span data-stu-id="09074-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-147">-Estado</span><span class="sxs-lookup"><span data-stu-id="09074-147">-State</span></span>
<span data-ttu-id="09074-148">Especifica um filtro de estado para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="09074-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="09074-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="09074-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09074-150">Aceitá</span><span class="sxs-lookup"><span data-stu-id="09074-150">Accepted</span></span>
- <span data-ttu-id="09074-151">Novo</span><span class="sxs-lookup"><span data-stu-id="09074-151">New</span></span>
- <span data-ttu-id="09074-152">Preciso</span><span class="sxs-lookup"><span data-stu-id="09074-152">Compiling</span></span>
- <span data-ttu-id="09074-153">Plano</span><span class="sxs-lookup"><span data-stu-id="09074-153">Scheduling</span></span>
- <span data-ttu-id="09074-154">Na fila</span><span class="sxs-lookup"><span data-stu-id="09074-154">Queued</span></span>
- <span data-ttu-id="09074-155">Iniciais</span><span class="sxs-lookup"><span data-stu-id="09074-155">Starting</span></span>
- <span data-ttu-id="09074-156">Pausado</span><span class="sxs-lookup"><span data-stu-id="09074-156">Paused</span></span>
- <span data-ttu-id="09074-157">Executando</span><span class="sxs-lookup"><span data-stu-id="09074-157">Running</span></span>
- <span data-ttu-id="09074-158">Abandona</span><span class="sxs-lookup"><span data-stu-id="09074-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="09074-159">-SubmittedAfter</span></span>
<span data-ttu-id="09074-160">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="09074-160">Specifies a date filter.</span></span>
<span data-ttu-id="09074-161">Use este parâmetro para filtrar o resultado da lista de trabalhos para trabalhos enviados após a data especificada.</span><span class="sxs-lookup"><span data-stu-id="09074-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="09074-162">-SubmittedBefore</span></span>
<span data-ttu-id="09074-163">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="09074-163">Specifies a date filter.</span></span>
<span data-ttu-id="09074-164">Use este parâmetro para filtrar o resultado da lista de trabalhos para trabalhos enviados antes da data especificada.</span><span class="sxs-lookup"><span data-stu-id="09074-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-165">-Emissor</span><span class="sxs-lookup"><span data-stu-id="09074-165">-Submitter</span></span>
<span data-ttu-id="09074-166">Especifica o endereço de email de um usuário.</span><span class="sxs-lookup"><span data-stu-id="09074-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="09074-167">Use este parâmetro para filtrar os resultados da lista de trabalhos para trabalhos enviados por um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="09074-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-168">-Início</span><span class="sxs-lookup"><span data-stu-id="09074-168">-Top</span></span>
<span data-ttu-id="09074-169">Um valor opcional que indica o número de trabalhos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="09074-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="09074-170">O valor padrão é 500</span><span class="sxs-lookup"><span data-stu-id="09074-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09074-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09074-171">CommonParameters</span></span>
<span data-ttu-id="09074-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09074-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09074-173">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09074-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09074-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09074-174">INPUTS</span></span>

### <span data-ttu-id="09074-175">System. String</span><span class="sxs-lookup"><span data-stu-id="09074-175">System.String</span></span>

### <span data-ttu-id="09074-176">System. GUID</span><span class="sxs-lookup"><span data-stu-id="09074-176">System.Guid</span></span>

### <span data-ttu-id="09074-177">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="09074-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="09074-178">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09074-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="09074-179">Microsoft. Azure. Management. datalake. Analytics. Models. JobState []</span><span class="sxs-lookup"><span data-stu-id="09074-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="09074-180">Microsoft. Azure. Management. datalake. Analytics. Models. JobResult []</span><span class="sxs-lookup"><span data-stu-id="09074-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="09074-181">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09074-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="09074-182">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09074-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="09074-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09074-183">OUTPUTS</span></span>

### <span data-ttu-id="09074-184">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="09074-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="09074-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09074-185">NOTES</span></span>

## <span data-ttu-id="09074-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09074-186">RELATED LINKS</span></span>

[<span data-ttu-id="09074-187">Parar-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="09074-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="09074-188">Enviar-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="09074-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="09074-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="09074-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


