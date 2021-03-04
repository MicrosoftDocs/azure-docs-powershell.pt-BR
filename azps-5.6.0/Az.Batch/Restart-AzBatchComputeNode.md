---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: daf89fec73ed18cf5b67c4100556d490795708d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889571"
---
# <span data-ttu-id="cfc4d-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cfc4d-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="cfc4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc4d-103">Reinicia o nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="cfc4d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cfc4d-104">SYNTAX</span></span>

### <span data-ttu-id="cfc4d-105">ID (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cfc4d-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfc4d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cfc4d-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfc4d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cfc4d-107">DESCRIPTION</span></span>
<span data-ttu-id="cfc4d-108">O cmdlet **Restart-AzBatchComputeNode** reinicia o nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="cfc4d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfc4d-109">EXAMPLES</span></span>

### <span data-ttu-id="cfc4d-110">Exemplo 1: Reiniciar um nó de computação</span><span class="sxs-lookup"><span data-stu-id="cfc4d-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="cfc4d-111">Este comando reinicia o nó de computação com a ID "tvm-3257026573_2-20150813t200938z" no pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="cfc4d-112">Exemplo 2: Reiniciar cada nó de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="cfc4d-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="cfc4d-113">Esse comando reinicia todos os nós de computação no pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="cfc4d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cfc4d-114">PARAMETERS</span></span>

### <span data-ttu-id="cfc4d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cfc4d-115">-BatchContext</span></span>
<span data-ttu-id="cfc4d-116">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cfc4d-117">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cfc4d-118">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cfc4d-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cfc4d-120">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cfc4d-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="cfc4d-121">-ComputeNode</span></span>
<span data-ttu-id="cfc4d-122">Especifica o **objeto PSComputeNode** que representa o nó de computação a ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="cfc4d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc4d-123">-DefaultProfile</span></span>
<span data-ttu-id="cfc4d-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfc4d-125">-Id</span><span class="sxs-lookup"><span data-stu-id="cfc4d-125">-Id</span></span>
<span data-ttu-id="cfc4d-126">Especifica a ID do nó de computação a ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="cfc4d-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="cfc4d-127">-PoolId</span></span>
<span data-ttu-id="cfc4d-128">Especifica a ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="cfc4d-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="cfc4d-129">-RebootOption</span></span>
<span data-ttu-id="cfc4d-130">Especifica quando reiniciar o nó e o que fazer com as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="cfc4d-131">O padrão é Requeue.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-131">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc4d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc4d-132">CommonParameters</span></span>
<span data-ttu-id="cfc4d-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc4d-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfc4d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc4d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfc4d-135">INPUTS</span></span>

### <span data-ttu-id="cfc4d-136">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="cfc4d-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="cfc4d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cfc4d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cfc4d-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cfc4d-138">OUTPUTS</span></span>

### <span data-ttu-id="cfc4d-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="cfc4d-139">System.Void</span></span>

## <span data-ttu-id="cfc4d-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="cfc4d-140">NOTES</span></span>

## <span data-ttu-id="cfc4d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfc4d-141">RELATED LINKS</span></span>

[<span data-ttu-id="cfc4d-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cfc4d-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="cfc4d-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cfc4d-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="cfc4d-144">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="cfc4d-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
