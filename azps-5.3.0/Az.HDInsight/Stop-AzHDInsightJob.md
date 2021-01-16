---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: bff9b9d44d8afcbc315293dc07be3592172f1a4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428331"
---
# <span data-ttu-id="d1bf4-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d1bf4-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="d1bf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bf4-103">Interrompe um trabalho em execução especificado em um cluster.</span><span class="sxs-lookup"><span data-stu-id="d1bf4-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="d1bf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1bf4-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1bf4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="d1bf4-106">O cmdlet **Stop-AzHDInsightJob** interrompe um trabalho em execução especificado em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d1bf4-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d1bf4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="d1bf4-108">Exemplo 1: parar um trabalho no cluster especificado</span><span class="sxs-lookup"><span data-stu-id="d1bf4-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="d1bf4-109">Esse comando interrompe um trabalho no cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d1bf4-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d1bf4-110">OS</span><span class="sxs-lookup"><span data-stu-id="d1bf4-110">PARAMETERS</span></span>

### <span data-ttu-id="d1bf4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d1bf4-111">-ClusterName</span></span>
<span data-ttu-id="d1bf4-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="d1bf4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d1bf4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bf4-113">-DefaultProfile</span></span>
<span data-ttu-id="d1bf4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d1bf4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1bf4-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d1bf4-115">-HttpCredential</span></span>
<span data-ttu-id="d1bf4-116">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="d1bf4-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="d1bf4-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d1bf4-117">-JobId</span></span>
<span data-ttu-id="d1bf4-118">Especifica a ID do trabalho do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d1bf4-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="d1bf4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1bf4-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1bf4-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1bf4-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d1bf4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bf4-121">CommonParameters</span></span>
<span data-ttu-id="d1bf4-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1bf4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1bf4-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1bf4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bf4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1bf4-124">INPUTS</span></span>

### <span data-ttu-id="d1bf4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d1bf4-125">System.String</span></span>

## <span data-ttu-id="d1bf4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1bf4-126">OUTPUTS</span></span>

### <span data-ttu-id="d1bf4-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d1bf4-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d1bf4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1bf4-128">NOTES</span></span>

## <span data-ttu-id="d1bf4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1bf4-129">RELATED LINKS</span></span>

[<span data-ttu-id="d1bf4-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d1bf4-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="d1bf4-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d1bf4-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="d1bf4-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d1bf4-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


