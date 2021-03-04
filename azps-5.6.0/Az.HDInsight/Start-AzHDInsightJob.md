---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 316ac2671fe60271ad0d994855189071e3da2b95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886975"
---
# <span data-ttu-id="89f62-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89f62-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="89f62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89f62-102">SYNOPSIS</span></span>
<span data-ttu-id="89f62-103">Inicia um trabalho definido do Azure HDInsight em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="89f62-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="89f62-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="89f62-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89f62-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="89f62-105">DESCRIPTION</span></span>
<span data-ttu-id="89f62-106">O cmdlet **Start-AzHDInsightJob** inicia um trabalho DEFINIDO do Azure HDInsight em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="89f62-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="89f62-107">Pode ser um trabalho MapReduce, um trabalho de Streaming MapReduce, um trabalho de Hive ou um trabalho de Leião.</span><span class="sxs-lookup"><span data-stu-id="89f62-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="89f62-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89f62-108">EXAMPLES</span></span>

### <span data-ttu-id="89f62-109">Exemplo 1: Iniciar um trabalho no cluster especificado</span><span class="sxs-lookup"><span data-stu-id="89f62-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="89f62-110">Este comando inicia um trabalho no cluster chamado your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="89f62-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="89f62-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="89f62-111">PARAMETERS</span></span>

### <span data-ttu-id="89f62-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="89f62-112">-ClusterName</span></span>
<span data-ttu-id="89f62-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="89f62-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="89f62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f62-114">-DefaultProfile</span></span>
<span data-ttu-id="89f62-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="89f62-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89f62-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="89f62-116">-HttpCredential</span></span>
<span data-ttu-id="89f62-117">Especifica as credenciais de logon de cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="89f62-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="89f62-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="89f62-118">-JobDefinition</span></span>
<span data-ttu-id="89f62-119">Especifica o trabalho a ser inicial no cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="89f62-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="89f62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f62-120">-ResourceGroupName</span></span>
<span data-ttu-id="89f62-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89f62-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="89f62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f62-122">CommonParameters</span></span>
<span data-ttu-id="89f62-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f62-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89f62-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f62-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89f62-125">INPUTS</span></span>

### <span data-ttu-id="89f62-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="89f62-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="89f62-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="89f62-127">OUTPUTS</span></span>

### <span data-ttu-id="89f62-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89f62-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="89f62-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="89f62-129">NOTES</span></span>

## <span data-ttu-id="89f62-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89f62-130">RELATED LINKS</span></span>

[<span data-ttu-id="89f62-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89f62-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="89f62-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="89f62-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="89f62-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89f62-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="89f62-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="89f62-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


