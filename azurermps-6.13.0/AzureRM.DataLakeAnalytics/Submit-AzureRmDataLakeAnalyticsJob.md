---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: acd61ac9da39a56cf03499d0a2a4fcd25d321525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432003"
---
# <span data-ttu-id="a5245-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5245-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="a5245-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5245-102">SYNOPSIS</span></span>
<span data-ttu-id="a5245-103">Envia um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5245-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5245-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5245-104">SYNTAX</span></span>

### <span data-ttu-id="a5245-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="a5245-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5245-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="a5245-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5245-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="a5245-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5245-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="a5245-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5245-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="a5245-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5245-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="a5245-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5245-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5245-111">DESCRIPTION</span></span>
<span data-ttu-id="a5245-112">O cmdlet **Submit-AzureRmDataLakeAnalyticsJob** envia um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a5245-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="a5245-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5245-113">EXAMPLES</span></span>

### <span data-ttu-id="a5245-114">Exemplo 1: enviar um trabalho</span><span class="sxs-lookup"><span data-stu-id="a5245-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="a5245-115">Esse comando envia um trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a5245-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="a5245-116">Exemplo 2: enviar um trabalho com parâmetros de script</span><span class="sxs-lookup"><span data-stu-id="a5245-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="a5245-117">Os parâmetros de script U-SQL são anexados acima do conteúdo principal do script, por exemplo: DECLARE @Department String = "Sales"; DECLARAR @NumRecords int = 1000; DECLARAR @StartDateTime DateTime = novo DateTime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="a5245-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="a5245-118">OS</span><span class="sxs-lookup"><span data-stu-id="a5245-118">PARAMETERS</span></span>

