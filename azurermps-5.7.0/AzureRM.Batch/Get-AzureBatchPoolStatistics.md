---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: e51f10fb7d1043e7a0f9addb9c874224ce952dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427699"
---
# <span data-ttu-id="cfff1-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="cfff1-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="cfff1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfff1-102">SYNOPSIS</span></span>
<span data-ttu-id="cfff1-103">Obtém estatísticas de Resumo de pool para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="cfff1-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfff1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfff1-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfff1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfff1-105">DESCRIPTION</span></span>
<span data-ttu-id="cfff1-106">O cmdlet **Get-AzureBatchPoolStatistics** Obtém as estatísticas de tempo de vida de todos os grupos na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="cfff1-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="cfff1-107">As estatísticas são agregadas em todos os pools que já existiam na conta, desde a criação da conta até a hora da última atualização das estatísticas.</span><span class="sxs-lookup"><span data-stu-id="cfff1-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="cfff1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfff1-108">EXAMPLES</span></span>

### <span data-ttu-id="cfff1-109">Exemplo 1: obter estatísticas de recursos de todos os pools em uma conta</span><span class="sxs-lookup"><span data-stu-id="cfff1-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzureBatchPoolStatistics -BatchContext $Context
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

<span data-ttu-id="cfff1-110">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="cfff1-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="cfff1-111">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="cfff1-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="cfff1-112">O segundo comando obtém as estatísticas de todos os grupos na conta especificada e, em seguida, os armazena no $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="cfff1-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>

<span data-ttu-id="cfff1-113">O comando final exibe a propriedade **ResourceStatistics** de $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="cfff1-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="cfff1-114">OS</span><span class="sxs-lookup"><span data-stu-id="cfff1-114">PARAMETERS</span></span>

### <span data-ttu-id="cfff1-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cfff1-115">-BatchContext</span></span>
<span data-ttu-id="cfff1-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="cfff1-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cfff1-117">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="cfff1-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cfff1-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="cfff1-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cfff1-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="cfff1-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cfff1-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cfff1-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfff1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfff1-121">-DefaultProfile</span></span>
<span data-ttu-id="cfff1-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfff1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfff1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfff1-123">CommonParameters</span></span>
<span data-ttu-id="cfff1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfff1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfff1-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfff1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfff1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfff1-126">INPUTS</span></span>

### <span data-ttu-id="cfff1-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cfff1-127">BatchAccountContext</span></span>
<span data-ttu-id="cfff1-128">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cfff1-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="cfff1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfff1-129">OUTPUTS</span></span>

### <span data-ttu-id="cfff1-130">PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="cfff1-130">PSPoolStatistics</span></span>

## <span data-ttu-id="cfff1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfff1-131">NOTES</span></span>

## <span data-ttu-id="cfff1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfff1-132">RELATED LINKS</span></span>

[<span data-ttu-id="cfff1-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cfff1-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cfff1-134">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="cfff1-134">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="cfff1-135">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="cfff1-135">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


