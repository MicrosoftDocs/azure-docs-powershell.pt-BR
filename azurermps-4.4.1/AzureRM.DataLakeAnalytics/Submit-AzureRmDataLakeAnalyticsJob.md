---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432236"
---
# <span data-ttu-id="4da67-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4da67-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="4da67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4da67-102">SYNOPSIS</span></span>
<span data-ttu-id="4da67-103">Envia um trabalho.</span><span class="sxs-lookup"><span data-stu-id="4da67-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4da67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4da67-104">SYNTAX</span></span>

### <span data-ttu-id="4da67-105">Enviar trabalho com caminho de script para U-SQL</span><span class="sxs-lookup"><span data-stu-id="4da67-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4da67-106">Enviar o trabalho U-SQL</span><span class="sxs-lookup"><span data-stu-id="4da67-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4da67-107">Enviar trabalho com caminho de script para o U-SQL com informações reucurrence</span><span class="sxs-lookup"><span data-stu-id="4da67-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4da67-108">Enviar o trabalho U-SQL com informações de recorrência</span><span class="sxs-lookup"><span data-stu-id="4da67-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4da67-109">Enviar trabalho com caminho de script para U-SQL com reucurrence e informações de pipeline</span><span class="sxs-lookup"><span data-stu-id="4da67-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4da67-110">Enviar o trabalho U-SQL com informações de recorrência e pipeline</span><span class="sxs-lookup"><span data-stu-id="4da67-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4da67-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4da67-111">DESCRIPTION</span></span>
<span data-ttu-id="4da67-112">O cmdlet **Submit-AzureRmDataLakeAnalyticsJob** envia um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4da67-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="4da67-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4da67-113">EXAMPLES</span></span>

### <span data-ttu-id="4da67-114">Exemplo 1: enviar um trabalho</span><span class="sxs-lookup"><span data-stu-id="4da67-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="4da67-115">Esse comando envia um trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4da67-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="4da67-116">OS</span><span class="sxs-lookup"><span data-stu-id="4da67-116">PARAMETERS</span></span>

### <span data-ttu-id="4da67-117">-Conta</span><span class="sxs-lookup"><span data-stu-id="4da67-117">-Account</span></span>
<span data-ttu-id="4da67-118">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4da67-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4da67-119">-Comcompilemode</span><span class="sxs-lookup"><span data-stu-id="4da67-119">-CompileMode</span></span>
<span data-ttu-id="4da67-120">Especifica o modo de compilação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4da67-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="4da67-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4da67-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4da67-122">Semântico</span><span class="sxs-lookup"><span data-stu-id="4da67-122">Semantic</span></span>
- <span data-ttu-id="4da67-123">Integral</span><span class="sxs-lookup"><span data-stu-id="4da67-123">Full</span></span>
- <span data-ttu-id="4da67-124">SingleBox</span><span class="sxs-lookup"><span data-stu-id="4da67-124">SingleBox</span></span>

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

### <span data-ttu-id="4da67-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="4da67-125">-CompileOnly</span></span>
<span data-ttu-id="4da67-126">Indica que esse cmdlet compila o trabalho sem executá-lo.</span><span class="sxs-lookup"><span data-stu-id="4da67-126">Indicates that this cmdlet compiles the job without running it.</span></span>

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

### <span data-ttu-id="4da67-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="4da67-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="4da67-128">Especifica as unidades de análise de data Lake (DLAU) do trabalho, que indica o paralelismo máximo permitido do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4da67-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="4da67-129">-Name</span></span>
<span data-ttu-id="4da67-130">Especifica o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4da67-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="4da67-131">-Pipelineid</span><span class="sxs-lookup"><span data-stu-id="4da67-131">-PipelineId</span></span>
<span data-ttu-id="4da67-132">Uma ID que indica que o envio desse trabalho é parte de um conjunto de trabalhos recorrentes e também associado a um pipeline de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4da67-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-133">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="4da67-133">-PipelineName</span></span>
<span data-ttu-id="4da67-134">Um nome amigável opcional para o pipeline associado a esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="4da67-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="4da67-135">-PipelineUri</span></span>
<span data-ttu-id="4da67-136">Um URI opcional que se vincula ao serviço de origem associado a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="4da67-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="4da67-137">-Priority</span></span>
<span data-ttu-id="4da67-138">Especifica a prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4da67-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="4da67-139">Se não for especificado, a prioridade será 1000.</span><span class="sxs-lookup"><span data-stu-id="4da67-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="4da67-140">Um número baixo indica uma prioridade de trabalho mais alta.</span><span class="sxs-lookup"><span data-stu-id="4da67-140">A low number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="4da67-141">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="4da67-141">-RecurrenceId</span></span>
<span data-ttu-id="4da67-142">Uma ID que indica o envio desse trabalho é uma parte de um conjunto de trabalhos recorrentes com a mesma ID de recorrência.</span><span class="sxs-lookup"><span data-stu-id="4da67-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-143">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="4da67-143">-RecurrenceName</span></span>
<span data-ttu-id="4da67-144">Um nome amigável opcional para a correlação de recorrência entre trabalhos.</span><span class="sxs-lookup"><span data-stu-id="4da67-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="4da67-145">-RunId</span></span>
<span data-ttu-id="4da67-146">Uma ID que identifica essa iteração de execução específica do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4da67-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-147">-Runtime</span><span class="sxs-lookup"><span data-stu-id="4da67-147">-Runtime</span></span>
<span data-ttu-id="4da67-148">Especifica a versão do tempo de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4da67-148">Specifies the runtime version of the job.</span></span>

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

### <span data-ttu-id="4da67-149">-Script</span><span class="sxs-lookup"><span data-stu-id="4da67-149">-Script</span></span>
<span data-ttu-id="4da67-150">Especifica o conteúdo do script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="4da67-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="4da67-151">-ScriptPath</span></span>
<span data-ttu-id="4da67-152">Especifica o caminho do arquivo local para o script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="4da67-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da67-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da67-153">-DefaultProfile</span></span>
<span data-ttu-id="4da67-154">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4da67-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4da67-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da67-155">CommonParameters</span></span>
<span data-ttu-id="4da67-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da67-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da67-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da67-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da67-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4da67-158">INPUTS</span></span>

### <span data-ttu-id="4da67-159">String</span><span class="sxs-lookup"><span data-stu-id="4da67-159">String</span></span>
<span data-ttu-id="4da67-160">O parâmetro ' script ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4da67-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4da67-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4da67-161">OUTPUTS</span></span>

### <span data-ttu-id="4da67-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="4da67-162">JobInformation</span></span>
<span data-ttu-id="4da67-163">Os detalhes iniciais do trabalho para o trabalho enviado.</span><span class="sxs-lookup"><span data-stu-id="4da67-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="4da67-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4da67-164">NOTES</span></span>

## <span data-ttu-id="4da67-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4da67-165">RELATED LINKS</span></span>

[<span data-ttu-id="4da67-166">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4da67-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4da67-167">Parar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4da67-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4da67-168">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4da67-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


