---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891054"
---
# <span data-ttu-id="4641c-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="4641c-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="4641c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4641c-102">SYNOPSIS</span></span>
<span data-ttu-id="4641c-103">Habilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="4641c-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="4641c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4641c-104">SYNTAX</span></span>

### <span data-ttu-id="4641c-105">ID (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4641c-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4641c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4641c-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4641c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4641c-107">DESCRIPTION</span></span>
<span data-ttu-id="4641c-108">O cmdlet **Enable-AzBatchComputeNodeScheduling** habilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="4641c-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="4641c-109">Um nó de computação é uma máquina virtual do Azure dedicada a uma carga de trabalho de aplicativo específica.</span><span class="sxs-lookup"><span data-stu-id="4641c-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="4641c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4641c-110">EXAMPLES</span></span>

### <span data-ttu-id="4641c-111">Exemplo 1: Habilitar o agendamento de tarefas em um nó de computação</span><span class="sxs-lookup"><span data-stu-id="4641c-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="4641c-112">Esses comandos habilitam o agendamento de tarefas no nó de computação tvm-1783593343_34-2015117t222514z.</span><span class="sxs-lookup"><span data-stu-id="4641c-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="4641c-113">Para fazer isso, o primeiro comando no exemplo cria uma referência de objeto contendo as chaves de conta da conta em lotes contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="4641c-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="4641c-114">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="4641c-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="4641c-115">O segundo comando usa essa referência de objeto e o cmdlet **Enable-AzBatchComputeNodeScheduling** para se conectar ao pool myPool e habilitar o agendamento de tarefas no tvm-1783593343_34-2015117t222514z.</span><span class="sxs-lookup"><span data-stu-id="4641c-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="4641c-116">Exemplo 2: Habilitar o agendamento de tarefas em nós de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="4641c-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="4641c-117">Esses comandos habilitam o agendamento de tarefas em todos os nós de computação encontrados no pool Pool06.</span><span class="sxs-lookup"><span data-stu-id="4641c-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="4641c-118">Para executar essa tarefa, o primeiro comando no exemplo cria uma referência de objeto contendo as chaves de conta para a conta em lotes contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="4641c-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="4641c-119">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="4641c-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="4641c-120">O segundo comando no exemplo usa essa referência de objeto e **Get-AzBatchComputeNode** para retornar uma coleção de todos os nós de computação encontrados no Pool06.</span><span class="sxs-lookup"><span data-stu-id="4641c-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="4641c-121">Essa coleção é então canalada para o cmdlet **Enable-AzBatchComputeNodeScheduling,** que habilita o agendamento de tarefas em cada nó de computação na coleção.</span><span class="sxs-lookup"><span data-stu-id="4641c-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="4641c-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4641c-122">PARAMETERS</span></span>

### <span data-ttu-id="4641c-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4641c-123">-BatchContext</span></span>
<span data-ttu-id="4641c-124">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="4641c-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4641c-125">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="4641c-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4641c-126">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="4641c-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4641c-127">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="4641c-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4641c-128">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4641c-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4641c-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="4641c-129">-ComputeNode</span></span>
<span data-ttu-id="4641c-130">Especifica uma referência de objeto ao nó de computação onde o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4641c-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="4641c-131">Essa referência de objeto é criada usando o cmdlet Get-AzBatchComputeNode e armazenar o objeto de nó de computação retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="4641c-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="4641c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4641c-132">-DefaultProfile</span></span>
<span data-ttu-id="4641c-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4641c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4641c-134">-Id</span><span class="sxs-lookup"><span data-stu-id="4641c-134">-Id</span></span>
<span data-ttu-id="4641c-135">Especifica a ID do nó de computação onde o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4641c-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="4641c-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4641c-136">-PoolId</span></span>
<span data-ttu-id="4641c-137">Especifica a ID do pool de lotes que contém o nó de computação onde o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4641c-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="4641c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4641c-138">CommonParameters</span></span>
<span data-ttu-id="4641c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4641c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4641c-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4641c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4641c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4641c-141">INPUTS</span></span>

### <span data-ttu-id="4641c-142">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="4641c-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="4641c-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4641c-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4641c-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4641c-144">OUTPUTS</span></span>

### <span data-ttu-id="4641c-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="4641c-145">System.Void</span></span>

## <span data-ttu-id="4641c-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="4641c-146">NOTES</span></span>

## <span data-ttu-id="4641c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4641c-147">RELATED LINKS</span></span>

[<span data-ttu-id="4641c-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="4641c-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


