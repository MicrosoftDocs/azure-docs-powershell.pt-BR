---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 7cf3a056ec4266cccac577920f2f5b9292ce03be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439899"
---
# <span data-ttu-id="cd304-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="cd304-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="cd304-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd304-102">SYNOPSIS</span></span>
<span data-ttu-id="cd304-103">Habilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="cd304-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd304-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd304-104">SYNTAX</span></span>

### <span data-ttu-id="cd304-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="cd304-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd304-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cd304-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd304-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd304-107">DESCRIPTION</span></span>
<span data-ttu-id="cd304-108">O cmdlet **Enable-AzureBatchComputeNodeScheduling** habilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="cd304-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="cd304-109">Um nó de computação é uma máquina virtual do Azure dedicada a uma carga de trabalho específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cd304-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="cd304-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd304-110">EXAMPLES</span></span>

### <span data-ttu-id="cd304-111">Exemplo 1: habilitar o agendamento de tarefas em um nó de computação</span><span class="sxs-lookup"><span data-stu-id="cd304-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="cd304-112">Esses comandos permitem o agendamento de tarefas no nó de computação TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="cd304-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="cd304-113">Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto contendo as chaves de conta para o contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="cd304-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="cd304-114">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="cd304-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="cd304-115">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Enable-AzureBatchComputeNodeScheduling** para se conectar ao pool mypool e habilitar o agendamento de tarefas no TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="cd304-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="cd304-116">Exemplo 2: habilitar o agendamento de tarefas em nós de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="cd304-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="cd304-117">Esses comandos permitem o agendamento de tarefas em todos os nós de computação encontrados na Pool06 do pool.</span><span class="sxs-lookup"><span data-stu-id="cd304-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="cd304-118">Para executar essa tarefa, o primeiro comando do exemplo cria uma referência de objeto que contém as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="cd304-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="cd304-119">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="cd304-119">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="cd304-120">O segundo comando no exemplo usa essa referência de objeto e **Get-AzureBatchComputeNode** para retornar uma coleção de todos os nós de computação encontrados em Pool06.</span><span class="sxs-lookup"><span data-stu-id="cd304-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="cd304-121">Essa coleção é então canalizada para o cmdlet **Enable-AzureBatchComputeNodeScheduling** , que permite o agendamento de tarefas em cada nó de computação na coleção.</span><span class="sxs-lookup"><span data-stu-id="cd304-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="cd304-122">OS</span><span class="sxs-lookup"><span data-stu-id="cd304-122">PARAMETERS</span></span>

### <span data-ttu-id="cd304-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cd304-123">-BatchContext</span></span>
<span data-ttu-id="cd304-124">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="cd304-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cd304-125">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="cd304-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cd304-126">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="cd304-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cd304-127">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="cd304-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cd304-128">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cd304-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cd304-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="cd304-129">-ComputeNode</span></span>
<span data-ttu-id="cd304-130">Especifica uma referência de objeto para o nó de computação em que o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="cd304-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="cd304-131">Essa referência de objeto é criada usando-se o cmdlet Get-AzureBatchComputeNode e armazenando o objeto do nó de computação retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="cd304-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="cd304-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd304-132">-DefaultProfile</span></span>
<span data-ttu-id="cd304-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd304-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd304-134">-ID</span><span class="sxs-lookup"><span data-stu-id="cd304-134">-Id</span></span>
<span data-ttu-id="cd304-135">Especifica a ID do nó de computação em que o agendamento da tarefa está habilitado.</span><span class="sxs-lookup"><span data-stu-id="cd304-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="cd304-136">-Poolid</span><span class="sxs-lookup"><span data-stu-id="cd304-136">-PoolId</span></span>
<span data-ttu-id="cd304-137">Especifica a ID do pool de lotes que contém o nó de computação no qual o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="cd304-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="cd304-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd304-138">CommonParameters</span></span>
<span data-ttu-id="cd304-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd304-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd304-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd304-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd304-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd304-141">INPUTS</span></span>

### <span data-ttu-id="cd304-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cd304-142">BatchAccountContext</span></span>
<span data-ttu-id="cd304-143">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cd304-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cd304-144">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="cd304-144">PSComputeNode</span></span>
<span data-ttu-id="cd304-145">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cd304-145">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="cd304-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd304-146">OUTPUTS</span></span>

## <span data-ttu-id="cd304-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd304-147">NOTES</span></span>

## <span data-ttu-id="cd304-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd304-148">RELATED LINKS</span></span>

[<span data-ttu-id="cd304-149">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="cd304-149">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)

