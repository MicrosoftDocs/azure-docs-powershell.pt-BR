---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610847"
---
# <span data-ttu-id="4ca66-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4ca66-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="4ca66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ca66-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca66-103">Habilita um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="4ca66-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ca66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ca66-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca66-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ca66-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca66-106">O cmdlet **Enable-AzureBatchJob** habilita um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca66-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="4ca66-107">Depois de habilitar um trabalho, novas tarefas podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="4ca66-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="4ca66-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ca66-108">EXAMPLES</span></span>

### <span data-ttu-id="4ca66-109">Exemplo 1: habilitar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="4ca66-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="4ca66-110">Esse comando habilita o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="4ca66-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4ca66-111">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="4ca66-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4ca66-112">OS</span><span class="sxs-lookup"><span data-stu-id="4ca66-112">PARAMETERS</span></span>

### <span data-ttu-id="4ca66-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4ca66-113">-BatchContext</span></span>
<span data-ttu-id="4ca66-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="4ca66-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4ca66-115">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="4ca66-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4ca66-116">-ID</span><span class="sxs-lookup"><span data-stu-id="4ca66-116">-Id</span></span>
<span data-ttu-id="4ca66-117">Especifica a ID do trabalho que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="4ca66-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="4ca66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca66-118">-DefaultProfile</span></span>
<span data-ttu-id="4ca66-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca66-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ca66-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca66-120">CommonParameters</span></span>
<span data-ttu-id="4ca66-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca66-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca66-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca66-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca66-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ca66-123">INPUTS</span></span>

### <span data-ttu-id="4ca66-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4ca66-124">BatchAccountContext</span></span>
<span data-ttu-id="4ca66-125">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4ca66-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4ca66-126">String</span><span class="sxs-lookup"><span data-stu-id="4ca66-126">String</span></span>
<span data-ttu-id="4ca66-127">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4ca66-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4ca66-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ca66-128">OUTPUTS</span></span>

## <span data-ttu-id="4ca66-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ca66-129">NOTES</span></span>

## <span data-ttu-id="4ca66-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ca66-130">RELATED LINKS</span></span>

[<span data-ttu-id="4ca66-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4ca66-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="4ca66-132">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4ca66-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="4ca66-133">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4ca66-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="4ca66-134">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4ca66-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="4ca66-135">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4ca66-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="4ca66-136">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="4ca66-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


