---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440119"
---
# <span data-ttu-id="24cd7-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="24cd7-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="24cd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="24cd7-103">Exclui uma tarefa em lotes.</span><span class="sxs-lookup"><span data-stu-id="24cd7-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24cd7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24cd7-104">SYNTAX</span></span>

### <span data-ttu-id="24cd7-105">%</span><span class="sxs-lookup"><span data-stu-id="24cd7-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24cd7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="24cd7-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24cd7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24cd7-107">DESCRIPTION</span></span>
<span data-ttu-id="24cd7-108">O cmdlet **Remove-AzureBatchTask** exclui uma tarefa em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="24cd7-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="24cd7-109">Esse cmdlet solicita confirmação, a menos que você especifique o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="24cd7-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="24cd7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24cd7-110">EXAMPLES</span></span>

### <span data-ttu-id="24cd7-111">Exemplo 1: excluir uma tarefa em lote por ID</span><span class="sxs-lookup"><span data-stu-id="24cd7-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="24cd7-112">Esse comando exclui uma tarefa com a ID Task23 sob o trabalho que tem o ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="24cd7-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="24cd7-113">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="24cd7-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="24cd7-114">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="24cd7-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="24cd7-115">Exemplo 2: excluir uma tarefa em lote usando o pipeline sem confirmação</span><span class="sxs-lookup"><span data-stu-id="24cd7-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="24cd7-116">Esse comando obtém a tarefa em lotes que tem a ID Task26 no trabalho com o ID Job-000001 usando o cmdlet **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="24cd7-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="24cd7-117">O comando transmite essa tarefa para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="24cd7-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="24cd7-118">O comando exclui essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="24cd7-118">The command deletes that task.</span></span>
<span data-ttu-id="24cd7-119">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="24cd7-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="24cd7-120">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="24cd7-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="24cd7-121">OS</span><span class="sxs-lookup"><span data-stu-id="24cd7-121">PARAMETERS</span></span>

### <span data-ttu-id="24cd7-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="24cd7-122">-BatchContext</span></span>
<span data-ttu-id="24cd7-123">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="24cd7-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="24cd7-124">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="24cd7-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="24cd7-125">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="24cd7-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="24cd7-126">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="24cd7-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="24cd7-127">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="24cd7-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="24cd7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cd7-128">-DefaultProfile</span></span>
<span data-ttu-id="24cd7-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24cd7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24cd7-130">-Force</span><span class="sxs-lookup"><span data-stu-id="24cd7-130">-Force</span></span>
<span data-ttu-id="24cd7-131">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="24cd7-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cd7-132">-ID</span><span class="sxs-lookup"><span data-stu-id="24cd7-132">-Id</span></span>
<span data-ttu-id="24cd7-133">Especifica a ID da tarefa que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="24cd7-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="24cd7-134">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="24cd7-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="24cd7-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24cd7-135">-InputObject</span></span>
<span data-ttu-id="24cd7-136">Especifica a tarefa que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="24cd7-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="24cd7-137">Para obter um objeto **PSCloudTask** , use o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="24cd7-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="24cd7-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="24cd7-138">-JobId</span></span>
<span data-ttu-id="24cd7-139">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="24cd7-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="24cd7-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24cd7-140">-Confirm</span></span>
<span data-ttu-id="24cd7-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24cd7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cd7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cd7-142">-WhatIf</span></span>
<span data-ttu-id="24cd7-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24cd7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cd7-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24cd7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cd7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cd7-145">CommonParameters</span></span>
<span data-ttu-id="24cd7-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24cd7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cd7-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24cd7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cd7-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24cd7-148">INPUTS</span></span>

### <span data-ttu-id="24cd7-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="24cd7-149">BatchAccountContext</span></span>
<span data-ttu-id="24cd7-150">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="24cd7-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="24cd7-151">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="24cd7-151">PSCloudTask</span></span>
<span data-ttu-id="24cd7-152">O parâmetro ' InputObject ' aceita o valor do tipo ' PSCloudTask ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="24cd7-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="24cd7-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24cd7-153">OUTPUTS</span></span>

## <span data-ttu-id="24cd7-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24cd7-154">NOTES</span></span>

## <span data-ttu-id="24cd7-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24cd7-155">RELATED LINKS</span></span>

[<span data-ttu-id="24cd7-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="24cd7-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="24cd7-157">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="24cd7-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="24cd7-158">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="24cd7-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="24cd7-159">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="24cd7-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="24cd7-160">Parar-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="24cd7-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="24cd7-161">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="24cd7-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


