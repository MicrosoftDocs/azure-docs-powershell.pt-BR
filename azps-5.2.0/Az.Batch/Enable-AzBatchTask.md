---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262433"
---
# <span data-ttu-id="72fc9-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="72fc9-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="72fc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="72fc9-103">Reativa uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="72fc9-103">Reactivates a task.</span></span>

## <span data-ttu-id="72fc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72fc9-104">SYNTAX</span></span>

### <span data-ttu-id="72fc9-105">%</span><span class="sxs-lookup"><span data-stu-id="72fc9-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72fc9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="72fc9-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72fc9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72fc9-107">DESCRIPTION</span></span>
<span data-ttu-id="72fc9-108">O cmdlet **Enable-AzBatchTask** reativa uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="72fc9-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="72fc9-109">Se uma tarefa tiver se esgotado sua contagem de repetição, esse cmdlet no entanto permitirá que ele seja executado.</span><span class="sxs-lookup"><span data-stu-id="72fc9-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="72fc9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72fc9-110">EXAMPLES</span></span>

### <span data-ttu-id="72fc9-111">Exemplo 1: reativar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="72fc9-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="72fc9-112">Esse comando reativará a tarefa Tarefa2 no Job Job7.</span><span class="sxs-lookup"><span data-stu-id="72fc9-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="72fc9-113">Exemplo 2: reativar uma tarefa usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="72fc9-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="72fc9-114">Esse comando obtém a tarefa em lotes que tem a ID Task3 no trabalho que tem a ID Job8 usando o cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="72fc9-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="72fc9-115">O comando transmite essa tarefa para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="72fc9-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="72fc9-116">O comando reativará a tarefa.</span><span class="sxs-lookup"><span data-stu-id="72fc9-116">The command reactivates that task.</span></span>

## <span data-ttu-id="72fc9-117">OS</span><span class="sxs-lookup"><span data-stu-id="72fc9-117">PARAMETERS</span></span>

### <span data-ttu-id="72fc9-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="72fc9-118">-BatchContext</span></span>
<span data-ttu-id="72fc9-119">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="72fc9-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="72fc9-120">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="72fc9-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="72fc9-121">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="72fc9-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="72fc9-122">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="72fc9-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="72fc9-123">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="72fc9-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="72fc9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fc9-124">-DefaultProfile</span></span>
<span data-ttu-id="72fc9-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72fc9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72fc9-126">-ID</span><span class="sxs-lookup"><span data-stu-id="72fc9-126">-Id</span></span>
<span data-ttu-id="72fc9-127">Especifica a ID da tarefa a ser reativada.</span><span class="sxs-lookup"><span data-stu-id="72fc9-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="72fc9-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="72fc9-128">-JobId</span></span>
<span data-ttu-id="72fc9-129">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="72fc9-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="72fc9-130">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="72fc9-130">-Task</span></span>
<span data-ttu-id="72fc9-131">Especifica a tarefa que esse cmdlet reativa.</span><span class="sxs-lookup"><span data-stu-id="72fc9-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="72fc9-132">Para obter um objeto **PSCloudTask** , use o cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="72fc9-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="72fc9-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72fc9-133">-Confirm</span></span>
<span data-ttu-id="72fc9-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fc9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72fc9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72fc9-135">-WhatIf</span></span>
<span data-ttu-id="72fc9-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72fc9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72fc9-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72fc9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72fc9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fc9-138">CommonParameters</span></span>
<span data-ttu-id="72fc9-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fc9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fc9-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72fc9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fc9-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72fc9-141">INPUTS</span></span>

### <span data-ttu-id="72fc9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="72fc9-142">System.String</span></span>

### <span data-ttu-id="72fc9-143">Microsoft.Azure.Commands.Batch. Modelos. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="72fc9-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="72fc9-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="72fc9-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="72fc9-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72fc9-145">OUTPUTS</span></span>

### <span data-ttu-id="72fc9-146">System. void</span><span class="sxs-lookup"><span data-stu-id="72fc9-146">System.Void</span></span>

## <span data-ttu-id="72fc9-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72fc9-147">NOTES</span></span>

## <span data-ttu-id="72fc9-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72fc9-148">RELATED LINKS</span></span>

[<span data-ttu-id="72fc9-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="72fc9-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="72fc9-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="72fc9-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="72fc9-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="72fc9-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="72fc9-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="72fc9-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="72fc9-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="72fc9-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="72fc9-154">Parar-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="72fc9-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


