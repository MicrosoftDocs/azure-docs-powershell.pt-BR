---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: 83ac1df0259d39dd1db301e836479193b17f1dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891514"
---
# <span data-ttu-id="fe8f4-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fe8f4-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="fe8f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8f4-103">Exclui uma tarefa Batch.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="fe8f4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fe8f4-104">SYNTAX</span></span>

### <span data-ttu-id="fe8f4-105">Id</span><span class="sxs-lookup"><span data-stu-id="fe8f4-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8f4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe8f4-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe8f4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fe8f4-107">DESCRIPTION</span></span>
<span data-ttu-id="fe8f4-108">O cmdlet **Remove-AzBatchTask** exclui uma tarefa do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="fe8f4-109">Este cmdlet solicita a confirmação, a menos que você especifique o *parâmetro Force.*</span><span class="sxs-lookup"><span data-stu-id="fe8f4-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="fe8f4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe8f4-110">EXAMPLES</span></span>

### <span data-ttu-id="fe8f4-111">Exemplo 1: Excluir uma tarefa em lotes por ID</span><span class="sxs-lookup"><span data-stu-id="fe8f4-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="fe8f4-112">Este comando exclui uma tarefa que tem a ID Task23 no trabalho que tem a ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="fe8f4-113">O comando solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="fe8f4-114">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fe8f4-115">Exemplo 2: Excluir uma tarefa em lote usando o pipeline sem confirmação</span><span class="sxs-lookup"><span data-stu-id="fe8f4-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="fe8f4-116">Este comando obtém a tarefa Batch que tem a ID Task26 no trabalho que tem a ID Job-000001 usando o cmdlet **Get-AzBatchTask.**</span><span class="sxs-lookup"><span data-stu-id="fe8f4-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="fe8f4-117">O comando passa essa tarefa para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fe8f4-118">O comando exclui essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-118">The command deletes that task.</span></span>
<span data-ttu-id="fe8f4-119">Este comando especifica o *parâmetro Force.*</span><span class="sxs-lookup"><span data-stu-id="fe8f4-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="fe8f4-120">Portanto, o comando não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="fe8f4-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fe8f4-121">PARAMETERS</span></span>

### <span data-ttu-id="fe8f4-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fe8f4-122">-BatchContext</span></span>
<span data-ttu-id="fe8f4-123">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fe8f4-124">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fe8f4-125">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fe8f4-126">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fe8f4-127">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fe8f4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8f4-128">-DefaultProfile</span></span>
<span data-ttu-id="fe8f4-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe8f4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="fe8f4-130">-Force</span></span>
<span data-ttu-id="fe8f4-131">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8f4-132">-Id</span><span class="sxs-lookup"><span data-stu-id="fe8f4-132">-Id</span></span>
<span data-ttu-id="fe8f4-133">Especifica a ID da tarefa que esse cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="fe8f4-134">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="fe8f4-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe8f4-135">-InputObject</span></span>
<span data-ttu-id="fe8f4-136">Especifica a tarefa que esse cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="fe8f4-137">Para obter um **objeto PSCloudTask,** use o cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="fe8f4-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="fe8f4-138">-JobId</span></span>
<span data-ttu-id="fe8f4-139">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="fe8f4-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe8f4-140">-Confirm</span></span>
<span data-ttu-id="fe8f4-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe8f4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe8f4-142">-WhatIf</span></span>
<span data-ttu-id="fe8f4-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe8f4-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe8f4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8f4-145">CommonParameters</span></span>
<span data-ttu-id="fe8f4-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe8f4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8f4-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe8f4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8f4-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe8f4-148">INPUTS</span></span>

### <span data-ttu-id="fe8f4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="fe8f4-149">System.String</span></span>

### <span data-ttu-id="fe8f4-150">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="fe8f4-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="fe8f4-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fe8f4-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fe8f4-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fe8f4-152">OUTPUTS</span></span>

### <span data-ttu-id="fe8f4-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="fe8f4-153">System.Void</span></span>

## <span data-ttu-id="fe8f4-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="fe8f4-154">NOTES</span></span>

## <span data-ttu-id="fe8f4-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe8f4-155">RELATED LINKS</span></span>

[<span data-ttu-id="fe8f4-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fe8f4-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fe8f4-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fe8f4-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="fe8f4-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fe8f4-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="fe8f4-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fe8f4-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="fe8f4-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fe8f4-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="fe8f4-161">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="fe8f4-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
