---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430540"
---
# <span data-ttu-id="f632d-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="f632d-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="f632d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f632d-102">SYNOPSIS</span></span>
<span data-ttu-id="f632d-103">Desabilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="f632d-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="f632d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f632d-104">SYNTAX</span></span>

### <span data-ttu-id="f632d-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="f632d-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f632d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f632d-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f632d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f632d-107">DESCRIPTION</span></span>
<span data-ttu-id="f632d-108">O cmdlet **Disable-AzBatchComputeNodeScheduling** desabilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="f632d-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="f632d-109">Um nó de computação é uma máquina virtual do Azure dedicada a uma carga de trabalho específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f632d-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="f632d-110">Ao desabilitar o agendamento de tarefas em um nó de computação, você também terá a opção de determinar o que fazer sobre os trabalhos atualmente na fila de tarefas do nó.</span><span class="sxs-lookup"><span data-stu-id="f632d-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="f632d-111">**Disable-AzBatchComputeNodeScheduling** permite que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f632d-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="f632d-112">Termine as tarefas e coloque-as de volta na fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f632d-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="f632d-113">Isso permite que essas tarefas sejam reagendadas em outro nó de computação.</span><span class="sxs-lookup"><span data-stu-id="f632d-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="f632d-114">Termine as tarefas e remova-as da fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f632d-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="f632d-115">As tarefas interrompidas dessa maneira não serão reagendadas.</span><span class="sxs-lookup"><span data-stu-id="f632d-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="f632d-116">Aguarde até que todas as tarefas executadas atualmente sejam concluídas e, em seguida, desabilite o agendamento de tarefas no nó de computação.</span><span class="sxs-lookup"><span data-stu-id="f632d-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="f632d-117">Aguarde até que todas as tarefas em execução sejam concluídas e todos os períodos de retenção de dados expirem e, em seguida, desabilite o agendamento de tarefas no nó de computação.</span><span class="sxs-lookup"><span data-stu-id="f632d-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="f632d-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f632d-118">EXAMPLES</span></span>

### <span data-ttu-id="f632d-119">Exemplo 1: desabilitar o agendamento de tarefas em um nó de computação</span><span class="sxs-lookup"><span data-stu-id="f632d-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="f632d-120">Esses comandos desativam o agendamento de tarefas no nó de computação TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="f632d-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="f632d-121">Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto para as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="f632d-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="f632d-122">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="f632d-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="f632d-123">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Disable-AzBatchComputeNodeScheduling** para se conectar ao pool mypool e desabilitar o agendamento de tarefas no nó TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="f632d-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="f632d-124">Como o parâmetro *DisableComputeNodeSchedulingOptions* não foi incluído, todas as tarefas em execução no nó de computação serão recolocadas em fila.</span><span class="sxs-lookup"><span data-stu-id="f632d-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="f632d-125">Exemplo 2: desabilitar o agendamento de tarefas em todos os nós de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="f632d-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="f632d-126">Esses comandos desativam o agendamento de tarefas em todos os nós de computador na Pool06 do pool de lotes.</span><span class="sxs-lookup"><span data-stu-id="f632d-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="f632d-127">Para executar essa tarefa, o primeiro comando do exemplo cria uma referência de objeto para as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="f632d-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="f632d-128">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="f632d-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="f632d-129">O segundo comando no exemplo usa essa referência de objeto e **Get-AzBatchComputeNode** para retornar uma coleção de todos os nós de computação encontrados em Pool06.</span><span class="sxs-lookup"><span data-stu-id="f632d-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="f632d-130">Essa Coleta Então é canalizada para desativar o cmdlet **Disable-AzBatchComputeNodeScheduling** para desabilitar o agendamento de tarefas em cada nó de computação na coleção.</span><span class="sxs-lookup"><span data-stu-id="f632d-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="f632d-131">Como o parâmetro *DisableComputeNodeSchedulingOptions* não foi incluído, todas as tarefas atualmente em execução nos nós de computação serão recolocadas em fila.</span><span class="sxs-lookup"><span data-stu-id="f632d-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="f632d-132">OS</span><span class="sxs-lookup"><span data-stu-id="f632d-132">PARAMETERS</span></span>

