---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945424"
---
# <span data-ttu-id="b769f-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b769f-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="b769f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b769f-102">SYNOPSIS</span></span>
<span data-ttu-id="b769f-103">Inicia um trabalho do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b769f-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="b769f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b769f-104">SYNTAX</span></span>

### <span data-ttu-id="b769f-105">Iniciar o jobDetails em um cluster HDInsight (padrão)</span><span class="sxs-lookup"><span data-stu-id="b769f-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b769f-106">Iniciar o jobDetails em um cluster HDInsight (com uma credencial de assinatura específica)</span><span class="sxs-lookup"><span data-stu-id="b769f-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b769f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b769f-107">DESCRIPTION</span></span>
<span data-ttu-id="b769f-108">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="b769f-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b769f-109">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="b769f-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b769f-110">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b769f-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b769f-111">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="b769f-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b769f-112">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="b769f-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b769f-113">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b769f-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b769f-114">O cmdlet **Start-AzureHDInsightJob** inicia um trabalho do Azure HDInsight definido em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="b769f-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="b769f-115">O trabalho a ser iniciado pode ser um trabalho MapReduce, um trabalho em fluxo, um trabalho de Hive ou um trabalho porco.</span><span class="sxs-lookup"><span data-stu-id="b769f-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="b769f-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b769f-116">EXAMPLES</span></span>

### <span data-ttu-id="b769f-117">Exemplo 1: iniciar um trabalho do HDInsight</span><span class="sxs-lookup"><span data-stu-id="b769f-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="b769f-118">O primeiro comando obtém a ID da assinatura atual e a armazena na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="b769f-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="b769f-119">O segundo comando atribui o nome Cluster01 à variável $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="b769f-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="b769f-120">O terceiro comando usa o cmdlet **New-AzureHDInsightMapReduceJobDefinition** para criar uma definição de trabalho MapReduce e, em seguida, armazena-o na variável $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="b769f-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="b769f-121">O comando final usa o operador pipeline para passar o $WordCountJob para o cmdlet **Start-AzureHDInsightJob** para iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="b769f-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="b769f-122">Após o início do trabalho, ele é passado para o cmdlet **Wait-AzureHDInsightJob** , que aguarda que o trabalho seja concluído antes de passá-lo para o cmdlet **Get-AzureHDInsightJobOutput** para obter a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b769f-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="b769f-123">OS</span><span class="sxs-lookup"><span data-stu-id="b769f-123">PARAMETERS</span></span>

### <span data-ttu-id="b769f-124">-Certificado</span><span class="sxs-lookup"><span data-stu-id="b769f-124">-Certificate</span></span>
<span data-ttu-id="b769f-125">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b769f-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b769f-126">-Cluster</span><span class="sxs-lookup"><span data-stu-id="b769f-126">-Cluster</span></span>
<span data-ttu-id="b769f-127">Especifica um cluster.</span><span class="sxs-lookup"><span data-stu-id="b769f-127">Specifies a cluster.</span></span>
<span data-ttu-id="b769f-128">Esse cmdlet inicia um trabalho no cluster que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b769f-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b769f-129">-Credential</span><span class="sxs-lookup"><span data-stu-id="b769f-129">-Credential</span></span>
<span data-ttu-id="b769f-130">Especifica as credenciais do cluster para acesso HTTP direto a um cluster.</span><span class="sxs-lookup"><span data-stu-id="b769f-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="b769f-131">Você pode especificar esse parâmetro em vez do parâmetro de *assinatura* para autenticar o acesso a um cluster.</span><span class="sxs-lookup"><span data-stu-id="b769f-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b769f-132">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="b769f-132">-Endpoint</span></span>
<span data-ttu-id="b769f-133">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="b769f-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b769f-134">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="b769f-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b769f-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b769f-135">-HostedService</span></span>
<span data-ttu-id="b769f-136">Especifica o namespace de um serviço HDInsight se você não quiser usar o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="b769f-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b769f-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b769f-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="b769f-138">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="b769f-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b769f-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="b769f-139">-JobDefinition</span></span>
<span data-ttu-id="b769f-140">Especifica o ponto de extremidade a ser usado ao se conectar ao Microsoft Azure se o ponto de extremidade for diferente do padrão.</span><span class="sxs-lookup"><span data-stu-id="b769f-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b769f-141">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b769f-141">-Profile</span></span>
<span data-ttu-id="b769f-142">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b769f-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b769f-143">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b769f-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b769f-144">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="b769f-144">-Subscription</span></span>
<span data-ttu-id="b769f-145">Especifica uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="b769f-145">Specifies a subscription.</span></span>
<span data-ttu-id="b769f-146">Esse cmdlet inicia um trabalho para a assinatura que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b769f-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b769f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b769f-147">CommonParameters</span></span>
<span data-ttu-id="b769f-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b769f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b769f-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b769f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b769f-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b769f-150">INPUTS</span></span>

## <span data-ttu-id="b769f-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b769f-151">OUTPUTS</span></span>

## <span data-ttu-id="b769f-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b769f-152">NOTES</span></span>

## <span data-ttu-id="b769f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b769f-153">RELATED LINKS</span></span>

[<span data-ttu-id="b769f-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b769f-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="b769f-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="b769f-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="b769f-156">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b769f-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="b769f-157">Parar-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b769f-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="b769f-158">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b769f-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


