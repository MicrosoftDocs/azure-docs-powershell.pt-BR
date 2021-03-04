---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4d4b3ff71142540ff5c5635938d31a16e3fd9603
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888360"
---
# <span data-ttu-id="235e6-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="235e6-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="235e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="235e6-102">SYNOPSIS</span></span>
<span data-ttu-id="235e6-103">Aguarda a conclusão ou falha de um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="235e6-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="235e6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="235e6-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="235e6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="235e6-105">DESCRIPTION</span></span>
<span data-ttu-id="235e6-106">O cmdlet **Wait-AzHDInsightJob** aguarda a conclusão ou falha de um trabalho HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="235e6-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="235e6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="235e6-107">EXAMPLES</span></span>

### <span data-ttu-id="235e6-108">Exemplo 1: Aguarde a conclusão ou falha de um trabalho</span><span class="sxs-lookup"><span data-stu-id="235e6-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="235e6-109">Este comando aguarda a conclusão ou falha de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="235e6-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="235e6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="235e6-110">PARAMETERS</span></span>

### <span data-ttu-id="235e6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="235e6-111">-ClusterName</span></span>
<span data-ttu-id="235e6-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="235e6-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="235e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235e6-113">-DefaultProfile</span></span>
<span data-ttu-id="235e6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="235e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="235e6-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="235e6-115">-HttpCredential</span></span>
<span data-ttu-id="235e6-116">Especifica as credenciais de logon de cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="235e6-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="235e6-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="235e6-117">-JobId</span></span>
<span data-ttu-id="235e6-118">Especifica a ID de trabalho do trabalho.</span><span class="sxs-lookup"><span data-stu-id="235e6-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="235e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="235e6-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="235e6-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="235e6-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="235e6-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="235e6-122">O tempo total para aguardar a conclusão do trabalho, em segundos.</span><span class="sxs-lookup"><span data-stu-id="235e6-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="235e6-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="235e6-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="235e6-124">O tempo de espera entre verificações de status do trabalho, em segundos.</span><span class="sxs-lookup"><span data-stu-id="235e6-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="235e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235e6-125">CommonParameters</span></span>
<span data-ttu-id="235e6-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="235e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235e6-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="235e6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235e6-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="235e6-128">INPUTS</span></span>

### <span data-ttu-id="235e6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="235e6-129">System.String</span></span>

## <span data-ttu-id="235e6-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="235e6-130">OUTPUTS</span></span>

### <span data-ttu-id="235e6-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="235e6-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="235e6-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="235e6-132">NOTES</span></span>

## <span data-ttu-id="235e6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="235e6-133">RELATED LINKS</span></span>

[<span data-ttu-id="235e6-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="235e6-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="235e6-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="235e6-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="235e6-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="235e6-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


