---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7ea8831b3fdb9f6d5b11f5419f05dd34313d100f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893351"
---
# <span data-ttu-id="88eab-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="88eab-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="88eab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88eab-102">SYNOPSIS</span></span>
<span data-ttu-id="88eab-103">Cria um objeto de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="88eab-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="88eab-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="88eab-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88eab-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="88eab-105">DESCRIPTION</span></span>
<span data-ttu-id="88eab-106">O cmdlet **New-AzHDInsightMapReduceJobDefinition** define um novo trabalho MapReduce para uso com um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="88eab-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="88eab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88eab-107">EXAMPLES</span></span>

### <span data-ttu-id="88eab-108">Exemplo 1: Criar uma definição de trabalho MapReduce</span><span class="sxs-lookup"><span data-stu-id="88eab-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="88eab-109">Este comando cria uma definição de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="88eab-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="88eab-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="88eab-110">PARAMETERS</span></span>

### <span data-ttu-id="88eab-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="88eab-111">-Arguments</span></span>
<span data-ttu-id="88eab-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="88eab-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="88eab-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="88eab-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="88eab-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="88eab-114">-ClassName</span></span>
<span data-ttu-id="88eab-115">Especifica a classe de trabalho no arquivo JAR.</span><span class="sxs-lookup"><span data-stu-id="88eab-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="88eab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88eab-116">-DefaultProfile</span></span>
<span data-ttu-id="88eab-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="88eab-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88eab-118">-Define</span><span class="sxs-lookup"><span data-stu-id="88eab-118">-Defines</span></span>
<span data-ttu-id="88eab-119">Especifica valores de configuração hadoop a ser definidos para quando o trabalho for executado.</span><span class="sxs-lookup"><span data-stu-id="88eab-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="88eab-120">-Files</span><span class="sxs-lookup"><span data-stu-id="88eab-120">-Files</span></span>
<span data-ttu-id="88eab-121">Especifica uma coleção de arquivos que estão associados a um trabalho hive.</span><span class="sxs-lookup"><span data-stu-id="88eab-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="88eab-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="88eab-122">-JarFile</span></span>
<span data-ttu-id="88eab-123">Especifica o arquivo JAR a ser usado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="88eab-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="88eab-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="88eab-124">-JobName</span></span>
<span data-ttu-id="88eab-125">Especifica o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="88eab-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="88eab-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="88eab-126">-LibJars</span></span>
<span data-ttu-id="88eab-127">Especifica o JARS de lib para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="88eab-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="88eab-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="88eab-128">-StatusFolder</span></span>
<span data-ttu-id="88eab-129">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="88eab-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="88eab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88eab-130">CommonParameters</span></span>
<span data-ttu-id="88eab-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88eab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88eab-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88eab-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88eab-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88eab-133">INPUTS</span></span>

### <span data-ttu-id="88eab-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88eab-134">None</span></span>

## <span data-ttu-id="88eab-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="88eab-135">OUTPUTS</span></span>

### <span data-ttu-id="88eab-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="88eab-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="88eab-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="88eab-137">NOTES</span></span>

## <span data-ttu-id="88eab-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88eab-138">RELATED LINKS</span></span>

[<span data-ttu-id="88eab-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="88eab-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


