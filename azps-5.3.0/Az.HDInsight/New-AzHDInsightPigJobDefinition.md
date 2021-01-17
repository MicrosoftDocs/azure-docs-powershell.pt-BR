---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: 4a21a8fdacdb53df7e513744cae31da4a7a61ca7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429295"
---
# <span data-ttu-id="76660-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="76660-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="76660-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76660-102">SYNOPSIS</span></span>
<span data-ttu-id="76660-103">Cria um objeto de trabalho porco.</span><span class="sxs-lookup"><span data-stu-id="76660-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="76660-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76660-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76660-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76660-105">DESCRIPTION</span></span>
<span data-ttu-id="76660-106">O cmdlet **New-AzHDInsightPigJobDefinition** define um objeto de trabalho porco para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="76660-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="76660-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76660-107">EXAMPLES</span></span>

### <span data-ttu-id="76660-108">Exemplo 1: criar uma definição de trabalho do porco</span><span class="sxs-lookup"><span data-stu-id="76660-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="76660-109">Esse comando cria uma definição de trabalho porco.</span><span class="sxs-lookup"><span data-stu-id="76660-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="76660-110">OS</span><span class="sxs-lookup"><span data-stu-id="76660-110">PARAMETERS</span></span>

### <span data-ttu-id="76660-111">-Argumentos</span><span class="sxs-lookup"><span data-stu-id="76660-111">-Arguments</span></span>
<span data-ttu-id="76660-112">Especifica uma matriz de argumentos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="76660-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="76660-113">Os argumentos são passados como argumentos de linha de comando para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="76660-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="76660-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76660-114">-DefaultProfile</span></span>
<span data-ttu-id="76660-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="76660-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76660-116">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="76660-116">-File</span></span>
<span data-ttu-id="76660-117">Especifica o caminho para um arquivo que contém a consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="76660-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="76660-118">O arquivo deve estar disponível na conta de armazenamento associada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="76660-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="76660-119">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="76660-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="76660-120">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="76660-120">-Files</span></span>
<span data-ttu-id="76660-121">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="76660-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="76660-122">-Consulta</span><span class="sxs-lookup"><span data-stu-id="76660-122">-Query</span></span>
<span data-ttu-id="76660-123">Especifica a consulta porco.</span><span class="sxs-lookup"><span data-stu-id="76660-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="76660-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="76660-124">-StatusFolder</span></span>
<span data-ttu-id="76660-125">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="76660-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="76660-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76660-126">CommonParameters</span></span>
<span data-ttu-id="76660-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76660-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76660-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76660-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76660-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76660-129">INPUTS</span></span>

### <span data-ttu-id="76660-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="76660-130">None</span></span>

## <span data-ttu-id="76660-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76660-131">OUTPUTS</span></span>

### <span data-ttu-id="76660-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="76660-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="76660-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76660-133">NOTES</span></span>

## <span data-ttu-id="76660-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76660-134">RELATED LINKS</span></span>

[<span data-ttu-id="76660-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="76660-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