### <span data-ttu-id="a5245-119">-Conta</span><span class="sxs-lookup"><span data-stu-id="a5245-119">-Account</span></span>
<span data-ttu-id="a5245-120">Nome da conta do data Lake Analytics na qual o trabalho será enviado.</span><span class="sxs-lookup"><span data-stu-id="a5245-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="a5245-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="a5245-121">-AnalyticsUnits</span></span>
<span data-ttu-id="a5245-122">As unidades de análise a serem usadas para esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5245-122">The analytics units to use for this job.</span></span> <span data-ttu-id="a5245-123">Geralmente, mais unidades de análise dedicadas a um script resultam em um tempo de execução de script mais rápido.</span><span class="sxs-lookup"><span data-stu-id="a5245-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="a5245-124">-Comcompilemode</span><span class="sxs-lookup"><span data-stu-id="a5245-124">-CompileMode</span></span>
<span data-ttu-id="a5245-125">O tipo de compilação a ser feita neste trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5245-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="a5245-126">Valores válidos:</span><span class="sxs-lookup"><span data-stu-id="a5245-126">Valid values:</span></span> 
- <span data-ttu-id="a5245-127">Semântica (executa verificações semânticas e verificações de integridade necessárias)</span><span class="sxs-lookup"><span data-stu-id="a5245-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="a5245-128">Completo (compilação completa)</span><span class="sxs-lookup"><span data-stu-id="a5245-128">Full (Full compilation)</span></span>
- <span data-ttu-id="a5245-129">SingleBox (compilação completa realizada localmente)</span><span class="sxs-lookup"><span data-stu-id="a5245-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="a5245-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="a5245-130">-CompileOnly</span></span>
<span data-ttu-id="a5245-131">Indica que o envio só deve compilar o trabalho e não executar se definido como true.</span><span class="sxs-lookup"><span data-stu-id="a5245-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="a5245-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5245-132">-DefaultProfile</span></span>
<span data-ttu-id="a5245-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a5245-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5245-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5245-134">-Name</span></span>
<span data-ttu-id="a5245-135">O nome amigável do trabalho a ser enviado.</span><span class="sxs-lookup"><span data-stu-id="a5245-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="a5245-136">-Pipelineid</span><span class="sxs-lookup"><span data-stu-id="a5245-136">-PipelineId</span></span>
<span data-ttu-id="a5245-137">Uma ID que indica que o envio desse trabalho é parte de um conjunto de trabalhos recorrentes e também associado a um pipeline de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5245-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="a5245-138">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="a5245-138">-PipelineName</span></span>
<span data-ttu-id="a5245-139">Um nome amigável opcional para o pipeline associado a esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5245-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="a5245-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="a5245-140">-PipelineUri</span></span>
<span data-ttu-id="a5245-141">Um URI opcional que se vincula ao serviço de origem associado a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5245-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="a5245-142">-Priority</span><span class="sxs-lookup"><span data-stu-id="a5245-142">-Priority</span></span>
<span data-ttu-id="a5245-143">A prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5245-143">The priority of the job.</span></span> <span data-ttu-id="a5245-144">Se não for especificado, a prioridade será 1000.</span><span class="sxs-lookup"><span data-stu-id="a5245-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="a5245-145">Um número menor indica uma prioridade de trabalho mais alta.</span><span class="sxs-lookup"><span data-stu-id="a5245-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="a5245-146">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="a5245-146">-RecurrenceId</span></span>
<span data-ttu-id="a5245-147">Uma ID que indica o envio desse trabalho é uma parte de um conjunto de trabalhos recorrentes com a mesma ID de recorrência.</span><span class="sxs-lookup"><span data-stu-id="a5245-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="a5245-148">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="a5245-148">-RecurrenceName</span></span>
<span data-ttu-id="a5245-149">Um nome amigável opcional para a correlação de recorrência entre trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a5245-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="a5245-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="a5245-150">-RunId</span></span>
<span data-ttu-id="a5245-151">Uma ID que identifica essa iteração de execução específica do pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5245-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="a5245-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="a5245-152">-Runtime</span></span>
<span data-ttu-id="a5245-153">Opcionalmente, defina a versão do tempo de execução para usar para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5245-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="a5245-154">Se esquerda não definida, o tempo de execução padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="a5245-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="a5245-155">-Script</span><span class="sxs-lookup"><span data-stu-id="a5245-155">-Script</span></span>
<span data-ttu-id="a5245-156">Script para executar (Inline embutido).</span><span class="sxs-lookup"><span data-stu-id="a5245-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="a5245-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="a5245-157">-ScriptParameter</span></span>
<span data-ttu-id="a5245-158">Os parâmetros de script para esse trabalho, como um dicionário de nomes de parâmetro (cadeia de caracteres) para valores (qualquer combinação de byte, SByte, int, uint (ou UInt32), Long, ULong (ou UInt64), float, Double, DateTime, bool, GUID ou byte []) (ou UInt16), Char, String, DateTime, bool, GUID ou byte [])</span><span class="sxs-lookup"><span data-stu-id="a5245-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="a5245-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="a5245-159">-ScriptPath</span></span>
<span data-ttu-id="a5245-160">Caminho para o arquivo de script a ser enviado.</span><span class="sxs-lookup"><span data-stu-id="a5245-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="a5245-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5245-161">CommonParameters</span></span>
<span data-ttu-id="a5245-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5245-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5245-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5245-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5245-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5245-164">INPUTS</span></span>

### <span data-ttu-id="a5245-165">System. String</span><span class="sxs-lookup"><span data-stu-id="a5245-165">System.String</span></span>

### <span data-ttu-id="a5245-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a5245-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a5245-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a5245-167">System.Int32</span></span>

### <span data-ttu-id="a5245-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="a5245-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="a5245-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a5245-169">System.Guid</span></span>

### <span data-ttu-id="a5245-170">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a5245-170">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a5245-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5245-171">OUTPUTS</span></span>

### <span data-ttu-id="a5245-172">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="a5245-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="a5245-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5245-173">NOTES</span></span>

## <span data-ttu-id="a5245-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5245-174">RELATED LINKS</span></span>

[<span data-ttu-id="a5245-175">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5245-175">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a5245-176">Parar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5245-176">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a5245-177">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5245-177">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


