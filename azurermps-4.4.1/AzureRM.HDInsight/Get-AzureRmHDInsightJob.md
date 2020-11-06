---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: e3cfd7978ecd7f8395a0c499d3d194f133960a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603115"
---
# <span data-ttu-id="2bf2c-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2bf2c-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="2bf2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bf2c-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf2c-103">Obtém a lista de trabalhos de um cluster e os lista em ordem cronológica inversa ou recupera um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bf2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bf2c-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bf2c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bf2c-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf2c-106">O cmdlet **Get-AzureRmHDInsightJob** Obtém trabalhos recentes para um cluster do Azure HDInsight especificado em ordem cronológica inversa, com o trabalho mais recente na parte superior da lista.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="2bf2c-107">Obtenha um trabalho específico fornecendo o parâmetro *JobID* .</span><span class="sxs-lookup"><span data-stu-id="2bf2c-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="2bf2c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bf2c-108">EXAMPLES</span></span>

### <span data-ttu-id="2bf2c-109">Exemplo 1: obter trabalhos recentes para um cluster do Azure HDInsight especificado</span><span class="sxs-lookup"><span data-stu-id="2bf2c-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2bf2c-110">Esse comando obtém todos os trabalhos recentes do cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2bf2c-111">OS</span><span class="sxs-lookup"><span data-stu-id="2bf2c-111">PARAMETERS</span></span>

### <span data-ttu-id="2bf2c-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2bf2c-112">-ClusterName</span></span>
<span data-ttu-id="2bf2c-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2bf2c-114">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2bf2c-114">-HttpCredential</span></span>
<span data-ttu-id="2bf2c-115">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-115">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2bf2c-116">-JobId</span><span class="sxs-lookup"><span data-stu-id="2bf2c-116">-JobId</span></span>
<span data-ttu-id="2bf2c-117">Especifica a ID do trabalho a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-117">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="2bf2c-118">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="2bf2c-118">-NumOfJobs</span></span>
<span data-ttu-id="2bf2c-119">Especifica o número de trabalhos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-119">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="2bf2c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf2c-120">-ResourceGroupName</span></span>
<span data-ttu-id="2bf2c-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2bf2c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf2c-122">-DefaultProfile</span></span>
<span data-ttu-id="2bf2c-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bf2c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf2c-124">CommonParameters</span></span>
<span data-ttu-id="2bf2c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf2c-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf2c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf2c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bf2c-127">INPUTS</span></span>

## <span data-ttu-id="2bf2c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bf2c-128">OUTPUTS</span></span>

### <span data-ttu-id="2bf2c-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2bf2c-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2bf2c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bf2c-130">NOTES</span></span>

## <span data-ttu-id="2bf2c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bf2c-131">RELATED LINKS</span></span>

[<span data-ttu-id="2bf2c-132">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2bf2c-132">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="2bf2c-133">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2bf2c-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="2bf2c-134">Parar-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2bf2c-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="2bf2c-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2bf2c-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


