---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2922e9b1a37f714b1ccfb19aea86556b9988ccca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601476"
---
# <span data-ttu-id="df6f2-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="df6f2-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="df6f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="df6f2-103">Habilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="df6f2-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="df6f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df6f2-104">SYNTAX</span></span>

### <span data-ttu-id="df6f2-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="df6f2-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df6f2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="df6f2-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df6f2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df6f2-107">DESCRIPTION</span></span>
<span data-ttu-id="df6f2-108">O cmdlet **Enable-AzBatchComputeNodeScheduling** habilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="df6f2-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="df6f2-109">Um nó de computação é uma máquina virtual do Azure dedicada a uma carga de trabalho específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="df6f2-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="df6f2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df6f2-110">EXAMPLES</span></span>

### <span data-ttu-id="df6f2-111">Exemplo 1: habilitar o agendamento de tarefas em um nó de computação</span><span class="sxs-lookup"><span data-stu-id="df6f2-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="df6f2-112">Esses comandos permitem o agendamento de tarefas no nó de computação TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="df6f2-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="df6f2-113">Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto contendo as chaves de conta para o contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="df6f2-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="df6f2-114">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="df6f2-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="df6f2-115">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Enable-AzBatchComputeNodeScheduling** para se conectar ao pool mypool e habilitar o agendamento de tarefas no TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="df6f2-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="df6f2-116">Exemplo 2: habilitar o agendamento de tarefas em nós de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="df6f2-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="df6f2-117">Esses comandos permitem o agendamento de tarefas em todos os nós de computação encontrados na Pool06 do pool.</span><span class="sxs-lookup"><span data-stu-id="df6f2-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="df6f2-118">Para executar essa tarefa, o primeiro comando do exemplo cria uma referência de objeto que contém as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="df6f2-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="df6f2-119">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="df6f2-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="df6f2-120">O segundo comando no exemplo usa essa referência de objeto e **Get-AzBatchComputeNode** para retornar uma coleção de todos os nós de computação encontrados em Pool06.</span><span class="sxs-lookup"><span data-stu-id="df6f2-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="df6f2-121">Essa coleção é então canalizada para o cmdlet **Enable-AzBatchComputeNodeScheduling** , que permite o agendamento de tarefas em cada nó de computação na coleção.</span><span class="sxs-lookup"><span data-stu-id="df6f2-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="df6f2-122">OS</span><span class="sxs-lookup"><span data-stu-id="df6f2-122">PARAMETERS</span></span>

### <span data-ttu-id="df6f2-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="df6f2-123">-BatchContext</span></span>
<span data-ttu-id="df6f2-124">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="df6f2-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="df6f2-125">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="df6f2-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="df6f2-126">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="df6f2-126">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="df6f2-127">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="df6f2-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="df6f2-128">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="df6f2-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="df6f2-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="df6f2-129">-ComputeNode</span></span>
<span data-ttu-id="df6f2-130">Especifica uma referência de objeto para o nó de computação em que o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="df6f2-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="df6f2-131">Essa referência de objeto é criada usando-se o cmdlet Get-AzBatchComputeNode e armazenando o objeto do nó de computação retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="df6f2-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="df6f2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6f2-132">-DefaultProfile</span></span>
<span data-ttu-id="df6f2-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df6f2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df6f2-134">-ID</span><span class="sxs-lookup"><span data-stu-id="df6f2-134">-Id</span></span>
<span data-ttu-id="df6f2-135">Especifica a ID do nó de computação em que o agendamento da tarefa está habilitado.</span><span class="sxs-lookup"><span data-stu-id="df6f2-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="df6f2-136">-Poolid</span><span class="sxs-lookup"><span data-stu-id="df6f2-136">-PoolId</span></span>
<span data-ttu-id="df6f2-137">Especifica a ID do pool de lotes que contém o nó de computação no qual o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="df6f2-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="df6f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6f2-138">CommonParameters</span></span>
<span data-ttu-id="df6f2-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6f2-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df6f2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6f2-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df6f2-141">INPUTS</span></span>

### <span data-ttu-id="df6f2-142">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="df6f2-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="df6f2-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="df6f2-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="df6f2-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df6f2-144">OUTPUTS</span></span>

### <span data-ttu-id="df6f2-145">System. void</span><span class="sxs-lookup"><span data-stu-id="df6f2-145">System.Void</span></span>

## <span data-ttu-id="df6f2-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df6f2-146">NOTES</span></span>

## <span data-ttu-id="df6f2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df6f2-147">RELATED LINKS</span></span>

[<span data-ttu-id="df6f2-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="df6f2-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


