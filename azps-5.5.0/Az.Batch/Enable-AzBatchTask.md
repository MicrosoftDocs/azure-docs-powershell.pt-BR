---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116604"
---
# <span data-ttu-id="de6ea-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="de6ea-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="de6ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="de6ea-103">Reativa uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="de6ea-103">Reactivates a task.</span></span>

## <span data-ttu-id="de6ea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de6ea-104">SYNTAX</span></span>

### <span data-ttu-id="de6ea-105">Id</span><span class="sxs-lookup"><span data-stu-id="de6ea-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de6ea-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="de6ea-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de6ea-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="de6ea-107">DESCRIPTION</span></span>
<span data-ttu-id="de6ea-108">O cmdlet **Enable-AzBatchTask** reativa uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="de6ea-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="de6ea-109">Se uma tarefa tiver desgastado sua contagem de tentativa, esse cmdlet, no entanto, permitirá que ela seja executado.</span><span class="sxs-lookup"><span data-stu-id="de6ea-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="de6ea-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de6ea-110">EXAMPLES</span></span>

### <span data-ttu-id="de6ea-111">Exemplo 1: Reativar uma tarefa</span><span class="sxs-lookup"><span data-stu-id="de6ea-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="de6ea-112">Esse comando reativa a tarefa Tarefa2 no trabalho 7.</span><span class="sxs-lookup"><span data-stu-id="de6ea-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="de6ea-113">Exemplo 2: Reativar uma tarefa usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="de6ea-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="de6ea-114">Esse comando obtém a tarefa Lote que tem a ID Tarefa3 no trabalho que tem a ID Job8 usando o cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="de6ea-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="de6ea-115">O comando passa essa tarefa para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="de6ea-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="de6ea-116">O comando reativa essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="de6ea-116">The command reactivates that task.</span></span>

## <span data-ttu-id="de6ea-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de6ea-117">PARAMETERS</span></span>

### <span data-ttu-id="de6ea-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="de6ea-118">-BatchContext</span></span>
<span data-ttu-id="de6ea-119">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="de6ea-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="de6ea-120">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="de6ea-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="de6ea-121">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="de6ea-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="de6ea-122">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="de6ea-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="de6ea-123">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="de6ea-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="de6ea-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6ea-124">-DefaultProfile</span></span>
<span data-ttu-id="de6ea-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="de6ea-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de6ea-126">-ID</span><span class="sxs-lookup"><span data-stu-id="de6ea-126">-Id</span></span>
<span data-ttu-id="de6ea-127">Especifica a ID da tarefa a ser reativada.</span><span class="sxs-lookup"><span data-stu-id="de6ea-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="de6ea-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="de6ea-128">-JobId</span></span>
<span data-ttu-id="de6ea-129">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="de6ea-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="de6ea-130">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="de6ea-130">-Task</span></span>
<span data-ttu-id="de6ea-131">Especifica a tarefa que este cmdlet reativa.</span><span class="sxs-lookup"><span data-stu-id="de6ea-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="de6ea-132">Para obter um **objeto PSCloudTask,** use Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de6ea-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="de6ea-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="de6ea-133">-Confirm</span></span>
<span data-ttu-id="de6ea-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de6ea-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de6ea-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de6ea-135">-WhatIf</span></span>
<span data-ttu-id="de6ea-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="de6ea-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de6ea-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de6ea-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de6ea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6ea-138">CommonParameters</span></span>
<span data-ttu-id="de6ea-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de6ea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6ea-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de6ea-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6ea-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="de6ea-141">INPUTS</span></span>

### <span data-ttu-id="de6ea-142">System.String</span><span class="sxs-lookup"><span data-stu-id="de6ea-142">System.String</span></span>

### <span data-ttu-id="de6ea-143">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="de6ea-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="de6ea-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="de6ea-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="de6ea-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="de6ea-145">OUTPUTS</span></span>

### <span data-ttu-id="de6ea-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="de6ea-146">System.Void</span></span>

## <span data-ttu-id="de6ea-147">Notas</span><span class="sxs-lookup"><span data-stu-id="de6ea-147">NOTES</span></span>

## <span data-ttu-id="de6ea-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de6ea-148">RELATED LINKS</span></span>

[<span data-ttu-id="de6ea-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="de6ea-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="de6ea-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="de6ea-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="de6ea-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="de6ea-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="de6ea-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="de6ea-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="de6ea-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="de6ea-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="de6ea-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="de6ea-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


