---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610845"
---
# <span data-ttu-id="bf3bf-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bf3bf-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="bf3bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="bf3bf-103">Reativa uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf3bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf3bf-104">SYNTAX</span></span>

### <span data-ttu-id="bf3bf-105">%</span><span class="sxs-lookup"><span data-stu-id="bf3bf-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf3bf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bf3bf-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf3bf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf3bf-107">DESCRIPTION</span></span>
<span data-ttu-id="bf3bf-108">O cmdlet **Enable-AzureBatchTask** reativa uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="bf3bf-109">Se uma tarefa tiver se esgotado sua contagem de repetição, esse cmdlet no entanto permitirá que ele seja executado.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="bf3bf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf3bf-110">EXAMPLES</span></span>

### <span data-ttu-id="bf3bf-111">Exemplo 1: reativar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="bf3bf-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="bf3bf-112">Esse comando reativará a tarefa Tarefa2 no Job Job7.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="bf3bf-113">Exemplo 2: reativar uma tarefa usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="bf3bf-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="bf3bf-114">Esse comando obtém a tarefa em lotes que tem a ID Task3 no trabalho que tem a ID Job8 usando o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="bf3bf-115">O comando transmite essa tarefa para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf3bf-116">O comando reativará a tarefa.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-116">The command reactivates that task.</span></span>

## <span data-ttu-id="bf3bf-117">OS</span><span class="sxs-lookup"><span data-stu-id="bf3bf-117">PARAMETERS</span></span>

### <span data-ttu-id="bf3bf-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf3bf-118">-BatchContext</span></span>
<span data-ttu-id="bf3bf-119">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bf3bf-120">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="bf3bf-121">-ID</span><span class="sxs-lookup"><span data-stu-id="bf3bf-121">-Id</span></span>
<span data-ttu-id="bf3bf-122">Especifica a ID da tarefa a ser reativada.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-122">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3bf-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="bf3bf-123">-JobId</span></span>
<span data-ttu-id="bf3bf-124">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-124">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3bf-125">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="bf3bf-125">-Task</span></span>
<span data-ttu-id="bf3bf-126">Especifica a tarefa que esse cmdlet reativa.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="bf3bf-127">Para obter um objeto **PSCloudTask** , use o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3bf-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf3bf-128">-Confirm</span></span>
<span data-ttu-id="bf3bf-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf3bf-130">-WhatIf</span></span>
<span data-ttu-id="bf3bf-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf3bf-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3bf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf3bf-133">-DefaultProfile</span></span>
<span data-ttu-id="bf3bf-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf3bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf3bf-135">CommonParameters</span></span>
<span data-ttu-id="bf3bf-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf3bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf3bf-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf3bf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf3bf-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf3bf-138">INPUTS</span></span>

### <span data-ttu-id="bf3bf-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf3bf-139">BatchAccountContext</span></span>
<span data-ttu-id="bf3bf-140">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bf3bf-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bf3bf-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bf3bf-141">PSCloudTask</span></span>
<span data-ttu-id="bf3bf-142">O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="bf3bf-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="bf3bf-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf3bf-143">OUTPUTS</span></span>

## <span data-ttu-id="bf3bf-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf3bf-144">NOTES</span></span>

## <span data-ttu-id="bf3bf-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf3bf-145">RELATED LINKS</span></span>

[<span data-ttu-id="bf3bf-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bf3bf-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bf3bf-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bf3bf-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="bf3bf-148">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bf3bf-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="bf3bf-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bf3bf-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="bf3bf-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bf3bf-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="bf3bf-151">Parar-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bf3bf-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


