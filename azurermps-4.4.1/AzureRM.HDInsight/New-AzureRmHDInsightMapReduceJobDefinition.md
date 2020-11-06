---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7b3bce866712565b5eeb6fc9deccc64f9da69891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441068"
---
# <span data-ttu-id="74c68-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="74c68-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="74c68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74c68-102">SYNOPSIS</span></span>
<span data-ttu-id="74c68-103">Cria um objeto de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="74c68-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74c68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74c68-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74c68-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74c68-105">DESCRIPTION</span></span>
<span data-ttu-id="74c68-106">O cmdlet **New-AzureRmHDInsightMapReduceJobDefinition** define um novo trabalho MapReduce para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="74c68-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="74c68-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74c68-107">EXAMPLES</span></span>

### <span data-ttu-id="74c68-108">Exemplo 1: criar uma definição de trabalho MapReduce</span><span class="sxs-lookup"><span data-stu-id="74c68-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="74c68-109">Esse comando cria uma definição de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="74c68-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="74c68-110">OS</span><span class="sxs-lookup"><span data-stu-id="74c68-110">PARAMETERS</span></span>

### <span data-ttu-id="74c68-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="74c68-111">-Arguments</span></span>
<span data-ttu-id="74c68-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="74c68-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="74c68-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="74c68-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="74c68-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="74c68-114">-ClassName</span></span>
<span data-ttu-id="74c68-115">Especifica a classe de trabalho no arquivo JAR.</span><span class="sxs-lookup"><span data-stu-id="74c68-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="74c68-116">-Define</span><span class="sxs-lookup"><span data-stu-id="74c68-116">-Defines</span></span>
<span data-ttu-id="74c68-117">Especifica os valores de configuração Hadoop para definir quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="74c68-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="74c68-118">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="74c68-118">-Files</span></span>
<span data-ttu-id="74c68-119">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="74c68-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="74c68-120">-JarFile</span><span class="sxs-lookup"><span data-stu-id="74c68-120">-JarFile</span></span>
<span data-ttu-id="74c68-121">Especifica o arquivo JAR a ser usado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="74c68-121">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="74c68-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="74c68-122">-JobName</span></span>
<span data-ttu-id="74c68-123">Especifica o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="74c68-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="74c68-124">-LibJars</span><span class="sxs-lookup"><span data-stu-id="74c68-124">-LibJars</span></span>
<span data-ttu-id="74c68-125">Especifica os JARS do lib para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="74c68-125">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="74c68-126">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="74c68-126">-StatusFolder</span></span>
<span data-ttu-id="74c68-127">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="74c68-127">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="74c68-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c68-128">-DefaultProfile</span></span>
<span data-ttu-id="74c68-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74c68-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74c68-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c68-130">CommonParameters</span></span>
<span data-ttu-id="74c68-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c68-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c68-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c68-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c68-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74c68-133">INPUTS</span></span>

## <span data-ttu-id="74c68-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74c68-134">OUTPUTS</span></span>

### <span data-ttu-id="74c68-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="74c68-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="74c68-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74c68-136">NOTES</span></span>

## <span data-ttu-id="74c68-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74c68-137">RELATED LINKS</span></span>

[<span data-ttu-id="74c68-138">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="74c68-138">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


