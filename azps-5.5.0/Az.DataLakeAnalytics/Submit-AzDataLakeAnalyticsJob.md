---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115399"
---
# <span data-ttu-id="8da4a-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8da4a-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="8da4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8da4a-102">SYNOPSIS</span></span>
<span data-ttu-id="8da4a-103">Envia um trabalho.</span><span class="sxs-lookup"><span data-stu-id="8da4a-103">Submits a job.</span></span>

## <span data-ttu-id="8da4a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8da4a-104">SYNTAX</span></span>

### <span data-ttu-id="8da4a-105">SubmitUSqlScriptWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="8da4a-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8da4a-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="8da4a-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8da4a-107">SubmitUSqlScriptWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="8da4a-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8da4a-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="8da4a-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8da4a-109">SubmitUSqlScriptWithScriptPathAndScriptline</span><span class="sxs-lookup"><span data-stu-id="8da4a-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8da4a-110">SubmitUSqlJobWith SubmitLine</span><span class="sxs-lookup"><span data-stu-id="8da4a-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8da4a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8da4a-111">DESCRIPTION</span></span>
<span data-ttu-id="8da4a-112">O cmdlet **Submit-AzDataLakeAnalytics Job** envia um trabalho do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8da4a-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="8da4a-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8da4a-113">EXAMPLES</span></span>

### <span data-ttu-id="8da4a-114">Exemplo 1: Enviar um trabalho</span><span class="sxs-lookup"><span data-stu-id="8da4a-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="8da4a-115">Este comando envia um trabalho do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8da4a-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="8da4a-116">Exemplo 2: Enviar um trabalho com parâmetros de script</span><span class="sxs-lookup"><span data-stu-id="8da4a-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="8da4a-117">Os parâmetros de script U-SQL são previamente anexados acima do conteúdo do script principal, por exemplo: cadeia de caracteres DECLARE @Department = "Vendas"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = novo DateTime(2017, 12, 6, 0, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="8da4a-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="8da4a-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8da4a-118">PARAMETERS</span></span>

