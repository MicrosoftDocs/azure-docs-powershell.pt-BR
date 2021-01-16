---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258334"
---
# <span data-ttu-id="3ef49-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="3ef49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ef49-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef49-103">Define um plano de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3ef49-103">Sets a job schedule.</span></span>

## <span data-ttu-id="3ef49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ef49-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ef49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ef49-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef49-106">O cmdlet **set-AzBatchJobSchedule** define um cronograma de trabalho no serviço de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef49-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="3ef49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ef49-107">EXAMPLES</span></span>

### <span data-ttu-id="3ef49-108">Exemplo 1: atualizar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="3ef49-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="3ef49-109">O primeiro comando obtém um trabalho usando **Get-AzBatchJobSchedule** e, em seguida, armazena-o na variável $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="3ef49-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="3ef49-110">O segundo comando modifica o intervalo de recorrência no `$JobSchedule.Schedule` objeto.</span><span class="sxs-lookup"><span data-stu-id="3ef49-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="3ef49-111">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="3ef49-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="3ef49-112">OS</span><span class="sxs-lookup"><span data-stu-id="3ef49-112">PARAMETERS</span></span>

### <span data-ttu-id="3ef49-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3ef49-113">-BatchContext</span></span>
<span data-ttu-id="3ef49-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="3ef49-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3ef49-115">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="3ef49-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3ef49-116">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="3ef49-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3ef49-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="3ef49-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3ef49-118">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3ef49-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3ef49-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef49-119">-DefaultProfile</span></span>
<span data-ttu-id="3ef49-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef49-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ef49-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-121">-JobSchedule</span></span>
<span data-ttu-id="3ef49-122">Especifica um objeto **PSCloudJobSchedule** que representa um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3ef49-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="3ef49-123">Para obter um objeto **PSCloudJobSchedule** , use o cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="3ef49-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef49-124">CommonParameters</span></span>
<span data-ttu-id="3ef49-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef49-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ef49-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef49-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ef49-127">INPUTS</span></span>

### <span data-ttu-id="3ef49-128">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="3ef49-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3ef49-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3ef49-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ef49-130">OUTPUTS</span></span>

### <span data-ttu-id="3ef49-131">System. void</span><span class="sxs-lookup"><span data-stu-id="3ef49-131">System.Void</span></span>

## <span data-ttu-id="3ef49-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ef49-132">NOTES</span></span>

## <span data-ttu-id="3ef49-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ef49-133">RELATED LINKS</span></span>

[<span data-ttu-id="3ef49-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="3ef49-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="3ef49-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="3ef49-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="3ef49-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="3ef49-139">Parar-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef49-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


