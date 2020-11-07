---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945832"
---
# <span data-ttu-id="642c2-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="642c2-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="642c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="642c2-102">SYNOPSIS</span></span>
<span data-ttu-id="642c2-103">Aguarda a conclusão ou a falha de um trabalho do HDInsight e exibe o progresso do trabalho.</span><span class="sxs-lookup"><span data-stu-id="642c2-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="642c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="642c2-104">SYNTAX</span></span>

### <span data-ttu-id="642c2-105">Obter jobDetails histórico de um cluster HDInsight (padrão)</span><span class="sxs-lookup"><span data-stu-id="642c2-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="642c2-106">Obter o histórico jobDetails de um cluster HDInsight (com uma credencial de assinatura específica)</span><span class="sxs-lookup"><span data-stu-id="642c2-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="642c2-107">Aguardar trabalho com JobId em um cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="642c2-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="642c2-108">Aguardar trabalho com o trabalho em um cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="642c2-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="642c2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="642c2-109">DESCRIPTION</span></span>
<span data-ttu-id="642c2-110">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="642c2-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="642c2-111">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="642c2-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="642c2-112">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="642c2-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="642c2-113">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="642c2-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="642c2-114">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="642c2-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="642c2-115">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="642c2-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="642c2-116">O cmdlet **Wait-AzureHDInsightJob** aguarda a conclusão ou a falha de um trabalho do Azure HDInsight e exibe o progresso do trabalho.</span><span class="sxs-lookup"><span data-stu-id="642c2-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="642c2-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="642c2-117">EXAMPLES</span></span>

### <span data-ttu-id="642c2-118">Exemplo 1: executar um trabalho e aguardar até que ele seja concluído</span><span class="sxs-lookup"><span data-stu-id="642c2-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="642c2-119">O primeiro comando obtém a ID da assinatura atual do Azure e armazena-a na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="642c2-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="642c2-120">O segundo comando obtém o cluster especificado e, em seguida, armazena-o na variável $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="642c2-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="642c2-121">O terceiro comando usa o cmdlet **New-AzureHDInsightMapReduceJobDefinition** para criar uma definição de trabalho MapReduce e, em seguida, armazena-o na variável $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="642c2-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="642c2-122">O quarto comando usa vários cmdlets em sequência:</span><span class="sxs-lookup"><span data-stu-id="642c2-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="642c2-123">Ele usa o operador pipeline para passar $WordCountJob para o cmdlet **Start-AzureHDInsightJob** para iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="642c2-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="642c2-124">O trabalho é passado para o cmdlet **Wait-AzureHDInsightJob** para esperar 3600 segundos para que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="642c2-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="642c2-125">Se o trabalho for concluído, o comando usará o cmdlet **Get-AzureHDInsightJobOutput** para obter a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="642c2-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="642c2-126">OS</span><span class="sxs-lookup"><span data-stu-id="642c2-126">PARAMETERS</span></span>

### <span data-ttu-id="642c2-127">-Certificado</span><span class="sxs-lookup"><span data-stu-id="642c2-127">-Certificate</span></span>
<span data-ttu-id="642c2-128">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="642c2-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-129">-Cluster</span><span class="sxs-lookup"><span data-stu-id="642c2-129">-Cluster</span></span>
<span data-ttu-id="642c2-130">Especifica um cluster.</span><span class="sxs-lookup"><span data-stu-id="642c2-130">Specifies a cluster.</span></span>
<span data-ttu-id="642c2-131">Esse cmdlet aguarda um trabalho no cluster que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="642c2-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="642c2-132">-Credential</span></span>
<span data-ttu-id="642c2-133">Especifica as credenciais a serem usadas para acesso HTTP direto a um cluster.</span><span class="sxs-lookup"><span data-stu-id="642c2-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="642c2-134">Você pode especificar esse parâmetro em vez do parâmetro de *assinatura* para autenticar o acesso a um cluster.</span><span class="sxs-lookup"><span data-stu-id="642c2-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-135">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="642c2-135">-Endpoint</span></span>
<span data-ttu-id="642c2-136">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="642c2-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="642c2-137">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="642c2-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="642c2-138">-HostedService</span></span>
<span data-ttu-id="642c2-139">Especifica o namespace de um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="642c2-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="642c2-140">Se você não especificar esse parâmetro, o namespace padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="642c2-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="642c2-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="642c2-142">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="642c2-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-143">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="642c2-143">-Job</span></span>
<span data-ttu-id="642c2-144">Especifica um trabalho do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="642c2-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="642c2-145">-JobId</span></span>
<span data-ttu-id="642c2-146">Especifica a ID do trabalho a ser aguardado.</span><span class="sxs-lookup"><span data-stu-id="642c2-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-147">-Perfil</span><span class="sxs-lookup"><span data-stu-id="642c2-147">-Profile</span></span>
<span data-ttu-id="642c2-148">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="642c2-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="642c2-149">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="642c2-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="642c2-150">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="642c2-150">-Subscription</span></span>
<span data-ttu-id="642c2-151">Especifica uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="642c2-151">Specifies a subscription.</span></span>
<span data-ttu-id="642c2-152">Esse cmdlet aguarda um trabalho para a assinatura que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="642c2-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="642c2-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="642c2-154">Especifica o tempo limite, em segundos, para a operação de espera.</span><span class="sxs-lookup"><span data-stu-id="642c2-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="642c2-155">Se o tempo limite expirar antes da conclusão do trabalho, o cmdlet deixará de ser executado.</span><span class="sxs-lookup"><span data-stu-id="642c2-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642c2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642c2-156">CommonParameters</span></span>
<span data-ttu-id="642c2-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="642c2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642c2-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="642c2-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642c2-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="642c2-159">INPUTS</span></span>

## <span data-ttu-id="642c2-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="642c2-160">OUTPUTS</span></span>

## <span data-ttu-id="642c2-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="642c2-161">NOTES</span></span>

## <span data-ttu-id="642c2-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="642c2-162">RELATED LINKS</span></span>

[<span data-ttu-id="642c2-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="642c2-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="642c2-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="642c2-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="642c2-165">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="642c2-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="642c2-166">Parar-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="642c2-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


