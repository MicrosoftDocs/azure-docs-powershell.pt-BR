---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942430"
---
# <span data-ttu-id="34cd7-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34cd7-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="34cd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="34cd7-103">Remove um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="34cd7-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="34cd7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34cd7-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34cd7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34cd7-105">DESCRIPTION</span></span>
<span data-ttu-id="34cd7-106">O cmdlet **Remove-AzBatchJobSchedule** remove um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="34cd7-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="34cd7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34cd7-107">EXAMPLES</span></span>

### <span data-ttu-id="34cd7-108">Exemplo 1: excluir um cronograma de trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="34cd7-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="34cd7-109">Esse comando exclui o agendamento de trabalho que tem a ID MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="34cd7-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="34cd7-110">O comando solicita confirmação antes de excluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="34cd7-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="34cd7-111">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="34cd7-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="34cd7-112">Exemplo 2: excluir um trabalho em lotes sem confirmação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="34cd7-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="34cd7-113">Esse comando obtém o agendamento de trabalho que tem a ID MyJobSchedule usando o cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="34cd7-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="34cd7-114">O comando passa o agendamento do trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="34cd7-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="34cd7-115">O comando exclui o agendamento do trabalho.</span><span class="sxs-lookup"><span data-stu-id="34cd7-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="34cd7-116">Como o comando inclui o parâmetro *Force* , ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="34cd7-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="34cd7-117">OS</span><span class="sxs-lookup"><span data-stu-id="34cd7-117">PARAMETERS</span></span>

### <span data-ttu-id="34cd7-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="34cd7-118">-BatchContext</span></span>
<span data-ttu-id="34cd7-119">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="34cd7-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="34cd7-120">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="34cd7-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="34cd7-121">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="34cd7-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="34cd7-122">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="34cd7-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="34cd7-123">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="34cd7-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="34cd7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34cd7-124">-DefaultProfile</span></span>
<span data-ttu-id="34cd7-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34cd7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34cd7-126">-Force</span><span class="sxs-lookup"><span data-stu-id="34cd7-126">-Force</span></span>
<span data-ttu-id="34cd7-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="34cd7-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34cd7-128">-ID</span><span class="sxs-lookup"><span data-stu-id="34cd7-128">-Id</span></span>
<span data-ttu-id="34cd7-129">Especifica a ID do plano de trabalho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="34cd7-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="34cd7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34cd7-130">-Confirm</span></span>
<span data-ttu-id="34cd7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34cd7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34cd7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34cd7-132">-WhatIf</span></span>
<span data-ttu-id="34cd7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34cd7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34cd7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34cd7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34cd7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34cd7-135">CommonParameters</span></span>
<span data-ttu-id="34cd7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34cd7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34cd7-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34cd7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34cd7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34cd7-138">INPUTS</span></span>

### <span data-ttu-id="34cd7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="34cd7-139">System.String</span></span>

### <span data-ttu-id="34cd7-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="34cd7-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="34cd7-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34cd7-141">OUTPUTS</span></span>

### <span data-ttu-id="34cd7-142">System. void</span><span class="sxs-lookup"><span data-stu-id="34cd7-142">System.Void</span></span>

## <span data-ttu-id="34cd7-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34cd7-143">NOTES</span></span>

## <span data-ttu-id="34cd7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34cd7-144">RELATED LINKS</span></span>

[<span data-ttu-id="34cd7-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34cd7-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="34cd7-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34cd7-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="34cd7-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34cd7-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="34cd7-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34cd7-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="34cd7-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34cd7-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="34cd7-150">Parar-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="34cd7-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


