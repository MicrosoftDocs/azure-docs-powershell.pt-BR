---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610842"
---
# <span data-ttu-id="fcf71-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="fcf71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcf71-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf71-103">Define um plano de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fcf71-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcf71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcf71-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcf71-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcf71-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf71-106">O cmdlet **set-AzureBatchJobSchedule** define um cronograma de trabalho no serviço de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf71-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="fcf71-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcf71-107">EXAMPLES</span></span>

## <span data-ttu-id="fcf71-108">OS</span><span class="sxs-lookup"><span data-stu-id="fcf71-108">PARAMETERS</span></span>

### <span data-ttu-id="fcf71-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fcf71-109">-BatchContext</span></span>
<span data-ttu-id="fcf71-110">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="fcf71-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fcf71-111">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="fcf71-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fcf71-112">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-112">-JobSchedule</span></span>
<span data-ttu-id="fcf71-113">Especifica um objeto **PSCloudJobSchedule** que representa um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fcf71-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="fcf71-114">Para obter um objeto **PSCloudJobSchedule** , use o cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="fcf71-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="fcf71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf71-115">-DefaultProfile</span></span>
<span data-ttu-id="fcf71-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf71-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcf71-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf71-117">CommonParameters</span></span>
<span data-ttu-id="fcf71-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf71-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf71-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf71-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf71-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcf71-120">INPUTS</span></span>

### <span data-ttu-id="fcf71-121">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fcf71-121">BatchAccountContext</span></span>
<span data-ttu-id="fcf71-122">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fcf71-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fcf71-123">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="fcf71-124">O parâmetro ' JobSchedule ' aceita o valor do tipo ' PSCloudJobSchedule ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fcf71-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="fcf71-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcf71-125">OUTPUTS</span></span>

## <span data-ttu-id="fcf71-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcf71-126">NOTES</span></span>

## <span data-ttu-id="fcf71-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcf71-127">RELATED LINKS</span></span>

[<span data-ttu-id="fcf71-128">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="fcf71-129">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="fcf71-130">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="fcf71-131">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="fcf71-132">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="fcf71-133">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fcf71-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


