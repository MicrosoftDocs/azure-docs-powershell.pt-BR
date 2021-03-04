---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 48a01d04609bfcb3d0bf70c7e454316ee3095dcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885492"
---
# <span data-ttu-id="ea00f-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="ea00f-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="ea00f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea00f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea00f-103">Obtém estatísticas de resumo de pool para uma conta batch.</span><span class="sxs-lookup"><span data-stu-id="ea00f-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="ea00f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ea00f-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea00f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ea00f-105">DESCRIPTION</span></span>
<span data-ttu-id="ea00f-106">O cmdlet **Get-AzBatchPoolStatistic** obtém as estatísticas de vida útil de todos os pools na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="ea00f-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="ea00f-107">As estatísticas são agregadas em todos os pools que já existiram na conta, desde a criação da conta até a última atualização das estatísticas.</span><span class="sxs-lookup"><span data-stu-id="ea00f-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="ea00f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea00f-108">EXAMPLES</span></span>

### <span data-ttu-id="ea00f-109">Exemplo 1: obter estatísticas de recursos de todos os pools em uma conta</span><span class="sxs-lookup"><span data-stu-id="ea00f-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="ea00f-110">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lote chamada ContosoBatchAccount usando **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="ea00f-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="ea00f-111">O comando armazena essa referência de objeto na $Context variável.</span><span class="sxs-lookup"><span data-stu-id="ea00f-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="ea00f-112">O segundo comando obtém as estatísticas de todos os pools na conta especificada e os armazena no $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="ea00f-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="ea00f-113">O comando final exibe a **propriedade ResourceStatistics** do $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="ea00f-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="ea00f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ea00f-114">PARAMETERS</span></span>

### <span data-ttu-id="ea00f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ea00f-115">-BatchContext</span></span>
<span data-ttu-id="ea00f-116">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="ea00f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ea00f-117">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="ea00f-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ea00f-118">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="ea00f-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ea00f-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="ea00f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ea00f-120">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ea00f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea00f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea00f-121">-DefaultProfile</span></span>
<span data-ttu-id="ea00f-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ea00f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea00f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea00f-123">CommonParameters</span></span>
<span data-ttu-id="ea00f-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea00f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea00f-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea00f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea00f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea00f-126">INPUTS</span></span>

### <span data-ttu-id="ea00f-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ea00f-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ea00f-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ea00f-128">OUTPUTS</span></span>

### <span data-ttu-id="ea00f-129">Microsoft.Azure.Commands.Batch. Models.PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="ea00f-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="ea00f-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="ea00f-130">NOTES</span></span>

## <span data-ttu-id="ea00f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea00f-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea00f-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ea00f-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ea00f-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="ea00f-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="ea00f-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="ea00f-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)
