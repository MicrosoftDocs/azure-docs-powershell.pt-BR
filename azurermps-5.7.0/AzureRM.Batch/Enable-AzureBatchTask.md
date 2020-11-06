---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 09e2c8dd4ce1eab68eb2a4237e022034696f9769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609978"
---
# <span data-ttu-id="c0a1e-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c0a1e-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="c0a1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a1e-103">Reativa uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0a1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0a1e-104">SYNTAX</span></span>

### <span data-ttu-id="c0a1e-105">%</span><span class="sxs-lookup"><span data-stu-id="c0a1e-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0a1e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c0a1e-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0a1e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0a1e-107">DESCRIPTION</span></span>
<span data-ttu-id="c0a1e-108">O cmdlet **Enable-AzureBatchTask** reativa uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="c0a1e-109">Se uma tarefa tiver se esgotado sua contagem de repetição, esse cmdlet no entanto permitirá que ele seja executado.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="c0a1e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0a1e-110">EXAMPLES</span></span>

### <span data-ttu-id="c0a1e-111">Exemplo 1: reativar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="c0a1e-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="c0a1e-112">Esse comando reativará a tarefa Tarefa2 no Job Job7.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="c0a1e-113">Exemplo 2: reativar uma tarefa usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="c0a1e-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="c0a1e-114">Esse comando obtém a tarefa em lotes que tem a ID Task3 no trabalho que tem a ID Job8 usando o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="c0a1e-115">O comando transmite essa tarefa para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0a1e-116">O comando reativará a tarefa.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-116">The command reactivates that task.</span></span>

## <span data-ttu-id="c0a1e-117">OS</span><span class="sxs-lookup"><span data-stu-id="c0a1e-117">PARAMETERS</span></span>

### <span data-ttu-id="c0a1e-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c0a1e-118">-BatchContext</span></span>
<span data-ttu-id="c0a1e-119">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c0a1e-120">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c0a1e-121">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c0a1e-122">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c0a1e-123">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c0a1e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a1e-124">-DefaultProfile</span></span>
<span data-ttu-id="c0a1e-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0a1e-126">-ID</span><span class="sxs-lookup"><span data-stu-id="c0a1e-126">-Id</span></span>
<span data-ttu-id="c0a1e-127">Especifica a ID da tarefa a ser reativada.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a1e-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="c0a1e-128">-JobId</span></span>
<span data-ttu-id="c0a1e-129">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a1e-130">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="c0a1e-130">-Task</span></span>
<span data-ttu-id="c0a1e-131">Especifica a tarefa que esse cmdlet reativa.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="c0a1e-132">Para obter um objeto **PSCloudTask** , use o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a1e-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0a1e-133">-Confirm</span></span>
<span data-ttu-id="c0a1e-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a1e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0a1e-135">-WhatIf</span></span>
<span data-ttu-id="c0a1e-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0a1e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a1e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a1e-138">CommonParameters</span></span>
<span data-ttu-id="c0a1e-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0a1e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a1e-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a1e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a1e-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0a1e-141">INPUTS</span></span>

### <span data-ttu-id="c0a1e-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c0a1e-142">BatchAccountContext</span></span>
<span data-ttu-id="c0a1e-143">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c0a1e-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c0a1e-144">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c0a1e-144">PSCloudTask</span></span>
<span data-ttu-id="c0a1e-145">O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="c0a1e-145">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="c0a1e-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0a1e-146">OUTPUTS</span></span>

## <span data-ttu-id="c0a1e-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0a1e-147">NOTES</span></span>

## <span data-ttu-id="c0a1e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0a1e-148">RELATED LINKS</span></span>

[<span data-ttu-id="c0a1e-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c0a1e-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c0a1e-150">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c0a1e-150">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="c0a1e-151">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c0a1e-151">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="c0a1e-152">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c0a1e-152">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="c0a1e-153">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c0a1e-153">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="c0a1e-154">Parar-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c0a1e-154">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


