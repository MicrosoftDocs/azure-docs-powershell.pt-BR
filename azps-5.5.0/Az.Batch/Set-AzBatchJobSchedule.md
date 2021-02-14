---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116597"
---
# <span data-ttu-id="daabc-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="daabc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daabc-102">SYNOPSIS</span></span>
<span data-ttu-id="daabc-103">Define um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="daabc-103">Sets a job schedule.</span></span>

## <span data-ttu-id="daabc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daabc-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daabc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="daabc-105">DESCRIPTION</span></span>
<span data-ttu-id="daabc-106">O cmdlet **Set-AzBatch JobSchedule** define um cronograma de trabalho no serviço Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="daabc-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="daabc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="daabc-107">EXAMPLES</span></span>

### <span data-ttu-id="daabc-108">Exemplo 1: Atualizar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="daabc-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="daabc-109">O primeiro comando obtém um trabalho usando **Get-AzBatch JobSchedule** e, em seguida, o armazena na variável $JobSchedule dados.</span><span class="sxs-lookup"><span data-stu-id="daabc-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="daabc-110">O segundo comando modifica o intervalo de recorrência no `$JobSchedule.Schedule` objeto.</span><span class="sxs-lookup"><span data-stu-id="daabc-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="daabc-111">O comando final atualiza o serviço Lote para corresponder ao objeto local no $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="daabc-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="daabc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daabc-112">PARAMETERS</span></span>

### <span data-ttu-id="daabc-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="daabc-113">-BatchContext</span></span>
<span data-ttu-id="daabc-114">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="daabc-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="daabc-115">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="daabc-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="daabc-116">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="daabc-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="daabc-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="daabc-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="daabc-118">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="daabc-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="daabc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daabc-119">-DefaultProfile</span></span>
<span data-ttu-id="daabc-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="daabc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daabc-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-121">-JobSchedule</span></span>
<span data-ttu-id="daabc-122">Especifica um objeto **PSCloudJobSchedule** que representa um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="daabc-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="daabc-123">Para obter um **objeto PSCloudJobSchedule,** use o cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="daabc-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="daabc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daabc-124">CommonParameters</span></span>
<span data-ttu-id="daabc-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daabc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daabc-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="daabc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daabc-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="daabc-127">INPUTS</span></span>

### <span data-ttu-id="daabc-128">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="daabc-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="daabc-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="daabc-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="daabc-130">OUTPUTS</span></span>

### <span data-ttu-id="daabc-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="daabc-131">System.Void</span></span>

## <span data-ttu-id="daabc-132">Notas</span><span class="sxs-lookup"><span data-stu-id="daabc-132">NOTES</span></span>

## <span data-ttu-id="daabc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daabc-133">RELATED LINKS</span></span>

[<span data-ttu-id="daabc-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="daabc-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="daabc-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="daabc-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="daabc-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="daabc-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="daabc-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


