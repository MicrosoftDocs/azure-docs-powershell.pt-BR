---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432252"
---
# <span data-ttu-id="27f30-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="27f30-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="27f30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27f30-102">SYNOPSIS</span></span>
<span data-ttu-id="27f30-103">Interrompe um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="27f30-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27f30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27f30-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27f30-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27f30-105">DESCRIPTION</span></span>
<span data-ttu-id="27f30-106">O cmdlet **Stop-AzureBatchJob** interrompe um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="27f30-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="27f30-107">Esse comando marca o trabalho como concluído.</span><span class="sxs-lookup"><span data-stu-id="27f30-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="27f30-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27f30-108">EXAMPLES</span></span>

### <span data-ttu-id="27f30-109">Exemplo 1: parar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="27f30-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="27f30-110">Esse comando interrompe o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="27f30-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="27f30-111">O comando especifica um motivo pelo qual você optou por interromper o trabalho.</span><span class="sxs-lookup"><span data-stu-id="27f30-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="27f30-112">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="27f30-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="27f30-113">OS</span><span class="sxs-lookup"><span data-stu-id="27f30-113">PARAMETERS</span></span>

### <span data-ttu-id="27f30-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="27f30-114">-BatchContext</span></span>
<span data-ttu-id="27f30-115">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="27f30-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="27f30-116">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="27f30-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="27f30-117">-ID</span><span class="sxs-lookup"><span data-stu-id="27f30-117">-Id</span></span>
<span data-ttu-id="27f30-118">Especifica a ID do trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="27f30-118">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="27f30-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="27f30-119">-TerminateReason</span></span>
<span data-ttu-id="27f30-120">Especifica o motivo pelo qual você decidiu parar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="27f30-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="27f30-121">Esse cmdlet armazena esse texto como a propriedade **TerminateReason** do trabalho.</span><span class="sxs-lookup"><span data-stu-id="27f30-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="27f30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f30-122">-DefaultProfile</span></span>
<span data-ttu-id="27f30-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27f30-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27f30-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f30-124">CommonParameters</span></span>
<span data-ttu-id="27f30-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27f30-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f30-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27f30-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f30-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27f30-127">INPUTS</span></span>

### <span data-ttu-id="27f30-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="27f30-128">BatchAccountContext</span></span>
<span data-ttu-id="27f30-129">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="27f30-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="27f30-130">String</span><span class="sxs-lookup"><span data-stu-id="27f30-130">String</span></span>
<span data-ttu-id="27f30-131">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="27f30-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="27f30-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27f30-132">OUTPUTS</span></span>

## <span data-ttu-id="27f30-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27f30-133">NOTES</span></span>

## <span data-ttu-id="27f30-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27f30-134">RELATED LINKS</span></span>

[<span data-ttu-id="27f30-135">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="27f30-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="27f30-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="27f30-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="27f30-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="27f30-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="27f30-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="27f30-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="27f30-139">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="27f30-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="27f30-140">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="27f30-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="27f30-141">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="27f30-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


