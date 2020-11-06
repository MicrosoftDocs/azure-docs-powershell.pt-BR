---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441407"
---
# <span data-ttu-id="16da6-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="16da6-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="16da6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16da6-102">SYNOPSIS</span></span>
<span data-ttu-id="16da6-103">Obtém as informações de subtarefas da tarefa especificada.</span><span class="sxs-lookup"><span data-stu-id="16da6-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16da6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16da6-104">SYNTAX</span></span>

### <span data-ttu-id="16da6-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="16da6-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16da6-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="16da6-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16da6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16da6-107">DESCRIPTION</span></span>
<span data-ttu-id="16da6-108">O cmdlet **Get-AzureBatchSubtask** recupera as informações de subtarefas sobre a tarefa especificada.</span><span class="sxs-lookup"><span data-stu-id="16da6-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="16da6-109">As subtarefas fornecem processamento paralelo para tarefas individuais e permitem o monitoramento preciso da execução e do progresso da tarefa.</span><span class="sxs-lookup"><span data-stu-id="16da6-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="16da6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16da6-110">EXAMPLES</span></span>

### <span data-ttu-id="16da6-111">Exemplo 1: retornar todas as subtarefas de uma tarefa especificada</span><span class="sxs-lookup"><span data-stu-id="16da6-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="16da6-112">Esses comandos retornam todas as subtarefas da tarefa com a ID MyTask.</span><span class="sxs-lookup"><span data-stu-id="16da6-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="16da6-113">Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto para as chaves de conta do contosobatchaccount da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="16da6-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="16da6-114">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="16da6-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="16da6-115">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzureBatchSubtask** para retornar todas as subtarefas de MyTask, uma tarefa que é executada como parte do trabalho do trabalho-01.</span><span class="sxs-lookup"><span data-stu-id="16da6-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="16da6-116">OS</span><span class="sxs-lookup"><span data-stu-id="16da6-116">PARAMETERS</span></span>

### <span data-ttu-id="16da6-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="16da6-117">-BatchContext</span></span>
<span data-ttu-id="16da6-118">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="16da6-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16da6-119">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="16da6-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="16da6-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="16da6-120">-JobId</span></span>
<span data-ttu-id="16da6-121">Especifica a ID do trabalho que contém a tarefa cujas subtarefas esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="16da6-121">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="16da6-122">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="16da6-122">-MaxCount</span></span>
<span data-ttu-id="16da6-123">Especifica o número máximo de subtarefas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="16da6-123">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="16da6-124">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="16da6-124">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="16da6-125">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="16da6-125">The default value is 1000.</span></span>

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

### <span data-ttu-id="16da6-126">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="16da6-126">-Task</span></span>
<span data-ttu-id="16da6-127">Especifica uma referência de objeto para a tarefa que contém as subtarefas que esse cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="16da6-127">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="16da6-128">Essa referência de objeto é criada usando-se o cmdlet Get-AzureBatchTask e armazenando o objeto retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="16da6-128">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="16da6-129">-TaskId</span><span class="sxs-lookup"><span data-stu-id="16da6-129">-TaskId</span></span>
<span data-ttu-id="16da6-130">Especifica a ID da tarefa cujas subtarefas esse cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="16da6-130">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="16da6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16da6-131">-DefaultProfile</span></span>
<span data-ttu-id="16da6-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16da6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16da6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16da6-133">CommonParameters</span></span>
<span data-ttu-id="16da6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16da6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16da6-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16da6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16da6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16da6-136">INPUTS</span></span>

### <span data-ttu-id="16da6-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="16da6-137">BatchAccountContext</span></span>
<span data-ttu-id="16da6-138">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="16da6-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="16da6-139">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="16da6-139">PSCloudTask</span></span>
<span data-ttu-id="16da6-140">O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="16da6-140">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="16da6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16da6-141">OUTPUTS</span></span>

###  
<span data-ttu-id="16da6-142">Esse cmdlet retorna instâncias do objeto **PSSubtaskInformation** .</span><span class="sxs-lookup"><span data-stu-id="16da6-142">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="16da6-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16da6-143">NOTES</span></span>

## <span data-ttu-id="16da6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16da6-144">RELATED LINKS</span></span>

[<span data-ttu-id="16da6-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="16da6-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


