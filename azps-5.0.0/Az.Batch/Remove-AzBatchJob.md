---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116815"
---
# <span data-ttu-id="3cdd0-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3cdd0-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="3cdd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cdd0-102">SYNOPSIS</span></span>
<span data-ttu-id="3cdd0-103">Exclui um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="3cdd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cdd0-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cdd0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3cdd0-105">DESCRIPTION</span></span>
<span data-ttu-id="3cdd0-106">O cmdlet **Remove-AzBatchJob** exclui um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="3cdd0-107">Esse cmdlet solicita confirmação antes de remover um trabalho, a menos que você especifique o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="3cdd0-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="3cdd0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3cdd0-108">EXAMPLES</span></span>

### <span data-ttu-id="3cdd0-109">Exemplo 1: excluir um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="3cdd0-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="3cdd0-110">Esse comando exclui o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="3cdd0-111">O comando solicita confirmação antes de excluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="3cdd0-112">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3cdd0-113">Exemplo 2: excluir um trabalho em lotes sem confirmação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="3cdd0-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="3cdd0-114">Esse comando obtém o trabalho com o ID Job-000002 usando o cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="3cdd0-115">O comando passa aquele trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3cdd0-116">O comando exclui esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-116">The command deletes that job.</span></span>
<span data-ttu-id="3cdd0-117">Como o comando inclui o parâmetro *Force* , ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3cdd0-118">OS</span><span class="sxs-lookup"><span data-stu-id="3cdd0-118">PARAMETERS</span></span>

### <span data-ttu-id="3cdd0-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3cdd0-119">-BatchContext</span></span>
<span data-ttu-id="3cdd0-120">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3cdd0-121">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3cdd0-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3cdd0-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3cdd0-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3cdd0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cdd0-125">-DefaultProfile</span></span>
<span data-ttu-id="3cdd0-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cdd0-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3cdd0-127">-Force</span></span>
<span data-ttu-id="3cdd0-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3cdd0-129">-ID</span><span class="sxs-lookup"><span data-stu-id="3cdd0-129">-Id</span></span>
<span data-ttu-id="3cdd0-130">Especifica a ID do trabalho que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="3cdd0-131">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="3cdd0-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3cdd0-132">-Confirm</span></span>
<span data-ttu-id="3cdd0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cdd0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cdd0-134">-WhatIf</span></span>
<span data-ttu-id="3cdd0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cdd0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cdd0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cdd0-137">CommonParameters</span></span>
<span data-ttu-id="3cdd0-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cdd0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cdd0-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cdd0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cdd0-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3cdd0-140">INPUTS</span></span>

### <span data-ttu-id="3cdd0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3cdd0-141">System.String</span></span>

### <span data-ttu-id="3cdd0-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3cdd0-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3cdd0-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3cdd0-143">OUTPUTS</span></span>

### <span data-ttu-id="3cdd0-144">System. void</span><span class="sxs-lookup"><span data-stu-id="3cdd0-144">System.Void</span></span>

## <span data-ttu-id="3cdd0-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3cdd0-145">NOTES</span></span>

## <span data-ttu-id="3cdd0-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cdd0-146">RELATED LINKS</span></span>

[<span data-ttu-id="3cdd0-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3cdd0-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="3cdd0-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3cdd0-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="3cdd0-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3cdd0-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="3cdd0-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3cdd0-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3cdd0-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3cdd0-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="3cdd0-152">Parar-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3cdd0-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="3cdd0-153">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="3cdd0-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
