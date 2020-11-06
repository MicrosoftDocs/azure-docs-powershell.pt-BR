---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 73c1efe9e25fa02dc06f367eae1d010562eba56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441477"
---
# <span data-ttu-id="8f9f4-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8f9f4-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="8f9f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8f9f4-103">Habilita o dimensionamento automático de um pool.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f9f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f9f4-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f9f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f9f4-105">DESCRIPTION</span></span>
<span data-ttu-id="8f9f4-106">O cmdlet **Enable-AzureBatchAutoScale** permite o dimensionamento automático do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="8f9f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f9f4-107">EXAMPLES</span></span>

### <span data-ttu-id="8f9f4-108">Exemplo 1: habilitar o dimensionamento automático para um pool</span><span class="sxs-lookup"><span data-stu-id="8f9f4-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="8f9f4-109">O primeiro comando define uma fórmula e, em seguida, salva-a na variável $Formula.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="8f9f4-110">O segundo comando habilita o dimensionamento automático no pool chamado mypool usando a fórmula em $Formula.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="8f9f4-111">OS</span><span class="sxs-lookup"><span data-stu-id="8f9f4-111">PARAMETERS</span></span>

### <span data-ttu-id="8f9f4-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="8f9f4-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="8f9f4-113">Especifica a quantidade de tempo (em minutos) decorrida antes que o tamanho do pool seja ajustado automaticamente de acordo com a fórmula de autoescala.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="8f9f4-114">O valor padrão é 15 minutos, e o valor mínimo é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f9f4-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="8f9f4-115">-AutoScaleFormula</span></span>
<span data-ttu-id="8f9f4-116">Especifica a fórmula para o número desejado de nós de computação no pool.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f9f4-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8f9f4-117">-BatchContext</span></span>
<span data-ttu-id="8f9f4-118">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8f9f4-119">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8f9f4-120">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8f9f4-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8f9f4-122">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8f9f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f9f4-123">-DefaultProfile</span></span>
<span data-ttu-id="8f9f4-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f9f4-125">-ID</span><span class="sxs-lookup"><span data-stu-id="8f9f4-125">-Id</span></span>
<span data-ttu-id="8f9f4-126">Especifica a ID de objeto do pool para o qual habilitar o dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="8f9f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f9f4-127">CommonParameters</span></span>
<span data-ttu-id="8f9f4-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f9f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f9f4-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f9f4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f9f4-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f9f4-130">INPUTS</span></span>

### <span data-ttu-id="8f9f4-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8f9f4-131">BatchAccountContext</span></span>
<span data-ttu-id="8f9f4-132">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8f9f4-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8f9f4-133">String</span><span class="sxs-lookup"><span data-stu-id="8f9f4-133">String</span></span>
<span data-ttu-id="8f9f4-134">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8f9f4-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8f9f4-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f9f4-135">OUTPUTS</span></span>

## <span data-ttu-id="8f9f4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f9f4-136">NOTES</span></span>

## <span data-ttu-id="8f9f4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f9f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="8f9f4-138">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8f9f4-138">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="8f9f4-139">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8f9f4-139">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="8f9f4-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="8f9f4-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


