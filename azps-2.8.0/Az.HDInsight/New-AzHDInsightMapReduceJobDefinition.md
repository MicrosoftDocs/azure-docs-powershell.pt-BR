---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: c1dab20f44edfd4e3714e4465a0bf295e8e78fb5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596347"
---
# <span data-ttu-id="e1b9b-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e1b9b-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="e1b9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b9b-103">Cria um objeto de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="e1b9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1b9b-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1b9b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="e1b9b-106">O cmdlet **New-AzHDInsightMapReduceJobDefinition** define um novo trabalho MapReduce para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e1b9b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1b9b-107">EXAMPLES</span></span>

### <span data-ttu-id="e1b9b-108">Exemplo 1: criar uma definição de trabalho MapReduce</span><span class="sxs-lookup"><span data-stu-id="e1b9b-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="e1b9b-109">Esse comando cria uma definição de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="e1b9b-110">OS</span><span class="sxs-lookup"><span data-stu-id="e1b9b-110">PARAMETERS</span></span>

### <span data-ttu-id="e1b9b-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="e1b9b-111">-Arguments</span></span>
<span data-ttu-id="e1b9b-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="e1b9b-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e1b9b-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="e1b9b-114">-ClassName</span></span>
<span data-ttu-id="e1b9b-115">Especifica a classe de trabalho no arquivo JAR.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="e1b9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b9b-116">-DefaultProfile</span></span>
<span data-ttu-id="e1b9b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e1b9b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1b9b-118">-Define</span><span class="sxs-lookup"><span data-stu-id="e1b9b-118">-Defines</span></span>
<span data-ttu-id="e1b9b-119">Especifica os valores de configuração Hadoop para definir quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="e1b9b-120">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="e1b9b-120">-Files</span></span>
<span data-ttu-id="e1b9b-121">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="e1b9b-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="e1b9b-122">-JarFile</span></span>
<span data-ttu-id="e1b9b-123">Especifica o arquivo JAR a ser usado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="e1b9b-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="e1b9b-124">-JobName</span></span>
<span data-ttu-id="e1b9b-125">Especifica o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="e1b9b-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="e1b9b-126">-LibJars</span></span>
<span data-ttu-id="e1b9b-127">Especifica os JARS do lib para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="e1b9b-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e1b9b-128">-StatusFolder</span></span>
<span data-ttu-id="e1b9b-129">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="e1b9b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b9b-130">CommonParameters</span></span>
<span data-ttu-id="e1b9b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b9b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b9b-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1b9b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b9b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1b9b-133">INPUTS</span></span>

### <span data-ttu-id="e1b9b-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e1b9b-134">None</span></span>

## <span data-ttu-id="e1b9b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1b9b-135">OUTPUTS</span></span>

### <span data-ttu-id="e1b9b-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e1b9b-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="e1b9b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1b9b-137">NOTES</span></span>

## <span data-ttu-id="e1b9b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1b9b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1b9b-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e1b9b-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


