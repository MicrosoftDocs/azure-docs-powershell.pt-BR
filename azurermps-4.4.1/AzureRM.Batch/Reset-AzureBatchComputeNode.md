---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602882"
---
# <span data-ttu-id="d8902-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8902-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="d8902-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8902-102">SYNOPSIS</span></span>
<span data-ttu-id="d8902-103">Reinstala o sistema operacional no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="d8902-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8902-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8902-104">SYNTAX</span></span>

### <span data-ttu-id="d8902-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8902-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8902-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d8902-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8902-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8902-107">DESCRIPTION</span></span>
<span data-ttu-id="d8902-108">O cmdlet **Reset-AzureBatchComputeNode** reinstala o sistema operacional no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="d8902-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="d8902-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8902-109">EXAMPLES</span></span>

### <span data-ttu-id="d8902-110">Exemplo 1: reimagem de um nó</span><span class="sxs-lookup"><span data-stu-id="d8902-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="d8902-111">Esse comando reimagemia o nó de computação com ID "TVM-3257026573_2-20150813t200938z" no pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="d8902-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="d8902-112">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="d8902-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d8902-113">Exemplo 2: reimagem de todos os nós em um pool</span><span class="sxs-lookup"><span data-stu-id="d8902-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="d8902-114">Esse comando reimagemia cada nó de computação no pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="d8902-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="d8902-115">OS</span><span class="sxs-lookup"><span data-stu-id="d8902-115">PARAMETERS</span></span>

### <span data-ttu-id="d8902-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d8902-116">-BatchContext</span></span>
<span data-ttu-id="d8902-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="d8902-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d8902-118">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="d8902-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d8902-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8902-119">-ComputeNode</span></span>
<span data-ttu-id="d8902-120">Especifica o objeto **PSComputeNode** que representa o nó de computação para fazer a nova imagem.</span><span class="sxs-lookup"><span data-stu-id="d8902-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="d8902-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d8902-121">-Id</span></span>
<span data-ttu-id="d8902-122">Especifica a ID do nó de computação para a nova imagem.</span><span class="sxs-lookup"><span data-stu-id="d8902-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="d8902-123">-Poolid</span><span class="sxs-lookup"><span data-stu-id="d8902-123">-PoolId</span></span>
<span data-ttu-id="d8902-124">Especifica a ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="d8902-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="d8902-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="d8902-125">-ReimageOption</span></span>
<span data-ttu-id="d8902-126">Especifica quando é possível refazer a nova imagem do nó e o que fazer com as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="d8902-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="d8902-127">O padrão é Refila.</span><span class="sxs-lookup"><span data-stu-id="d8902-127">The default is Requeue.</span></span>

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

### <span data-ttu-id="d8902-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8902-128">-DefaultProfile</span></span>
<span data-ttu-id="d8902-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8902-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8902-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8902-130">CommonParameters</span></span>
<span data-ttu-id="d8902-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8902-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8902-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8902-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8902-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8902-133">INPUTS</span></span>

### <span data-ttu-id="d8902-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d8902-134">BatchAccountContext</span></span>
<span data-ttu-id="d8902-135">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d8902-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d8902-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8902-136">PSComputeNode</span></span>
<span data-ttu-id="d8902-137">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d8902-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="d8902-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8902-138">OUTPUTS</span></span>

## <span data-ttu-id="d8902-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8902-139">NOTES</span></span>

## <span data-ttu-id="d8902-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8902-140">RELATED LINKS</span></span>

[<span data-ttu-id="d8902-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8902-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="d8902-142">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8902-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="d8902-143">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="d8902-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


