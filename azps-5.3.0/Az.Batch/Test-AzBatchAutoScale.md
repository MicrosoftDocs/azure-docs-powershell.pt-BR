---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: 6732fb89775cea289bf82a5675a482f94b7f95ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434512"
---
# <span data-ttu-id="dce41-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dce41-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="dce41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dce41-102">SYNOPSIS</span></span>
<span data-ttu-id="dce41-103">Obtém o resultado de uma fórmula de dimensionamento automático em um pool.</span><span class="sxs-lookup"><span data-stu-id="dce41-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="dce41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dce41-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dce41-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dce41-105">DESCRIPTION</span></span>
<span data-ttu-id="dce41-106">O cmdlet **Test-AzBatchAutoScale** Obtém o resultado de uma fórmula de dimensionamento automático no pool especificado.</span><span class="sxs-lookup"><span data-stu-id="dce41-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="dce41-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dce41-107">EXAMPLES</span></span>

### <span data-ttu-id="dce41-108">Exemplo 1: avaliar uma fórmula de autoescala em um pool</span><span class="sxs-lookup"><span data-stu-id="dce41-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="dce41-109">O primeiro comando armazena uma fórmula na variável $Formula para uso no exemplo.</span><span class="sxs-lookup"><span data-stu-id="dce41-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="dce41-110">O segundo comando avalia a fórmula de autoescala no pool que tem a ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="dce41-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="dce41-111">O comando final exibe os **resultados** usando a sintaxe ponto padrão.</span><span class="sxs-lookup"><span data-stu-id="dce41-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="dce41-112">OS</span><span class="sxs-lookup"><span data-stu-id="dce41-112">PARAMETERS</span></span>

### <span data-ttu-id="dce41-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="dce41-113">-AutoScaleFormula</span></span>
<span data-ttu-id="dce41-114">Especifica a fórmula para o número desejado de nós de computação no pool.</span><span class="sxs-lookup"><span data-stu-id="dce41-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce41-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dce41-115">-BatchContext</span></span>
<span data-ttu-id="dce41-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="dce41-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dce41-117">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="dce41-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dce41-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="dce41-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dce41-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="dce41-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dce41-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="dce41-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dce41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce41-121">-DefaultProfile</span></span>
<span data-ttu-id="dce41-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dce41-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dce41-123">-ID</span><span class="sxs-lookup"><span data-stu-id="dce41-123">-Id</span></span>
<span data-ttu-id="dce41-124">Especifica a ID de objeto do pool para o qual testar o dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="dce41-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dce41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce41-125">CommonParameters</span></span>
<span data-ttu-id="dce41-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce41-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dce41-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce41-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dce41-128">INPUTS</span></span>

### <span data-ttu-id="dce41-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dce41-129">System.String</span></span>

### <span data-ttu-id="dce41-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dce41-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dce41-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dce41-131">OUTPUTS</span></span>

### <span data-ttu-id="dce41-132">Microsoft.Azure.Commands.Batch. Modelos. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="dce41-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="dce41-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dce41-133">NOTES</span></span>

## <span data-ttu-id="dce41-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dce41-134">RELATED LINKS</span></span>

[<span data-ttu-id="dce41-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dce41-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="dce41-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="dce41-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="dce41-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dce41-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dce41-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="dce41-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
