---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116601"
---
# <span data-ttu-id="74f16-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74f16-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="74f16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74f16-102">SYNOPSIS</span></span>
<span data-ttu-id="74f16-103">Exclui um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="74f16-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="74f16-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74f16-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f16-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="74f16-105">DESCRIPTION</span></span>
<span data-ttu-id="74f16-106">O **cmdlet Remove-AzBatch Job** exclui um trabalho do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="74f16-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="74f16-107">Este cmdlet solicita a confirmação antes de remover um trabalho, a menos que você especifique o *parâmetro Forçar.*</span><span class="sxs-lookup"><span data-stu-id="74f16-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="74f16-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="74f16-108">EXAMPLES</span></span>

### <span data-ttu-id="74f16-109">Exemplo 1: Excluir um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="74f16-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="74f16-110">Esse comando exclui o trabalho que tem a ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="74f16-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="74f16-111">O comando solicita a confirmação antes de excluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="74f16-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="74f16-112">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="74f16-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="74f16-113">Exemplo 2: Excluir um trabalho em lote sem confirmação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="74f16-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="74f16-114">Esse comando obtém o trabalho que tem o trabalho de ID Job-000002 usando o cmdlet Get-AzBatchJob usuário.</span><span class="sxs-lookup"><span data-stu-id="74f16-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="74f16-115">O comando passa esse trabalho para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="74f16-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="74f16-116">O comando exclui esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="74f16-116">The command deletes that job.</span></span>
<span data-ttu-id="74f16-117">Como o comando inclui o parâmetro *Forçar,* ele não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="74f16-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="74f16-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74f16-118">PARAMETERS</span></span>

### <span data-ttu-id="74f16-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="74f16-119">-BatchContext</span></span>
<span data-ttu-id="74f16-120">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="74f16-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="74f16-121">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="74f16-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="74f16-122">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="74f16-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="74f16-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="74f16-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="74f16-124">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="74f16-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="74f16-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f16-125">-DefaultProfile</span></span>
<span data-ttu-id="74f16-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="74f16-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f16-127">-Forçar</span><span class="sxs-lookup"><span data-stu-id="74f16-127">-Force</span></span>
<span data-ttu-id="74f16-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="74f16-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74f16-129">-ID</span><span class="sxs-lookup"><span data-stu-id="74f16-129">-Id</span></span>
<span data-ttu-id="74f16-130">Especifica a ID do trabalho que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="74f16-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="74f16-131">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="74f16-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="74f16-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="74f16-132">-Confirm</span></span>
<span data-ttu-id="74f16-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74f16-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74f16-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f16-134">-WhatIf</span></span>
<span data-ttu-id="74f16-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="74f16-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f16-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74f16-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74f16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f16-137">CommonParameters</span></span>
<span data-ttu-id="74f16-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f16-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74f16-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f16-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="74f16-140">INPUTS</span></span>

### <span data-ttu-id="74f16-141">System.String</span><span class="sxs-lookup"><span data-stu-id="74f16-141">System.String</span></span>

### <span data-ttu-id="74f16-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="74f16-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="74f16-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="74f16-143">OUTPUTS</span></span>

### <span data-ttu-id="74f16-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="74f16-144">System.Void</span></span>

## <span data-ttu-id="74f16-145">Notas</span><span class="sxs-lookup"><span data-stu-id="74f16-145">NOTES</span></span>

## <span data-ttu-id="74f16-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74f16-146">RELATED LINKS</span></span>

[<span data-ttu-id="74f16-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74f16-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="74f16-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74f16-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="74f16-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74f16-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="74f16-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="74f16-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="74f16-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74f16-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="74f16-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74f16-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="74f16-153">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="74f16-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
