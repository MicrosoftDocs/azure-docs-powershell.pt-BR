---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945915"
---
# <span data-ttu-id="9bed6-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9bed6-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="9bed6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bed6-102">SYNOPSIS</span></span>
<span data-ttu-id="9bed6-103">Define um novo trabalho do Sqoop.</span><span class="sxs-lookup"><span data-stu-id="9bed6-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="9bed6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bed6-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9bed6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bed6-105">DESCRIPTION</span></span>
<span data-ttu-id="9bed6-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="9bed6-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="9bed6-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="9bed6-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="9bed6-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9bed6-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="9bed6-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="9bed6-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="9bed6-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="9bed6-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="9bed6-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9bed6-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="9bed6-112">O cmdlet **New-AzureHDInsightSqoopJobDefinition** cria um trabalho Sqoop para ser executado em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9bed6-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="9bed6-113">Sqoop é uma ferramenta para transferir dados entre clusters Hadoop e bancos de dados relacionais.</span><span class="sxs-lookup"><span data-stu-id="9bed6-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="9bed6-114">Você pode usar Sqoop para importar dados de um banco de dados do SQL Server para um sistema de arquivos distribuído Hadoop (HDFS), transformar os dados com o Hadoop MapReduce e, em seguida, exportar os dados do HDFS de volta para o banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9bed6-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="9bed6-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bed6-115">EXAMPLES</span></span>

### <span data-ttu-id="9bed6-116">Exemplo 1: importar dados</span><span class="sxs-lookup"><span data-stu-id="9bed6-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="9bed6-117">Esse comando define um trabalho Sqoop que importa todas as linhas de uma tabela de um banco de dados de servidor do AzureSQL para um cluster HDInsight e, em seguida, armazena a definição do trabalho na variável $SqoopJobDef.</span><span class="sxs-lookup"><span data-stu-id="9bed6-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="9bed6-118">OS</span><span class="sxs-lookup"><span data-stu-id="9bed6-118">PARAMETERS</span></span>

### <span data-ttu-id="9bed6-119">-Comando</span><span class="sxs-lookup"><span data-stu-id="9bed6-119">-Command</span></span>
<span data-ttu-id="9bed6-120">Especifica um comando Sqoop e seus argumentos.</span><span class="sxs-lookup"><span data-stu-id="9bed6-120">Specifies a Sqoop command and its arguments.</span></span>

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

### <span data-ttu-id="9bed6-121">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="9bed6-121">-File</span></span>
<span data-ttu-id="9bed6-122">Especifica o caminho para um arquivo de script que contém os comandos a serem executados.</span><span class="sxs-lookup"><span data-stu-id="9bed6-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="9bed6-123">O arquivo de script deve estar localizado em WASB.</span><span class="sxs-lookup"><span data-stu-id="9bed6-123">The script file must be located on WASB.</span></span>

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

### <span data-ttu-id="9bed6-124">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="9bed6-124">-Files</span></span>
<span data-ttu-id="9bed6-125">Especifica a coleção de arquivos WASB necessários para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="9bed6-125">Specifies the collection of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="9bed6-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9bed6-126">-Profile</span></span>
<span data-ttu-id="9bed6-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9bed6-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9bed6-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9bed6-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9bed6-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="9bed6-129">-StatusFolder</span></span>
<span data-ttu-id="9bed6-130">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho, incluindo o código de saída e os logs de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9bed6-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="9bed6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bed6-131">CommonParameters</span></span>
<span data-ttu-id="9bed6-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bed6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bed6-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bed6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bed6-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bed6-134">INPUTS</span></span>

## <span data-ttu-id="9bed6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bed6-135">OUTPUTS</span></span>

## <span data-ttu-id="9bed6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bed6-136">NOTES</span></span>

## <span data-ttu-id="9bed6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bed6-137">RELATED LINKS</span></span>

[<span data-ttu-id="9bed6-138">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9bed6-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="9bed6-139">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9bed6-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="9bed6-140">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9bed6-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="9bed6-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9bed6-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


