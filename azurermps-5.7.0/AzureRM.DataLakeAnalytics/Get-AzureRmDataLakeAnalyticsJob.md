---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426710"
---
# <span data-ttu-id="d5c1d-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d5c1d-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d5c1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c1d-103">Obtém um trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5c1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5c1d-104">SYNTAX</span></span>

### <span data-ttu-id="d5c1d-105">GetAllInResourceGroupAndAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5c1d-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c1d-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="d5c1d-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5c1d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5c1d-107">DESCRIPTION</span></span>
<span data-ttu-id="d5c1d-108">O cmdlet **Get-AzureRmDataLakeAnalyticsJob** Obtém um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="d5c1d-109">Se você não especificar um trabalho, esse cmdlet receberá todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="d5c1d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5c1d-110">EXAMPLES</span></span>

### <span data-ttu-id="d5c1d-111">Exemplo 1: obter um trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="d5c1d-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="d5c1d-112">Este comando obtém o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="d5c1d-113">Exemplo 2: obter trabalhos enviados na semana passada</span><span class="sxs-lookup"><span data-stu-id="d5c1d-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="d5c1d-114">Este comando obtém os trabalhos enviados na última semana.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="d5c1d-115">OS</span><span class="sxs-lookup"><span data-stu-id="d5c1d-115">PARAMETERS</span></span>

