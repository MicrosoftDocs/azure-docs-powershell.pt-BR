---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 85226072ca3e94a1e9cd10cd5a29e4fbee229c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887029"
---
# <span data-ttu-id="60a40-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="60a40-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="60a40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a40-102">SYNOPSIS</span></span>
<span data-ttu-id="60a40-103">Interrompe um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="60a40-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="60a40-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="60a40-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a40-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="60a40-105">DESCRIPTION</span></span>
<span data-ttu-id="60a40-106">O cmdlet **Stop-AzBatchJobSchedule** interrompe um cronograma de trabalho do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="60a40-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="60a40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60a40-107">EXAMPLES</span></span>

### <span data-ttu-id="60a40-108">Exemplo 1: Interromper um agendamento de trabalho</span><span class="sxs-lookup"><span data-stu-id="60a40-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="60a40-109">Este comando interrompe o cronograma de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="60a40-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="60a40-110">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="60a40-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="60a40-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="60a40-111">PARAMETERS</span></span>

### <span data-ttu-id="60a40-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="60a40-112">-BatchContext</span></span>
<span data-ttu-id="60a40-113">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="60a40-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="60a40-114">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="60a40-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="60a40-115">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="60a40-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="60a40-116">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="60a40-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="60a40-117">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="60a40-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="60a40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a40-118">-DefaultProfile</span></span>
<span data-ttu-id="60a40-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="60a40-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a40-120">-Id</span><span class="sxs-lookup"><span data-stu-id="60a40-120">-Id</span></span>
<span data-ttu-id="60a40-121">Especifica a ID do cronograma de trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="60a40-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="60a40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a40-122">CommonParameters</span></span>
<span data-ttu-id="60a40-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a40-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60a40-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a40-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60a40-125">INPUTS</span></span>

### <span data-ttu-id="60a40-126">System.String</span><span class="sxs-lookup"><span data-stu-id="60a40-126">System.String</span></span>

### <span data-ttu-id="60a40-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="60a40-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="60a40-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="60a40-128">OUTPUTS</span></span>

### <span data-ttu-id="60a40-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="60a40-129">System.Void</span></span>

## <span data-ttu-id="60a40-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="60a40-130">NOTES</span></span>

## <span data-ttu-id="60a40-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60a40-131">RELATED LINKS</span></span>

[<span data-ttu-id="60a40-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="60a40-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="60a40-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="60a40-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="60a40-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="60a40-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="60a40-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="60a40-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="60a40-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="60a40-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="60a40-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="60a40-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="60a40-138">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="60a40-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
