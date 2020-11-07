---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946248"
---
# <span data-ttu-id="d1a34-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="d1a34-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="d1a34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1a34-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a34-103">Envia consultas de Hive para um cluster HDInsight, mostra o progresso da execução da consulta e obtém resultados de consulta em uma operação.</span><span class="sxs-lookup"><span data-stu-id="d1a34-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="d1a34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1a34-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d1a34-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1a34-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a34-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="d1a34-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d1a34-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="d1a34-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d1a34-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d1a34-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d1a34-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d1a34-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d1a34-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="d1a34-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d1a34-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d1a34-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d1a34-112">O cmdlet **Invoke-AzureHDInsightHiveJob** envia consultas de Hive para um cluster HDInsight, exibe o progresso da execução da consulta e obtém os resultados da consulta em uma operação.</span><span class="sxs-lookup"><span data-stu-id="d1a34-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="d1a34-113">Você deve executar o cmdlet Use-AzureHDInsightCluster antes de executar **Invoke-AzureHDInsightHiveJob** para especificar o cluster HDInsight para o qual enviar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="d1a34-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="d1a34-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1a34-114">EXAMPLES</span></span>

### <span data-ttu-id="d1a34-115">Exemplo 1: Enviar uma consulta de Hive</span><span class="sxs-lookup"><span data-stu-id="d1a34-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="d1a34-116">O primeiro comando usa o cmdlet **use-AzureHDInsightCluster** para especificar um cluster na assinatura atual a ser usada para uma consulta de Hive.</span><span class="sxs-lookup"><span data-stu-id="d1a34-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="d1a34-117">O segundo comando usa o cmdlet **Invoke-AzureHDInsightHiveJob** para enviar a consulta Hive.</span><span class="sxs-lookup"><span data-stu-id="d1a34-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="d1a34-118">OS</span><span class="sxs-lookup"><span data-stu-id="d1a34-118">PARAMETERS</span></span>

### <span data-ttu-id="d1a34-119">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="d1a34-119">-Arguments</span></span>
<span data-ttu-id="d1a34-120">Especifica uma matriz de argumentos para um trabalho Hadoop.</span><span class="sxs-lookup"><span data-stu-id="d1a34-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="d1a34-121">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="d1a34-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="d1a34-122">-Define</span><span class="sxs-lookup"><span data-stu-id="d1a34-122">-Defines</span></span>
<span data-ttu-id="d1a34-123">Especifica os valores de configuração Hadoop a serem definidos quando um trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="d1a34-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="d1a34-124">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="d1a34-124">-File</span></span>
<span data-ttu-id="d1a34-125">Especifica o caminho do Windows Azure Storage BLOB (WASB) para um arquivo no armazenamento de blob do Azure que contém a consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="d1a34-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="d1a34-126">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="d1a34-126">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a34-127">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="d1a34-127">-Files</span></span>
<span data-ttu-id="d1a34-128">Especifica uma coleção de arquivos necessários para um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="d1a34-128">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="d1a34-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="d1a34-129">-JobName</span></span>
<span data-ttu-id="d1a34-130">Especifica o nome de um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="d1a34-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="d1a34-131">Se você não especificar esse parâmetro, esse cmdlet usará o valor padrão: "Hive: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="d1a34-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="d1a34-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d1a34-132">-Profile</span></span>
<span data-ttu-id="d1a34-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d1a34-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1a34-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d1a34-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d1a34-135">-Consulta</span><span class="sxs-lookup"><span data-stu-id="d1a34-135">-Query</span></span>
<span data-ttu-id="d1a34-136">Especifica uma consulta Hive.</span><span class="sxs-lookup"><span data-stu-id="d1a34-136">Specifies a Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a34-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="d1a34-137">-RunAsFileJob</span></span>
<span data-ttu-id="d1a34-138">Indica que esse cmdlet cria um arquivo na conta de armazenamento padrão do Azure para armazenar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="d1a34-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="d1a34-139">Esse cmdlet envia o trabalho que faz referência a esse arquivo como um script para ser executado.</span><span class="sxs-lookup"><span data-stu-id="d1a34-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="d1a34-140">Você pode usar essa funcionalidade para manipular caracteres especiais, como o sinal de porcentagem (%) Isso falharia em um envio de trabalho por meio de Templeton, porque Templeton interpreta uma consulta com um sinal de porcentagem como parâmetro de URL.</span><span class="sxs-lookup"><span data-stu-id="d1a34-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="d1a34-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d1a34-141">-StatusFolder</span></span>
<span data-ttu-id="d1a34-142">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho, incluindo o código de saída e os logs de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d1a34-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="d1a34-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a34-143">CommonParameters</span></span>
<span data-ttu-id="d1a34-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a34-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a34-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1a34-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a34-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1a34-146">INPUTS</span></span>

## <span data-ttu-id="d1a34-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1a34-147">OUTPUTS</span></span>

## <span data-ttu-id="d1a34-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1a34-148">NOTES</span></span>

## <span data-ttu-id="d1a34-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1a34-149">RELATED LINKS</span></span>

[<span data-ttu-id="d1a34-150">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d1a34-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="d1a34-151">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d1a34-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


