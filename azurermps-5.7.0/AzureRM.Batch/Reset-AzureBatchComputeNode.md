---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 8e1fd78c51a6a41f1f455fc3672a0c340309f76c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610664"
---
# <span data-ttu-id="95654-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="95654-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="95654-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95654-102">SYNOPSIS</span></span>
<span data-ttu-id="95654-103">Reinstala o sistema operacional no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="95654-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95654-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95654-104">SYNTAX</span></span>

### <span data-ttu-id="95654-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="95654-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95654-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="95654-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95654-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95654-107">DESCRIPTION</span></span>
<span data-ttu-id="95654-108">O cmdlet **Reset-AzureBatchComputeNode** reinstala o sistema operacional no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="95654-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="95654-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95654-109">EXAMPLES</span></span>

### <span data-ttu-id="95654-110">Exemplo 1: reimagem de um nó</span><span class="sxs-lookup"><span data-stu-id="95654-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="95654-111">Esse comando reimagemia o nó de computação com ID "TVM-3257026573_2-20150813t200938z" no pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="95654-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="95654-112">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="95654-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="95654-113">Exemplo 2: reimagem de todos os nós em um pool</span><span class="sxs-lookup"><span data-stu-id="95654-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="95654-114">Esse comando reimagemia cada nó de computação no pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="95654-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="95654-115">OS</span><span class="sxs-lookup"><span data-stu-id="95654-115">PARAMETERS</span></span>

### <span data-ttu-id="95654-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="95654-116">-BatchContext</span></span>
<span data-ttu-id="95654-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="95654-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="95654-118">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="95654-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="95654-119">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="95654-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="95654-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="95654-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="95654-121">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="95654-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="95654-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="95654-122">-ComputeNode</span></span>
<span data-ttu-id="95654-123">Especifica o objeto **PSComputeNode** que representa o nó de computação para fazer a nova imagem.</span><span class="sxs-lookup"><span data-stu-id="95654-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95654-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95654-124">-DefaultProfile</span></span>
<span data-ttu-id="95654-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95654-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95654-126">-ID</span><span class="sxs-lookup"><span data-stu-id="95654-126">-Id</span></span>
<span data-ttu-id="95654-127">Especifica a ID do nó de computação para a nova imagem.</span><span class="sxs-lookup"><span data-stu-id="95654-127">Specifies the ID of the compute node to reimage.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95654-128">-Poolid</span><span class="sxs-lookup"><span data-stu-id="95654-128">-PoolId</span></span>
<span data-ttu-id="95654-129">Especifica a ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="95654-129">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95654-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="95654-130">-ReimageOption</span></span>
<span data-ttu-id="95654-131">Especifica quando é possível refazer a nova imagem do nó e o que fazer com as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="95654-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="95654-132">O padrão é Refila.</span><span class="sxs-lookup"><span data-stu-id="95654-132">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeReimageOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95654-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95654-133">CommonParameters</span></span>
<span data-ttu-id="95654-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95654-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95654-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95654-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95654-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95654-136">INPUTS</span></span>

### <span data-ttu-id="95654-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="95654-137">BatchAccountContext</span></span>
<span data-ttu-id="95654-138">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="95654-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="95654-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="95654-139">PSComputeNode</span></span>
<span data-ttu-id="95654-140">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="95654-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="95654-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95654-141">OUTPUTS</span></span>

## <span data-ttu-id="95654-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95654-142">NOTES</span></span>

## <span data-ttu-id="95654-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95654-143">RELATED LINKS</span></span>

[<span data-ttu-id="95654-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="95654-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="95654-145">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="95654-145">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="95654-146">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="95654-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


