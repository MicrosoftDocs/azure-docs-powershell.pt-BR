---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426431"
---
# <span data-ttu-id="1b400-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="1b400-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b400-102">SYNOPSIS</span></span>
<span data-ttu-id="1b400-103">Define um plano de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b400-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b400-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b400-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b400-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b400-105">DESCRIPTION</span></span>
<span data-ttu-id="1b400-106">O cmdlet **set-AzureBatchJobSchedule** define um cronograma de trabalho no serviço de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b400-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="1b400-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b400-107">EXAMPLES</span></span>

## <span data-ttu-id="1b400-108">OS</span><span class="sxs-lookup"><span data-stu-id="1b400-108">PARAMETERS</span></span>

### <span data-ttu-id="1b400-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1b400-109">-BatchContext</span></span>
<span data-ttu-id="1b400-110">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="1b400-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1b400-111">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="1b400-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1b400-112">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="1b400-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1b400-113">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="1b400-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1b400-114">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1b400-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1b400-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b400-115">-DefaultProfile</span></span>
<span data-ttu-id="1b400-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b400-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b400-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-117">-JobSchedule</span></span>
<span data-ttu-id="1b400-118">Especifica um objeto **PSCloudJobSchedule** que representa um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b400-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="1b400-119">Para obter um objeto **PSCloudJobSchedule** , use o cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="1b400-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="1b400-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b400-120">CommonParameters</span></span>
<span data-ttu-id="1b400-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b400-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b400-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b400-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b400-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b400-123">INPUTS</span></span>

### <span data-ttu-id="1b400-124">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="1b400-125">Parâmetros: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b400-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="1b400-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1b400-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="1b400-127">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b400-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="1b400-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b400-128">OUTPUTS</span></span>

### <span data-ttu-id="1b400-129">System. void</span><span class="sxs-lookup"><span data-stu-id="1b400-129">System.Void</span></span>

## <span data-ttu-id="1b400-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b400-130">NOTES</span></span>

## <span data-ttu-id="1b400-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b400-131">RELATED LINKS</span></span>

[<span data-ttu-id="1b400-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="1b400-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="1b400-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="1b400-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="1b400-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="1b400-137">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1b400-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


