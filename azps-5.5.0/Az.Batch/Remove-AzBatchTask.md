---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: e067eea86e3a4350d08c5c0f9ec34b4af65b07f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116964"
---
# <span data-ttu-id="ba6b8-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ba6b8-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="ba6b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6b8-103">Exclui uma tarefa em lotes.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="ba6b8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba6b8-104">SYNTAX</span></span>

### <span data-ttu-id="ba6b8-105">Id</span><span class="sxs-lookup"><span data-stu-id="ba6b8-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba6b8-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba6b8-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba6b8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba6b8-107">DESCRIPTION</span></span>
<span data-ttu-id="ba6b8-108">O **cmdlet Remove-AzBatchTask** exclui uma tarefa do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="ba6b8-109">Este cmdlet solicita confirmação, a menos que você especifique o *parâmetro* Force.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="ba6b8-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ba6b8-110">EXAMPLES</span></span>

### <span data-ttu-id="ba6b8-111">Exemplo 1: Excluir uma tarefa em lotes por ID</span><span class="sxs-lookup"><span data-stu-id="ba6b8-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="ba6b8-112">Esse comando exclui uma tarefa que tem a Tarefa23 de ID sob o trabalho que tem a ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ba6b8-113">O comando solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="ba6b8-114">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ba6b8-115">Exemplo 2: Excluir uma tarefa em lotes usando o pipeline sem confirmação</span><span class="sxs-lookup"><span data-stu-id="ba6b8-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="ba6b8-116">Esse comando obtém a tarefa Em lotes que tem a Tarefa de ID26 no trabalho que tem o Trabalho de ID-000001 usando o cmdlet **Get-AzBatchTask.**</span><span class="sxs-lookup"><span data-stu-id="ba6b8-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="ba6b8-117">O comando passa essa tarefa para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ba6b8-118">O comando exclui essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-118">The command deletes that task.</span></span>
<span data-ttu-id="ba6b8-119">Esse comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="ba6b8-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ba6b8-120">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ba6b8-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba6b8-121">PARAMETERS</span></span>

### <span data-ttu-id="ba6b8-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ba6b8-122">-BatchContext</span></span>
<span data-ttu-id="ba6b8-123">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba6b8-124">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ba6b8-125">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ba6b8-126">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ba6b8-127">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ba6b8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6b8-128">-DefaultProfile</span></span>
<span data-ttu-id="ba6b8-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba6b8-130">-Forçar</span><span class="sxs-lookup"><span data-stu-id="ba6b8-130">-Force</span></span>
<span data-ttu-id="ba6b8-131">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba6b8-132">-ID</span><span class="sxs-lookup"><span data-stu-id="ba6b8-132">-Id</span></span>
<span data-ttu-id="ba6b8-133">Especifica a ID da tarefa que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="ba6b8-134">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ba6b8-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba6b8-135">-InputObject</span></span>
<span data-ttu-id="ba6b8-136">Especifica a tarefa que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="ba6b8-137">Para obter um **objeto PSCloudTask,** use Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="ba6b8-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="ba6b8-138">-JobId</span></span>
<span data-ttu-id="ba6b8-139">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="ba6b8-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ba6b8-140">-Confirm</span></span>
<span data-ttu-id="ba6b8-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba6b8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba6b8-142">-WhatIf</span></span>
<span data-ttu-id="ba6b8-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba6b8-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba6b8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6b8-145">CommonParameters</span></span>
<span data-ttu-id="ba6b8-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba6b8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6b8-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba6b8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6b8-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="ba6b8-148">INPUTS</span></span>

### <span data-ttu-id="ba6b8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ba6b8-149">System.String</span></span>

### <span data-ttu-id="ba6b8-150">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ba6b8-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="ba6b8-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba6b8-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ba6b8-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="ba6b8-152">OUTPUTS</span></span>

### <span data-ttu-id="ba6b8-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="ba6b8-153">System.Void</span></span>

## <span data-ttu-id="ba6b8-154">Notas</span><span class="sxs-lookup"><span data-stu-id="ba6b8-154">NOTES</span></span>

## <span data-ttu-id="ba6b8-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba6b8-155">RELATED LINKS</span></span>

[<span data-ttu-id="ba6b8-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba6b8-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ba6b8-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ba6b8-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="ba6b8-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ba6b8-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="ba6b8-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ba6b8-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="ba6b8-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ba6b8-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="ba6b8-161">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="ba6b8-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
