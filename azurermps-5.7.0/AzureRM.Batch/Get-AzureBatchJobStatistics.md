---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 80ee6f881731f61b045e448e8a231ae9c971552d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431732"
---
# <span data-ttu-id="beaa3-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="beaa3-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="beaa3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="beaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="beaa3-103">Obtém estatísticas de Resumo de trabalho para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="beaa3-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beaa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="beaa3-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="beaa3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="beaa3-105">DESCRIPTION</span></span>
<span data-ttu-id="beaa3-106">O cmdlet **Get-AzureBatchJobStatistics** tem estatísticas resumidas de tempo de vida para todos os trabalhos em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="beaa3-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="beaa3-107">As estatísticas são agregadas em todos os trabalhos que já existiam na conta, desde a criação da conta até a hora da última atualização das estatísticas.</span><span class="sxs-lookup"><span data-stu-id="beaa3-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="beaa3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="beaa3-108">EXAMPLES</span></span>

### <span data-ttu-id="beaa3-109">Exemplo 1: obter estatísticas resumidas para todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="beaa3-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="beaa3-110">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="beaa3-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="beaa3-111">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="beaa3-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="beaa3-112">O segundo comando obtém as estatísticas resumidas para todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="beaa3-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="beaa3-113">O comando usa o valor $Context do primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="beaa3-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="beaa3-114">OS</span><span class="sxs-lookup"><span data-stu-id="beaa3-114">PARAMETERS</span></span>

### <span data-ttu-id="beaa3-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="beaa3-115">-BatchContext</span></span>
<span data-ttu-id="beaa3-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="beaa3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="beaa3-117">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="beaa3-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="beaa3-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="beaa3-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="beaa3-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="beaa3-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="beaa3-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="beaa3-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="beaa3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaa3-121">-DefaultProfile</span></span>
<span data-ttu-id="beaa3-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="beaa3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beaa3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaa3-123">CommonParameters</span></span>
<span data-ttu-id="beaa3-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beaa3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaa3-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beaa3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaa3-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="beaa3-126">INPUTS</span></span>

### <span data-ttu-id="beaa3-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="beaa3-127">BatchAccountContext</span></span>
<span data-ttu-id="beaa3-128">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="beaa3-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="beaa3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="beaa3-129">OUTPUTS</span></span>

### <span data-ttu-id="beaa3-130">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="beaa3-130">PSJobStatistics</span></span>

## <span data-ttu-id="beaa3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="beaa3-131">NOTES</span></span>

## <span data-ttu-id="beaa3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="beaa3-132">RELATED LINKS</span></span>

[<span data-ttu-id="beaa3-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="beaa3-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="beaa3-134">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="beaa3-134">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="beaa3-135">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="beaa3-135">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


