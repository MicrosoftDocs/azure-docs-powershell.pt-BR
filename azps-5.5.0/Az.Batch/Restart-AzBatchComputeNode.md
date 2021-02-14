---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116961"
---
# <span data-ttu-id="cd87a-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cd87a-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="cd87a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd87a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd87a-103">Reinicia o nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="cd87a-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="cd87a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd87a-104">SYNTAX</span></span>

### <span data-ttu-id="cd87a-105">ID (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cd87a-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd87a-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd87a-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd87a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd87a-107">DESCRIPTION</span></span>
<span data-ttu-id="cd87a-108">O cmdlet **Restart-AzBatchComputeNode** reinicia o nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="cd87a-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="cd87a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cd87a-109">EXAMPLES</span></span>

### <span data-ttu-id="cd87a-110">Exemplo 1: Reiniciar um nó de computação</span><span class="sxs-lookup"><span data-stu-id="cd87a-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="cd87a-111">Este comando reinicia o nó de computação com a ID "tvm-3257026573_2-20150813t200938z" no pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="cd87a-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="cd87a-112">Exemplo 2: Reiniciar cada nó de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="cd87a-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="cd87a-113">Esse comando reinicia todos os nó de computação no pool MyPool.</span><span class="sxs-lookup"><span data-stu-id="cd87a-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="cd87a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd87a-114">PARAMETERS</span></span>

### <span data-ttu-id="cd87a-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cd87a-115">-BatchContext</span></span>
<span data-ttu-id="cd87a-116">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="cd87a-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cd87a-117">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="cd87a-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cd87a-118">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="cd87a-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cd87a-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="cd87a-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cd87a-120">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cd87a-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cd87a-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="cd87a-121">-ComputeNode</span></span>
<span data-ttu-id="cd87a-122">Especifica o objeto **PSComputeNode** que representa o nó de computação a ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="cd87a-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="cd87a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd87a-123">-DefaultProfile</span></span>
<span data-ttu-id="cd87a-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cd87a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd87a-125">-ID</span><span class="sxs-lookup"><span data-stu-id="cd87a-125">-Id</span></span>
<span data-ttu-id="cd87a-126">Especifica a ID do nó de computação a ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="cd87a-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="cd87a-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="cd87a-127">-PoolId</span></span>
<span data-ttu-id="cd87a-128">Especifica a ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="cd87a-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="cd87a-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="cd87a-129">-RebootOption</span></span>
<span data-ttu-id="cd87a-130">Especifica quando reiniciar o nó e o que fazer com as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="cd87a-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="cd87a-131">O padrão é a sequência.</span><span class="sxs-lookup"><span data-stu-id="cd87a-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="cd87a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd87a-132">CommonParameters</span></span>
<span data-ttu-id="cd87a-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd87a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd87a-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd87a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd87a-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="cd87a-135">INPUTS</span></span>

### <span data-ttu-id="cd87a-136">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="cd87a-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="cd87a-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cd87a-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cd87a-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="cd87a-138">OUTPUTS</span></span>

### <span data-ttu-id="cd87a-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="cd87a-139">System.Void</span></span>

## <span data-ttu-id="cd87a-140">Notas</span><span class="sxs-lookup"><span data-stu-id="cd87a-140">NOTES</span></span>

## <span data-ttu-id="cd87a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd87a-141">RELATED LINKS</span></span>

[<span data-ttu-id="cd87a-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cd87a-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="cd87a-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cd87a-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="cd87a-144">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="cd87a-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
