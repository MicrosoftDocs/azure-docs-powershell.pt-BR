---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: fabc983e8c7b70685477a640d408beb65251b253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891524"
---
# <span data-ttu-id="30327-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="30327-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="30327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30327-102">SYNOPSIS</span></span>
<span data-ttu-id="30327-103">Desabilita um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="30327-103">Disables a Batch job.</span></span>

## <span data-ttu-id="30327-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="30327-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30327-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="30327-105">DESCRIPTION</span></span>
<span data-ttu-id="30327-106">O cmdlet **Disable-AzBatchJob** desabilita um trabalho do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="30327-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="30327-107">Depois de habilitar um trabalho, novas tarefas podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="30327-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="30327-108">Os trabalhos desabilitados não são executados em novas tarefas.</span><span class="sxs-lookup"><span data-stu-id="30327-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="30327-109">Você pode habilitar um trabalho desabilitado mais tarde.</span><span class="sxs-lookup"><span data-stu-id="30327-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="30327-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30327-110">EXAMPLES</span></span>

### <span data-ttu-id="30327-111">Exemplo 1: Desabilitar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="30327-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="30327-112">Este comando desabilita o trabalho que tem a ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="30327-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="30327-113">O comando encerra tarefas ativas para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="30327-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="30327-114">Use o cmdlet **Get-AzBatchAccountKey** para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="30327-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="30327-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="30327-115">PARAMETERS</span></span>

### <span data-ttu-id="30327-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="30327-116">-BatchContext</span></span>
<span data-ttu-id="30327-117">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="30327-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="30327-118">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="30327-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="30327-119">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="30327-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="30327-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="30327-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="30327-121">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="30327-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="30327-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30327-122">-DefaultProfile</span></span>
<span data-ttu-id="30327-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="30327-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30327-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="30327-124">-DisableJobOption</span></span>
<span data-ttu-id="30327-125">Especifica o que fazer com tarefas ativas associadas ao trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="30327-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="30327-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="30327-126">Valid values are:</span></span>
- <span data-ttu-id="30327-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="30327-127">Requeue</span></span>
- <span data-ttu-id="30327-128">Encerrar</span><span class="sxs-lookup"><span data-stu-id="30327-128">Terminate</span></span>
- <span data-ttu-id="30327-129">Wait</span><span class="sxs-lookup"><span data-stu-id="30327-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30327-130">-Id</span><span class="sxs-lookup"><span data-stu-id="30327-130">-Id</span></span>
<span data-ttu-id="30327-131">Especifica a ID do trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="30327-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30327-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30327-132">CommonParameters</span></span>
<span data-ttu-id="30327-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30327-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30327-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30327-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30327-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30327-135">INPUTS</span></span>

### <span data-ttu-id="30327-136">System.String</span><span class="sxs-lookup"><span data-stu-id="30327-136">System.String</span></span>

### <span data-ttu-id="30327-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="30327-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="30327-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="30327-138">OUTPUTS</span></span>

### <span data-ttu-id="30327-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="30327-139">System.Void</span></span>

## <span data-ttu-id="30327-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="30327-140">NOTES</span></span>

## <span data-ttu-id="30327-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30327-141">RELATED LINKS</span></span>

[<span data-ttu-id="30327-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="30327-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="30327-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="30327-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="30327-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="30327-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="30327-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="30327-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="30327-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="30327-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="30327-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="30327-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="30327-148">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="30327-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
