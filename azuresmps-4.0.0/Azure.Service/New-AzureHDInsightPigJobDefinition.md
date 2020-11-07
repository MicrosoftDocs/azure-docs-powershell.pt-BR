---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946010"
---
# <span data-ttu-id="3c525-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c525-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="3c525-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c525-102">SYNOPSIS</span></span>
<span data-ttu-id="3c525-103">Define um novo trabalho do porco para um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3c525-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="3c525-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c525-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c525-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c525-105">DESCRIPTION</span></span>
<span data-ttu-id="3c525-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="3c525-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="3c525-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="3c525-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="3c525-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3c525-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="3c525-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="3c525-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="3c525-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="3c525-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="3c525-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3c525-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="3c525-112">O **New-AzureHDInsightPigJobDefinition** define um trabalho porco para um serviço do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3c525-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="3c525-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c525-113">EXAMPLES</span></span>

### <span data-ttu-id="3c525-114">Exemplo 1: definir um novo trabalho de porco</span><span class="sxs-lookup"><span data-stu-id="3c525-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="3c525-115">O primeiro comando declara um valor de cadeia de caracteres e, em seguida, armazena na variável $0.</span><span class="sxs-lookup"><span data-stu-id="3c525-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="3c525-116">O segundo comando cria uma consulta de trabalho porco e armazena-a na variável $QueryString.</span><span class="sxs-lookup"><span data-stu-id="3c525-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="3c525-117">O comando final cria uma definição de trabalho porco que usa a consulta no $QueryString e, em seguida, armazena a definição do trabalho na variável $PigJobDefinition.</span><span class="sxs-lookup"><span data-stu-id="3c525-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="3c525-118">OS</span><span class="sxs-lookup"><span data-stu-id="3c525-118">PARAMETERS</span></span>

### <span data-ttu-id="3c525-119">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="3c525-119">-Arguments</span></span>
<span data-ttu-id="3c525-120">Especifica uma matriz de argumentos para um trabalho do porco.</span><span class="sxs-lookup"><span data-stu-id="3c525-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="3c525-121">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="3c525-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="3c525-122">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="3c525-122">-File</span></span>
<span data-ttu-id="3c525-123">Especifica o caminho para um arquivo que contém uma consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="3c525-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="3c525-124">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="3c525-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="3c525-125">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="3c525-125">-Files</span></span>
<span data-ttu-id="3c525-126">Especifica uma coleção de arquivos que estão associados a um trabalho do porco.</span><span class="sxs-lookup"><span data-stu-id="3c525-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="3c525-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3c525-127">-Profile</span></span>
<span data-ttu-id="3c525-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3c525-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c525-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3c525-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c525-130">-Consulta</span><span class="sxs-lookup"><span data-stu-id="3c525-130">-Query</span></span>
<span data-ttu-id="3c525-131">Especifica uma consulta de trabalho do porco.</span><span class="sxs-lookup"><span data-stu-id="3c525-131">Specifies a Pig job query.</span></span>

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

### <span data-ttu-id="3c525-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="3c525-132">-StatusFolder</span></span>
<span data-ttu-id="3c525-133">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho, incluindo o código de saída e os logs de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3c525-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="3c525-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c525-134">CommonParameters</span></span>
<span data-ttu-id="3c525-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c525-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c525-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c525-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c525-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c525-137">INPUTS</span></span>

## <span data-ttu-id="3c525-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c525-138">OUTPUTS</span></span>

## <span data-ttu-id="3c525-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c525-139">NOTES</span></span>

## <span data-ttu-id="3c525-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c525-140">RELATED LINKS</span></span>

[<span data-ttu-id="3c525-141">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c525-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="3c525-142">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c525-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="3c525-143">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c525-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="3c525-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c525-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


