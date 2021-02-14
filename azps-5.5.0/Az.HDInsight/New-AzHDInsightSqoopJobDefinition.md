---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 69bb20b8a6610d2701a6c2256317b081dc11ad3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116772"
---
# <span data-ttu-id="b9874-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b9874-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b9874-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9874-102">SYNOPSIS</span></span>
<span data-ttu-id="b9874-103">Cria um objeto de trabalho Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b9874-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="b9874-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9874-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9874-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9874-105">DESCRIPTION</span></span>
<span data-ttu-id="b9874-106">O cmdlet **New-AzHDInsightSqoop JobDefinition** define um objeto de trabalho Sqoop para ser usado com um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9874-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b9874-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9874-107">EXAMPLES</span></span>

### <span data-ttu-id="b9874-108">Exemplo 1: Criar uma definição de trabalho do Sqoop</span><span class="sxs-lookup"><span data-stu-id="b9874-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b9874-109">Esse comando cria uma definição de trabalho do Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b9874-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="b9874-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9874-110">PARAMETERS</span></span>

### <span data-ttu-id="b9874-111">-Command</span><span class="sxs-lookup"><span data-stu-id="b9874-111">-Command</span></span>
<span data-ttu-id="b9874-112">Especifica o comando Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b9874-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="b9874-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9874-113">-DefaultProfile</span></span>
<span data-ttu-id="b9874-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b9874-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9874-115">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="b9874-115">-File</span></span>
<span data-ttu-id="b9874-116">Especifica o caminho para um arquivo que contém a consulta a ser executado.</span><span class="sxs-lookup"><span data-stu-id="b9874-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b9874-117">O arquivo deve estar disponível na conta de armazenamento associada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="b9874-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="b9874-118">Você pode usar esse parâmetro em vez do *parâmetro Consulta.*</span><span class="sxs-lookup"><span data-stu-id="b9874-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b9874-119">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="b9874-119">-Files</span></span>
<span data-ttu-id="b9874-120">Especifica um conjunto de arquivos associados a um trabalho de Colmeia.</span><span class="sxs-lookup"><span data-stu-id="b9874-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b9874-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="b9874-121">-LibDir</span></span>
<span data-ttu-id="b9874-122">Especifica o diretório da biblioteca para o trabalho do Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b9874-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="b9874-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b9874-123">-StatusFolder</span></span>
<span data-ttu-id="b9874-124">Especifica o local da pasta que contém saídas padrão e saídas de erros para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="b9874-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b9874-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9874-125">CommonParameters</span></span>
<span data-ttu-id="b9874-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9874-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9874-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9874-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9874-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="b9874-128">INPUTS</span></span>

### <span data-ttu-id="b9874-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b9874-129">None</span></span>

## <span data-ttu-id="b9874-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="b9874-130">OUTPUTS</span></span>

### <span data-ttu-id="b9874-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b9874-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b9874-132">Notas</span><span class="sxs-lookup"><span data-stu-id="b9874-132">NOTES</span></span>

## <span data-ttu-id="b9874-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9874-133">RELATED LINKS</span></span>

[<span data-ttu-id="b9874-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b9874-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


