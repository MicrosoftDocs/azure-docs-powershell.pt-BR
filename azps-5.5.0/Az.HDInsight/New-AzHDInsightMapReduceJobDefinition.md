---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: d6ab15fffd71776188291c58f2e21bbee5f27423
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116773"
---
# <span data-ttu-id="4d812-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4d812-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="4d812-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d812-102">SYNOPSIS</span></span>
<span data-ttu-id="4d812-103">Cria um objeto de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="4d812-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="4d812-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d812-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d812-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d812-105">DESCRIPTION</span></span>
<span data-ttu-id="4d812-106">O cmdlet **New-AzHDInsightMapReduceJobDefinition** define um novo trabalho de MapReduce para ser usado com um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d812-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4d812-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d812-107">EXAMPLES</span></span>

### <span data-ttu-id="4d812-108">Exemplo 1: Criar uma definição de trabalho MapReduce</span><span class="sxs-lookup"><span data-stu-id="4d812-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="4d812-109">Esse comando cria uma definição de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="4d812-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="4d812-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d812-110">PARAMETERS</span></span>

### <span data-ttu-id="4d812-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="4d812-111">-Arguments</span></span>
<span data-ttu-id="4d812-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d812-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="4d812-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="4d812-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="4d812-114">-NomeDa Classe</span><span class="sxs-lookup"><span data-stu-id="4d812-114">-ClassName</span></span>
<span data-ttu-id="4d812-115">Especifica a classe do trabalho no arquivo JAR.</span><span class="sxs-lookup"><span data-stu-id="4d812-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="4d812-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d812-116">-DefaultProfile</span></span>
<span data-ttu-id="4d812-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4d812-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d812-118">-Define</span><span class="sxs-lookup"><span data-stu-id="4d812-118">-Defines</span></span>
<span data-ttu-id="4d812-119">Especifica valores de configuração hadoop para definir quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="4d812-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="4d812-120">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="4d812-120">-Files</span></span>
<span data-ttu-id="4d812-121">Especifica um conjunto de arquivos associados a um trabalho de Colmeia.</span><span class="sxs-lookup"><span data-stu-id="4d812-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="4d812-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="4d812-122">-JarFile</span></span>
<span data-ttu-id="4d812-123">Especifica o arquivo JAR a ser usado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d812-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="4d812-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="4d812-124">-JobName</span></span>
<span data-ttu-id="4d812-125">Especifica o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d812-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="4d812-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="4d812-126">-LibJars</span></span>
<span data-ttu-id="4d812-127">Especifica os JARS de liberdade para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d812-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="4d812-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="4d812-128">-StatusFolder</span></span>
<span data-ttu-id="4d812-129">Especifica o local da pasta que contém saídas padrão e saídas de erros para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d812-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="4d812-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d812-130">CommonParameters</span></span>
<span data-ttu-id="4d812-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d812-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d812-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d812-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d812-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d812-133">INPUTS</span></span>

### <span data-ttu-id="4d812-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4d812-134">None</span></span>

## <span data-ttu-id="4d812-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d812-135">OUTPUTS</span></span>

### <span data-ttu-id="4d812-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4d812-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="4d812-137">Notas</span><span class="sxs-lookup"><span data-stu-id="4d812-137">NOTES</span></span>

## <span data-ttu-id="4d812-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d812-138">RELATED LINKS</span></span>

[<span data-ttu-id="4d812-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4d812-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


