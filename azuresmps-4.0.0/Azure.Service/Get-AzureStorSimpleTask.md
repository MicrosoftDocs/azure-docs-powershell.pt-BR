---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945552"
---
# <span data-ttu-id="2e2cb-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="2e2cb-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="2e2cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2cb-103">Obtém o status de uma tarefa em um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="2e2cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e2cb-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e2cb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="2e2cb-106">O cmdlet **Get-AzureStorSimpleTask** recupera o status de uma tarefa que é executada assincronamente em um dispositivo Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="2e2cb-107">Embora você gerencie um dispositivo StorSimple, a maioria das ações criar, ler, atualizar e excluir pode ser executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="2e2cb-108">O Windows PowerShell retorna uma **TaskId**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="2e2cb-109">Use a ID para obter o status atual da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="2e2cb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e2cb-110">EXAMPLES</span></span>

### <span data-ttu-id="2e2cb-111">Exemplo 1: obter o status de uma tarefa</span><span class="sxs-lookup"><span data-stu-id="2e2cb-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="2e2cb-112">Esse comando obtém o status da tarefa com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="2e2cb-113">Os resultados mostram que a tarefa tem o status concluído e um resultado de êxito.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="2e2cb-114">OS</span><span class="sxs-lookup"><span data-stu-id="2e2cb-114">PARAMETERS</span></span>

### <span data-ttu-id="2e2cb-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2e2cb-115">-InstanceId</span></span>
<span data-ttu-id="2e2cb-116">Especifica a ID da tarefa para a qual esse cmdlet rastreia o status.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2cb-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2e2cb-117">-Profile</span></span>
<span data-ttu-id="2e2cb-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e2cb-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2cb-120">CommonParameters</span></span>
<span data-ttu-id="2e2cb-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2cb-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e2cb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2cb-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e2cb-123">INPUTS</span></span>

### <span data-ttu-id="2e2cb-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2e2cb-124">None</span></span>

## <span data-ttu-id="2e2cb-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e2cb-125">OUTPUTS</span></span>

### <span data-ttu-id="2e2cb-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="2e2cb-126">JobStatusInfo</span></span>
<span data-ttu-id="2e2cb-127">Esse cmdlet retorna um objeto **TaskStatusInfo** que contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="2e2cb-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="2e2cb-128">**Erro**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-128">**Error**.</span></span>
<span data-ttu-id="2e2cb-129">**ErrorDetails** , que contém **código** e **mensagem**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="2e2cb-130">**TaskId**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-130">**TaskId**.</span></span>
<span data-ttu-id="2e2cb-131">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-131">**String**.</span></span>
<span data-ttu-id="2e2cb-132">A ID da tarefa para a qual o status é retornado.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="2e2cb-133">**TaskSteps**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-133">**TaskSteps**.</span></span>
<span data-ttu-id="2e2cb-134">**IList \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="2e2cb-135">Cada objeto **TaskStep** contém **detalhe** , **ErrorCode** , **mensagem** , **resultado** e **status**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="2e2cb-136">**Resultado**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-136">**Result**.</span></span>
<span data-ttu-id="2e2cb-137">**TaskResult** , que contém o resultado geral da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="2e2cb-138">Os valores válidos são: falha, êxito, PartialSuccess, cancelado e inválido.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="2e2cb-139">**Status**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-139">**Status**.</span></span>
<span data-ttu-id="2e2cb-140">**TaskStatus** , que contém o status geral de execução da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="2e2cb-141">Os valores válidos são: InProgress, invalide e Completed.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="2e2cb-142">**TaskResult**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-142">**TaskResult**.</span></span>
<span data-ttu-id="2e2cb-143">**TaskResult** , um valor calculado com base em **resultado** e **status**.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="2e2cb-144">Os valores válidos são: falha, êxito, InProgress, PartialSuccess, cancelado e inválido.</span><span class="sxs-lookup"><span data-stu-id="2e2cb-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="2e2cb-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e2cb-145">NOTES</span></span>

## <span data-ttu-id="2e2cb-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e2cb-146">RELATED LINKS</span></span>

