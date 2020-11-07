---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946009"
---
# <span data-ttu-id="79606-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="79606-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="79606-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79606-102">SYNOPSIS</span></span>
<span data-ttu-id="79606-103">Define um novo trabalho de MapReduce de fluxo contínuo.</span><span class="sxs-lookup"><span data-stu-id="79606-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="79606-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79606-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="79606-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79606-105">DESCRIPTION</span></span>
<span data-ttu-id="79606-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="79606-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="79606-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="79606-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="79606-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="79606-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="79606-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="79606-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="79606-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="79606-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="79606-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="79606-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="79606-112">O cmdlet **New-AzureHDInsightStreamingMapReduceJobDefinition** define um novo objeto de definição de trabalho que representa os parâmetros de um trabalho de streaming Hadoop.</span><span class="sxs-lookup"><span data-stu-id="79606-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="79606-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79606-113">EXAMPLES</span></span>

### <span data-ttu-id="79606-114">Exemplo 1: criar uma definição de trabalho de MapReduce de streaming</span><span class="sxs-lookup"><span data-stu-id="79606-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="79606-115">Esse comando cria a definição do trabalho de transmissão de fluxo contínuo especificado e armazena-a na variável $StreamingWordCount.</span><span class="sxs-lookup"><span data-stu-id="79606-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="79606-116">OS</span><span class="sxs-lookup"><span data-stu-id="79606-116">PARAMETERS</span></span>

### <span data-ttu-id="79606-117">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="79606-117">-Arguments</span></span>
<span data-ttu-id="79606-118">Especifica uma matriz de argumentos para um trabalho Hadoop.</span><span class="sxs-lookup"><span data-stu-id="79606-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="79606-119">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="79606-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="79606-120">-CmdEnv</span></span>
<span data-ttu-id="79606-121">Especifica uma matriz de variáveis de ambiente de linha de comando a serem definidas quando um trabalho é executado em nós de dados.</span><span class="sxs-lookup"><span data-stu-id="79606-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-122">-Combine</span><span class="sxs-lookup"><span data-stu-id="79606-122">-Combiner</span></span>
<span data-ttu-id="79606-123">Especifica um nome de arquivo de combinação.</span><span class="sxs-lookup"><span data-stu-id="79606-123">Specifies a Combiner file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-124">-Define</span><span class="sxs-lookup"><span data-stu-id="79606-124">-Defines</span></span>
<span data-ttu-id="79606-125">Especifica os valores de configuração Hadoop a serem definidos quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="79606-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-126">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="79606-126">-Files</span></span>
<span data-ttu-id="79606-127">Especifica uma matriz de arquivos necessários para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="79606-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="79606-128">-InputPath</span></span>
<span data-ttu-id="79606-129">Especifica o caminho WASB para os arquivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="79606-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="79606-130">-JobName</span></span>
<span data-ttu-id="79606-131">Especifica o nome da nova definição de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="79606-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="79606-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79606-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-133">-Mapeador</span><span class="sxs-lookup"><span data-stu-id="79606-133">-Mapper</span></span>
<span data-ttu-id="79606-134">Especifica um nome de arquivo do mapeador.</span><span class="sxs-lookup"><span data-stu-id="79606-134">Specifies a Mapper file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="79606-135">-OutputPath</span></span>
<span data-ttu-id="79606-136">Especifica o caminho WASB para a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="79606-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-137">-Perfil</span><span class="sxs-lookup"><span data-stu-id="79606-137">-Profile</span></span>
<span data-ttu-id="79606-138">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="79606-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79606-139">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="79606-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-140">-Reducer</span><span class="sxs-lookup"><span data-stu-id="79606-140">-Reducer</span></span>
<span data-ttu-id="79606-141">Especifica um nome de arquivo Reducer.</span><span class="sxs-lookup"><span data-stu-id="79606-141">Specifies a Reducer file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="79606-142">-StatusFolder</span></span>
<span data-ttu-id="79606-143">Especifica a pasta que contém as saídas padrão e saídas de erro para o trabalho, incluindo o código de saída e os logs de tarefas.</span><span class="sxs-lookup"><span data-stu-id="79606-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79606-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79606-144">CommonParameters</span></span>
<span data-ttu-id="79606-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79606-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79606-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79606-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79606-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79606-147">INPUTS</span></span>

## <span data-ttu-id="79606-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79606-148">OUTPUTS</span></span>

## <span data-ttu-id="79606-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79606-149">NOTES</span></span>

## <span data-ttu-id="79606-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79606-150">RELATED LINKS</span></span>

[<span data-ttu-id="79606-151">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="79606-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="79606-152">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="79606-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="79606-153">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="79606-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="79606-154">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="79606-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


