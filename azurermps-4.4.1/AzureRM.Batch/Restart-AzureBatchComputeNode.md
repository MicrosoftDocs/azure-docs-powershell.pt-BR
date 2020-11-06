---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432671"
---
# <span data-ttu-id="48f45-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="48f45-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="48f45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48f45-102">SYNOPSIS</span></span>
<span data-ttu-id="48f45-103">Reinicializa o nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="48f45-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48f45-104">SYNTAX</span></span>

### <span data-ttu-id="48f45-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="48f45-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48f45-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="48f45-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48f45-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48f45-107">DESCRIPTION</span></span>
<span data-ttu-id="48f45-108">O cmdlet **Restart-AzureBatchComputeNode** reinicializa o nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="48f45-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="48f45-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48f45-109">EXAMPLES</span></span>

### <span data-ttu-id="48f45-110">Exemplo 1: reiniciar um nó de computação</span><span class="sxs-lookup"><span data-stu-id="48f45-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="48f45-111">Esse comando reinicializa o nó de computação com a ID "TVM-3257026573_2-20150813t200938z" no pool mypool.</span><span class="sxs-lookup"><span data-stu-id="48f45-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="48f45-112">Exemplo 2: reiniciar cada nó de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="48f45-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="48f45-113">Esse comando reinicializa cada nó de computação no pool de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="48f45-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="48f45-114">OS</span><span class="sxs-lookup"><span data-stu-id="48f45-114">PARAMETERS</span></span>

### <span data-ttu-id="48f45-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48f45-115">-BatchContext</span></span>
<span data-ttu-id="48f45-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="48f45-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="48f45-117">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="48f45-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="48f45-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="48f45-118">-ComputeNode</span></span>
<span data-ttu-id="48f45-119">Especifica o objeto **PSComputeNode** que representa o nó de computação a ser reinicializado.</span><span class="sxs-lookup"><span data-stu-id="48f45-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="48f45-120">-ID</span><span class="sxs-lookup"><span data-stu-id="48f45-120">-Id</span></span>
<span data-ttu-id="48f45-121">Especifica a ID do nó de computação a ser reinicializado.</span><span class="sxs-lookup"><span data-stu-id="48f45-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="48f45-122">-Poolid</span><span class="sxs-lookup"><span data-stu-id="48f45-122">-PoolId</span></span>
<span data-ttu-id="48f45-123">Especifica a ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="48f45-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="48f45-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="48f45-124">-RebootOption</span></span>
<span data-ttu-id="48f45-125">Especifica quando reinicializar o nó e o que fazer com as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="48f45-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="48f45-126">O padrão é Refila.</span><span class="sxs-lookup"><span data-stu-id="48f45-126">The default is Requeue.</span></span>

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

### <span data-ttu-id="48f45-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f45-127">-DefaultProfile</span></span>
<span data-ttu-id="48f45-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48f45-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48f45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f45-129">CommonParameters</span></span>
<span data-ttu-id="48f45-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f45-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f45-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f45-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48f45-132">INPUTS</span></span>

### <span data-ttu-id="48f45-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48f45-133">BatchAccountContext</span></span>
<span data-ttu-id="48f45-134">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="48f45-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="48f45-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="48f45-135">PSComputeNode</span></span>
<span data-ttu-id="48f45-136">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="48f45-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="48f45-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48f45-137">OUTPUTS</span></span>

## <span data-ttu-id="48f45-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48f45-138">NOTES</span></span>

## <span data-ttu-id="48f45-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48f45-139">RELATED LINKS</span></span>

[<span data-ttu-id="48f45-140">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="48f45-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="48f45-141">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="48f45-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="48f45-142">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="48f45-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


