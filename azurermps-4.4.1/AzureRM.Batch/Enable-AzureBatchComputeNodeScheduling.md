---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 6c890836d8ca22e617fdc88788a6809cbce8581c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610030"
---
# <span data-ttu-id="65bb4-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="65bb4-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="65bb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="65bb4-103">Habilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="65bb4-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65bb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65bb4-104">SYNTAX</span></span>

### <span data-ttu-id="65bb4-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="65bb4-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65bb4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="65bb4-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65bb4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65bb4-107">DESCRIPTION</span></span>
<span data-ttu-id="65bb4-108">O cmdlet **Enable-AzureBatchComputeNodeScheduling** habilita o agendamento de tarefas no nó de computação especificado.</span><span class="sxs-lookup"><span data-stu-id="65bb4-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="65bb4-109">Um nó de computação é uma máquina virtual do Azure dedicada a uma carga de trabalho específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="65bb4-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="65bb4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65bb4-110">EXAMPLES</span></span>

### <span data-ttu-id="65bb4-111">Exemplo 1: habilitar o agendamento de tarefas em um nó de computação</span><span class="sxs-lookup"><span data-stu-id="65bb4-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="65bb4-112">Esses comandos permitem o agendamento de tarefas no nó de computação TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="65bb4-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="65bb4-113">Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto contendo as chaves de conta para o contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="65bb4-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="65bb4-114">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="65bb4-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="65bb4-115">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Enable-AzureBatchComputeNodeScheduling** para se conectar ao pool mypool e habilitar o agendamento de tarefas no TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="65bb4-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="65bb4-116">Exemplo 2: habilitar o agendamento de tarefas em nós de computação em um pool</span><span class="sxs-lookup"><span data-stu-id="65bb4-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="65bb4-117">Esses comandos permitem o agendamento de tarefas em todos os nós de computação encontrados na Pool06 do pool.</span><span class="sxs-lookup"><span data-stu-id="65bb4-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="65bb4-118">Para executar essa tarefa, o primeiro comando do exemplo cria uma referência de objeto que contém as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="65bb4-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="65bb4-119">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="65bb4-119">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="65bb4-120">O segundo comando no exemplo usa essa referência de objeto e **Get-AzureBatchComputeNode** para retornar uma coleção de todos os nós de computação encontrados em Pool06.</span><span class="sxs-lookup"><span data-stu-id="65bb4-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="65bb4-121">Essa coleção é então canalizada para o cmdlet **Enable-AzureBatchComputeNodeScheduling** , que permite o agendamento de tarefas em cada nó de computação na coleção.</span><span class="sxs-lookup"><span data-stu-id="65bb4-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="65bb4-122">OS</span><span class="sxs-lookup"><span data-stu-id="65bb4-122">PARAMETERS</span></span>

### <span data-ttu-id="65bb4-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="65bb4-123">-BatchContext</span></span>
<span data-ttu-id="65bb4-124">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="65bb4-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="65bb4-125">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="65bb4-125">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="65bb4-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="65bb4-126">-ComputeNode</span></span>
<span data-ttu-id="65bb4-127">Especifica uma referência de objeto para o nó de computação em que o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="65bb4-127">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="65bb4-128">Essa referência de objeto é criada usando-se o cmdlet Get-AzureBatchComputeNode e armazenando o objeto do nó de computação retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="65bb4-128">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="65bb4-129">-ID</span><span class="sxs-lookup"><span data-stu-id="65bb4-129">-Id</span></span>
<span data-ttu-id="65bb4-130">Especifica a ID do nó de computação em que o agendamento da tarefa está habilitado.</span><span class="sxs-lookup"><span data-stu-id="65bb4-130">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="65bb4-131">-Poolid</span><span class="sxs-lookup"><span data-stu-id="65bb4-131">-PoolId</span></span>
<span data-ttu-id="65bb4-132">Especifica a ID do pool de lotes que contém o nó de computação no qual o agendamento de tarefas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="65bb4-132">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="65bb4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65bb4-133">-DefaultProfile</span></span>
<span data-ttu-id="65bb4-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65bb4-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65bb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65bb4-135">CommonParameters</span></span>
<span data-ttu-id="65bb4-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65bb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65bb4-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65bb4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65bb4-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65bb4-138">INPUTS</span></span>

### <span data-ttu-id="65bb4-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="65bb4-139">BatchAccountContext</span></span>
<span data-ttu-id="65bb4-140">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="65bb4-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="65bb4-141">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="65bb4-141">PSComputeNode</span></span>
<span data-ttu-id="65bb4-142">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="65bb4-142">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="65bb4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65bb4-143">OUTPUTS</span></span>

## <span data-ttu-id="65bb4-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65bb4-144">NOTES</span></span>

## <span data-ttu-id="65bb4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65bb4-145">RELATED LINKS</span></span>

[<span data-ttu-id="65bb4-146">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="65bb4-146">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


