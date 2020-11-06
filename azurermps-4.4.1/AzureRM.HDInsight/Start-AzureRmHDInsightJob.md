---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 5512482b6b8edc0d9c336c8879eb43072143ff53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610779"
---
# <span data-ttu-id="28210-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="28210-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="28210-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28210-102">SYNOPSIS</span></span>
<span data-ttu-id="28210-103">Inicia um trabalho do Azure HDInsight definido em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="28210-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28210-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28210-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28210-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28210-105">DESCRIPTION</span></span>
<span data-ttu-id="28210-106">O cmdlet **Start-AzureRMHDInsightJob** inicia um trabalho do Azure HDInsight definido em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="28210-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="28210-107">Isso pode ser um trabalho MapReduce, um trabalho de MapReduce de fluxo de serviço, um trabalho de Hive ou um trabalho porco.</span><span class="sxs-lookup"><span data-stu-id="28210-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="28210-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28210-108">EXAMPLES</span></span>

### <span data-ttu-id="28210-109">Exemplo 1: iniciar um trabalho no cluster especificado</span><span class="sxs-lookup"><span data-stu-id="28210-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="28210-110">Esse comando inicia um trabalho no cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="28210-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="28210-111">OS</span><span class="sxs-lookup"><span data-stu-id="28210-111">PARAMETERS</span></span>

### <span data-ttu-id="28210-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="28210-112">-ClusterName</span></span>
<span data-ttu-id="28210-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="28210-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28210-114">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="28210-114">-HttpCredential</span></span>
<span data-ttu-id="28210-115">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="28210-115">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28210-116">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="28210-116">-JobDefinition</span></span>
<span data-ttu-id="28210-117">Especifica o trabalho a ser iniciado no cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="28210-117">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28210-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28210-118">-ResourceGroupName</span></span>
<span data-ttu-id="28210-119">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="28210-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="28210-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28210-120">-DefaultProfile</span></span>
<span data-ttu-id="28210-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28210-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28210-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28210-122">CommonParameters</span></span>
<span data-ttu-id="28210-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28210-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28210-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28210-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28210-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28210-125">INPUTS</span></span>

### <span data-ttu-id="28210-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="28210-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="28210-127">O parâmetro ' JobDefinition ' aceita o valor do tipo ' AzureHDInsightJobDefinition ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="28210-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="28210-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28210-128">OUTPUTS</span></span>

### <span data-ttu-id="28210-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="28210-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="28210-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28210-130">NOTES</span></span>

## <span data-ttu-id="28210-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28210-131">RELATED LINKS</span></span>

[<span data-ttu-id="28210-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="28210-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="28210-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="28210-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="28210-134">Parar-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="28210-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="28210-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="28210-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


