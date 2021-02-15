---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111954"
---
# <span data-ttu-id="6a6d2-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6a6d2-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="6a6d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6d2-103">Obtém um trabalho do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="6a6d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a6d2-104">SYNTAX</span></span>

### <span data-ttu-id="6a6d2-105">GetAllInResourceGroupAndAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6a6d2-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a6d2-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="6a6d2-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a6d2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a6d2-107">DESCRIPTION</span></span>
<span data-ttu-id="6a6d2-108">O cmdlet **Get-AzDataLakeAnalytics Job** obtém um trabalho do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="6a6d2-109">Se você não especificar um trabalho, este cmdlet obtém todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="6a6d2-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a6d2-110">EXAMPLES</span></span>

### <span data-ttu-id="6a6d2-111">Exemplo 1: Obter um trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="6a6d2-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="6a6d2-112">Esse comando obtém o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="6a6d2-113">Exemplo 2: Obter trabalhos enviados na semana passada</span><span class="sxs-lookup"><span data-stu-id="6a6d2-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="6a6d2-114">Esse comando recebe trabalhos enviados na semana passada.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="6a6d2-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a6d2-115">PARAMETERS</span></span>

### <span data-ttu-id="6a6d2-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="6a6d2-116">-Account</span></span>
<span data-ttu-id="6a6d2-117">Especifica o nome de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6a6d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6d2-118">-DefaultProfile</span></span>
<span data-ttu-id="6a6d2-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6a6d2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a6d2-120">-Incluir</span><span class="sxs-lookup"><span data-stu-id="6a6d2-120">-Include</span></span>
<span data-ttu-id="6a6d2-121">Especifica as opções que indicam o tipo de informação adicional a ser recuperada sobre o trabalho.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="6a6d2-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a6d2-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6a6d2-123">None</span></span>
- <span data-ttu-id="6a6d2-124">Debuginfo</span><span class="sxs-lookup"><span data-stu-id="6a6d2-124">DebugInfo</span></span>
- <span data-ttu-id="6a6d2-125">Estatísticas</span><span class="sxs-lookup"><span data-stu-id="6a6d2-125">Statistics</span></span>
- <span data-ttu-id="6a6d2-126">Todos</span><span class="sxs-lookup"><span data-stu-id="6a6d2-126">All</span></span>

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

### <span data-ttu-id="6a6d2-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="6a6d2-127">-JobId</span></span>
<span data-ttu-id="6a6d2-128">Especifica a ID do trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="6a6d2-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a6d2-129">-Name</span></span>
<span data-ttu-id="6a6d2-130">Especifica um nome a ser usado para filtrar os resultados da lista de empregos.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="6a6d2-131">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a6d2-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6a6d2-132">None</span></span>
- <span data-ttu-id="6a6d2-133">Debuginfo</span><span class="sxs-lookup"><span data-stu-id="6a6d2-133">DebugInfo</span></span>
- <span data-ttu-id="6a6d2-134">Estatísticas</span><span class="sxs-lookup"><span data-stu-id="6a6d2-134">Statistics</span></span>
- <span data-ttu-id="6a6d2-135">Todos</span><span class="sxs-lookup"><span data-stu-id="6a6d2-135">All</span></span>

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

### <span data-ttu-id="6a6d2-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="6a6d2-136">-PipelineId</span></span>
<span data-ttu-id="6a6d2-137">Uma ID opcional que indica que apenas parte dos trabalhos do pipeline especificado deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="6a6d2-138">-RecorrênciaId</span><span class="sxs-lookup"><span data-stu-id="6a6d2-138">-RecurrenceId</span></span>
<span data-ttu-id="6a6d2-139">Uma ID opcional que indica apenas trabalhos de parte da recorrência especificada deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="6a6d2-140">-Resultado</span><span class="sxs-lookup"><span data-stu-id="6a6d2-140">-Result</span></span>
<span data-ttu-id="6a6d2-141">Especifica um filtro de resultados para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="6a6d2-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a6d2-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6a6d2-143">None</span></span>
- <span data-ttu-id="6a6d2-144">Cancelado</span><span class="sxs-lookup"><span data-stu-id="6a6d2-144">Cancelled</span></span>
- <span data-ttu-id="6a6d2-145">Falhou</span><span class="sxs-lookup"><span data-stu-id="6a6d2-145">Failed</span></span>
- <span data-ttu-id="6a6d2-146">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="6a6d2-146">Succeeded</span></span>

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

