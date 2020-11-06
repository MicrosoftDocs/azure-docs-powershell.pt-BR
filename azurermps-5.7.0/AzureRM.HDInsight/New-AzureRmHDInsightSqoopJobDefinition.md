---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 6f7045773dc1bf5582e2c480fd9e4aed283bf8ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430488"
---
# <span data-ttu-id="f9077-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f9077-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="f9077-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9077-102">SYNOPSIS</span></span>
<span data-ttu-id="f9077-103">Cria um objeto de trabalho Sqoop.</span><span class="sxs-lookup"><span data-stu-id="f9077-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9077-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9077-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9077-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9077-105">DESCRIPTION</span></span>
<span data-ttu-id="f9077-106">O cmdlet **New-AzureRmHDInsightSqoopJobDefinition** define um objeto de trabalho Sqoop para uso com um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f9077-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f9077-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9077-107">EXAMPLES</span></span>

### <span data-ttu-id="f9077-108">Exemplo 1: criar uma definição de trabalho do Sqoop</span><span class="sxs-lookup"><span data-stu-id="f9077-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f9077-109">Esse comando cria uma definição de trabalho Sqoop.</span><span class="sxs-lookup"><span data-stu-id="f9077-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="f9077-110">OS</span><span class="sxs-lookup"><span data-stu-id="f9077-110">PARAMETERS</span></span>

### <span data-ttu-id="f9077-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="f9077-111">-Command</span></span>
<span data-ttu-id="f9077-112">Especifica o comando Sqoop.</span><span class="sxs-lookup"><span data-stu-id="f9077-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="f9077-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9077-113">-DefaultProfile</span></span>
<span data-ttu-id="f9077-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f9077-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9077-115">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="f9077-115">-File</span></span>
<span data-ttu-id="f9077-116">Especifica o caminho para um arquivo que contém a consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="f9077-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="f9077-117">O arquivo deve estar disponível na conta de armazenamento associada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="f9077-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="f9077-118">Você pode usar esse parâmetro em vez do parâmetro de *consulta* .</span><span class="sxs-lookup"><span data-stu-id="f9077-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="f9077-119">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="f9077-119">-Files</span></span>
<span data-ttu-id="f9077-120">Especifica uma coleção de arquivos que estão associados a um trabalho de Hive.</span><span class="sxs-lookup"><span data-stu-id="f9077-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="f9077-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="f9077-121">-LibDir</span></span>
<span data-ttu-id="f9077-122">Especifica o diretório de bibliotecas para o trabalho do Sqoop.</span><span class="sxs-lookup"><span data-stu-id="f9077-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="f9077-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f9077-123">-StatusFolder</span></span>
<span data-ttu-id="f9077-124">Especifica o local da pasta que contém saídas padrão e saídas de erro para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f9077-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="f9077-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9077-125">CommonParameters</span></span>
<span data-ttu-id="f9077-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9077-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9077-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9077-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9077-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9077-128">INPUTS</span></span>

### <span data-ttu-id="f9077-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f9077-129">None</span></span>
<span data-ttu-id="f9077-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f9077-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9077-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9077-131">OUTPUTS</span></span>

### <span data-ttu-id="f9077-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f9077-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="f9077-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9077-133">NOTES</span></span>

## <span data-ttu-id="f9077-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9077-134">RELATED LINKS</span></span>

[<span data-ttu-id="f9077-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f9077-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


