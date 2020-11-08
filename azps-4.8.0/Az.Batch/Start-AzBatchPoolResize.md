---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110620"
---
# <span data-ttu-id="df209-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="df209-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="df209-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df209-102">SYNOPSIS</span></span>
<span data-ttu-id="df209-103">Começa a redimensionar um pool.</span><span class="sxs-lookup"><span data-stu-id="df209-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="df209-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df209-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df209-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df209-105">DESCRIPTION</span></span>
<span data-ttu-id="df209-106">O cmdlet **Start-AzBatchPoolResize** inicia uma operação de redimensionamento em lotes do Azure em um pool.</span><span class="sxs-lookup"><span data-stu-id="df209-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="df209-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df209-107">EXAMPLES</span></span>

### <span data-ttu-id="df209-108">Exemplo 1: redimensionar um pool para 12 nós</span><span class="sxs-lookup"><span data-stu-id="df209-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="df209-109">Esse comando inicia uma operação de redimensionamento no pool que tem a ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="df209-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="df209-110">O destino para a operação é 12 nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="df209-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="df209-111">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="df209-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="df209-112">Exemplo 2: redimensionar um pool usando uma opção de desalocação</span><span class="sxs-lookup"><span data-stu-id="df209-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="df209-113">Esse cmdlet redimensiona um pool para cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="df209-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="df209-114">O comando obtém o pool com a ID ContosoPool06 usando o cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="df209-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="df209-115">O comando passa esse objeto de pool para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="df209-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="df209-116">O comando inicia uma operação de redimensionamento no pool.</span><span class="sxs-lookup"><span data-stu-id="df209-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="df209-117">O destino é cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="df209-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="df209-118">O comando especifica o período de tempo limite de uma hora.</span><span class="sxs-lookup"><span data-stu-id="df209-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="df209-119">O comando especifica uma opção de desalocação de Terminate.</span><span class="sxs-lookup"><span data-stu-id="df209-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="df209-120">OS</span><span class="sxs-lookup"><span data-stu-id="df209-120">PARAMETERS</span></span>

### <span data-ttu-id="df209-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="df209-121">-BatchContext</span></span>
<span data-ttu-id="df209-122">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="df209-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="df209-123">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="df209-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="df209-124">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="df209-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="df209-125">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="df209-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="df209-126">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="df209-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="df209-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="df209-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="df209-128">Especifica uma opção de desalocação para a operação de redimensionamento que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="df209-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="df209-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df209-129">-DefaultProfile</span></span>
<span data-ttu-id="df209-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df209-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df209-131">-ID</span><span class="sxs-lookup"><span data-stu-id="df209-131">-Id</span></span>
<span data-ttu-id="df209-132">Especifica a ID do pool que esse cmdlet redimensiona.</span><span class="sxs-lookup"><span data-stu-id="df209-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="df209-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="df209-133">-ResizeTimeout</span></span>
<span data-ttu-id="df209-134">Especifica um período de tempo limite para a operação de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="df209-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="df209-135">Se o pool não atingir o tamanho de destino até o momento, a operação de redimensionamento será interrompida.</span><span class="sxs-lookup"><span data-stu-id="df209-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="df209-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="df209-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="df209-137">O número de nós de computação dedicados de destino.</span><span class="sxs-lookup"><span data-stu-id="df209-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="df209-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="df209-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="df209-139">O número de nós de computação de baixa prioridade de destino.</span><span class="sxs-lookup"><span data-stu-id="df209-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="df209-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df209-140">CommonParameters</span></span>
<span data-ttu-id="df209-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df209-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df209-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df209-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df209-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df209-143">INPUTS</span></span>

### <span data-ttu-id="df209-144">System. String</span><span class="sxs-lookup"><span data-stu-id="df209-144">System.String</span></span>

### <span data-ttu-id="df209-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="df209-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="df209-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df209-146">OUTPUTS</span></span>

### <span data-ttu-id="df209-147">System. void</span><span class="sxs-lookup"><span data-stu-id="df209-147">System.Void</span></span>

## <span data-ttu-id="df209-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df209-148">NOTES</span></span>

## <span data-ttu-id="df209-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df209-149">RELATED LINKS</span></span>

[<span data-ttu-id="df209-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="df209-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="df209-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="df209-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="df209-152">Parar-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="df209-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="df209-153">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="df209-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