### <span data-ttu-id="6a6d2-147">-Estado</span><span class="sxs-lookup"><span data-stu-id="6a6d2-147">-State</span></span>
<span data-ttu-id="6a6d2-148">Especifica um filtro de estado para os resultados do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="6a6d2-149">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a6d2-150">Aceito</span><span class="sxs-lookup"><span data-stu-id="6a6d2-150">Accepted</span></span>
- <span data-ttu-id="6a6d2-151">Novo</span><span class="sxs-lookup"><span data-stu-id="6a6d2-151">New</span></span>
- <span data-ttu-id="6a6d2-152">Compilação</span><span class="sxs-lookup"><span data-stu-id="6a6d2-152">Compiling</span></span>
- <span data-ttu-id="6a6d2-153">Agendamento</span><span class="sxs-lookup"><span data-stu-id="6a6d2-153">Scheduling</span></span>
- <span data-ttu-id="6a6d2-154">Enfileirado</span><span class="sxs-lookup"><span data-stu-id="6a6d2-154">Queued</span></span>
- <span data-ttu-id="6a6d2-155">Começando</span><span class="sxs-lookup"><span data-stu-id="6a6d2-155">Starting</span></span>
- <span data-ttu-id="6a6d2-156">Pausado</span><span class="sxs-lookup"><span data-stu-id="6a6d2-156">Paused</span></span>
- <span data-ttu-id="6a6d2-157">Executando</span><span class="sxs-lookup"><span data-stu-id="6a6d2-157">Running</span></span>
- <span data-ttu-id="6a6d2-158">Terminou</span><span class="sxs-lookup"><span data-stu-id="6a6d2-158">Ended</span></span>

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

### <span data-ttu-id="6a6d2-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="6a6d2-159">-SubmittedAfter</span></span>
<span data-ttu-id="6a6d2-160">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-160">Specifies a date filter.</span></span>
<span data-ttu-id="6a6d2-161">Use este parâmetro para filtrar o resultado da lista de empregos para trabalhos enviados após a data especificada.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="6a6d2-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="6a6d2-162">-SubmittedBefore</span></span>
<span data-ttu-id="6a6d2-163">Especifica um filtro de data.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-163">Specifies a date filter.</span></span>
<span data-ttu-id="6a6d2-164">Use este parâmetro para filtrar o resultado da lista de empregos para trabalhos enviados antes da data especificada.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="6a6d2-165">-Enviador</span><span class="sxs-lookup"><span data-stu-id="6a6d2-165">-Submitter</span></span>
<span data-ttu-id="6a6d2-166">Especifica o endereço de email de um usuário.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="6a6d2-167">Use este parâmetro para filtrar os resultados da lista de empregos para trabalhos enviados por um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="6a6d2-168">-Superior</span><span class="sxs-lookup"><span data-stu-id="6a6d2-168">-Top</span></span>
<span data-ttu-id="6a6d2-169">Um valor opcional que indica o número de trabalhos a retornar.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="6a6d2-170">O valor padrão é 500</span><span class="sxs-lookup"><span data-stu-id="6a6d2-170">Default value is 500</span></span>

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

### <span data-ttu-id="6a6d2-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6d2-171">CommonParameters</span></span>
<span data-ttu-id="6a6d2-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6d2-173">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a6d2-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6d2-174">Entradas</span><span class="sxs-lookup"><span data-stu-id="6a6d2-174">INPUTS</span></span>

### <span data-ttu-id="6a6d2-175">System.String</span><span class="sxs-lookup"><span data-stu-id="6a6d2-175">System.String</span></span>

### <span data-ttu-id="6a6d2-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6a6d2-176">System.Guid</span></span>

### <span data-ttu-id="6a6d2-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedData</span><span class="sxs-lookup"><span data-stu-id="6a6d2-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="6a6d2-178">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a6d2-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6a6d2-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="6a6d2-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="6a6d2-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="6a6d2-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="6a6d2-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a6d2-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6a6d2-182">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a6d2-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6a6d2-183">Saídas</span><span class="sxs-lookup"><span data-stu-id="6a6d2-183">OUTPUTS</span></span>

### <span data-ttu-id="6a6d2-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="6a6d2-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="6a6d2-185">Notas</span><span class="sxs-lookup"><span data-stu-id="6a6d2-185">NOTES</span></span>

## <span data-ttu-id="6a6d2-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a6d2-186">RELATED LINKS</span></span>

[<span data-ttu-id="6a6d2-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6a6d2-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="6a6d2-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6a6d2-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="6a6d2-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6a6d2-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


