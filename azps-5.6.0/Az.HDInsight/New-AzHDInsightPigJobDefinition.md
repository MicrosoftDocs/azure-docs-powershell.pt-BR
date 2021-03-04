---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: abe1a0eaa03d498e151a58d5970f85be088e489e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889471"
---
# <span data-ttu-id="1206d-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1206d-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="1206d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1206d-102">SYNOPSIS</span></span>
<span data-ttu-id="1206d-103">Cria um objeto de trabalho Descarado.</span><span class="sxs-lookup"><span data-stu-id="1206d-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="1206d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1206d-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1206d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1206d-105">DESCRIPTION</span></span>
<span data-ttu-id="1206d-106">O cmdlet **New-AzHDInsightPigJobDefinition** define um objeto de trabalho Demão para uso com um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="1206d-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1206d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1206d-107">EXAMPLES</span></span>

### <span data-ttu-id="1206d-108">Exemplo 1: Criar uma definição de trabalho de Leião</span><span class="sxs-lookup"><span data-stu-id="1206d-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1206d-109">Este comando cria uma definição de trabalho de Leião.</span><span class="sxs-lookup"><span data-stu-id="1206d-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="1206d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1206d-110">PARAMETERS</span></span>

### <span data-ttu-id="1206d-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="1206d-111">-Arguments</span></span>
<span data-ttu-id="1206d-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1206d-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="1206d-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="1206d-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="1206d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1206d-114">-DefaultProfile</span></span>
<span data-ttu-id="1206d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1206d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1206d-116">-File</span><span class="sxs-lookup"><span data-stu-id="1206d-116">-File</span></span>
<span data-ttu-id="1206d-117">Especifica o caminho para um arquivo que contém a consulta a ser executado.</span><span class="sxs-lookup"><span data-stu-id="1206d-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="1206d-118">O arquivo deve estar disponível na conta de armazenamento associada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="1206d-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="1206d-119">Você pode usar esse parâmetro em vez do *parâmetro Query.*</span><span class="sxs-lookup"><span data-stu-id="1206d-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="1206d-120">-Files</span><span class="sxs-lookup"><span data-stu-id="1206d-120">-Files</span></span>
<span data-ttu-id="1206d-121">Especifica uma coleção de arquivos que estão associados a um trabalho hive.</span><span class="sxs-lookup"><span data-stu-id="1206d-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="1206d-122">-Query</span><span class="sxs-lookup"><span data-stu-id="1206d-122">-Query</span></span>
<span data-ttu-id="1206d-123">Especifica a consulta Descarado.</span><span class="sxs-lookup"><span data-stu-id="1206d-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="1206d-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="1206d-124">-StatusFolder</span></span>
<span data-ttu-id="1206d-125">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="1206d-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="1206d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1206d-126">CommonParameters</span></span>
<span data-ttu-id="1206d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1206d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1206d-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1206d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1206d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1206d-129">INPUTS</span></span>

### <span data-ttu-id="1206d-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1206d-130">None</span></span>

## <span data-ttu-id="1206d-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1206d-131">OUTPUTS</span></span>

### <span data-ttu-id="1206d-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1206d-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="1206d-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="1206d-133">NOTES</span></span>

## <span data-ttu-id="1206d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1206d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1206d-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1206d-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