### <span data-ttu-id="d5c1d-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="d5c1d-116">-Account</span></span>
<span data-ttu-id="d5c1d-117">Especifica o nome de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c1d-118">-DefaultProfile</span></span>
<span data-ttu-id="d5c1d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d5c1d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-120">-Include</span><span class="sxs-lookup"><span data-stu-id="d5c1d-120">-Include</span></span>
<span data-ttu-id="d5c1d-121">Especifica as opções que indicam o tipo de informação adicional a ser recuperada sobre o trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="d5c1d-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d5c1d-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5c1d-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d5c1d-123">None</span></span>
- <span data-ttu-id="d5c1d-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="d5c1d-124">DebugInfo</span></span>
- <span data-ttu-id="d5c1d-125">As</span><span class="sxs-lookup"><span data-stu-id="d5c1d-125">Statistics</span></span>
- <span data-ttu-id="d5c1d-126">Todo</span><span class="sxs-lookup"><span data-stu-id="d5c1d-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="d5c1d-127">-JobId</span></span>
<span data-ttu-id="d5c1d-128">Especifica a ID do trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5c1d-129">-Name</span></span>
<span data-ttu-id="d5c1d-130">Especifica um nome a ser usado para filtrar os resultados da lista de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="d5c1d-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d5c1d-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5c1d-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d5c1d-132">None</span></span>
- <span data-ttu-id="d5c1d-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="d5c1d-133">DebugInfo</span></span>
- <span data-ttu-id="d5c1d-134">As</span><span class="sxs-lookup"><span data-stu-id="d5c1d-134">Statistics</span></span>
- <span data-ttu-id="d5c1d-135">Todo</span><span class="sxs-lookup"><span data-stu-id="d5c1d-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-136">-Pipelineid</span><span class="sxs-lookup"><span data-stu-id="d5c1d-136">-PipelineId</span></span>
<span data-ttu-id="d5c1d-137">Uma ID opcional que indica apenas as tarefas que parte do pipeline especificado deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-138">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="d5c1d-138">-RecurrenceId</span></span>
<span data-ttu-id="d5c1d-139">Uma ID opcional que indica apenas as tarefas que parte da recorrência especificada deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-140">-Resultado</span><span class="sxs-lookup"><span data-stu-id="d5c1d-140">-Result</span></span>
<span data-ttu-id="d5c1d-141">Especifica um filtro de resultado para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="d5c1d-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d5c1d-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5c1d-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d5c1d-143">None</span></span>
- <span data-ttu-id="d5c1d-144">Cela</span><span class="sxs-lookup"><span data-stu-id="d5c1d-144">Cancelled</span></span>
- <span data-ttu-id="d5c1d-145">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="d5c1d-145">Failed</span></span>
- <span data-ttu-id="d5c1d-146">Foi</span><span class="sxs-lookup"><span data-stu-id="d5c1d-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-147">-Estado</span><span class="sxs-lookup"><span data-stu-id="d5c1d-147">-State</span></span>
<span data-ttu-id="d5c1d-148">Especifica um filtro de estado para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="d5c1d-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d5c1d-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5c1d-150">Aceitá</span><span class="sxs-lookup"><span data-stu-id="d5c1d-150">Accepted</span></span>
- <span data-ttu-id="d5c1d-151">Novo</span><span class="sxs-lookup"><span data-stu-id="d5c1d-151">New</span></span>
- <span data-ttu-id="d5c1d-152">Preciso</span><span class="sxs-lookup"><span data-stu-id="d5c1d-152">Compiling</span></span>
- <span data-ttu-id="d5c1d-153">Plano</span><span class="sxs-lookup"><span data-stu-id="d5c1d-153">Scheduling</span></span>
- <span data-ttu-id="d5c1d-154">Na fila</span><span class="sxs-lookup"><span data-stu-id="d5c1d-154">Queued</span></span>
- <span data-ttu-id="d5c1d-155">Iniciais</span><span class="sxs-lookup"><span data-stu-id="d5c1d-155">Starting</span></span>
- <span data-ttu-id="d5c1d-156">Pausado</span><span class="sxs-lookup"><span data-stu-id="d5c1d-156">Paused</span></span>
- <span data-ttu-id="d5c1d-157">Executando</span><span class="sxs-lookup"><span data-stu-id="d5c1d-157">Running</span></span>
- <span data-ttu-id="d5c1d-158">Abandona</span><span class="sxs-lookup"><span data-stu-id="d5c1d-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="d5c1d-159">-SubmittedAfter</span></span>
<span data-ttu-id="d5c1d-160">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-160">Specifies a date filter.</span></span>
<span data-ttu-id="d5c1d-161">Use este parâmetro para filtrar o resultado da lista de trabalhos para trabalhos enviados após a data especificada.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="d5c1d-162">-SubmittedBefore</span></span>
<span data-ttu-id="d5c1d-163">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-163">Specifies a date filter.</span></span>
<span data-ttu-id="d5c1d-164">Use este parâmetro para filtrar o resultado da lista de trabalhos para trabalhos enviados antes da data especificada.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-165">-Emissor</span><span class="sxs-lookup"><span data-stu-id="d5c1d-165">-Submitter</span></span>
<span data-ttu-id="d5c1d-166">Especifica o endereço de email de um usuário.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="d5c1d-167">Use este parâmetro para filtrar os resultados da lista de trabalhos para trabalhos enviados por um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-168">-Início</span><span class="sxs-lookup"><span data-stu-id="d5c1d-168">-Top</span></span>
<span data-ttu-id="d5c1d-169">Um valor opcional que indica o número de trabalhos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="d5c1d-170">O valor padrão é 500</span><span class="sxs-lookup"><span data-stu-id="d5c1d-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c1d-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c1d-171">CommonParameters</span></span>
<span data-ttu-id="d5c1d-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c1d-173">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c1d-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c1d-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5c1d-174">INPUTS</span></span>

### <span data-ttu-id="d5c1d-175">#C0</span><span class="sxs-lookup"><span data-stu-id="d5c1d-175">Guid</span></span>
<span data-ttu-id="d5c1d-176">O parâmetro ' JobId ' aceita o valor do tipo ' GUID ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d5c1d-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="d5c1d-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5c1d-177">OUTPUTS</span></span>

### <span data-ttu-id="d5c1d-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="d5c1d-178">JobInformation</span></span>
<span data-ttu-id="d5c1d-179">Os detalhes da informação do trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="d5c1d-179">The specified job information details</span></span>

### <span data-ttu-id="d5c1d-180">Programação<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="d5c1d-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="d5c1d-181">A lista de trabalhos na conta especificada do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="d5c1d-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5c1d-182">NOTES</span></span>

## <span data-ttu-id="d5c1d-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5c1d-183">RELATED LINKS</span></span>

[<span data-ttu-id="d5c1d-184">Parar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d5c1d-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="d5c1d-185">Enviar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d5c1d-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="d5c1d-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d5c1d-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


