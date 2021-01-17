---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: 11532648242438983ae1bc9222dbc3ac12fa05e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430504"
---
# <span data-ttu-id="bd552-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="bd552-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="bd552-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd552-102">SYNOPSIS</span></span>
<span data-ttu-id="bd552-103">Obtém estatísticas de Resumo de trabalho para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="bd552-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="bd552-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd552-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd552-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd552-105">DESCRIPTION</span></span>
<span data-ttu-id="bd552-106">O cmdlet **Get-AzBatchJobStatistic** tem estatísticas resumidas de tempo de vida para todos os trabalhos em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd552-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="bd552-107">As estatísticas são agregadas em todos os trabalhos que já existiam na conta, desde a criação da conta até a hora da última atualização das estatísticas.</span><span class="sxs-lookup"><span data-stu-id="bd552-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="bd552-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd552-108">EXAMPLES</span></span>

### <span data-ttu-id="bd552-109">Exemplo 1: obter estatísticas resumidas para todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="bd552-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
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

<span data-ttu-id="bd552-110">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="bd552-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="bd552-111">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="bd552-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="bd552-112">O segundo comando obtém as estatísticas resumidas para todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="bd552-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="bd552-113">O comando usa o valor $Context do primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="bd552-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="bd552-114">OS</span><span class="sxs-lookup"><span data-stu-id="bd552-114">PARAMETERS</span></span>

### <span data-ttu-id="bd552-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bd552-115">-BatchContext</span></span>
<span data-ttu-id="bd552-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="bd552-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bd552-117">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="bd552-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bd552-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="bd552-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bd552-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="bd552-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bd552-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bd552-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bd552-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd552-121">-DefaultProfile</span></span>
<span data-ttu-id="bd552-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd552-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd552-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd552-123">CommonParameters</span></span>
<span data-ttu-id="bd552-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd552-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd552-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd552-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd552-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd552-126">INPUTS</span></span>

### <span data-ttu-id="bd552-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bd552-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bd552-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd552-128">OUTPUTS</span></span>

### <span data-ttu-id="bd552-129">Microsoft.Azure.Commands.Batch. Modelos. PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="bd552-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="bd552-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd552-130">NOTES</span></span>

## <span data-ttu-id="bd552-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd552-131">RELATED LINKS</span></span>

[<span data-ttu-id="bd552-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bd552-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bd552-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="bd552-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="bd552-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="bd552-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
