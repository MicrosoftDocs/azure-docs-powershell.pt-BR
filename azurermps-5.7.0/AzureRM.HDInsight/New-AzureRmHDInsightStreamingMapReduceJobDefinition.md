---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: f74d0e56265e5b976de9cf289f3b6a4900b76d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430485"
---
# <span data-ttu-id="b7168-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b7168-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="b7168-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7168-102">SYNOPSIS</span></span>
<span data-ttu-id="b7168-103">Cria um objeto de trabalho de MapReduce de fluxo contínuo.</span><span class="sxs-lookup"><span data-stu-id="b7168-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7168-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7168-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7168-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7168-105">DESCRIPTION</span></span>
<span data-ttu-id="b7168-106">O cmdlet **New-AzureRmHDInsightStreamingMapReduceJobDefinition** define um objeto de trabalho de MapReduce de fluxo contínuo para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b7168-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b7168-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7168-107">EXAMPLES</span></span>

### <span data-ttu-id="b7168-108">Exemplo 1: criar uma definição de trabalho de MapReduce de streaming</span><span class="sxs-lookup"><span data-stu-id="b7168-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b7168-109">Esse comando cria uma definição de trabalho de MapReduce de fluxo contínuo.</span><span class="sxs-lookup"><span data-stu-id="b7168-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="b7168-110">OS</span><span class="sxs-lookup"><span data-stu-id="b7168-110">PARAMETERS</span></span>

### <span data-ttu-id="b7168-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="b7168-111">-Arguments</span></span>
<span data-ttu-id="b7168-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="b7168-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b7168-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="b7168-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b7168-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="b7168-114">-CommandEnvironment</span></span>
<span data-ttu-id="b7168-115">Especifica uma matriz de variáveis de ambiente de linha de comando a serem definidas quando um trabalho é executado em nós de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b7168-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7168-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7168-116">-DefaultProfile</span></span>
<span data-ttu-id="b7168-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b7168-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7168-118">-Define</span><span class="sxs-lookup"><span data-stu-id="b7168-118">-Defines</span></span>
<span data-ttu-id="b7168-119">Especifica os valores de configuração Hadoop para definir quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="b7168-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7168-120">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="b7168-120">-File</span></span>
<span data-ttu-id="b7168-121">Especifica o caminho para um arquivo que contém uma consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="b7168-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="b7168-122">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="b7168-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b7168-123">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="b7168-123">-Files</span></span>
<span data-ttu-id="b7168-124">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="b7168-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b7168-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="b7168-125">-InputPath</span></span>
<span data-ttu-id="b7168-126">Especifica o caminho para os arquivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="b7168-126">Specifies the path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7168-127">-Mapeador</span><span class="sxs-lookup"><span data-stu-id="b7168-127">-Mapper</span></span>
<span data-ttu-id="b7168-128">Especifica um nome de arquivo do mapeador.</span><span class="sxs-lookup"><span data-stu-id="b7168-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="b7168-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b7168-129">-OutputPath</span></span>
<span data-ttu-id="b7168-130">Especifica o caminho para a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b7168-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="b7168-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="b7168-131">-Reducer</span></span>
<span data-ttu-id="b7168-132">Especifica um nome de arquivo Reducer.</span><span class="sxs-lookup"><span data-stu-id="b7168-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="b7168-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b7168-133">-StatusFolder</span></span>
<span data-ttu-id="b7168-134">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="b7168-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b7168-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7168-135">CommonParameters</span></span>
<span data-ttu-id="b7168-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7168-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7168-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7168-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7168-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7168-138">INPUTS</span></span>

### <span data-ttu-id="b7168-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b7168-139">None</span></span>
<span data-ttu-id="b7168-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b7168-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7168-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7168-141">OUTPUTS</span></span>

### <span data-ttu-id="b7168-142">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b7168-142">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="b7168-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7168-143">NOTES</span></span>

## <span data-ttu-id="b7168-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7168-144">RELATED LINKS</span></span>

[<span data-ttu-id="b7168-145">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b7168-145">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