### <span data-ttu-id="f632d-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f632d-133">-BatchContext</span></span>
<span data-ttu-id="f632d-134">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f632d-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f632d-135">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f632d-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f632d-136">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="f632d-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f632d-137">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="f632d-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f632d-138">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f632d-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f632d-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="f632d-139">-ComputeNode</span></span>
<span data-ttu-id="f632d-140">Especifica uma referência de objeto para o nó de computação em que o agendamento da tarefa está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f632d-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="f632d-141">Essa referência de objeto é criada usando-se o cmdlet Get-AzBatchComputeNode e armazenando o objeto do nó de computação retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="f632d-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="f632d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f632d-142">-DefaultProfile</span></span>
<span data-ttu-id="f632d-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f632d-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f632d-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="f632d-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="f632d-145">Especifica como esse cmdlet lida com todas as tarefas que estão sendo executadas no nó do computador em que o agendamento está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f632d-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="f632d-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f632d-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f632d-147">Refilar.</span><span class="sxs-lookup"><span data-stu-id="f632d-147">Requeue.</span></span>
<span data-ttu-id="f632d-148">As tarefas são interrompidas imediatamente e retornadas à fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f632d-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="f632d-149">Isso permite que as tarefas sejam reagendadas em outro nó de computação.</span><span class="sxs-lookup"><span data-stu-id="f632d-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="f632d-150">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f632d-150">This is the default value.</span></span> 
- <span data-ttu-id="f632d-151">Inesperada.</span><span class="sxs-lookup"><span data-stu-id="f632d-151">Terminate.</span></span>
<span data-ttu-id="f632d-152">As tarefas são interrompidas imediatamente e removidas da fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f632d-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="f632d-153">Essas tarefas não serão reagendadas.</span><span class="sxs-lookup"><span data-stu-id="f632d-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="f632d-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="f632d-154">TaskCompletion.</span></span>
<span data-ttu-id="f632d-155">Tarefas em execução no momento poderão ser concluídas antes de o agendamento da tarefa ser desabilitado no nó de computação.</span><span class="sxs-lookup"><span data-stu-id="f632d-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="f632d-156">Nenhuma nova tarefa será agendada neste nó.</span><span class="sxs-lookup"><span data-stu-id="f632d-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="f632d-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="f632d-157">RetainedData.</span></span>
<span data-ttu-id="f632d-158">As tarefas em execução no momento poderão ser concluídas e os períodos de retenção de dados poderão expirar antes de o agendamento da tarefa ser desabilitado no nó de computação.</span><span class="sxs-lookup"><span data-stu-id="f632d-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="f632d-159">Nenhuma nova tarefa será agendada neste nó.</span><span class="sxs-lookup"><span data-stu-id="f632d-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="f632d-160">-ID</span><span class="sxs-lookup"><span data-stu-id="f632d-160">-Id</span></span>
<span data-ttu-id="f632d-161">Especifica a ID do nó de computação em que o agendamento da tarefa está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f632d-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="f632d-162">-Poolid</span><span class="sxs-lookup"><span data-stu-id="f632d-162">-PoolId</span></span>
<span data-ttu-id="f632d-163">Especifica a ID do pool de lotes que contém o nó de computação em que o agendamento da tarefa está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f632d-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="f632d-164">Se você usar o parâmetro *poolid* , não use o parâmetro *ComputeNode* nesse mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="f632d-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="f632d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f632d-165">CommonParameters</span></span>
<span data-ttu-id="f632d-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f632d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f632d-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f632d-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f632d-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f632d-168">INPUTS</span></span>

### <span data-ttu-id="f632d-169">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="f632d-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="f632d-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f632d-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f632d-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f632d-171">OUTPUTS</span></span>

### <span data-ttu-id="f632d-172">System. void</span><span class="sxs-lookup"><span data-stu-id="f632d-172">System.Void</span></span>

## <span data-ttu-id="f632d-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f632d-173">NOTES</span></span>

## <span data-ttu-id="f632d-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f632d-174">RELATED LINKS</span></span>

[<span data-ttu-id="f632d-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f632d-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f632d-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="f632d-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


