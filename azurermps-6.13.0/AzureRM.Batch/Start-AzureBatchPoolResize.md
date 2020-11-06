---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/start-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: c635061ac19b0fcc9543222da176324f84bea3a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431400"
---
# <span data-ttu-id="c3245-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c3245-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="c3245-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3245-102">SYNOPSIS</span></span>
<span data-ttu-id="c3245-103">Começa a redimensionar um pool.</span><span class="sxs-lookup"><span data-stu-id="c3245-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3245-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3245-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3245-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3245-105">DESCRIPTION</span></span>
<span data-ttu-id="c3245-106">O cmdlet **Start-AzureBatchPoolResize** inicia uma operação de redimensionamento em lotes do Azure em um pool.</span><span class="sxs-lookup"><span data-stu-id="c3245-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="c3245-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3245-107">EXAMPLES</span></span>

### <span data-ttu-id="c3245-108">Exemplo 1: redimensionar um pool para 12 nós</span><span class="sxs-lookup"><span data-stu-id="c3245-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="c3245-109">Esse comando inicia uma operação de redimensionamento no pool que tem a ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="c3245-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="c3245-110">O destino para a operação é 12 nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="c3245-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="c3245-111">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="c3245-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c3245-112">Exemplo 2: redimensionar um pool usando uma opção de desalocação</span><span class="sxs-lookup"><span data-stu-id="c3245-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="c3245-113">Esse cmdlet redimensiona um pool para cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="c3245-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="c3245-114">O comando obtém o pool com a ID ContosoPool06 usando o cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="c3245-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="c3245-115">O comando passa esse objeto de pool para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3245-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c3245-116">O comando inicia uma operação de redimensionamento no pool.</span><span class="sxs-lookup"><span data-stu-id="c3245-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="c3245-117">O destino é cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="c3245-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="c3245-118">O comando especifica o período de tempo limite de uma hora.</span><span class="sxs-lookup"><span data-stu-id="c3245-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="c3245-119">O comando especifica uma opção de desalocação de Terminate.</span><span class="sxs-lookup"><span data-stu-id="c3245-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="c3245-120">OS</span><span class="sxs-lookup"><span data-stu-id="c3245-120">PARAMETERS</span></span>

### <span data-ttu-id="c3245-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3245-121">-BatchContext</span></span>
<span data-ttu-id="c3245-122">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c3245-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3245-123">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c3245-123">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c3245-124">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="c3245-124">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c3245-125">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="c3245-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c3245-126">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c3245-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c3245-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="c3245-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="c3245-128">Especifica uma opção de desalocação para a operação de redimensionamento que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="c3245-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3245-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3245-129">-DefaultProfile</span></span>
<span data-ttu-id="c3245-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3245-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3245-131">-ID</span><span class="sxs-lookup"><span data-stu-id="c3245-131">-Id</span></span>
<span data-ttu-id="c3245-132">Especifica a ID do pool que esse cmdlet redimensiona.</span><span class="sxs-lookup"><span data-stu-id="c3245-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="c3245-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="c3245-133">-ResizeTimeout</span></span>
<span data-ttu-id="c3245-134">Especifica um período de tempo limite para a operação de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="c3245-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="c3245-135">Se o pool não atingir o tamanho de destino até o momento, a operação de redimensionamento será interrompida.</span><span class="sxs-lookup"><span data-stu-id="c3245-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3245-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="c3245-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="c3245-137">O número de nós de computação dedicados de destino.</span><span class="sxs-lookup"><span data-stu-id="c3245-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3245-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="c3245-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="c3245-139">O número de nós de computação de baixa prioridade de destino.</span><span class="sxs-lookup"><span data-stu-id="c3245-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3245-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3245-140">CommonParameters</span></span>
<span data-ttu-id="c3245-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3245-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3245-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3245-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3245-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3245-143">INPUTS</span></span>

### <span data-ttu-id="c3245-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c3245-144">System.String</span></span>

### <span data-ttu-id="c3245-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3245-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c3245-146">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3245-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c3245-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3245-147">OUTPUTS</span></span>

### <span data-ttu-id="c3245-148">System. void</span><span class="sxs-lookup"><span data-stu-id="c3245-148">System.Void</span></span>

## <span data-ttu-id="c3245-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3245-149">NOTES</span></span>

## <span data-ttu-id="c3245-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3245-150">RELATED LINKS</span></span>

[<span data-ttu-id="c3245-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c3245-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c3245-152">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c3245-152">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c3245-153">Parar-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c3245-153">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="c3245-154">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="c3245-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


