---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441211"
---
# <span data-ttu-id="d3d28-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d3d28-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="d3d28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3d28-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d28-103">Habilita um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="d3d28-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3d28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3d28-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3d28-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3d28-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d28-106">O cmdlet **Enable-AzureBatchJobSchedule** habilita um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d28-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="d3d28-107">Depois de habilitar um plano de trabalho, os trabalhos podem ser criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="d3d28-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="d3d28-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3d28-108">EXAMPLES</span></span>

### <span data-ttu-id="d3d28-109">Exemplo 1: habilitar um plano de trabalho</span><span class="sxs-lookup"><span data-stu-id="d3d28-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="d3d28-110">Esse comando habilita o agendamento de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="d3d28-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="d3d28-111">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="d3d28-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d3d28-112">OS</span><span class="sxs-lookup"><span data-stu-id="d3d28-112">PARAMETERS</span></span>

### <span data-ttu-id="d3d28-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d3d28-113">-BatchContext</span></span>
<span data-ttu-id="d3d28-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="d3d28-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d3d28-115">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="d3d28-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d3d28-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d3d28-116">-Id</span></span>
<span data-ttu-id="d3d28-117">Especifica a ID do agendamento de trabalho que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="d3d28-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="d3d28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d28-118">-DefaultProfile</span></span>
<span data-ttu-id="d3d28-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d28-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3d28-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d28-120">CommonParameters</span></span>
<span data-ttu-id="d3d28-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d28-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d28-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3d28-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d28-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3d28-123">INPUTS</span></span>

### <span data-ttu-id="d3d28-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d3d28-124">BatchAccountContext</span></span>
<span data-ttu-id="d3d28-125">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d3d28-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d3d28-126">String</span><span class="sxs-lookup"><span data-stu-id="d3d28-126">String</span></span>
<span data-ttu-id="d3d28-127">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d3d28-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d3d28-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3d28-128">OUTPUTS</span></span>

## <span data-ttu-id="d3d28-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3d28-129">NOTES</span></span>

## <span data-ttu-id="d3d28-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3d28-130">RELATED LINKS</span></span>

[<span data-ttu-id="d3d28-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d3d28-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d3d28-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d3d28-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d3d28-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d3d28-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="d3d28-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d3d28-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="d3d28-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d3d28-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="d3d28-136">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d3d28-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="d3d28-137">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="d3d28-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


