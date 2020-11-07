---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945917"
---
# <span data-ttu-id="770f3-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="770f3-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="770f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="770f3-102">SYNOPSIS</span></span>
<span data-ttu-id="770f3-103">Define um novo trabalho de Hive para um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="770f3-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="770f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="770f3-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="770f3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="770f3-105">DESCRIPTION</span></span>
<span data-ttu-id="770f3-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="770f3-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="770f3-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="770f3-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="770f3-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="770f3-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="770f3-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="770f3-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="770f3-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="770f3-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="770f3-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="770f3-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="770f3-112">O cmdlet **New-AzureHDInsightHiveJobDefinition** define um trabalho de Hive para um serviço do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="770f3-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="770f3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="770f3-113">EXAMPLES</span></span>

### <span data-ttu-id="770f3-114">Exemplo 1: criar uma definição de trabalho de Hive</span><span class="sxs-lookup"><span data-stu-id="770f3-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="770f3-115">Esse comando cria uma definição de trabalho de Hive que usa uma cadeia de caracteres de consulta predefinida e, em seguida, armazena-a na variável $HiveJobDefinition.</span><span class="sxs-lookup"><span data-stu-id="770f3-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="770f3-116">OS</span><span class="sxs-lookup"><span data-stu-id="770f3-116">PARAMETERS</span></span>

### <span data-ttu-id="770f3-117">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="770f3-117">-Arguments</span></span>
<span data-ttu-id="770f3-118">Especifica uma matriz de argumentos para um trabalho Hadoop.</span><span class="sxs-lookup"><span data-stu-id="770f3-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="770f3-119">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="770f3-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="770f3-120">-Define</span><span class="sxs-lookup"><span data-stu-id="770f3-120">-Defines</span></span>
<span data-ttu-id="770f3-121">Especifica os valores de configuração do Hadoop para definir quando um trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="770f3-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

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

### <span data-ttu-id="770f3-122">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="770f3-122">-File</span></span>
<span data-ttu-id="770f3-123">Especifica o caminho para um arquivo que contém uma consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="770f3-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="770f3-124">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="770f3-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="770f3-125">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="770f3-125">-Files</span></span>
<span data-ttu-id="770f3-126">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="770f3-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="770f3-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="770f3-127">-JobName</span></span>
<span data-ttu-id="770f3-128">Especifica o nome do trabalho de Hive a ser definido.</span><span class="sxs-lookup"><span data-stu-id="770f3-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="770f3-129">Se você não especificar esse parâmetro, o nome padrão será usado: "Hive: \<first 100 characters of query\> ".</span><span class="sxs-lookup"><span data-stu-id="770f3-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

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

### <span data-ttu-id="770f3-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="770f3-130">-Profile</span></span>
<span data-ttu-id="770f3-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="770f3-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="770f3-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="770f3-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="770f3-133">-Consulta</span><span class="sxs-lookup"><span data-stu-id="770f3-133">-Query</span></span>
<span data-ttu-id="770f3-134">Especifica uma consulta Hive.</span><span class="sxs-lookup"><span data-stu-id="770f3-134">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="770f3-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="770f3-135">-RunAsFileJob</span></span>
<span data-ttu-id="770f3-136">Indica que esse cmdlet cria um arquivo na conta de armazenamento padrão do Azure para armazenar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="770f3-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="770f3-137">Esse cmdlet envia o trabalho que faz referência a esse arquivo como um script para ser executado.</span><span class="sxs-lookup"><span data-stu-id="770f3-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="770f3-138">Você pode usar essa funcionalidade para manipular caracteres especiais, como o sinal de porcentagem (%) Isso falharia em um envio de trabalho por meio de Templeton, porque Templeton interpreta uma consulta com um sinal de porcentagem como parâmetro de URL.</span><span class="sxs-lookup"><span data-stu-id="770f3-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="770f3-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="770f3-139">-StatusFolder</span></span>
<span data-ttu-id="770f3-140">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho, incluindo o código de saída e os logs de tarefas.</span><span class="sxs-lookup"><span data-stu-id="770f3-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="770f3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770f3-141">CommonParameters</span></span>
<span data-ttu-id="770f3-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770f3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770f3-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770f3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770f3-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="770f3-144">INPUTS</span></span>

## <span data-ttu-id="770f3-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="770f3-145">OUTPUTS</span></span>

## <span data-ttu-id="770f3-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="770f3-146">NOTES</span></span>

## <span data-ttu-id="770f3-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="770f3-147">RELATED LINKS</span></span>

[<span data-ttu-id="770f3-148">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="770f3-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="770f3-149">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="770f3-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="770f3-150">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="770f3-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="770f3-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="770f3-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


