---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: eb15991e0bf7aefd60b53dbb02785a1b2004cb22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441202"
---
# <span data-ttu-id="29003-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="29003-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="29003-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29003-102">SYNOPSIS</span></span>
<span data-ttu-id="29003-103">Atualiza um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="29003-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29003-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29003-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29003-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29003-105">DESCRIPTION</span></span>
<span data-ttu-id="29003-106">O cmdlet **set-AzureBatchJob** atualiza um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="29003-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="29003-107">Use o cmdlet Get-AzureBatchJob para obter um objeto **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="29003-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="29003-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="29003-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="29003-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29003-109">EXAMPLES</span></span>

### <span data-ttu-id="29003-110">Exemplo 1: atualizar um trabalho</span><span class="sxs-lookup"><span data-stu-id="29003-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="29003-111">O primeiro comando obtém um pool usando **Get-AzureBatchJob** e, em seguida, armazena-o na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="29003-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="29003-112">O segundo comando modifica a especificação de prioridade no objeto $Job.</span><span class="sxs-lookup"><span data-stu-id="29003-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="29003-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Job.</span><span class="sxs-lookup"><span data-stu-id="29003-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="29003-114">OS</span><span class="sxs-lookup"><span data-stu-id="29003-114">PARAMETERS</span></span>

### <span data-ttu-id="29003-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="29003-115">-BatchContext</span></span>
<span data-ttu-id="29003-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="29003-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="29003-117">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="29003-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="29003-118">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="29003-118">-Job</span></span>
<span data-ttu-id="29003-119">Especifica um **PSCloudJob** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="29003-119">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29003-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29003-120">-DefaultProfile</span></span>
<span data-ttu-id="29003-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29003-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29003-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29003-122">CommonParameters</span></span>
<span data-ttu-id="29003-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29003-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29003-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29003-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29003-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29003-125">INPUTS</span></span>

### <span data-ttu-id="29003-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="29003-126">BatchAccountContext</span></span>
<span data-ttu-id="29003-127">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="29003-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="29003-128">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="29003-128">PSCloudJob</span></span>
<span data-ttu-id="29003-129">O parâmetro ' Job ' aceita o valor do tipo ' PSCloudJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="29003-129">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="29003-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29003-130">OUTPUTS</span></span>

## <span data-ttu-id="29003-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29003-131">NOTES</span></span>

## <span data-ttu-id="29003-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29003-132">RELATED LINKS</span></span>

[<span data-ttu-id="29003-133">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="29003-133">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="29003-134">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="29003-134">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="29003-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="29003-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="29003-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="29003-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="29003-137">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="29003-137">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="29003-138">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="29003-138">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="29003-139">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="29003-139">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="29003-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="29003-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


