---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: 43ec21e3c2bb7a0f80dc14c8051e4c3fed20ac42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901515"
---
# <span data-ttu-id="f6bfb-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f6bfb-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="f6bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bfb-103">Interrompe um trabalho em lote.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-103">Stops a Batch job.</span></span>

## <span data-ttu-id="f6bfb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f6bfb-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6bfb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f6bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="f6bfb-106">O cmdlet **Stop-AzBatchJob** interrompe um trabalho do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="f6bfb-107">Este comando marca o trabalho como concluído.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="f6bfb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6bfb-108">EXAMPLES</span></span>

### <span data-ttu-id="f6bfb-109">Exemplo 1: Parar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="f6bfb-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="f6bfb-110">Este comando interrompe o trabalho que tem a ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f6bfb-111">O comando especifica um motivo pelo qual você optou por interromper o trabalho.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="f6bfb-112">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f6bfb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f6bfb-113">PARAMETERS</span></span>

### <span data-ttu-id="f6bfb-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f6bfb-114">-BatchContext</span></span>
<span data-ttu-id="f6bfb-115">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f6bfb-116">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f6bfb-117">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f6bfb-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f6bfb-119">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f6bfb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6bfb-120">-DefaultProfile</span></span>
<span data-ttu-id="f6bfb-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6bfb-122">-Id</span><span class="sxs-lookup"><span data-stu-id="f6bfb-122">-Id</span></span>
<span data-ttu-id="f6bfb-123">Especifica a ID do trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="f6bfb-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="f6bfb-124">-TerminateReason</span></span>
<span data-ttu-id="f6bfb-125">Especifica o motivo pelo qual você decidiu interromper o trabalho.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="f6bfb-126">Este cmdlet armazena esse texto como a **propriedade TerminateReason** do trabalho.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="f6bfb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bfb-127">CommonParameters</span></span>
<span data-ttu-id="f6bfb-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6bfb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bfb-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6bfb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bfb-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6bfb-130">INPUTS</span></span>

### <span data-ttu-id="f6bfb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f6bfb-131">System.String</span></span>

### <span data-ttu-id="f6bfb-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f6bfb-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f6bfb-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f6bfb-133">OUTPUTS</span></span>

### <span data-ttu-id="f6bfb-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="f6bfb-134">System.Void</span></span>

## <span data-ttu-id="f6bfb-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="f6bfb-135">NOTES</span></span>

## <span data-ttu-id="f6bfb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6bfb-136">RELATED LINKS</span></span>

[<span data-ttu-id="f6bfb-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f6bfb-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="f6bfb-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f6bfb-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="f6bfb-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f6bfb-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f6bfb-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f6bfb-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="f6bfb-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f6bfb-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="f6bfb-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f6bfb-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="f6bfb-143">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="f6bfb-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
