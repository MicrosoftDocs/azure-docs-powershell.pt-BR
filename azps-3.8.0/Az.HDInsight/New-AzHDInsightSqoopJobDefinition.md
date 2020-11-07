---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 2cc5acb2017a9db2bf5ed1f80ccfd1069bc1a465
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778481"
---
# <span data-ttu-id="6f98c-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6f98c-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="6f98c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f98c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f98c-103">Cria um objeto de trabalho Sqoop.</span><span class="sxs-lookup"><span data-stu-id="6f98c-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="6f98c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f98c-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f98c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f98c-105">DESCRIPTION</span></span>
<span data-ttu-id="6f98c-106">O cmdlet **New-AzHDInsightSqoopJobDefinition** define um objeto de trabalho Sqoop para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6f98c-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6f98c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f98c-107">EXAMPLES</span></span>

### <span data-ttu-id="6f98c-108">Exemplo 1: criar uma definição de trabalho do Sqoop</span><span class="sxs-lookup"><span data-stu-id="6f98c-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="6f98c-109">Esse comando cria uma definição de trabalho Sqoop.</span><span class="sxs-lookup"><span data-stu-id="6f98c-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="6f98c-110">OS</span><span class="sxs-lookup"><span data-stu-id="6f98c-110">PARAMETERS</span></span>

### <span data-ttu-id="6f98c-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="6f98c-111">-Command</span></span>
<span data-ttu-id="6f98c-112">Especifica o comando Sqoop.</span><span class="sxs-lookup"><span data-stu-id="6f98c-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="6f98c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f98c-113">-DefaultProfile</span></span>
<span data-ttu-id="6f98c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6f98c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f98c-115">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="6f98c-115">-File</span></span>
<span data-ttu-id="6f98c-116">Especifica o caminho para um arquivo que contém a consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="6f98c-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="6f98c-117">O arquivo deve estar disponível na conta de armazenamento associada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="6f98c-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="6f98c-118">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="6f98c-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="6f98c-119">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="6f98c-119">-Files</span></span>
<span data-ttu-id="6f98c-120">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="6f98c-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="6f98c-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="6f98c-121">-LibDir</span></span>
<span data-ttu-id="6f98c-122">Especifica o diretório de bibliotecas para o trabalho do Sqoop.</span><span class="sxs-lookup"><span data-stu-id="6f98c-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="6f98c-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="6f98c-123">-StatusFolder</span></span>
<span data-ttu-id="6f98c-124">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="6f98c-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="6f98c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f98c-125">CommonParameters</span></span>
<span data-ttu-id="6f98c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f98c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f98c-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f98c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f98c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f98c-128">INPUTS</span></span>

### <span data-ttu-id="6f98c-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6f98c-129">None</span></span>

## <span data-ttu-id="6f98c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f98c-130">OUTPUTS</span></span>

### <span data-ttu-id="6f98c-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6f98c-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="6f98c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f98c-132">NOTES</span></span>

## <span data-ttu-id="6f98c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f98c-133">RELATED LINKS</span></span>

[<span data-ttu-id="6f98c-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6f98c-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


