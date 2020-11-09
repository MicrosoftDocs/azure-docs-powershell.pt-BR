---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282261"
---
# <span data-ttu-id="e7e14-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7e14-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="e7e14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7e14-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e14-103">Interrompe um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="e7e14-103">Stops a Batch job.</span></span>

## <span data-ttu-id="e7e14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7e14-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e14-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7e14-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e14-106">O cmdlet **Stop-AzBatchJob** interrompe um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e14-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="e7e14-107">Esse comando marca o trabalho como concluído.</span><span class="sxs-lookup"><span data-stu-id="e7e14-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="e7e14-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7e14-108">EXAMPLES</span></span>

### <span data-ttu-id="e7e14-109">Exemplo 1: parar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="e7e14-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="e7e14-110">Esse comando interrompe o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="e7e14-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e7e14-111">O comando especifica um motivo pelo qual você optou por interromper o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e7e14-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="e7e14-112">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="e7e14-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e7e14-113">OS</span><span class="sxs-lookup"><span data-stu-id="e7e14-113">PARAMETERS</span></span>

### <span data-ttu-id="e7e14-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7e14-114">-BatchContext</span></span>
<span data-ttu-id="e7e14-115">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e7e14-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7e14-116">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e7e14-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7e14-117">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="e7e14-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7e14-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e7e14-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7e14-119">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e7e14-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7e14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e14-120">-DefaultProfile</span></span>
<span data-ttu-id="e7e14-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e14-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7e14-122">-ID</span><span class="sxs-lookup"><span data-stu-id="e7e14-122">-Id</span></span>
<span data-ttu-id="e7e14-123">Especifica a ID do trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="e7e14-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e7e14-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="e7e14-124">-TerminateReason</span></span>
<span data-ttu-id="e7e14-125">Especifica o motivo pelo qual você decidiu parar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e7e14-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="e7e14-126">Esse cmdlet armazena esse texto como a propriedade **TerminateReason** do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e7e14-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e14-127">CommonParameters</span></span>
<span data-ttu-id="e7e14-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e14-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7e14-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e14-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7e14-130">INPUTS</span></span>

### <span data-ttu-id="e7e14-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e7e14-131">System.String</span></span>

### <span data-ttu-id="e7e14-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7e14-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e7e14-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7e14-133">OUTPUTS</span></span>

### <span data-ttu-id="e7e14-134">System. void</span><span class="sxs-lookup"><span data-stu-id="e7e14-134">System.Void</span></span>

## <span data-ttu-id="e7e14-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7e14-135">NOTES</span></span>

## <span data-ttu-id="e7e14-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7e14-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7e14-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7e14-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="e7e14-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7e14-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="e7e14-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7e14-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e7e14-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7e14-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e7e14-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7e14-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="e7e14-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e7e14-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="e7e14-143">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="e7e14-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