### <span data-ttu-id="8da4a-119">-Conta</span><span class="sxs-lookup"><span data-stu-id="8da4a-119">-Account</span></span>
<span data-ttu-id="8da4a-120">Nome da conta do Data Lake Analytics na qual o trabalho será enviado.</span><span class="sxs-lookup"><span data-stu-id="8da4a-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="8da4a-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="8da4a-121">-AnalyticsUnits</span></span>
<span data-ttu-id="8da4a-122">As unidades de análise a ser usadas para este trabalho.</span><span class="sxs-lookup"><span data-stu-id="8da4a-122">The analytics units to use for this job.</span></span> <span data-ttu-id="8da4a-123">Normalmente, mais unidades de análise dedicadas a um script resulta em tempo de execução de script mais rápido.</span><span class="sxs-lookup"><span data-stu-id="8da4a-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="8da4a-124">-CompileMode</span></span>
<span data-ttu-id="8da4a-125">O tipo de compilação a ser feita neste trabalho.</span><span class="sxs-lookup"><span data-stu-id="8da4a-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="8da4a-126">Valores válidos:</span><span class="sxs-lookup"><span data-stu-id="8da4a-126">Valid values:</span></span> 
- <span data-ttu-id="8da4a-127">Semântico (executa apenas verificações semânticas e verificações de osidade necessárias)</span><span class="sxs-lookup"><span data-stu-id="8da4a-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="8da4a-128">Completo (compilação completa)</span><span class="sxs-lookup"><span data-stu-id="8da4a-128">Full (Full compilation)</span></span>
- <span data-ttu-id="8da4a-129">SingleBox (compilação completa executada localmente)</span><span class="sxs-lookup"><span data-stu-id="8da4a-129">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="8da4a-130">-CompileOnly</span></span>
<span data-ttu-id="8da4a-131">Indica que o envio só deve criar o trabalho e não executá-lo se estiver definido como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="8da4a-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da4a-132">-DefaultProfile</span></span>
<span data-ttu-id="8da4a-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8da4a-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8da4a-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="8da4a-134">-Name</span></span>
<span data-ttu-id="8da4a-135">O nome amigável do trabalho a ser enviar.</span><span class="sxs-lookup"><span data-stu-id="8da4a-135">The friendly name of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="8da4a-136">-PipelineId</span></span>
<span data-ttu-id="8da4a-137">Uma ID que indica o envio deste trabalho faz parte de um conjunto de trabalhos recorrentes e também está associada a um pipeline de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8da4a-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="8da4a-138">-PipelineName</span></span>
<span data-ttu-id="8da4a-139">Um nome opcional amigável para o pipeline associado a este trabalho.</span><span class="sxs-lookup"><span data-stu-id="8da4a-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="8da4a-140">-PipelineUri</span></span>
<span data-ttu-id="8da4a-141">Um uri opcional que vincula ao serviço de origem associado a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="8da4a-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-142">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="8da4a-142">-Priority</span></span>
<span data-ttu-id="8da4a-143">A prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8da4a-143">The priority of the job.</span></span> <span data-ttu-id="8da4a-144">Se não especificado, a prioridade será 1000.</span><span class="sxs-lookup"><span data-stu-id="8da4a-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="8da4a-145">Um número mais baixo indica uma prioridade de trabalho mais alta.</span><span class="sxs-lookup"><span data-stu-id="8da4a-145">A lower number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-146">-RecorrênciaId</span><span class="sxs-lookup"><span data-stu-id="8da4a-146">-RecurrenceId</span></span>
<span data-ttu-id="8da4a-147">Uma ID que indica o envio deste trabalho faz parte de um conjunto de trabalhos recorrentes com a mesma ID de recorrência.</span><span class="sxs-lookup"><span data-stu-id="8da4a-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-148">-Nome da Recorrência</span><span class="sxs-lookup"><span data-stu-id="8da4a-148">-RecurrenceName</span></span>
<span data-ttu-id="8da4a-149">Um nome opcional amigável para a correlação de recorrência entre trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8da4a-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="8da4a-150">-RunId</span></span>
<span data-ttu-id="8da4a-151">Uma ID que identifica essa iteração de executar específica do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8da4a-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-152">-Tempo de execução</span><span class="sxs-lookup"><span data-stu-id="8da4a-152">-Runtime</span></span>
<span data-ttu-id="8da4a-153">Opcionalmente, de definir a versão do tempo de execução a ser usada para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="8da4a-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="8da4a-154">Se o tempo de execução for esquerdo, o tempo de execução padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="8da4a-154">If left unset, the default runtime is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-155">-Script</span><span class="sxs-lookup"><span data-stu-id="8da4a-155">-Script</span></span>
<span data-ttu-id="8da4a-156">Script a ser executado (escrito em linha).</span><span class="sxs-lookup"><span data-stu-id="8da4a-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="8da4a-157">-ScriptParameter</span></span>
<span data-ttu-id="8da4a-158">Os parâmetros de script para este trabalho, como um dicionário de nomes de parâmetros (cadeia de caracteres) para valores (qualquer combinação de byte, sbyte, int, uint (ou uint32), long, ulong (ou uint64), float, double, decimal, short (ou int16), ushort (ou uint16), char, string, DateTime, bool, Guid ou byte[]).</span><span class="sxs-lookup"><span data-stu-id="8da4a-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="8da4a-159">-ScriptPath</span></span>
<span data-ttu-id="8da4a-160">Caminho para o arquivo de script a ser enviar.</span><span class="sxs-lookup"><span data-stu-id="8da4a-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da4a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da4a-161">CommonParameters</span></span>
<span data-ttu-id="8da4a-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da4a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da4a-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da4a-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da4a-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="8da4a-164">INPUTS</span></span>

### <span data-ttu-id="8da4a-165">System.String</span><span class="sxs-lookup"><span data-stu-id="8da4a-165">System.String</span></span>

### <span data-ttu-id="8da4a-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8da4a-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8da4a-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8da4a-167">System.Int32</span></span>

### <span data-ttu-id="8da4a-168">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="8da4a-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="8da4a-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8da4a-169">System.Guid</span></span>

### <span data-ttu-id="8da4a-170">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8da4a-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8da4a-171">Saídas</span><span class="sxs-lookup"><span data-stu-id="8da4a-171">OUTPUTS</span></span>

### <span data-ttu-id="8da4a-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="8da4a-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="8da4a-173">Notas</span><span class="sxs-lookup"><span data-stu-id="8da4a-173">NOTES</span></span>

## <span data-ttu-id="8da4a-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8da4a-174">RELATED LINKS</span></span>

[<span data-ttu-id="8da4a-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8da4a-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8da4a-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8da4a-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8da4a-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8da4a-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


