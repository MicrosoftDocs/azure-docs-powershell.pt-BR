---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 3d40596b5797ca6b08b896e9ca973e491d130017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431003"
---
# <span data-ttu-id="02e07-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="02e07-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="02e07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02e07-102">SYNOPSIS</span></span>
<span data-ttu-id="02e07-103">Cria um objeto de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="02e07-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02e07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02e07-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02e07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02e07-105">DESCRIPTION</span></span>
<span data-ttu-id="02e07-106">O cmdlet **New-AzureRmHDInsightMapReduceJobDefinition** define um novo trabalho MapReduce para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="02e07-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="02e07-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02e07-107">EXAMPLES</span></span>

### <span data-ttu-id="02e07-108">Exemplo 1: criar uma definição de trabalho MapReduce</span><span class="sxs-lookup"><span data-stu-id="02e07-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="02e07-109">Esse comando cria uma definição de trabalho MapReduce.</span><span class="sxs-lookup"><span data-stu-id="02e07-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="02e07-110">OS</span><span class="sxs-lookup"><span data-stu-id="02e07-110">PARAMETERS</span></span>

### <span data-ttu-id="02e07-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="02e07-111">-Arguments</span></span>
<span data-ttu-id="02e07-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="02e07-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="02e07-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="02e07-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="02e07-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="02e07-114">-ClassName</span></span>
<span data-ttu-id="02e07-115">Especifica a classe de trabalho no arquivo JAR.</span><span class="sxs-lookup"><span data-stu-id="02e07-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="02e07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e07-116">-DefaultProfile</span></span>
<span data-ttu-id="02e07-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="02e07-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02e07-118">-Define</span><span class="sxs-lookup"><span data-stu-id="02e07-118">-Defines</span></span>
<span data-ttu-id="02e07-119">Especifica os valores de configuração Hadoop para definir quando o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="02e07-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="02e07-120">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="02e07-120">-Files</span></span>
<span data-ttu-id="02e07-121">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="02e07-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="02e07-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="02e07-122">-JarFile</span></span>
<span data-ttu-id="02e07-123">Especifica o arquivo JAR a ser usado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="02e07-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="02e07-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="02e07-124">-JobName</span></span>
<span data-ttu-id="02e07-125">Especifica o nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="02e07-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="02e07-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="02e07-126">-LibJars</span></span>
<span data-ttu-id="02e07-127">Especifica os JARS do lib para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="02e07-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="02e07-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="02e07-128">-StatusFolder</span></span>
<span data-ttu-id="02e07-129">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="02e07-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="02e07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e07-130">CommonParameters</span></span>
<span data-ttu-id="02e07-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02e07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e07-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e07-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e07-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02e07-133">INPUTS</span></span>

### <span data-ttu-id="02e07-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="02e07-134">None</span></span>
<span data-ttu-id="02e07-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="02e07-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02e07-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02e07-136">OUTPUTS</span></span>

### <span data-ttu-id="02e07-137">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="02e07-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="02e07-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02e07-138">NOTES</span></span>

## <span data-ttu-id="02e07-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02e07-139">RELATED LINKS</span></span>

[<span data-ttu-id="02e07-140">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="02e07-140">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


