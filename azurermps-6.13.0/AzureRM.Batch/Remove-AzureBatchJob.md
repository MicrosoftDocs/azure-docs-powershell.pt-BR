---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: fa7dede61cd19ec0ea0a4ccd59f2eca3e0cc8f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602804"
---
# <span data-ttu-id="5d846-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5d846-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="5d846-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d846-102">SYNOPSIS</span></span>
<span data-ttu-id="5d846-103">Exclui um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="5d846-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d846-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d846-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d846-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d846-105">DESCRIPTION</span></span>
<span data-ttu-id="5d846-106">O cmdlet **Remove-AzureBatchJob** exclui um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d846-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="5d846-107">Esse cmdlet solicita confirmação antes de remover um trabalho, a menos que você especifique o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="5d846-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="5d846-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d846-108">EXAMPLES</span></span>

### <span data-ttu-id="5d846-109">Exemplo 1: excluir um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="5d846-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="5d846-110">Esse comando exclui o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="5d846-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5d846-111">O comando solicita confirmação antes de excluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d846-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="5d846-112">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="5d846-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5d846-113">Exemplo 2: excluir um trabalho em lotes sem confirmação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="5d846-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="5d846-114">Esse comando obtém o trabalho com o ID Job-000002 usando o cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="5d846-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="5d846-115">O comando passa aquele trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d846-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5d846-116">O comando exclui esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d846-116">The command deletes that job.</span></span>
<span data-ttu-id="5d846-117">Como o comando inclui o parâmetro *Force* , ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="5d846-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5d846-118">OS</span><span class="sxs-lookup"><span data-stu-id="5d846-118">PARAMETERS</span></span>

### <span data-ttu-id="5d846-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5d846-119">-BatchContext</span></span>
<span data-ttu-id="5d846-120">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="5d846-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5d846-121">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="5d846-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5d846-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="5d846-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5d846-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="5d846-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5d846-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5d846-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5d846-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d846-125">-DefaultProfile</span></span>
<span data-ttu-id="5d846-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d846-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d846-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5d846-127">-Force</span></span>
<span data-ttu-id="5d846-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5d846-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d846-129">-ID</span><span class="sxs-lookup"><span data-stu-id="5d846-129">-Id</span></span>
<span data-ttu-id="5d846-130">Especifica a ID do trabalho que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="5d846-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="5d846-131">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="5d846-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d846-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5d846-132">-Confirm</span></span>
<span data-ttu-id="5d846-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d846-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d846-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d846-134">-WhatIf</span></span>
<span data-ttu-id="5d846-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d846-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d846-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d846-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d846-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d846-137">CommonParameters</span></span>
<span data-ttu-id="5d846-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d846-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d846-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d846-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d846-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d846-140">INPUTS</span></span>

### <span data-ttu-id="5d846-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5d846-141">System.String</span></span>

### <span data-ttu-id="5d846-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5d846-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="5d846-143">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5d846-143">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="5d846-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d846-144">OUTPUTS</span></span>

### <span data-ttu-id="5d846-145">System. void</span><span class="sxs-lookup"><span data-stu-id="5d846-145">System.Void</span></span>

## <span data-ttu-id="5d846-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d846-146">NOTES</span></span>

## <span data-ttu-id="5d846-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d846-147">RELATED LINKS</span></span>

[<span data-ttu-id="5d846-148">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5d846-148">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="5d846-149">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5d846-149">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5d846-150">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5d846-150">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="5d846-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5d846-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5d846-152">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5d846-152">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5d846-153">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5d846-153">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="5d846-154">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="5d846-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


