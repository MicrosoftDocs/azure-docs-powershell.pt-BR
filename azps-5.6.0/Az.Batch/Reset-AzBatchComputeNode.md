---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: c6ad25e5c6ba327ddcd5b4877cbac39937ec4feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889573"
---
# <span data-ttu-id="46d7a-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="46d7a-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="46d7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="46d7a-103">Reinstala o sistema operacional no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="46d7a-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="46d7a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="46d7a-104">SYNTAX</span></span>

### <span data-ttu-id="46d7a-105">ID (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46d7a-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46d7a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="46d7a-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46d7a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="46d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="46d7a-108">O cmdlet **Reset-AzBatchComputeNode** reinstala o sistema operacional no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="46d7a-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="46d7a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46d7a-109">EXAMPLES</span></span>

### <span data-ttu-id="46d7a-110">Exemplo 1: Reimage um nó</span><span class="sxs-lookup"><span data-stu-id="46d7a-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="46d7a-111">Este comando reimaima o nó de computação com a ID "tvm-3257026573_2-20150813t200938z" no pool chamado MyPool.</span><span class="sxs-lookup"><span data-stu-id="46d7a-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="46d7a-112">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="46d7a-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="46d7a-113">Exemplo 2: Reimage todos os nós em um pool</span><span class="sxs-lookup"><span data-stu-id="46d7a-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="46d7a-114">Esse comando reimaja cada nó de computação no pool chamado MyPool.</span><span class="sxs-lookup"><span data-stu-id="46d7a-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="46d7a-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="46d7a-115">PARAMETERS</span></span>

### <span data-ttu-id="46d7a-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="46d7a-116">-BatchContext</span></span>
<span data-ttu-id="46d7a-117">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="46d7a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="46d7a-118">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="46d7a-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="46d7a-119">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="46d7a-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="46d7a-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="46d7a-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="46d7a-121">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="46d7a-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="46d7a-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="46d7a-122">-ComputeNode</span></span>
<span data-ttu-id="46d7a-123">Especifica o **objeto PSComputeNode** que representa o nó de computação para reimage.</span><span class="sxs-lookup"><span data-stu-id="46d7a-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d7a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d7a-124">-DefaultProfile</span></span>
<span data-ttu-id="46d7a-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="46d7a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46d7a-126">-Id</span><span class="sxs-lookup"><span data-stu-id="46d7a-126">-Id</span></span>
<span data-ttu-id="46d7a-127">Especifica a ID do nó de computação a ser reimage.</span><span class="sxs-lookup"><span data-stu-id="46d7a-127">Specifies the ID of the compute node to reimage.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d7a-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="46d7a-128">-PoolId</span></span>
<span data-ttu-id="46d7a-129">Especifica a ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="46d7a-129">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d7a-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="46d7a-130">-ReimageOption</span></span>
<span data-ttu-id="46d7a-131">Especifica quando reimage o nó e o que fazer com as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="46d7a-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="46d7a-132">O padrão é Requeue.</span><span class="sxs-lookup"><span data-stu-id="46d7a-132">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d7a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d7a-133">CommonParameters</span></span>
<span data-ttu-id="46d7a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d7a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d7a-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46d7a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d7a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46d7a-136">INPUTS</span></span>

### <span data-ttu-id="46d7a-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="46d7a-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="46d7a-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="46d7a-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="46d7a-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="46d7a-139">OUTPUTS</span></span>

### <span data-ttu-id="46d7a-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="46d7a-140">System.Void</span></span>

## <span data-ttu-id="46d7a-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="46d7a-141">NOTES</span></span>

## <span data-ttu-id="46d7a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46d7a-142">RELATED LINKS</span></span>

[<span data-ttu-id="46d7a-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="46d7a-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="46d7a-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="46d7a-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="46d7a-145">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="46d7a-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
