---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432251"
---
# <span data-ttu-id="655ee-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="655ee-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="655ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="655ee-102">SYNOPSIS</span></span>
<span data-ttu-id="655ee-103">Interrompe um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="655ee-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="655ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="655ee-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="655ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="655ee-105">DESCRIPTION</span></span>
<span data-ttu-id="655ee-106">O cmdlet **Stop-AzureBatchJobSchedule** interrompe um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="655ee-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="655ee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="655ee-107">EXAMPLES</span></span>

### <span data-ttu-id="655ee-108">Exemplo 1: interromper um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="655ee-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="655ee-109">Esse comando interrompe o agendamento de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="655ee-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="655ee-110">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="655ee-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="655ee-111">OS</span><span class="sxs-lookup"><span data-stu-id="655ee-111">PARAMETERS</span></span>

### <span data-ttu-id="655ee-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="655ee-112">-BatchContext</span></span>
<span data-ttu-id="655ee-113">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="655ee-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="655ee-114">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="655ee-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="655ee-115">-ID</span><span class="sxs-lookup"><span data-stu-id="655ee-115">-Id</span></span>
<span data-ttu-id="655ee-116">Especifica a ID do agendamento de trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="655ee-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="655ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="655ee-117">-DefaultProfile</span></span>
<span data-ttu-id="655ee-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="655ee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="655ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655ee-119">CommonParameters</span></span>
<span data-ttu-id="655ee-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="655ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655ee-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="655ee-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655ee-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="655ee-122">INPUTS</span></span>

### <span data-ttu-id="655ee-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="655ee-123">BatchAccountContext</span></span>
<span data-ttu-id="655ee-124">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="655ee-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="655ee-125">String</span><span class="sxs-lookup"><span data-stu-id="655ee-125">String</span></span>
<span data-ttu-id="655ee-126">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="655ee-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="655ee-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="655ee-127">OUTPUTS</span></span>

## <span data-ttu-id="655ee-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="655ee-128">NOTES</span></span>

## <span data-ttu-id="655ee-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="655ee-129">RELATED LINKS</span></span>

[<span data-ttu-id="655ee-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="655ee-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="655ee-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="655ee-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="655ee-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="655ee-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="655ee-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="655ee-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="655ee-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="655ee-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="655ee-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="655ee-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="655ee-136">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="655ee-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


