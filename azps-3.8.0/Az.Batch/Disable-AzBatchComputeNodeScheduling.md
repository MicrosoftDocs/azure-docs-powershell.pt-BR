---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777876"
---
# <span data-ttu-id="87768-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="87768-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="87768-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87768-102">SYNOPSIS</span></span>
<span data-ttu-id="87768-103">Desabilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="87768-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="87768-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87768-104">SYNTAX</span></span>

### <span data-ttu-id="87768-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="87768-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87768-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="87768-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87768-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87768-107">DESCRIPTION</span></span>
<span data-ttu-id="87768-108">O cmdlet **Disable-AzBatchComputeNodeScheduling** desabilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="87768-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="87768-109">Um nó de computação é uma máquina virtual do Azure dedicada a uma carga de trabalho específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87768-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="87768-110">Ao desabilitar o agendamento de tarefas em um nó de computação, você também terá a opção de determinar o que fazer sobre os trabalhos atualmente na fila de tarefas do nó.</span><span class="sxs-lookup"><span data-stu-id="87768-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="87768-111">**Disable-AzBatchComputeNodeScheduling** permite que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="87768-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="87768-112">Termine as tarefas e coloque-as de volta na fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="87768-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="87768-113">Isso permite que essas tarefas sejam reagendadas em outro nó de computação.</span><span class="sxs-lookup"><span data-stu-id="87768-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="87768-114">Termine as tarefas e remova-as da fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="87768-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="87768-115">As tarefas interrompidas dessa maneira não serão reagendadas.</span><span class="sxs-lookup"><span data-stu-id="87768-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="87768-116">Aguarde até que todas as tarefas executadas atualmente sejam concluídas e, em seguida, desabilite o agendamento de tarefas no nó de computação.</span><span class="sxs-lookup"><span data-stu-id="87768-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="87768-117">Aguarde até que todas as tarefas em execução sejam concluídas e todos os períodos de retenção de dados expirem e, em seguida, desabilite o agendamento de tarefas no nó de computação.</span><span class="sxs-lookup"><span data-stu-id="87768-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="87768-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87768-118">EXAMPLES</span></span>

### <span data-ttu-id="87768-119">Exemplo 1: desabilitar o agendamento de tarefas em um nó de computação</span><span class="sxs-lookup"><span data-stu-id="87768-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="87768-120">Esses comandos desativam o agendamento de tarefas no nó de computação TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="87768-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="87768-121">Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto para as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="87768-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="87768-122">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="87768-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="87768-123">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Disable-AzBatchComputeNodeScheduling** para se conectar ao pool mypool e desabilitar o agendamento de tarefas no nó TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="87768-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="87768-124">Como o parâmetro *DisableComputeNodeSchedulingOptions* não foi incluído, todas as tarefas em execução no nó de computação serão recolocadas em fila.</span><span class="sxs-lookup"><span data-stu-id="87768-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="87768-125">Exemplo 2: desabilitar o agendamento de tarefas em todos os nós de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="87768-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="87768-126">Esses comandos desativam o agendamento de tarefas em todos os nós de computador na Pool06 do pool de lotes.</span><span class="sxs-lookup"><span data-stu-id="87768-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="87768-127">Para executar essa tarefa, o primeiro comando do exemplo cria uma referência de objeto para as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="87768-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="87768-128">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="87768-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="87768-129">O segundo comando no exemplo usa essa referência de objeto e **Get-AzBatchComputeNode** para retornar uma coleção de todos os nós de computação encontrados em Pool06.</span><span class="sxs-lookup"><span data-stu-id="87768-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="87768-130">Essa Coleta Então é canalizada para desativar o cmdlet **Disable-AzBatchComputeNodeScheduling** para desabilitar o agendamento de tarefas em cada nó de computação na coleção.</span><span class="sxs-lookup"><span data-stu-id="87768-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="87768-131">Como o parâmetro *DisableComputeNodeSchedulingOptions* não foi incluído, todas as tarefas atualmente em execução nos nós de computação serão recolocadas em fila.</span><span class="sxs-lookup"><span data-stu-id="87768-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="87768-132">OS</span><span class="sxs-lookup"><span data-stu-id="87768-132">PARAMETERS</span></span>

