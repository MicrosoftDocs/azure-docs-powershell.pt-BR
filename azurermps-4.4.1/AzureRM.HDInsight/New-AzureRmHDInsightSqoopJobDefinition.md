---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 769406d0eb47672fcaaea8acfb3b3fdccd6810d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610503"
---
# <span data-ttu-id="88ce1-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="88ce1-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="88ce1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="88ce1-103">Cria um objeto de trabalho Sqoop.</span><span class="sxs-lookup"><span data-stu-id="88ce1-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88ce1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88ce1-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88ce1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88ce1-105">DESCRIPTION</span></span>
<span data-ttu-id="88ce1-106">O cmdlet **New-AzureRmHDInsightSqoopJobDefinition** define um objeto de trabalho Sqoop para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="88ce1-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="88ce1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88ce1-107">EXAMPLES</span></span>

### <span data-ttu-id="88ce1-108">Exemplo 1: criar uma definição de trabalho do Sqoop</span><span class="sxs-lookup"><span data-stu-id="88ce1-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="88ce1-109">Esse comando cria uma definição de trabalho Sqoop.</span><span class="sxs-lookup"><span data-stu-id="88ce1-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="88ce1-110">OS</span><span class="sxs-lookup"><span data-stu-id="88ce1-110">PARAMETERS</span></span>

### <span data-ttu-id="88ce1-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="88ce1-111">-Command</span></span>
<span data-ttu-id="88ce1-112">Especifica o comando Sqoop.</span><span class="sxs-lookup"><span data-stu-id="88ce1-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="88ce1-113">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="88ce1-113">-File</span></span>
<span data-ttu-id="88ce1-114">Especifica o caminho para um arquivo que contém a consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="88ce1-114">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="88ce1-115">O arquivo deve estar disponível na conta de armazenamento associada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="88ce1-115">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="88ce1-116">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="88ce1-116">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="88ce1-117">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="88ce1-117">-Files</span></span>
<span data-ttu-id="88ce1-118">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="88ce1-118">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="88ce1-119">-LibDir</span><span class="sxs-lookup"><span data-stu-id="88ce1-119">-LibDir</span></span>
<span data-ttu-id="88ce1-120">Especifica o diretório de bibliotecas para o trabalho do Sqoop.</span><span class="sxs-lookup"><span data-stu-id="88ce1-120">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="88ce1-121">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="88ce1-121">-StatusFolder</span></span>
<span data-ttu-id="88ce1-122">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="88ce1-122">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="88ce1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ce1-123">-DefaultProfile</span></span>
<span data-ttu-id="88ce1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88ce1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ce1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ce1-125">CommonParameters</span></span>
<span data-ttu-id="88ce1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ce1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ce1-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88ce1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ce1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88ce1-128">INPUTS</span></span>

## <span data-ttu-id="88ce1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88ce1-129">OUTPUTS</span></span>

### <span data-ttu-id="88ce1-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="88ce1-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="88ce1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88ce1-131">NOTES</span></span>

## <span data-ttu-id="88ce1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88ce1-132">RELATED LINKS</span></span>

[<span data-ttu-id="88ce1-133">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="88ce1-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


