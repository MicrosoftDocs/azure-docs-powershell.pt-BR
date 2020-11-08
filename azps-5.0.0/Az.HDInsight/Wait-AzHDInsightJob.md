---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117824"
---
# <span data-ttu-id="84da9-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84da9-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="84da9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84da9-102">SYNOPSIS</span></span>
<span data-ttu-id="84da9-103">Aguarda a conclusão ou a falha de um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="84da9-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="84da9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84da9-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84da9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84da9-105">DESCRIPTION</span></span>
<span data-ttu-id="84da9-106">O cmdlet **Wait-AzHDInsightJob** aguarda a conclusão ou falha de um trabalho do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="84da9-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="84da9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84da9-107">EXAMPLES</span></span>

### <span data-ttu-id="84da9-108">Exemplo 1: Aguarde a conclusão ou a falha de um trabalho</span><span class="sxs-lookup"><span data-stu-id="84da9-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="84da9-109">Esse comando aguarda a conclusão ou falha de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="84da9-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="84da9-110">OS</span><span class="sxs-lookup"><span data-stu-id="84da9-110">PARAMETERS</span></span>

### <span data-ttu-id="84da9-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="84da9-111">-ClusterName</span></span>
<span data-ttu-id="84da9-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="84da9-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="84da9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84da9-113">-DefaultProfile</span></span>
<span data-ttu-id="84da9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="84da9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84da9-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="84da9-115">-HttpCredential</span></span>
<span data-ttu-id="84da9-116">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="84da9-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="84da9-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="84da9-117">-JobId</span></span>
<span data-ttu-id="84da9-118">Especifica a ID do trabalho do trabalho.</span><span class="sxs-lookup"><span data-stu-id="84da9-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="84da9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84da9-119">-ResourceGroupName</span></span>
<span data-ttu-id="84da9-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84da9-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="84da9-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="84da9-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="84da9-122">O tempo total de espera para a conclusão do trabalho, em segundos.</span><span class="sxs-lookup"><span data-stu-id="84da9-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="84da9-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="84da9-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="84da9-124">O tempo de espera entre as verificações de status do trabalho em segundos.</span><span class="sxs-lookup"><span data-stu-id="84da9-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="84da9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84da9-125">CommonParameters</span></span>
<span data-ttu-id="84da9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84da9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84da9-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84da9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84da9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84da9-128">INPUTS</span></span>

### <span data-ttu-id="84da9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="84da9-129">System.String</span></span>

## <span data-ttu-id="84da9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84da9-130">OUTPUTS</span></span>

### <span data-ttu-id="84da9-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84da9-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="84da9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84da9-132">NOTES</span></span>

## <span data-ttu-id="84da9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84da9-133">RELATED LINKS</span></span>

[<span data-ttu-id="84da9-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84da9-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="84da9-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84da9-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="84da9-136">Parar-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="84da9-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