### <span data-ttu-id="87768-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="87768-133">-BatchContext</span></span>
<span data-ttu-id="87768-134">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="87768-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="87768-135">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="87768-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="87768-136">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="87768-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="87768-137">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="87768-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="87768-138">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="87768-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="87768-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="87768-139">-ComputeNode</span></span>
<span data-ttu-id="87768-140">Especifica uma referência de objeto para o nó de computação em que o agendamento da tarefa está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="87768-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="87768-141">Essa referência de objeto é criada usando-se o cmdlet Get-AzBatchComputeNode e armazenando o objeto do nó de computação retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="87768-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="87768-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87768-142">-DefaultProfile</span></span>
<span data-ttu-id="87768-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87768-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87768-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="87768-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="87768-145">Especifica como esse cmdlet lida com todas as tarefas que estão sendo executadas no nó do computador em que o agendamento está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="87768-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="87768-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="87768-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87768-147">Refilar.</span><span class="sxs-lookup"><span data-stu-id="87768-147">Requeue.</span></span>
<span data-ttu-id="87768-148">As tarefas são interrompidas imediatamente e retornadas à fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="87768-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="87768-149">Isso permite que as tarefas sejam reagendadas em outro nó de computação.</span><span class="sxs-lookup"><span data-stu-id="87768-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="87768-150">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="87768-150">This is the default value.</span></span> 
- <span data-ttu-id="87768-151">Inesperada.</span><span class="sxs-lookup"><span data-stu-id="87768-151">Terminate.</span></span>
<span data-ttu-id="87768-152">As tarefas são interrompidas imediatamente e removidas da fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="87768-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="87768-153">Essas tarefas não serão reagendadas.</span><span class="sxs-lookup"><span data-stu-id="87768-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="87768-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="87768-154">TaskCompletion.</span></span>
<span data-ttu-id="87768-155">Tarefas em execução no momento poderão ser concluídas antes de o agendamento da tarefa ser desabilitado no nó de computação.</span><span class="sxs-lookup"><span data-stu-id="87768-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="87768-156">Nenhuma nova tarefa será agendada neste nó.</span><span class="sxs-lookup"><span data-stu-id="87768-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="87768-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="87768-157">RetainedData.</span></span>
<span data-ttu-id="87768-158">As tarefas em execução no momento poderão ser concluídas e os períodos de retenção de dados poderão expirar antes de o agendamento da tarefa ser desabilitado no nó de computação.</span><span class="sxs-lookup"><span data-stu-id="87768-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="87768-159">Nenhuma nova tarefa será agendada neste nó.</span><span class="sxs-lookup"><span data-stu-id="87768-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87768-160">-ID</span><span class="sxs-lookup"><span data-stu-id="87768-160">-Id</span></span>
<span data-ttu-id="87768-161">Especifica a ID do nó de computação em que o agendamento da tarefa está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="87768-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="87768-162">-Poolid</span><span class="sxs-lookup"><span data-stu-id="87768-162">-PoolId</span></span>
<span data-ttu-id="87768-163">Especifica a ID do pool de lotes que contém o nó de computação em que o agendamento da tarefa está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="87768-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="87768-164">Se você usar o parâmetro *poolid* , não use o parâmetro *ComputeNode* nesse mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="87768-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="87768-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87768-165">CommonParameters</span></span>
<span data-ttu-id="87768-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87768-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87768-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87768-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87768-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87768-168">INPUTS</span></span>

### <span data-ttu-id="87768-169">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="87768-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="87768-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="87768-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="87768-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87768-171">OUTPUTS</span></span>

### <span data-ttu-id="87768-172">System. void</span><span class="sxs-lookup"><span data-stu-id="87768-172">System.Void</span></span>

## <span data-ttu-id="87768-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87768-173">NOTES</span></span>

## <span data-ttu-id="87768-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87768-174">RELATED LINKS</span></span>

[<span data-ttu-id="87768-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="87768-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="87768-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="87768-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


