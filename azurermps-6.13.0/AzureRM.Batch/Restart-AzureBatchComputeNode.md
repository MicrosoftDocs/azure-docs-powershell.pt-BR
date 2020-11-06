---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 2b604b1bedf7843d21c9595227ab1ff446028133
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427285"
---
# <span data-ttu-id="48cd1-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="48cd1-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="48cd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="48cd1-103">Reinicializa o nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="48cd1-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48cd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48cd1-104">SYNTAX</span></span>

### <span data-ttu-id="48cd1-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="48cd1-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48cd1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="48cd1-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48cd1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48cd1-107">DESCRIPTION</span></span>
<span data-ttu-id="48cd1-108">O cmdlet **Restart-AzureBatchComputeNode** reinicializa o nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="48cd1-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="48cd1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48cd1-109">EXAMPLES</span></span>

### <span data-ttu-id="48cd1-110">Exemplo 1: reiniciar um nó de computação</span><span class="sxs-lookup"><span data-stu-id="48cd1-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="48cd1-111">Esse comando reinicializa o nó de computação com a ID "TVM-3257026573_2-20150813t200938z" no pool mypool.</span><span class="sxs-lookup"><span data-stu-id="48cd1-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="48cd1-112">Exemplo 2: reiniciar cada nó de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="48cd1-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="48cd1-113">Esse comando reinicializa cada nó de computação no pool de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="48cd1-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="48cd1-114">OS</span><span class="sxs-lookup"><span data-stu-id="48cd1-114">PARAMETERS</span></span>

### <span data-ttu-id="48cd1-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48cd1-115">-BatchContext</span></span>
<span data-ttu-id="48cd1-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="48cd1-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="48cd1-117">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="48cd1-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="48cd1-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="48cd1-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="48cd1-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="48cd1-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="48cd1-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="48cd1-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="48cd1-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="48cd1-121">-ComputeNode</span></span>
<span data-ttu-id="48cd1-122">Especifica o objeto **PSComputeNode** que representa o nó de computação a ser reinicializado.</span><span class="sxs-lookup"><span data-stu-id="48cd1-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="48cd1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cd1-123">-DefaultProfile</span></span>
<span data-ttu-id="48cd1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48cd1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48cd1-125">-ID</span><span class="sxs-lookup"><span data-stu-id="48cd1-125">-Id</span></span>
<span data-ttu-id="48cd1-126">Especifica a ID do nó de computação a ser reinicializado.</span><span class="sxs-lookup"><span data-stu-id="48cd1-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="48cd1-127">-Poolid</span><span class="sxs-lookup"><span data-stu-id="48cd1-127">-PoolId</span></span>
<span data-ttu-id="48cd1-128">Especifica a ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="48cd1-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="48cd1-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="48cd1-129">-RebootOption</span></span>
<span data-ttu-id="48cd1-130">Especifica quando reinicializar o nó e o que fazer com as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="48cd1-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="48cd1-131">O padrão é Refila.</span><span class="sxs-lookup"><span data-stu-id="48cd1-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="48cd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cd1-132">CommonParameters</span></span>
<span data-ttu-id="48cd1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48cd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cd1-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48cd1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cd1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48cd1-135">INPUTS</span></span>

### <span data-ttu-id="48cd1-136">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="48cd1-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="48cd1-137">Parâmetros: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48cd1-137">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="48cd1-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48cd1-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="48cd1-139">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48cd1-139">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="48cd1-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48cd1-140">OUTPUTS</span></span>

### <span data-ttu-id="48cd1-141">System. void</span><span class="sxs-lookup"><span data-stu-id="48cd1-141">System.Void</span></span>

## <span data-ttu-id="48cd1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48cd1-142">NOTES</span></span>

## <span data-ttu-id="48cd1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48cd1-143">RELATED LINKS</span></span>

[<span data-ttu-id="48cd1-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="48cd1-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="48cd1-145">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="48cd1-145">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="48cd1-146">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="48cd1-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


