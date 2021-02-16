---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4c1d991d3236c8e631b2b5c7f0026e91af2f8cf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113179"
---
# <span data-ttu-id="a2cae-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a2cae-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="a2cae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2cae-102">SYNOPSIS</span></span>
<span data-ttu-id="a2cae-103">Aguarda a conclusão ou a falha de um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="a2cae-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="a2cae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2cae-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2cae-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2cae-105">DESCRIPTION</span></span>
<span data-ttu-id="a2cae-106">O cmdlet **Wait-AzHDInsight Job** aguarda a conclusão ou falha de um trabalho HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2cae-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="a2cae-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a2cae-107">EXAMPLES</span></span>

### <span data-ttu-id="a2cae-108">Exemplo 1: Aguardar a conclusão ou a falha de um trabalho</span><span class="sxs-lookup"><span data-stu-id="a2cae-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="a2cae-109">Esse comando aguarda a conclusão ou a falha de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2cae-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="a2cae-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2cae-110">PARAMETERS</span></span>

### <span data-ttu-id="a2cae-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a2cae-111">-ClusterName</span></span>
<span data-ttu-id="a2cae-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a2cae-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a2cae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2cae-113">-DefaultProfile</span></span>
<span data-ttu-id="a2cae-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a2cae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2cae-115">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="a2cae-115">-HttpCredential</span></span>
<span data-ttu-id="a2cae-116">Especifica as credenciais de logon de cluster (HTTP) do cluster.</span><span class="sxs-lookup"><span data-stu-id="a2cae-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="a2cae-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="a2cae-117">-JobId</span></span>
<span data-ttu-id="a2cae-118">Especifica a ID do trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2cae-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="a2cae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2cae-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2cae-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a2cae-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a2cae-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="a2cae-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="a2cae-122">O tempo total para aguardar a conclusão do trabalho em segundos.</span><span class="sxs-lookup"><span data-stu-id="a2cae-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="a2cae-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a2cae-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="a2cae-124">O tempo de espera entre verificações de status do trabalho, em segundos.</span><span class="sxs-lookup"><span data-stu-id="a2cae-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="a2cae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2cae-125">CommonParameters</span></span>
<span data-ttu-id="a2cae-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2cae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2cae-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2cae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2cae-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="a2cae-128">INPUTS</span></span>

### <span data-ttu-id="a2cae-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a2cae-129">System.String</span></span>

## <span data-ttu-id="a2cae-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="a2cae-130">OUTPUTS</span></span>

### <span data-ttu-id="a2cae-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a2cae-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="a2cae-132">Notas</span><span class="sxs-lookup"><span data-stu-id="a2cae-132">NOTES</span></span>

## <span data-ttu-id="a2cae-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2cae-133">RELATED LINKS</span></span>

[<span data-ttu-id="a2cae-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a2cae-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="a2cae-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a2cae-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="a2cae-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a2cae-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


