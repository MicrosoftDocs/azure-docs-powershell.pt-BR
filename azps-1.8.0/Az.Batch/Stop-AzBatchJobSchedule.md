---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 94c4fe3292e07045382e432377111d0849db2668
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93784978"
---
# <span data-ttu-id="55fe5-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55fe5-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="55fe5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="55fe5-103">Interrompe um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="55fe5-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="55fe5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55fe5-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55fe5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="55fe5-106">O cmdlet **Stop-AzBatchJobSchedule** interrompe um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="55fe5-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="55fe5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="55fe5-108">Exemplo 1: interromper um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="55fe5-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="55fe5-109">Esse comando interrompe o agendamento de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="55fe5-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="55fe5-110">Use o cmdlet Get-AzBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="55fe5-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="55fe5-111">OS</span><span class="sxs-lookup"><span data-stu-id="55fe5-111">PARAMETERS</span></span>

### <span data-ttu-id="55fe5-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="55fe5-112">-BatchContext</span></span>
<span data-ttu-id="55fe5-113">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="55fe5-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="55fe5-114">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="55fe5-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="55fe5-115">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="55fe5-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="55fe5-116">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="55fe5-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="55fe5-117">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="55fe5-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="55fe5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fe5-118">-DefaultProfile</span></span>
<span data-ttu-id="55fe5-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55fe5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55fe5-120">-ID</span><span class="sxs-lookup"><span data-stu-id="55fe5-120">-Id</span></span>
<span data-ttu-id="55fe5-121">Especifica a ID do agendamento de trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="55fe5-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="55fe5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fe5-122">CommonParameters</span></span>
<span data-ttu-id="55fe5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55fe5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fe5-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55fe5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fe5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55fe5-125">INPUTS</span></span>

### <span data-ttu-id="55fe5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="55fe5-126">System.String</span></span>

### <span data-ttu-id="55fe5-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="55fe5-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="55fe5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55fe5-128">OUTPUTS</span></span>

### <span data-ttu-id="55fe5-129">System. void</span><span class="sxs-lookup"><span data-stu-id="55fe5-129">System.Void</span></span>

## <span data-ttu-id="55fe5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55fe5-130">NOTES</span></span>

## <span data-ttu-id="55fe5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55fe5-131">RELATED LINKS</span></span>

[<span data-ttu-id="55fe5-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55fe5-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="55fe5-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55fe5-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="55fe5-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="55fe5-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="55fe5-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55fe5-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="55fe5-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55fe5-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="55fe5-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="55fe5-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="55fe5-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="55fe5-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


