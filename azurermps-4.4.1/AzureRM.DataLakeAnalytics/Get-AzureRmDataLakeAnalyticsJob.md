---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441120"
---
# <span data-ttu-id="6d337-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6d337-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="6d337-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d337-102">SYNOPSIS</span></span>
<span data-ttu-id="6d337-103">Obtém um trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d337-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d337-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d337-104">SYNTAX</span></span>

### <span data-ttu-id="6d337-105">Tudo na conta e grupo de recursos (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d337-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d337-106">JobInformation específico</span><span class="sxs-lookup"><span data-stu-id="6d337-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d337-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d337-107">DESCRIPTION</span></span>
<span data-ttu-id="6d337-108">O cmdlet **Get-AzureRmDataLakeAnalyticsJob** Obtém um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d337-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="6d337-109">Se você não especificar um trabalho, esse cmdlet receberá todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="6d337-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="6d337-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d337-110">EXAMPLES</span></span>

### <span data-ttu-id="6d337-111">Exemplo 1: obter um trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="6d337-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="6d337-112">Este comando obtém o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="6d337-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="6d337-113">Exemplo 2: obter trabalhos enviados na semana passada</span><span class="sxs-lookup"><span data-stu-id="6d337-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="6d337-114">Este comando obtém os trabalhos enviados na última semana.</span><span class="sxs-lookup"><span data-stu-id="6d337-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="6d337-115">OS</span><span class="sxs-lookup"><span data-stu-id="6d337-115">PARAMETERS</span></span>

