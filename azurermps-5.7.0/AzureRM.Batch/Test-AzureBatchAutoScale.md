---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 4258c5d83b15c2cecb6e2cd4e3edc216efec7a97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426815"
---
# <span data-ttu-id="c4eab-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c4eab-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="c4eab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4eab-102">SYNOPSIS</span></span>
<span data-ttu-id="c4eab-103">Obtém o resultado de uma fórmula de dimensionamento automático em um pool.</span><span class="sxs-lookup"><span data-stu-id="c4eab-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4eab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4eab-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4eab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4eab-105">DESCRIPTION</span></span>
<span data-ttu-id="c4eab-106">O cmdlet **Test-AzureBatchAutoScale** Obtém o resultado de uma fórmula de dimensionamento automático no pool especificado.</span><span class="sxs-lookup"><span data-stu-id="c4eab-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="c4eab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4eab-107">EXAMPLES</span></span>

### <span data-ttu-id="c4eab-108">Exemplo 1: avaliar uma fórmula de autoescala em um pool</span><span class="sxs-lookup"><span data-stu-id="c4eab-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="c4eab-109">O primeiro comando armazena uma fórmula na variável $Formula para uso no exemplo.</span><span class="sxs-lookup"><span data-stu-id="c4eab-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="c4eab-110">O segundo comando avalia a fórmula de autoescala no pool que tem a ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="c4eab-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="c4eab-111">O comando final exibe os **resultados** usando a sintaxe ponto padrão.</span><span class="sxs-lookup"><span data-stu-id="c4eab-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="c4eab-112">OS</span><span class="sxs-lookup"><span data-stu-id="c4eab-112">PARAMETERS</span></span>

### <span data-ttu-id="c4eab-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="c4eab-113">-AutoScaleFormula</span></span>
<span data-ttu-id="c4eab-114">Especifica a fórmula para o número desejado de nós de computação no pool.</span><span class="sxs-lookup"><span data-stu-id="c4eab-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4eab-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c4eab-115">-BatchContext</span></span>
<span data-ttu-id="c4eab-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c4eab-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c4eab-117">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c4eab-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c4eab-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="c4eab-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c4eab-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="c4eab-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c4eab-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c4eab-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c4eab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4eab-121">-DefaultProfile</span></span>
<span data-ttu-id="c4eab-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4eab-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4eab-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c4eab-123">-Id</span></span>
<span data-ttu-id="c4eab-124">Especifica a ID de objeto do pool para o qual testar o dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="c4eab-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4eab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4eab-125">CommonParameters</span></span>
<span data-ttu-id="c4eab-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4eab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4eab-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4eab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4eab-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4eab-128">INPUTS</span></span>

### <span data-ttu-id="c4eab-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c4eab-129">BatchAccountContext</span></span>
<span data-ttu-id="c4eab-130">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c4eab-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c4eab-131">String</span><span class="sxs-lookup"><span data-stu-id="c4eab-131">String</span></span>
<span data-ttu-id="c4eab-132">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c4eab-132">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c4eab-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4eab-133">OUTPUTS</span></span>

### <span data-ttu-id="c4eab-134">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="c4eab-134">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="c4eab-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4eab-135">NOTES</span></span>

## <span data-ttu-id="c4eab-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4eab-136">RELATED LINKS</span></span>

[<span data-ttu-id="c4eab-137">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c4eab-137">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="c4eab-138">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c4eab-138">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="c4eab-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c4eab-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c4eab-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="c4eab-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

