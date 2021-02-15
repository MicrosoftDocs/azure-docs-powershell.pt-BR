---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112227"
---
# <span data-ttu-id="feb0b-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="feb0b-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="feb0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="feb0b-102">SYNOPSIS</span></span>
<span data-ttu-id="feb0b-103">Começa a reorganizar um pool.</span><span class="sxs-lookup"><span data-stu-id="feb0b-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="feb0b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="feb0b-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb0b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="feb0b-105">DESCRIPTION</span></span>
<span data-ttu-id="feb0b-106">O cmdlet **Start-AzBatchPoolResize** inicia uma operação de resize do Azure Batch em um pool.</span><span class="sxs-lookup"><span data-stu-id="feb0b-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="feb0b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="feb0b-107">EXAMPLES</span></span>

### <span data-ttu-id="feb0b-108">Exemplo 1: Reorganizar um pool para 12 nós</span><span class="sxs-lookup"><span data-stu-id="feb0b-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="feb0b-109">Esse comando inicia uma operação de resize no pool que tem a ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="feb0b-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="feb0b-110">O destino da operação é 12 nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="feb0b-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="feb0b-111">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="feb0b-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="feb0b-112">Exemplo 2: Reorganizar um pool usando uma opção de localização de negócios</span><span class="sxs-lookup"><span data-stu-id="feb0b-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="feb0b-113">Este cmdlet resize um pool para cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="feb0b-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="feb0b-114">O comando obtém o pool que tem a ID ContosoPool06 usando o cmdlet Get-AzBatchPool usuário.</span><span class="sxs-lookup"><span data-stu-id="feb0b-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="feb0b-115">O comando passa esse objeto de pool para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="feb0b-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="feb0b-116">O comando inicia uma operação de resize no pool.</span><span class="sxs-lookup"><span data-stu-id="feb0b-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="feb0b-117">O destino é cinco nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="feb0b-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="feb0b-118">O comando especifica o período de tempo de uma hora.</span><span class="sxs-lookup"><span data-stu-id="feb0b-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="feb0b-119">O comando especifica uma opção de localização de Terminação.</span><span class="sxs-lookup"><span data-stu-id="feb0b-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="feb0b-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="feb0b-120">PARAMETERS</span></span>

### <span data-ttu-id="feb0b-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="feb0b-121">-BatchContext</span></span>
<span data-ttu-id="feb0b-122">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="feb0b-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="feb0b-123">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="feb0b-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="feb0b-124">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="feb0b-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="feb0b-125">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="feb0b-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="feb0b-126">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="feb0b-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="feb0b-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="feb0b-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="feb0b-128">Especifica uma opção de localização para a operação de reizing que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="feb0b-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="feb0b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb0b-129">-DefaultProfile</span></span>
<span data-ttu-id="feb0b-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="feb0b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feb0b-131">-ID</span><span class="sxs-lookup"><span data-stu-id="feb0b-131">-Id</span></span>
<span data-ttu-id="feb0b-132">Especifica a ID do pool que este cmdlet resize.</span><span class="sxs-lookup"><span data-stu-id="feb0b-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="feb0b-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="feb0b-133">-ResizeTimeout</span></span>
<span data-ttu-id="feb0b-134">Especifica um período de tempo para a operação de resizing.</span><span class="sxs-lookup"><span data-stu-id="feb0b-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="feb0b-135">Se o pool não atingir o tamanho de destino até esse momento, a operação de resize para.</span><span class="sxs-lookup"><span data-stu-id="feb0b-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="feb0b-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="feb0b-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="feb0b-137">O número de nós de computação dedicados de destino.</span><span class="sxs-lookup"><span data-stu-id="feb0b-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="feb0b-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="feb0b-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="feb0b-139">O número de nós de computação de baixa prioridade de destino.</span><span class="sxs-lookup"><span data-stu-id="feb0b-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="feb0b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb0b-140">CommonParameters</span></span>
<span data-ttu-id="feb0b-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb0b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb0b-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="feb0b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb0b-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="feb0b-143">INPUTS</span></span>

### <span data-ttu-id="feb0b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="feb0b-144">System.String</span></span>

### <span data-ttu-id="feb0b-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="feb0b-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="feb0b-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="feb0b-146">OUTPUTS</span></span>

### <span data-ttu-id="feb0b-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="feb0b-147">System.Void</span></span>

## <span data-ttu-id="feb0b-148">Notas</span><span class="sxs-lookup"><span data-stu-id="feb0b-148">NOTES</span></span>

## <span data-ttu-id="feb0b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="feb0b-149">RELATED LINKS</span></span>

[<span data-ttu-id="feb0b-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="feb0b-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="feb0b-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="feb0b-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="feb0b-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="feb0b-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="feb0b-153">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="feb0b-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
