---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 0078196d8b06ae791fa0855345eec02d1f2eb59c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888255"
---
# <span data-ttu-id="96d78-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96d78-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="96d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96d78-102">SYNOPSIS</span></span>
<span data-ttu-id="96d78-103">Obtém um trabalho do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="96d78-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="96d78-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="96d78-104">SYNTAX</span></span>

### <span data-ttu-id="96d78-105">GetAllInResourceGroupAndAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96d78-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96d78-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="96d78-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96d78-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="96d78-107">DESCRIPTION</span></span>
<span data-ttu-id="96d78-108">O cmdlet **Get-AzDataLakeAnalyticsJob** obtém um trabalho do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="96d78-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="96d78-109">Se você não especificar um trabalho, este cmdlet obtém todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="96d78-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="96d78-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96d78-110">EXAMPLES</span></span>

### <span data-ttu-id="96d78-111">Exemplo 1: Obter um trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="96d78-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="96d78-112">Este comando obtém o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="96d78-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="96d78-113">Exemplo 2: Obter trabalhos enviados na semana passada</span><span class="sxs-lookup"><span data-stu-id="96d78-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="96d78-114">Este comando obtém trabalhos enviados na semana passada.</span><span class="sxs-lookup"><span data-stu-id="96d78-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="96d78-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="96d78-115">PARAMETERS</span></span>

### <span data-ttu-id="96d78-116">-Account</span><span class="sxs-lookup"><span data-stu-id="96d78-116">-Account</span></span>
<span data-ttu-id="96d78-117">Especifica o nome de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="96d78-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="96d78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d78-118">-DefaultProfile</span></span>
<span data-ttu-id="96d78-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="96d78-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96d78-120">-Include</span><span class="sxs-lookup"><span data-stu-id="96d78-120">-Include</span></span>
<span data-ttu-id="96d78-121">Especifica opções que indicam o tipo de informação adicional a ser recuperada sobre o trabalho.</span><span class="sxs-lookup"><span data-stu-id="96d78-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="96d78-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="96d78-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96d78-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="96d78-123">None</span></span>
- <span data-ttu-id="96d78-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="96d78-124">DebugInfo</span></span>
- <span data-ttu-id="96d78-125">Estatísticas</span><span class="sxs-lookup"><span data-stu-id="96d78-125">Statistics</span></span>
- <span data-ttu-id="96d78-126">All</span><span class="sxs-lookup"><span data-stu-id="96d78-126">All</span></span>

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

### <span data-ttu-id="96d78-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="96d78-127">-JobId</span></span>
<span data-ttu-id="96d78-128">Especifica a ID do trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="96d78-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="96d78-129">-Name</span><span class="sxs-lookup"><span data-stu-id="96d78-129">-Name</span></span>
<span data-ttu-id="96d78-130">Especifica um nome a ser usado para filtrar os resultados da lista de trabalho.</span><span class="sxs-lookup"><span data-stu-id="96d78-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="96d78-131">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="96d78-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96d78-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="96d78-132">None</span></span>
- <span data-ttu-id="96d78-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="96d78-133">DebugInfo</span></span>
- <span data-ttu-id="96d78-134">Estatísticas</span><span class="sxs-lookup"><span data-stu-id="96d78-134">Statistics</span></span>
- <span data-ttu-id="96d78-135">All</span><span class="sxs-lookup"><span data-stu-id="96d78-135">All</span></span>

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

### <span data-ttu-id="96d78-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="96d78-136">-PipelineId</span></span>
<span data-ttu-id="96d78-137">Uma ID opcional que indica que apenas parte dos trabalhos do pipeline especificado deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="96d78-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="96d78-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="96d78-138">-RecurrenceId</span></span>
<span data-ttu-id="96d78-139">Uma ID opcional que indica que apenas parte dos trabalhos da recorrência especificada deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="96d78-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="96d78-140">-Result</span><span class="sxs-lookup"><span data-stu-id="96d78-140">-Result</span></span>
<span data-ttu-id="96d78-141">Especifica um filtro de resultados para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="96d78-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="96d78-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="96d78-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96d78-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="96d78-143">None</span></span>
- <span data-ttu-id="96d78-144">Cancelado</span><span class="sxs-lookup"><span data-stu-id="96d78-144">Cancelled</span></span>
- <span data-ttu-id="96d78-145">Falha</span><span class="sxs-lookup"><span data-stu-id="96d78-145">Failed</span></span>
- <span data-ttu-id="96d78-146">Bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="96d78-146">Succeeded</span></span>

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

