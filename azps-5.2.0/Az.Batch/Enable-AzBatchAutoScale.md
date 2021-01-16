---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262699"
---
# <span data-ttu-id="66ef1-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="66ef1-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="66ef1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="66ef1-103">Habilita o dimensionamento automático de um pool.</span><span class="sxs-lookup"><span data-stu-id="66ef1-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="66ef1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66ef1-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66ef1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="66ef1-106">O cmdlet **Enable-AzBatchAutoScale** permite o dimensionamento automático do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="66ef1-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="66ef1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66ef1-107">EXAMPLES</span></span>

### <span data-ttu-id="66ef1-108">Exemplo 1: habilitar o dimensionamento automático para um pool</span><span class="sxs-lookup"><span data-stu-id="66ef1-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="66ef1-109">O primeiro comando define uma fórmula e, em seguida, salva-a na variável $Formula.</span><span class="sxs-lookup"><span data-stu-id="66ef1-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="66ef1-110">O segundo comando habilita o dimensionamento automático no pool chamado mypool usando a fórmula em $Formula.</span><span class="sxs-lookup"><span data-stu-id="66ef1-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="66ef1-111">OS</span><span class="sxs-lookup"><span data-stu-id="66ef1-111">PARAMETERS</span></span>

### <span data-ttu-id="66ef1-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="66ef1-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="66ef1-113">Especifica a quantidade de tempo (em minutos) decorrida antes que o tamanho do pool seja ajustado automaticamente de acordo com a fórmula de autoescala.</span><span class="sxs-lookup"><span data-stu-id="66ef1-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="66ef1-114">O valor padrão é 15 minutos, e o valor mínimo é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="66ef1-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ef1-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="66ef1-115">-AutoScaleFormula</span></span>
<span data-ttu-id="66ef1-116">Especifica a fórmula para o número desejado de nós de computação no pool.</span><span class="sxs-lookup"><span data-stu-id="66ef1-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ef1-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="66ef1-117">-BatchContext</span></span>
<span data-ttu-id="66ef1-118">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="66ef1-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="66ef1-119">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="66ef1-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="66ef1-120">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="66ef1-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="66ef1-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="66ef1-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="66ef1-122">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="66ef1-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="66ef1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ef1-123">-DefaultProfile</span></span>
<span data-ttu-id="66ef1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66ef1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66ef1-125">-ID</span><span class="sxs-lookup"><span data-stu-id="66ef1-125">-Id</span></span>
<span data-ttu-id="66ef1-126">Especifica a ID de objeto do pool para o qual habilitar o dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="66ef1-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="66ef1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ef1-127">CommonParameters</span></span>
<span data-ttu-id="66ef1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66ef1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ef1-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66ef1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ef1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66ef1-130">INPUTS</span></span>

### <span data-ttu-id="66ef1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="66ef1-131">System.String</span></span>

### <span data-ttu-id="66ef1-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="66ef1-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="66ef1-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66ef1-133">OUTPUTS</span></span>

### <span data-ttu-id="66ef1-134">System. void</span><span class="sxs-lookup"><span data-stu-id="66ef1-134">System.Void</span></span>

## <span data-ttu-id="66ef1-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66ef1-135">NOTES</span></span>

## <span data-ttu-id="66ef1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66ef1-136">RELATED LINKS</span></span>

[<span data-ttu-id="66ef1-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="66ef1-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="66ef1-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="66ef1-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="66ef1-139">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="66ef1-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
