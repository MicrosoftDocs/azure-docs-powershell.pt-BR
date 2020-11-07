---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945916"
---
# <span data-ttu-id="ce076-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ce076-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="ce076-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce076-102">SYNOPSIS</span></span>
<span data-ttu-id="ce076-103">Define um novo trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="ce076-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="ce076-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce076-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce076-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce076-105">DESCRIPTION</span></span>
<span data-ttu-id="ce076-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="ce076-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ce076-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="ce076-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ce076-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ce076-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ce076-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ce076-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ce076-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ce076-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ce076-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ce076-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ce076-112">O cmdlet **New-AzureHDInsightMapReduceJobDefinition** define um novo trabalho MapReduce para ser executado em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ce076-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ce076-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce076-113">EXAMPLES</span></span>

### <span data-ttu-id="ce076-114">Exemplo 1: definir um trabalho MapReduce, executar o trabalho e obter a saída</span><span class="sxs-lookup"><span data-stu-id="ce076-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="ce076-115">O primeiro comando obtém a ID da assinatura atual e, em seguida, armazena-a na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="ce076-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="ce076-116">O segundo comando atribui o nome mycluster à variável $Clustername.</span><span class="sxs-lookup"><span data-stu-id="ce076-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="ce076-117">O terceiro comando usa o cmdlet **New-AzureHDInsightMapReduceJobDefinition** para criar uma definição de trabalho MapReduce e, em seguida, armazená-la na variável $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="ce076-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="ce076-118">O quarto comando executa uma sequência de operações usando estes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="ce076-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="ce076-119">**Start-AzureHDInsightJob** para iniciar o trabalho em $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="ce076-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="ce076-120">**Wait-AzureHDInsightJob** para esperar a conclusão do trabalho e exibir o progresso na conclusão.</span><span class="sxs-lookup"><span data-stu-id="ce076-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="ce076-121">**Get-AzureHDInsightJobOutput** para obter a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ce076-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="ce076-122">OS</span><span class="sxs-lookup"><span data-stu-id="ce076-122">PARAMETERS</span></span>

### <span data-ttu-id="ce076-123">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="ce076-123">-Arguments</span></span>
<span data-ttu-id="ce076-124">Especifica uma matriz de argumentos para um trabalho Hadoop.</span><span class="sxs-lookup"><span data-stu-id="ce076-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="ce076-125">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce076-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="ce076-126">-ClassName</span><span class="sxs-lookup"><span data-stu-id="ce076-126">-ClassName</span></span>
<span data-ttu-id="ce076-127">Especifica o nome da classe de trabalho no arquivo Java Archive (JAR).</span><span class="sxs-lookup"><span data-stu-id="ce076-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce076-128">-Define</span><span class="sxs-lookup"><span data-stu-id="ce076-128">-Defines</span></span>
<span data-ttu-id="ce076-129">Especifica os valores de configuração Hadoop a serem definidos quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="ce076-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="ce076-130">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="ce076-130">-Files</span></span>
<span data-ttu-id="ce076-131">Especifica uma matriz de arquivos WASB necessários para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="ce076-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="ce076-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="ce076-132">-JarFile</span></span>
<span data-ttu-id="ce076-133">Especifica o nome totalmente qualificado de um arquivo JAR que contém o código e as dependências de um trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="ce076-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce076-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="ce076-134">-JobName</span></span>
<span data-ttu-id="ce076-135">Especifica o nome de um trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="ce076-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="ce076-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ce076-136">This parameter is optional.</span></span>
<span data-ttu-id="ce076-137">Se você não especificar esse parâmetro, o valor do parâmetro *ClassName* será usado.</span><span class="sxs-lookup"><span data-stu-id="ce076-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="ce076-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="ce076-138">-LibJars</span></span>
<span data-ttu-id="ce076-139">Especifica uma matriz de referências LibJar do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ce076-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="ce076-140">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ce076-140">-Profile</span></span>
<span data-ttu-id="ce076-141">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ce076-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce076-142">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ce076-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce076-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="ce076-143">-StatusFolder</span></span>
<span data-ttu-id="ce076-144">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho, incluindo o código de saída e os logs de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ce076-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="ce076-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce076-145">CommonParameters</span></span>
<span data-ttu-id="ce076-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce076-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce076-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce076-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce076-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce076-148">INPUTS</span></span>

## <span data-ttu-id="ce076-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce076-149">OUTPUTS</span></span>

## <span data-ttu-id="ce076-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce076-150">NOTES</span></span>

## <span data-ttu-id="ce076-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce076-151">RELATED LINKS</span></span>

[<span data-ttu-id="ce076-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="ce076-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="ce076-153">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ce076-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="ce076-154">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ce076-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="ce076-155">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ce076-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="ce076-156">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ce076-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="ce076-157">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ce076-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


