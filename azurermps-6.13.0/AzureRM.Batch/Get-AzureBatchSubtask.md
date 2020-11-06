---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 5aa0ccc7da257cf20deb4a79d2b5415aa4c45885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433317"
---
# <span data-ttu-id="b846b-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="b846b-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="b846b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b846b-102">SYNOPSIS</span></span>
<span data-ttu-id="b846b-103">Obtém as informações de subtarefas da tarefa especificada.</span><span class="sxs-lookup"><span data-stu-id="b846b-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b846b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b846b-104">SYNTAX</span></span>

### <span data-ttu-id="b846b-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="b846b-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b846b-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b846b-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b846b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b846b-107">DESCRIPTION</span></span>
<span data-ttu-id="b846b-108">O cmdlet **Get-AzureBatchSubtask** recupera as informações de subtarefas sobre a tarefa especificada.</span><span class="sxs-lookup"><span data-stu-id="b846b-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="b846b-109">As subtarefas fornecem processamento paralelo para tarefas individuais e permitem o monitoramento preciso da execução e do progresso da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b846b-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="b846b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b846b-110">EXAMPLES</span></span>

### <span data-ttu-id="b846b-111">Exemplo 1: retornar todas as subtarefas de uma tarefa especificada</span><span class="sxs-lookup"><span data-stu-id="b846b-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="b846b-112">Esses comandos retornam todas as subtarefas da tarefa com a ID MyTask.</span><span class="sxs-lookup"><span data-stu-id="b846b-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="b846b-113">Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto para as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="b846b-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="b846b-114">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="b846b-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="b846b-115">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzureBatchSubtask** para retornar todas as subtarefas de MyTask, uma tarefa que é executada como parte do trabalho do trabalho-01.</span><span class="sxs-lookup"><span data-stu-id="b846b-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="b846b-116">OS</span><span class="sxs-lookup"><span data-stu-id="b846b-116">PARAMETERS</span></span>

### <span data-ttu-id="b846b-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b846b-117">-BatchContext</span></span>
<span data-ttu-id="b846b-118">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="b846b-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b846b-119">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="b846b-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b846b-120">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="b846b-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b846b-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="b846b-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b846b-122">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b846b-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b846b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b846b-123">-DefaultProfile</span></span>
<span data-ttu-id="b846b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b846b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b846b-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="b846b-125">-JobId</span></span>
<span data-ttu-id="b846b-126">Especifica a ID do trabalho que contém a tarefa cujas subtarefas esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b846b-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b846b-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b846b-127">-MaxCount</span></span>
<span data-ttu-id="b846b-128">Especifica o número máximo de subtarefas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="b846b-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="b846b-129">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="b846b-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b846b-130">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="b846b-130">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b846b-131">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="b846b-131">-Task</span></span>
<span data-ttu-id="b846b-132">Especifica uma referência de objeto para a tarefa que contém as subtarefas que esse cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="b846b-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="b846b-133">Essa referência de objeto é criada usando-se o cmdlet Get-AzureBatchTask e armazenando o objeto retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="b846b-133">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b846b-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="b846b-134">-TaskId</span></span>
<span data-ttu-id="b846b-135">Especifica a ID da tarefa cujas subtarefas esse cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="b846b-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b846b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b846b-136">CommonParameters</span></span>
<span data-ttu-id="b846b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b846b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b846b-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b846b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b846b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b846b-139">INPUTS</span></span>

### <span data-ttu-id="b846b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b846b-140">System.String</span></span>

### <span data-ttu-id="b846b-141">Microsoft.Azure.Commands.Batch. Modelos. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="b846b-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="b846b-142">Parâmetros: Task (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b846b-142">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="b846b-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b846b-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b846b-144">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b846b-144">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b846b-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b846b-145">OUTPUTS</span></span>

### <span data-ttu-id="b846b-146">Microsoft.Azure.Commands.Batch. Modelos. PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="b846b-146">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="b846b-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b846b-147">NOTES</span></span>

## <span data-ttu-id="b846b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b846b-148">RELATED LINKS</span></span>

[<span data-ttu-id="b846b-149">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b846b-149">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

