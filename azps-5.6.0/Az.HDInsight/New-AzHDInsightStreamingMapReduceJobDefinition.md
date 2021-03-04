---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 60e0f8e6799a89d673b3c9ca7de7827b197440fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886340"
---
# <span data-ttu-id="e13c1-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e13c1-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="e13c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e13c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e13c1-103">Cria um objeto de trabalho Streaming MapReduce.</span><span class="sxs-lookup"><span data-stu-id="e13c1-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="e13c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e13c1-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e13c1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e13c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e13c1-106">O cmdlet **New-AzHDInsightStreamingMapReduceJobDefinition** define um objeto de trabalho Streaming MapReduce para uso com um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="e13c1-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e13c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e13c1-107">EXAMPLES</span></span>

### <span data-ttu-id="e13c1-108">Exemplo 1: Criar uma definição de trabalho de Streaming MapReduce</span><span class="sxs-lookup"><span data-stu-id="e13c1-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="e13c1-109">Este comando cria uma definição de trabalho de Streaming MapReduce.</span><span class="sxs-lookup"><span data-stu-id="e13c1-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="e13c1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e13c1-110">PARAMETERS</span></span>

### <span data-ttu-id="e13c1-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="e13c1-111">-Arguments</span></span>
<span data-ttu-id="e13c1-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e13c1-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="e13c1-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="e13c1-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e13c1-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="e13c1-114">-CommandEnvironment</span></span>
<span data-ttu-id="e13c1-115">Especifica uma matriz de variáveis de ambiente de linha de comando a ser definida quando um trabalho é executado em nós de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e13c1-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="e13c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13c1-116">-DefaultProfile</span></span>
<span data-ttu-id="e13c1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e13c1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e13c1-118">-Define</span><span class="sxs-lookup"><span data-stu-id="e13c1-118">-Defines</span></span>
<span data-ttu-id="e13c1-119">Especifica valores de configuração hadoop a ser definidos para quando o trabalho for executado.</span><span class="sxs-lookup"><span data-stu-id="e13c1-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="e13c1-120">-File</span><span class="sxs-lookup"><span data-stu-id="e13c1-120">-File</span></span>
<span data-ttu-id="e13c1-121">Especifica o caminho para um arquivo que contém uma consulta a ser executado.</span><span class="sxs-lookup"><span data-stu-id="e13c1-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="e13c1-122">Você pode usar esse parâmetro em vez do *parâmetro Query.*</span><span class="sxs-lookup"><span data-stu-id="e13c1-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="e13c1-123">-Files</span><span class="sxs-lookup"><span data-stu-id="e13c1-123">-Files</span></span>
<span data-ttu-id="e13c1-124">Especifica uma coleção de arquivos que estão associados a um trabalho hive.</span><span class="sxs-lookup"><span data-stu-id="e13c1-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="e13c1-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="e13c1-125">-InputPath</span></span>
<span data-ttu-id="e13c1-126">Especifica o caminho para os arquivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="e13c1-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="e13c1-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="e13c1-127">-Mapper</span></span>
<span data-ttu-id="e13c1-128">Especifica um nome de arquivo Mapper.</span><span class="sxs-lookup"><span data-stu-id="e13c1-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="e13c1-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e13c1-129">-OutputPath</span></span>
<span data-ttu-id="e13c1-130">Especifica o caminho para a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e13c1-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="e13c1-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="e13c1-131">-Reducer</span></span>
<span data-ttu-id="e13c1-132">Especifica um nome de arquivo do Redutor.</span><span class="sxs-lookup"><span data-stu-id="e13c1-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="e13c1-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e13c1-133">-StatusFolder</span></span>
<span data-ttu-id="e13c1-134">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="e13c1-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="e13c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13c1-135">CommonParameters</span></span>
<span data-ttu-id="e13c1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e13c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13c1-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e13c1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13c1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e13c1-138">INPUTS</span></span>

### <span data-ttu-id="e13c1-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e13c1-139">None</span></span>

## <span data-ttu-id="e13c1-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e13c1-140">OUTPUTS</span></span>

### <span data-ttu-id="e13c1-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e13c1-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="e13c1-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="e13c1-142">NOTES</span></span>

## <span data-ttu-id="e13c1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e13c1-143">RELATED LINKS</span></span>

[<span data-ttu-id="e13c1-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e13c1-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