### <span data-ttu-id="6d337-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="6d337-116">-Account</span></span>
<span data-ttu-id="6d337-117">Especifica o nome de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d337-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6d337-118">-Include</span><span class="sxs-lookup"><span data-stu-id="6d337-118">-Include</span></span>
<span data-ttu-id="6d337-119">Especifica as opções que indicam o tipo de informação adicional a ser recuperada sobre o trabalho.</span><span class="sxs-lookup"><span data-stu-id="6d337-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="6d337-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6d337-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d337-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6d337-121">None</span></span>
- <span data-ttu-id="6d337-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="6d337-122">DebugInfo</span></span>
- <span data-ttu-id="6d337-123">As</span><span class="sxs-lookup"><span data-stu-id="6d337-123">Statistics</span></span>
- <span data-ttu-id="6d337-124">Todo</span><span class="sxs-lookup"><span data-stu-id="6d337-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="6d337-125">-JobId</span></span>
<span data-ttu-id="6d337-126">Especifica a ID do trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="6d337-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d337-127">-Name</span></span>
<span data-ttu-id="6d337-128">Especifica um nome a ser usado para filtrar os resultados da lista de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="6d337-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="6d337-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6d337-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d337-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6d337-130">None</span></span>
- <span data-ttu-id="6d337-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="6d337-131">DebugInfo</span></span>
- <span data-ttu-id="6d337-132">As</span><span class="sxs-lookup"><span data-stu-id="6d337-132">Statistics</span></span>
- <span data-ttu-id="6d337-133">Todo</span><span class="sxs-lookup"><span data-stu-id="6d337-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-134">-Pipelineid</span><span class="sxs-lookup"><span data-stu-id="6d337-134">-PipelineId</span></span>
<span data-ttu-id="6d337-135">Uma ID opcional que indica apenas as tarefas que parte do pipeline especificado deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="6d337-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-136">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="6d337-136">-RecurrenceId</span></span>
<span data-ttu-id="6d337-137">Uma ID opcional que indica apenas as tarefas que parte da recorrência especificada deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="6d337-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-138">-Resultado</span><span class="sxs-lookup"><span data-stu-id="6d337-138">-Result</span></span>
<span data-ttu-id="6d337-139">Especifica um filtro de resultado para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6d337-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="6d337-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6d337-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d337-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6d337-141">None</span></span>
- <span data-ttu-id="6d337-142">Cela</span><span class="sxs-lookup"><span data-stu-id="6d337-142">Cancelled</span></span>
- <span data-ttu-id="6d337-143">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="6d337-143">Failed</span></span>
- <span data-ttu-id="6d337-144">Foi</span><span class="sxs-lookup"><span data-stu-id="6d337-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-145">-Estado</span><span class="sxs-lookup"><span data-stu-id="6d337-145">-State</span></span>
<span data-ttu-id="6d337-146">Especifica um filtro de estado para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6d337-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="6d337-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6d337-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d337-148">Aceitá</span><span class="sxs-lookup"><span data-stu-id="6d337-148">Accepted</span></span>
- <span data-ttu-id="6d337-149">Novo</span><span class="sxs-lookup"><span data-stu-id="6d337-149">New</span></span>
- <span data-ttu-id="6d337-150">Preciso</span><span class="sxs-lookup"><span data-stu-id="6d337-150">Compiling</span></span>
- <span data-ttu-id="6d337-151">Plano</span><span class="sxs-lookup"><span data-stu-id="6d337-151">Scheduling</span></span>
- <span data-ttu-id="6d337-152">Na fila</span><span class="sxs-lookup"><span data-stu-id="6d337-152">Queued</span></span>
- <span data-ttu-id="6d337-153">Iniciais</span><span class="sxs-lookup"><span data-stu-id="6d337-153">Starting</span></span>
- <span data-ttu-id="6d337-154">Pausado</span><span class="sxs-lookup"><span data-stu-id="6d337-154">Paused</span></span>
- <span data-ttu-id="6d337-155">Executando</span><span class="sxs-lookup"><span data-stu-id="6d337-155">Running</span></span>
- <span data-ttu-id="6d337-156">Abandona</span><span class="sxs-lookup"><span data-stu-id="6d337-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="6d337-157">-SubmittedAfter</span></span>
<span data-ttu-id="6d337-158">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="6d337-158">Specifies a date filter.</span></span>
<span data-ttu-id="6d337-159">Use este parâmetro para filtrar o resultado da lista de trabalhos para trabalhos enviados após a data especificada.</span><span class="sxs-lookup"><span data-stu-id="6d337-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-160">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="6d337-160">-SubmittedBefore</span></span>
<span data-ttu-id="6d337-161">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="6d337-161">Specifies a date filter.</span></span>
<span data-ttu-id="6d337-162">Use este parâmetro para filtrar o resultado da lista de trabalhos para trabalhos enviados antes da data especificada.</span><span class="sxs-lookup"><span data-stu-id="6d337-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-163">-Emissor</span><span class="sxs-lookup"><span data-stu-id="6d337-163">-Submitter</span></span>
<span data-ttu-id="6d337-164">Especifica o endereço de email de um usuário.</span><span class="sxs-lookup"><span data-stu-id="6d337-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="6d337-165">Use este parâmetro para filtrar os resultados da lista de trabalhos para trabalhos enviados por um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="6d337-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-166">-Início</span><span class="sxs-lookup"><span data-stu-id="6d337-166">-Top</span></span>
<span data-ttu-id="6d337-167">Um valor opcional que indica o número de trabalhos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="6d337-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="6d337-168">O valor padrão é 500</span><span class="sxs-lookup"><span data-stu-id="6d337-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d337-169">-DefaultProfile</span></span>
<span data-ttu-id="6d337-170">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d337-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d337-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d337-171">CommonParameters</span></span>
<span data-ttu-id="6d337-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d337-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d337-173">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d337-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d337-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d337-174">INPUTS</span></span>

### <span data-ttu-id="6d337-175">#C0</span><span class="sxs-lookup"><span data-stu-id="6d337-175">Guid</span></span>
<span data-ttu-id="6d337-176">O parâmetro ' JobId ' aceita o valor do tipo ' GUID ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6d337-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="6d337-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d337-177">OUTPUTS</span></span>

### <span data-ttu-id="6d337-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="6d337-178">JobInformation</span></span>
<span data-ttu-id="6d337-179">Os detalhes da informação do trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="6d337-179">The specified job information details</span></span>

### <span data-ttu-id="6d337-180">Programação<JobInformation></span><span class="sxs-lookup"><span data-stu-id="6d337-180">List<JobInformation></span></span>
<span data-ttu-id="6d337-181">A lista de trabalhos na conta especificada do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d337-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="6d337-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d337-182">NOTES</span></span>

## <span data-ttu-id="6d337-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d337-183">RELATED LINKS</span></span>

[<span data-ttu-id="6d337-184">Parar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6d337-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="6d337-185">Enviar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6d337-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="6d337-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6d337-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


