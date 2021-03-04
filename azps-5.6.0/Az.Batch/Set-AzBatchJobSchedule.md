---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: cf4512bc0d219c164be6543d5633a43c9052cc4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892229"
---
# <span data-ttu-id="415dc-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="415dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="415dc-102">SYNOPSIS</span></span>
<span data-ttu-id="415dc-103">Define um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="415dc-103">Sets a job schedule.</span></span>

## <span data-ttu-id="415dc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="415dc-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="415dc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="415dc-105">DESCRIPTION</span></span>
<span data-ttu-id="415dc-106">O cmdlet **Set-AzBatchJobSchedule** define um cronograma de trabalho no serviço batch do Azure.</span><span class="sxs-lookup"><span data-stu-id="415dc-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="415dc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="415dc-107">EXAMPLES</span></span>

### <span data-ttu-id="415dc-108">Exemplo 1: atualizar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="415dc-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="415dc-109">O primeiro comando obtém um trabalho usando **Get-AzBatchJobSchedule** e o armazena na variável $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="415dc-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="415dc-110">O segundo comando modifica o intervalo de recorrência no `$JobSchedule.Schedule` objeto.</span><span class="sxs-lookup"><span data-stu-id="415dc-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="415dc-111">O comando final atualiza o serviço Batch para corresponder ao objeto local no $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="415dc-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="415dc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="415dc-112">PARAMETERS</span></span>

### <span data-ttu-id="415dc-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="415dc-113">-BatchContext</span></span>
<span data-ttu-id="415dc-114">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="415dc-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="415dc-115">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="415dc-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="415dc-116">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="415dc-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="415dc-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="415dc-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="415dc-118">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="415dc-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="415dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415dc-119">-DefaultProfile</span></span>
<span data-ttu-id="415dc-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="415dc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="415dc-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-121">-JobSchedule</span></span>
<span data-ttu-id="415dc-122">Especifica um **objeto PSCloudJobSchedule** que representa um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="415dc-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="415dc-123">Para obter um **objeto PSCloudJobSchedule,** use o cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="415dc-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="415dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415dc-124">CommonParameters</span></span>
<span data-ttu-id="415dc-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="415dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415dc-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="415dc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415dc-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="415dc-127">INPUTS</span></span>

### <span data-ttu-id="415dc-128">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="415dc-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="415dc-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="415dc-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="415dc-130">OUTPUTS</span></span>

### <span data-ttu-id="415dc-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="415dc-131">System.Void</span></span>

## <span data-ttu-id="415dc-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="415dc-132">NOTES</span></span>

## <span data-ttu-id="415dc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="415dc-133">RELATED LINKS</span></span>

[<span data-ttu-id="415dc-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="415dc-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="415dc-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="415dc-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="415dc-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="415dc-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="415dc-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


