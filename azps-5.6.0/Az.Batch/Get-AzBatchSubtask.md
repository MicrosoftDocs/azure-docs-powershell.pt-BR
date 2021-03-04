---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 622b25a4cd84fcdd6ffb8179b3990ac786733e06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890305"
---
# <span data-ttu-id="fae7f-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="fae7f-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="fae7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae7f-102">SYNOPSIS</span></span>
<span data-ttu-id="fae7f-103">Obtém as informações de subtarefa da tarefa especificada.</span><span class="sxs-lookup"><span data-stu-id="fae7f-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="fae7f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fae7f-104">SYNTAX</span></span>

### <span data-ttu-id="fae7f-105">ODataFilter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fae7f-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fae7f-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="fae7f-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae7f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fae7f-107">DESCRIPTION</span></span>
<span data-ttu-id="fae7f-108">O cmdlet **Get-AzBatchSubtask** recupera as informações de subtarefas sobre a tarefa especificada.</span><span class="sxs-lookup"><span data-stu-id="fae7f-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="fae7f-109">As subtarefas fornecem processamento paralelo para tarefas individuais e permitem o monitoramento preciso da execução e do progresso da tarefa.</span><span class="sxs-lookup"><span data-stu-id="fae7f-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="fae7f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fae7f-110">EXAMPLES</span></span>

### <span data-ttu-id="fae7f-111">Exemplo 1: Retornar todas as subtarefas para uma tarefa especificada</span><span class="sxs-lookup"><span data-stu-id="fae7f-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="fae7f-112">Esses comandos retornam todas as subtarefas da tarefa com a ID myTask.</span><span class="sxs-lookup"><span data-stu-id="fae7f-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="fae7f-113">Para fazer isso, o primeiro comando no exemplo cria uma referência de objeto às chaves de conta da conta em lotes contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="fae7f-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="fae7f-114">Essa referência de objeto é armazenada em uma variável chamada $context.</span><span class="sxs-lookup"><span data-stu-id="fae7f-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="fae7f-115">O segundo comando usa essa referência de objeto e o cmdlet **Get-AzBatchSubtask** para retornar todas as subtarefas para myTask, uma tarefa que é executado como parte do trabalho Job-01.</span><span class="sxs-lookup"><span data-stu-id="fae7f-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="fae7f-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fae7f-116">PARAMETERS</span></span>

### <span data-ttu-id="fae7f-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fae7f-117">-BatchContext</span></span>
<span data-ttu-id="fae7f-118">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="fae7f-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fae7f-119">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="fae7f-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fae7f-120">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="fae7f-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fae7f-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="fae7f-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fae7f-122">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fae7f-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fae7f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae7f-123">-DefaultProfile</span></span>
<span data-ttu-id="fae7f-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fae7f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae7f-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="fae7f-125">-JobId</span></span>
<span data-ttu-id="fae7f-126">Especifica a ID do trabalho que contém a tarefa cujas subtarefas esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fae7f-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="fae7f-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fae7f-127">-MaxCount</span></span>
<span data-ttu-id="fae7f-128">Especifica o número máximo de subtarefas a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="fae7f-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="fae7f-129">Se você especificar um valor zero (0) ou menor, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="fae7f-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="fae7f-130">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="fae7f-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="fae7f-131">-Task</span><span class="sxs-lookup"><span data-stu-id="fae7f-131">-Task</span></span>
<span data-ttu-id="fae7f-132">Especifica uma referência de objeto à tarefa que contém as subtarefas que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="fae7f-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="fae7f-133">Essa referência de objeto é criada usando o cmdlet Get-AzBatchTask e armazenar o objeto retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="fae7f-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="fae7f-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="fae7f-134">-TaskId</span></span>
<span data-ttu-id="fae7f-135">Especifica a ID da tarefa cuja subtarefas este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="fae7f-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="fae7f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae7f-136">CommonParameters</span></span>
<span data-ttu-id="fae7f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae7f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae7f-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fae7f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae7f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fae7f-139">INPUTS</span></span>

### <span data-ttu-id="fae7f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fae7f-140">System.String</span></span>

### <span data-ttu-id="fae7f-141">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="fae7f-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="fae7f-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fae7f-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fae7f-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fae7f-143">OUTPUTS</span></span>

### <span data-ttu-id="fae7f-144">Microsoft.Azure.Commands.Batch. Models.PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="fae7f-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="fae7f-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="fae7f-145">NOTES</span></span>

## <span data-ttu-id="fae7f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fae7f-146">RELATED LINKS</span></span>

[<span data-ttu-id="fae7f-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fae7f-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


