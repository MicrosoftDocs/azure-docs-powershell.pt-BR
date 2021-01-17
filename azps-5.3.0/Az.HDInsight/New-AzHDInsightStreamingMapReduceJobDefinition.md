---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 4f9fe1ef3ab16812553eb6ea22909ce37bd5ee69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429294"
---
# <span data-ttu-id="97363-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="97363-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="97363-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97363-102">SYNOPSIS</span></span>
<span data-ttu-id="97363-103">Cria um objeto de trabalho de MapReduce de fluxo contínuo.</span><span class="sxs-lookup"><span data-stu-id="97363-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="97363-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97363-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97363-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97363-105">DESCRIPTION</span></span>
<span data-ttu-id="97363-106">O cmdlet **New-AzHDInsightStreamingMapReduceJobDefinition** define um objeto de trabalho de MapReduce de fluxo contínuo para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="97363-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="97363-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97363-107">EXAMPLES</span></span>

### <span data-ttu-id="97363-108">Exemplo 1: criar uma definição de trabalho de MapReduce de streaming</span><span class="sxs-lookup"><span data-stu-id="97363-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="97363-109">Esse comando cria uma definição de trabalho de MapReduce de fluxo contínuo.</span><span class="sxs-lookup"><span data-stu-id="97363-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="97363-110">OS</span><span class="sxs-lookup"><span data-stu-id="97363-110">PARAMETERS</span></span>

### <span data-ttu-id="97363-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="97363-111">-Arguments</span></span>
<span data-ttu-id="97363-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="97363-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="97363-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="97363-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="97363-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="97363-114">-CommandEnvironment</span></span>
<span data-ttu-id="97363-115">Especifica uma matriz de variáveis de ambiente de linha de comando a serem definidas quando um trabalho é executado em nós de trabalho.</span><span class="sxs-lookup"><span data-stu-id="97363-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="97363-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97363-116">-DefaultProfile</span></span>
<span data-ttu-id="97363-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="97363-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97363-118">-Define</span><span class="sxs-lookup"><span data-stu-id="97363-118">-Defines</span></span>
<span data-ttu-id="97363-119">Especifica os valores de configuração Hadoop para definir quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="97363-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="97363-120">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="97363-120">-File</span></span>
<span data-ttu-id="97363-121">Especifica o caminho para um arquivo que contém uma consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="97363-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="97363-122">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="97363-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="97363-123">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="97363-123">-Files</span></span>
<span data-ttu-id="97363-124">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="97363-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="97363-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="97363-125">-InputPath</span></span>
<span data-ttu-id="97363-126">Especifica o caminho para os arquivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="97363-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="97363-127">-Mapeador</span><span class="sxs-lookup"><span data-stu-id="97363-127">-Mapper</span></span>
<span data-ttu-id="97363-128">Especifica um nome de arquivo do mapeador.</span><span class="sxs-lookup"><span data-stu-id="97363-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="97363-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="97363-129">-OutputPath</span></span>
<span data-ttu-id="97363-130">Especifica o caminho para a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="97363-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="97363-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="97363-131">-Reducer</span></span>
<span data-ttu-id="97363-132">Especifica um nome de arquivo Reducer.</span><span class="sxs-lookup"><span data-stu-id="97363-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="97363-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="97363-133">-StatusFolder</span></span>
<span data-ttu-id="97363-134">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="97363-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="97363-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97363-135">CommonParameters</span></span>
<span data-ttu-id="97363-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97363-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97363-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97363-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97363-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97363-138">INPUTS</span></span>

### <span data-ttu-id="97363-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="97363-139">None</span></span>

## <span data-ttu-id="97363-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97363-140">OUTPUTS</span></span>

### <span data-ttu-id="97363-141">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="97363-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="97363-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97363-142">NOTES</span></span>

## <span data-ttu-id="97363-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97363-143">RELATED LINKS</span></span>

[<span data-ttu-id="97363-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="97363-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


