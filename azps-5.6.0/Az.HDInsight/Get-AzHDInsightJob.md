---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: 87a5b306619bd3d16b9a7c4e76256f2d0e74d568
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891424"
---
# <span data-ttu-id="3137f-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3137f-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="3137f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3137f-102">SYNOPSIS</span></span>
<span data-ttu-id="3137f-103">Obtém a lista de trabalhos de um cluster e os lista em ordem cronológica inversa ou recupera um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="3137f-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="3137f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3137f-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3137f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3137f-105">DESCRIPTION</span></span>
<span data-ttu-id="3137f-106">O cmdlet **Get-AzHDInsightJob** obtém trabalhos recentes para um cluster HDInsight do Azure especificado em ordem cronológica inversa, com o trabalho mais recente na parte superior da lista.</span><span class="sxs-lookup"><span data-stu-id="3137f-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="3137f-107">Obter um trabalho específico fornecendo o *parâmetro JobId.*</span><span class="sxs-lookup"><span data-stu-id="3137f-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="3137f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3137f-108">EXAMPLES</span></span>

### <span data-ttu-id="3137f-109">Exemplo 1: Obter trabalhos recentes para um cluster HDInsight do Azure especificado</span><span class="sxs-lookup"><span data-stu-id="3137f-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="3137f-110">Este comando obtém todos os trabalhos recentes para o cluster chamado your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="3137f-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3137f-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3137f-111">PARAMETERS</span></span>

### <span data-ttu-id="3137f-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3137f-112">-ClusterName</span></span>
<span data-ttu-id="3137f-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3137f-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3137f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3137f-114">-DefaultProfile</span></span>
<span data-ttu-id="3137f-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3137f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3137f-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="3137f-116">-HttpCredential</span></span>
<span data-ttu-id="3137f-117">Especifica as credenciais de logon de cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="3137f-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="3137f-118">-JobId</span></span>
<span data-ttu-id="3137f-119">Especifica a ID de trabalho do trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="3137f-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="3137f-120">-NumOfJobs</span></span>
<span data-ttu-id="3137f-121">Especifica o número de trabalhos a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3137f-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3137f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3137f-123">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3137f-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3137f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3137f-124">CommonParameters</span></span>
<span data-ttu-id="3137f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3137f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3137f-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3137f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3137f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3137f-127">INPUTS</span></span>

### <span data-ttu-id="3137f-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3137f-128">None</span></span>

## <span data-ttu-id="3137f-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3137f-129">OUTPUTS</span></span>

### <span data-ttu-id="3137f-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3137f-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="3137f-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="3137f-131">NOTES</span></span>

## <span data-ttu-id="3137f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3137f-132">RELATED LINKS</span></span>

[<span data-ttu-id="3137f-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3137f-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="3137f-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3137f-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="3137f-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3137f-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="3137f-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3137f-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