### <span data-ttu-id="96d78-147">-State</span><span class="sxs-lookup"><span data-stu-id="96d78-147">-State</span></span>
<span data-ttu-id="96d78-148">Especifica um filtro de estado para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="96d78-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="96d78-149">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="96d78-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96d78-150">Aceito</span><span class="sxs-lookup"><span data-stu-id="96d78-150">Accepted</span></span>
- <span data-ttu-id="96d78-151">Novo</span><span class="sxs-lookup"><span data-stu-id="96d78-151">New</span></span>
- <span data-ttu-id="96d78-152">Compilando</span><span class="sxs-lookup"><span data-stu-id="96d78-152">Compiling</span></span>
- <span data-ttu-id="96d78-153">Agendamento</span><span class="sxs-lookup"><span data-stu-id="96d78-153">Scheduling</span></span>
- <span data-ttu-id="96d78-154">En fila</span><span class="sxs-lookup"><span data-stu-id="96d78-154">Queued</span></span>
- <span data-ttu-id="96d78-155">Iniciando</span><span class="sxs-lookup"><span data-stu-id="96d78-155">Starting</span></span>
- <span data-ttu-id="96d78-156">Pausado</span><span class="sxs-lookup"><span data-stu-id="96d78-156">Paused</span></span>
- <span data-ttu-id="96d78-157">Executando</span><span class="sxs-lookup"><span data-stu-id="96d78-157">Running</span></span>
- <span data-ttu-id="96d78-158">Encerrado</span><span class="sxs-lookup"><span data-stu-id="96d78-158">Ended</span></span>

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

### <span data-ttu-id="96d78-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="96d78-159">-SubmittedAfter</span></span>
<span data-ttu-id="96d78-160">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="96d78-160">Specifies a date filter.</span></span>
<span data-ttu-id="96d78-161">Use este parâmetro para filtrar o resultado da lista de trabalhos para trabalhos enviados após a data especificada.</span><span class="sxs-lookup"><span data-stu-id="96d78-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="96d78-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="96d78-162">-SubmittedBefore</span></span>
<span data-ttu-id="96d78-163">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="96d78-163">Specifies a date filter.</span></span>
<span data-ttu-id="96d78-164">Use este parâmetro para filtrar o resultado da lista de trabalhos para trabalhos enviados antes da data especificada.</span><span class="sxs-lookup"><span data-stu-id="96d78-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="96d78-165">-Submitter</span><span class="sxs-lookup"><span data-stu-id="96d78-165">-Submitter</span></span>
<span data-ttu-id="96d78-166">Especifica o endereço de email de um usuário.</span><span class="sxs-lookup"><span data-stu-id="96d78-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="96d78-167">Use este parâmetro para filtrar os resultados da lista de trabalhos para trabalhos enviados por um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="96d78-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="96d78-168">-Top</span><span class="sxs-lookup"><span data-stu-id="96d78-168">-Top</span></span>
<span data-ttu-id="96d78-169">Um valor opcional que indica o número de trabalhos a retornar.</span><span class="sxs-lookup"><span data-stu-id="96d78-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="96d78-170">O valor padrão é 500</span><span class="sxs-lookup"><span data-stu-id="96d78-170">Default value is 500</span></span>

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

### <span data-ttu-id="96d78-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d78-171">CommonParameters</span></span>
<span data-ttu-id="96d78-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d78-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d78-173">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d78-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d78-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96d78-174">INPUTS</span></span>

### <span data-ttu-id="96d78-175">System.String</span><span class="sxs-lookup"><span data-stu-id="96d78-175">System.String</span></span>

### <span data-ttu-id="96d78-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="96d78-176">System.Guid</span></span>

### <span data-ttu-id="96d78-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="96d78-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="96d78-178">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96d78-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96d78-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="96d78-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="96d78-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="96d78-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="96d78-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96d78-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96d78-182">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96d78-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="96d78-183">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="96d78-183">OUTPUTS</span></span>

### <span data-ttu-id="96d78-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="96d78-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="96d78-185">NOTES</span><span class="sxs-lookup"><span data-stu-id="96d78-185">NOTES</span></span>

## <span data-ttu-id="96d78-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96d78-186">RELATED LINKS</span></span>

[<span data-ttu-id="96d78-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96d78-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="96d78-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96d78-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="96d78-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96d78-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


