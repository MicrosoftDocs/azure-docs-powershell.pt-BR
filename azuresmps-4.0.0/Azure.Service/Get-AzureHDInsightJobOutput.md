---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945640"
---
# <span data-ttu-id="37772-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="37772-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="37772-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37772-102">SYNOPSIS</span></span>
<span data-ttu-id="37772-103">Obtém a saída de log para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="37772-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="37772-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37772-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37772-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37772-105">DESCRIPTION</span></span>
<span data-ttu-id="37772-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="37772-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="37772-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="37772-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="37772-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="37772-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="37772-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte Criar clusters baseados em Linux no [HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="37772-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="37772-110">Para obter informações sobre como enviar trabalhos usando o PowerShell do Azure e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="37772-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="37772-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets Hdinsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="37772-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="37772-112">O cmdlet **Get-AzureHDInsightJobOutput** Obtém a saída de log para um trabalho da conta de armazenamento associada a um cluster.</span><span class="sxs-lookup"><span data-stu-id="37772-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="37772-113">Você pode obter vários tipos de logs de trabalho, incluindo saída padrão, erro padrão, logs de tarefas e um resumo dos logs de tarefas.</span><span class="sxs-lookup"><span data-stu-id="37772-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="37772-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37772-114">EXAMPLES</span></span>

### <span data-ttu-id="37772-115">Exemplo 1: obter saída do trabalho</span><span class="sxs-lookup"><span data-stu-id="37772-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="37772-116">O primeiro comando obtém a ID da assinatura atual e, em seguida, armazena-a na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="37772-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="37772-117">O segundo comando armazena o nome mycluster na variável $Clustername.</span><span class="sxs-lookup"><span data-stu-id="37772-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="37772-118">O terceiro comando cria uma definição de trabalho MapReduce e, em seguida, armazena-a na variável $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="37772-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="37772-119">O comando passa o trabalho em $WordCountJob para o cmdlet **Start-AzureHDInsightJob** para iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="37772-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="37772-120">Ele também passa $WordCountJob para o cmdlet **Wait-AzureHDInsightJob** aguardar a conclusão do trabalho e, em seguida, usa **Get-AzureHDInsightJobOutput** para obter a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="37772-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="37772-121">OS</span><span class="sxs-lookup"><span data-stu-id="37772-121">PARAMETERS</span></span>

### <span data-ttu-id="37772-122">-Certificado</span><span class="sxs-lookup"><span data-stu-id="37772-122">-Certificate</span></span>
<span data-ttu-id="37772-123">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="37772-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-124">-Cluster</span><span class="sxs-lookup"><span data-stu-id="37772-124">-Cluster</span></span>
<span data-ttu-id="37772-125">Especifica um cluster.</span><span class="sxs-lookup"><span data-stu-id="37772-125">Specifies a cluster.</span></span>
<span data-ttu-id="37772-126">Esse cmdlet obtém logs de trabalho do cluster que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="37772-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37772-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="37772-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="37772-128">Indica que esse cmdlet obtém os logs de tarefa para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="37772-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-129">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="37772-129">-Endpoint</span></span>
<span data-ttu-id="37772-130">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="37772-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="37772-131">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="37772-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="37772-132">-HostedService</span></span>
<span data-ttu-id="37772-133">Especifica o namespace de um serviço HDInsight se você não quiser usar o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="37772-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="37772-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="37772-135">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="37772-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="37772-136">-JobId</span></span>
<span data-ttu-id="37772-137">Especifica a ID do trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="37772-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37772-138">-Perfil</span><span class="sxs-lookup"><span data-stu-id="37772-138">-Profile</span></span>
<span data-ttu-id="37772-139">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="37772-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37772-140">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="37772-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37772-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="37772-141">-StandardError</span></span>
<span data-ttu-id="37772-142">Indica que esse cmdlet obtém a saída StdErr de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="37772-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="37772-143">-StandardOutput</span></span>
<span data-ttu-id="37772-144">Indica que esse cmdlet obtém a saída SdtOut de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="37772-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-145">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="37772-145">-Subscription</span></span>
<span data-ttu-id="37772-146">Especifica a assinatura que contém o cluster HDInsight a obter.</span><span class="sxs-lookup"><span data-stu-id="37772-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="37772-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="37772-148">Especifica uma pasta local na qual armazenar logs de tarefas.</span><span class="sxs-lookup"><span data-stu-id="37772-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="37772-149">-TaskSummary</span></span>
<span data-ttu-id="37772-150">Indica que este cmdlets Obtém o resumo do log de tarefas.</span><span class="sxs-lookup"><span data-stu-id="37772-150">Indicates that this cmdlets gets the task log summary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37772-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37772-151">CommonParameters</span></span>
<span data-ttu-id="37772-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37772-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37772-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37772-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37772-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37772-154">INPUTS</span></span>

## <span data-ttu-id="37772-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37772-155">OUTPUTS</span></span>

## <span data-ttu-id="37772-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37772-156">NOTES</span></span>

## <span data-ttu-id="37772-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37772-157">RELATED LINKS</span></span>

[<span data-ttu-id="37772-158">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="37772-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="37772-159">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="37772-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="37772-160">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="37772-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
