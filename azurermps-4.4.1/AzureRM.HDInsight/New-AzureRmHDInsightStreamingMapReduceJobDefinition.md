---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 526f2005f1c6594128af7e259e2ccb0aa296a71b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440664"
---
# <span data-ttu-id="12064-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12064-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="12064-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12064-102">SYNOPSIS</span></span>
<span data-ttu-id="12064-103">Cria um objeto de trabalho de MapReduce de fluxo contínuo.</span><span class="sxs-lookup"><span data-stu-id="12064-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12064-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12064-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12064-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12064-105">DESCRIPTION</span></span>
<span data-ttu-id="12064-106">O cmdlet **New-AzureRmHDInsightStreamingMapReduceJobDefinition** define um objeto de trabalho de MapReduce de fluxo contínuo para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="12064-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="12064-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12064-107">EXAMPLES</span></span>

### <span data-ttu-id="12064-108">Exemplo 1: criar uma definição de trabalho de MapReduce de streaming</span><span class="sxs-lookup"><span data-stu-id="12064-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="12064-109">Esse comando cria uma definição de trabalho de MapReduce de fluxo contínuo.</span><span class="sxs-lookup"><span data-stu-id="12064-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="12064-110">OS</span><span class="sxs-lookup"><span data-stu-id="12064-110">PARAMETERS</span></span>

### <span data-ttu-id="12064-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="12064-111">-Arguments</span></span>
<span data-ttu-id="12064-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="12064-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="12064-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="12064-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="12064-114">-CommandEnvironment</span></span>
<span data-ttu-id="12064-115">Especifica uma matriz de variáveis de ambiente de linha de comando a serem definidas quando um trabalho é executado em nós de trabalho.</span><span class="sxs-lookup"><span data-stu-id="12064-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-116">-Define</span><span class="sxs-lookup"><span data-stu-id="12064-116">-Defines</span></span>
<span data-ttu-id="12064-117">Especifica os valores de configuração Hadoop para definir quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="12064-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-118">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="12064-118">-File</span></span>
<span data-ttu-id="12064-119">Especifica o caminho para um arquivo que contém uma consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="12064-119">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="12064-120">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="12064-120">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-121">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="12064-121">-Files</span></span>
<span data-ttu-id="12064-122">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="12064-122">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-123">-InputPath</span><span class="sxs-lookup"><span data-stu-id="12064-123">-InputPath</span></span>
<span data-ttu-id="12064-124">Especifica o caminho para os arquivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="12064-124">Specifies the path to the input files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-125">-Mapeador</span><span class="sxs-lookup"><span data-stu-id="12064-125">-Mapper</span></span>
<span data-ttu-id="12064-126">Especifica um nome de arquivo do mapeador.</span><span class="sxs-lookup"><span data-stu-id="12064-126">Specifies a Mapper file name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="12064-127">-OutputPath</span></span>
<span data-ttu-id="12064-128">Especifica o caminho para a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="12064-128">Specifies the path for the job output.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-129">-Reducer</span><span class="sxs-lookup"><span data-stu-id="12064-129">-Reducer</span></span>
<span data-ttu-id="12064-130">Especifica um nome de arquivo Reducer.</span><span class="sxs-lookup"><span data-stu-id="12064-130">Specifies a Reducer file name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-131">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="12064-131">-StatusFolder</span></span>
<span data-ttu-id="12064-132">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="12064-132">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12064-133">-DefaultProfile</span></span>
<span data-ttu-id="12064-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12064-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12064-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12064-135">CommonParameters</span></span>
<span data-ttu-id="12064-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12064-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12064-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12064-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12064-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12064-138">INPUTS</span></span>

## <span data-ttu-id="12064-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12064-139">OUTPUTS</span></span>

### <span data-ttu-id="12064-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12064-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="12064-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12064-141">NOTES</span></span>

## <span data-ttu-id="12064-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12064-142">RELATED LINKS</span></span>

[<span data-ttu-id="12064-143">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="12064-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


