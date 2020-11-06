---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440867"
---
# <span data-ttu-id="d6320-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6320-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="d6320-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6320-102">SYNOPSIS</span></span>
<span data-ttu-id="d6320-103">Inicia um trabalho do Azure HDInsight definido em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="d6320-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6320-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6320-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6320-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6320-105">DESCRIPTION</span></span>
<span data-ttu-id="d6320-106">O cmdlet **Start-AzureRMHDInsightJob** inicia um trabalho do Azure HDInsight definido em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="d6320-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="d6320-107">Isso pode ser um trabalho MapReduce, um trabalho de MapReduce de fluxo de serviço, um trabalho de Hive ou um trabalho porco.</span><span class="sxs-lookup"><span data-stu-id="d6320-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="d6320-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6320-108">EXAMPLES</span></span>

### <span data-ttu-id="d6320-109">Exemplo 1: iniciar um trabalho no cluster especificado</span><span class="sxs-lookup"><span data-stu-id="d6320-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="d6320-110">Esse comando inicia um trabalho no cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d6320-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d6320-111">OS</span><span class="sxs-lookup"><span data-stu-id="d6320-111">PARAMETERS</span></span>

### <span data-ttu-id="d6320-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d6320-112">-ClusterName</span></span>
<span data-ttu-id="d6320-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="d6320-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6320-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6320-114">-DefaultProfile</span></span>
<span data-ttu-id="d6320-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d6320-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6320-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d6320-116">-HttpCredential</span></span>
<span data-ttu-id="d6320-117">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="d6320-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6320-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="d6320-118">-JobDefinition</span></span>
<span data-ttu-id="d6320-119">Especifica o trabalho a ser iniciado no cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d6320-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6320-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6320-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6320-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6320-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d6320-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6320-122">CommonParameters</span></span>
<span data-ttu-id="d6320-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6320-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6320-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6320-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6320-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6320-125">INPUTS</span></span>

### <span data-ttu-id="d6320-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d6320-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="d6320-127">O parâmetro ' JobDefinition ' aceita o valor do tipo ' AzureHDInsightJobDefinition ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d6320-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="d6320-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6320-128">OUTPUTS</span></span>

### <span data-ttu-id="d6320-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6320-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d6320-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6320-130">NOTES</span></span>

## <span data-ttu-id="d6320-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6320-131">RELATED LINKS</span></span>

[<span data-ttu-id="d6320-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6320-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="d6320-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d6320-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="d6320-134">Parar-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6320-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="d6320-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6320-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


