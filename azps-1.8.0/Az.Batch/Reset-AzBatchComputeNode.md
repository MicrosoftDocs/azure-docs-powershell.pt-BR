---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: 530db3d911d0300e1bd587cd953fb357ca810c9c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601832"
---
# <span data-ttu-id="7665b-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7665b-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="7665b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7665b-102">SYNOPSIS</span></span>
<span data-ttu-id="7665b-103">Reinstala o sistema operacional no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="7665b-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="7665b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7665b-104">SYNTAX</span></span>

### <span data-ttu-id="7665b-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="7665b-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7665b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7665b-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7665b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7665b-107">DESCRIPTION</span></span>
<span data-ttu-id="7665b-108">O cmdlet **Reset-AzBatchComputeNode** reinstala o sistema operacional no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="7665b-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="7665b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7665b-109">EXAMPLES</span></span>

### <span data-ttu-id="7665b-110">Exemplo 1: reimagem de um nó</span><span class="sxs-lookup"><span data-stu-id="7665b-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="7665b-111">Esse comando reimagemia o nó de computação com ID "TVM-3257026573_2-20150813t200938z" no pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="7665b-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="7665b-112">Use o cmdlet Get-AzBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="7665b-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7665b-113">Exemplo 2: reimagem de todos os nós em um pool</span><span class="sxs-lookup"><span data-stu-id="7665b-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="7665b-114">Esse comando reimagemia cada nó de computação no pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="7665b-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="7665b-115">OS</span><span class="sxs-lookup"><span data-stu-id="7665b-115">PARAMETERS</span></span>

### <span data-ttu-id="7665b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7665b-116">-BatchContext</span></span>
<span data-ttu-id="7665b-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="7665b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7665b-118">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="7665b-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7665b-119">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="7665b-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7665b-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="7665b-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7665b-121">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7665b-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7665b-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7665b-122">-ComputeNode</span></span>
<span data-ttu-id="7665b-123">Especifica o objeto **PSComputeNode** que representa o nó de computação para fazer a nova imagem.</span><span class="sxs-lookup"><span data-stu-id="7665b-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="7665b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7665b-124">-DefaultProfile</span></span>
<span data-ttu-id="7665b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7665b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7665b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="7665b-126">-Id</span></span>
<span data-ttu-id="7665b-127">Especifica a ID do nó de computação para a nova imagem.</span><span class="sxs-lookup"><span data-stu-id="7665b-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="7665b-128">-Poolid</span><span class="sxs-lookup"><span data-stu-id="7665b-128">-PoolId</span></span>
<span data-ttu-id="7665b-129">Especifica a ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="7665b-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="7665b-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="7665b-130">-ReimageOption</span></span>
<span data-ttu-id="7665b-131">Especifica quando é possível refazer a nova imagem do nó e o que fazer com as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="7665b-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="7665b-132">O padrão é Refila.</span><span class="sxs-lookup"><span data-stu-id="7665b-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="7665b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7665b-133">CommonParameters</span></span>
<span data-ttu-id="7665b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7665b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7665b-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7665b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7665b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7665b-136">INPUTS</span></span>

### <span data-ttu-id="7665b-137">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="7665b-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="7665b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7665b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7665b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7665b-139">OUTPUTS</span></span>

### <span data-ttu-id="7665b-140">System. void</span><span class="sxs-lookup"><span data-stu-id="7665b-140">System.Void</span></span>

## <span data-ttu-id="7665b-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7665b-141">NOTES</span></span>

## <span data-ttu-id="7665b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7665b-142">RELATED LINKS</span></span>

[<span data-ttu-id="7665b-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7665b-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="7665b-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7665b-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="7665b-145">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="7665b-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


