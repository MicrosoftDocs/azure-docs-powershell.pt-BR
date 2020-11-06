---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 7247a4f5e23bc4f0f3c520f909cec221ee03e1ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429541"
---
# <span data-ttu-id="2ca4d-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ca4d-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="2ca4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ca4d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca4d-103">Interrompe um trabalho em execução especificado em um cluster.</span><span class="sxs-lookup"><span data-stu-id="2ca4d-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ca4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ca4d-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ca4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ca4d-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca4d-106">O cmdlet **Stop-AzureRmHDInsightJob** interrompe um trabalho em execução especificado em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2ca4d-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2ca4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ca4d-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca4d-108">Exemplo 1: parar um trabalho no cluster especificado</span><span class="sxs-lookup"><span data-stu-id="2ca4d-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="2ca4d-109">Esse comando interrompe um trabalho no cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2ca4d-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2ca4d-110">OS</span><span class="sxs-lookup"><span data-stu-id="2ca4d-110">PARAMETERS</span></span>

### <span data-ttu-id="2ca4d-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2ca4d-111">-ClusterName</span></span>
<span data-ttu-id="2ca4d-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2ca4d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2ca4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca4d-113">-DefaultProfile</span></span>
<span data-ttu-id="2ca4d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2ca4d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ca4d-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2ca4d-115">-HttpCredential</span></span>
<span data-ttu-id="2ca4d-116">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="2ca4d-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2ca4d-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="2ca4d-117">-JobId</span></span>
<span data-ttu-id="2ca4d-118">Especifica a ID do trabalho do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2ca4d-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="2ca4d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca4d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ca4d-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ca4d-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2ca4d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca4d-121">CommonParameters</span></span>
<span data-ttu-id="2ca4d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ca4d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca4d-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca4d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca4d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ca4d-124">INPUTS</span></span>

### <span data-ttu-id="2ca4d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2ca4d-125">System.String</span></span>
<span data-ttu-id="2ca4d-126">Parâmetros: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ca4d-126">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="2ca4d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ca4d-127">OUTPUTS</span></span>

### <span data-ttu-id="2ca4d-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ca4d-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2ca4d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ca4d-129">NOTES</span></span>

## <span data-ttu-id="2ca4d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ca4d-130">RELATED LINKS</span></span>

[<span data-ttu-id="2ca4d-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ca4d-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="2ca4d-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ca4d-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="2ca4d-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ca4d-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


