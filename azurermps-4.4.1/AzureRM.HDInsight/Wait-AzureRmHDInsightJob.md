---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: 6e19594cfcd79c6be82373af6245ea2154296b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611118"
---
# <span data-ttu-id="2f174-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2f174-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="2f174-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f174-102">SYNOPSIS</span></span>
<span data-ttu-id="2f174-103">Aguarda a conclusão ou a falha de um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="2f174-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f174-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f174-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f174-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f174-105">DESCRIPTION</span></span>
<span data-ttu-id="2f174-106">O cmdlet **Wait-AzureRmHDInsightJob** aguarda a conclusão ou falha de um trabalho do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2f174-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="2f174-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f174-107">EXAMPLES</span></span>

### <span data-ttu-id="2f174-108">Exemplo 1: Aguarde a conclusão ou a falha de um trabalho</span><span class="sxs-lookup"><span data-stu-id="2f174-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2f174-109">Esse comando aguarda a conclusão ou falha de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="2f174-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="2f174-110">OS</span><span class="sxs-lookup"><span data-stu-id="2f174-110">PARAMETERS</span></span>

### <span data-ttu-id="2f174-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2f174-111">-ClusterName</span></span>
<span data-ttu-id="2f174-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2f174-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2f174-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2f174-113">-HttpCredential</span></span>
<span data-ttu-id="2f174-114">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="2f174-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2f174-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="2f174-115">-JobId</span></span>
<span data-ttu-id="2f174-116">Especifica a ID do trabalho do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2f174-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="2f174-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f174-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f174-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f174-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2f174-119">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="2f174-119">-TimeoutInSeconds</span></span>
<span data-ttu-id="2f174-120">O tempo total de espera para a conclusão do trabalho, em segundos.</span><span class="sxs-lookup"><span data-stu-id="2f174-120">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="2f174-121">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2f174-121">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="2f174-122">O tempo de espera entre as verificações de status do trabalho em segundos.</span><span class="sxs-lookup"><span data-stu-id="2f174-122">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="2f174-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f174-123">-DefaultProfile</span></span>
<span data-ttu-id="2f174-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f174-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f174-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f174-125">CommonParameters</span></span>
<span data-ttu-id="2f174-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f174-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f174-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f174-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f174-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f174-128">INPUTS</span></span>

### <span data-ttu-id="2f174-129">String</span><span class="sxs-lookup"><span data-stu-id="2f174-129">String</span></span>
<span data-ttu-id="2f174-130">O parâmetro ' JobId ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2f174-130">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2f174-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f174-131">OUTPUTS</span></span>

### <span data-ttu-id="2f174-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2f174-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2f174-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f174-133">NOTES</span></span>

## <span data-ttu-id="2f174-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f174-134">RELATED LINKS</span></span>

[<span data-ttu-id="2f174-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2f174-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="2f174-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2f174-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="2f174-137">Parar-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2f174-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


