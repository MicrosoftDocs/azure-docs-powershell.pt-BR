---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: b312a94a971a5ff17a153a8a9b0112e14886fe12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887228"
---
# <span data-ttu-id="adc8d-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="adc8d-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="adc8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="adc8d-103">Começa a resizer um pool.</span><span class="sxs-lookup"><span data-stu-id="adc8d-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="adc8d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="adc8d-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adc8d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="adc8d-105">DESCRIPTION</span></span>
<span data-ttu-id="adc8d-106">O cmdlet **Start-AzBatchPoolResize** inicia uma operação de resize do Lote do Azure em um pool.</span><span class="sxs-lookup"><span data-stu-id="adc8d-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="adc8d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adc8d-107">EXAMPLES</span></span>

### <span data-ttu-id="adc8d-108">Exemplo 1: Resize um pool para 12 nós</span><span class="sxs-lookup"><span data-stu-id="adc8d-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="adc8d-109">Este comando inicia uma operação de resize no pool que tem a ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="adc8d-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="adc8d-110">O destino da operação é 12 nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="adc8d-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="adc8d-111">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="adc8d-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="adc8d-112">Exemplo 2: Resize um pool usando uma opção de localização</span><span class="sxs-lookup"><span data-stu-id="adc8d-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="adc8d-113">Este cmdlet resize um pool para cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="adc8d-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="adc8d-114">O comando obtém o pool que tem a ID ContosoPool06 usando o cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="adc8d-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="adc8d-115">O comando passa esse objeto pool para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="adc8d-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="adc8d-116">O comando inicia uma operação de resize no pool.</span><span class="sxs-lookup"><span data-stu-id="adc8d-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="adc8d-117">O destino é cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="adc8d-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="adc8d-118">O comando especifica o período de tempo de uma hora.</span><span class="sxs-lookup"><span data-stu-id="adc8d-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="adc8d-119">O comando especifica uma opção de localização de acordo de Terminate.</span><span class="sxs-lookup"><span data-stu-id="adc8d-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="adc8d-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="adc8d-120">PARAMETERS</span></span>

### <span data-ttu-id="adc8d-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="adc8d-121">-BatchContext</span></span>
<span data-ttu-id="adc8d-122">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="adc8d-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="adc8d-123">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="adc8d-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="adc8d-124">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="adc8d-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="adc8d-125">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="adc8d-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="adc8d-126">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="adc8d-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="adc8d-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="adc8d-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="adc8d-128">Especifica uma opção de localização para a operação de ressalto que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="adc8d-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="adc8d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc8d-129">-DefaultProfile</span></span>
<span data-ttu-id="adc8d-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="adc8d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adc8d-131">-Id</span><span class="sxs-lookup"><span data-stu-id="adc8d-131">-Id</span></span>
<span data-ttu-id="adc8d-132">Especifica a ID do pool que este cmdlet resize.</span><span class="sxs-lookup"><span data-stu-id="adc8d-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="adc8d-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="adc8d-133">-ResizeTimeout</span></span>
<span data-ttu-id="adc8d-134">Especifica um período de tempo de tempo para a operação de ressarção.</span><span class="sxs-lookup"><span data-stu-id="adc8d-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="adc8d-135">Se o pool não atingir o tamanho de destino até esse momento, a operação de resize será interrompida.</span><span class="sxs-lookup"><span data-stu-id="adc8d-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="adc8d-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="adc8d-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="adc8d-137">O número de nós de computação dedicados de destino.</span><span class="sxs-lookup"><span data-stu-id="adc8d-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="adc8d-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="adc8d-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="adc8d-139">O número de nós de computação de baixa prioridade de destino.</span><span class="sxs-lookup"><span data-stu-id="adc8d-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="adc8d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc8d-140">CommonParameters</span></span>
<span data-ttu-id="adc8d-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc8d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc8d-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adc8d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc8d-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adc8d-143">INPUTS</span></span>

### <span data-ttu-id="adc8d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="adc8d-144">System.String</span></span>

### <span data-ttu-id="adc8d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="adc8d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="adc8d-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="adc8d-146">OUTPUTS</span></span>

### <span data-ttu-id="adc8d-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="adc8d-147">System.Void</span></span>

## <span data-ttu-id="adc8d-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="adc8d-148">NOTES</span></span>

## <span data-ttu-id="adc8d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adc8d-149">RELATED LINKS</span></span>

[<span data-ttu-id="adc8d-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="adc8d-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="adc8d-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="adc8d-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="adc8d-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="adc8d-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="adc8d-153">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="adc8d-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
