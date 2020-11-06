---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 54fb8305b14272fb34b6329cf057372da7c42a88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596326"
---
# <span data-ttu-id="00d99-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="00d99-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="00d99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00d99-102">SYNOPSIS</span></span>
<span data-ttu-id="00d99-103">Inicia um trabalho do Azure HDInsight definido em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="00d99-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="00d99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00d99-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00d99-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00d99-105">DESCRIPTION</span></span>
<span data-ttu-id="00d99-106">O cmdlet **Start-AzHDInsightJob** inicia um trabalho do Azure HDInsight definido em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="00d99-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="00d99-107">Isso pode ser um trabalho MapReduce, um trabalho de MapReduce de fluxo de serviço, um trabalho de Hive ou um trabalho porco.</span><span class="sxs-lookup"><span data-stu-id="00d99-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="00d99-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00d99-108">EXAMPLES</span></span>

### <span data-ttu-id="00d99-109">Exemplo 1: iniciar um trabalho no cluster especificado</span><span class="sxs-lookup"><span data-stu-id="00d99-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="00d99-110">Esse comando inicia um trabalho no cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="00d99-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="00d99-111">OS</span><span class="sxs-lookup"><span data-stu-id="00d99-111">PARAMETERS</span></span>

### <span data-ttu-id="00d99-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="00d99-112">-ClusterName</span></span>
<span data-ttu-id="00d99-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="00d99-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="00d99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d99-114">-DefaultProfile</span></span>
<span data-ttu-id="00d99-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="00d99-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00d99-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="00d99-116">-HttpCredential</span></span>
<span data-ttu-id="00d99-117">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="00d99-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="00d99-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="00d99-118">-JobDefinition</span></span>
<span data-ttu-id="00d99-119">Especifica o trabalho a ser iniciado no cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="00d99-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="00d99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00d99-120">-ResourceGroupName</span></span>
<span data-ttu-id="00d99-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00d99-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="00d99-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d99-122">CommonParameters</span></span>
<span data-ttu-id="00d99-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d99-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d99-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d99-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d99-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00d99-125">INPUTS</span></span>

### <span data-ttu-id="00d99-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="00d99-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="00d99-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00d99-127">OUTPUTS</span></span>

### <span data-ttu-id="00d99-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="00d99-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="00d99-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00d99-129">NOTES</span></span>

## <span data-ttu-id="00d99-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00d99-130">RELATED LINKS</span></span>

[<span data-ttu-id="00d99-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="00d99-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="00d99-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="00d99-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="00d99-133">Parar-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="00d99-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="00d99-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="00d99-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


