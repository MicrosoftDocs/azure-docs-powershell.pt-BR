---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 0f33807c112ea770e3d02d972d52ca7a166bb791
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427675"
---
# <span data-ttu-id="5da0e-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5da0e-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="5da0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5da0e-102">SYNOPSIS</span></span>
<span data-ttu-id="5da0e-103">Interrompe um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="5da0e-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5da0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5da0e-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5da0e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5da0e-105">DESCRIPTION</span></span>
<span data-ttu-id="5da0e-106">O cmdlet **Stop-AzureBatchJob** interrompe um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="5da0e-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="5da0e-107">Esse comando marca o trabalho como concluído.</span><span class="sxs-lookup"><span data-stu-id="5da0e-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="5da0e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5da0e-108">EXAMPLES</span></span>

### <span data-ttu-id="5da0e-109">Exemplo 1: parar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="5da0e-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="5da0e-110">Esse comando interrompe o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="5da0e-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5da0e-111">O comando especifica um motivo pelo qual você optou por interromper o trabalho.</span><span class="sxs-lookup"><span data-stu-id="5da0e-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="5da0e-112">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="5da0e-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5da0e-113">OS</span><span class="sxs-lookup"><span data-stu-id="5da0e-113">PARAMETERS</span></span>

### <span data-ttu-id="5da0e-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5da0e-114">-BatchContext</span></span>
<span data-ttu-id="5da0e-115">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="5da0e-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5da0e-116">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="5da0e-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5da0e-117">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="5da0e-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5da0e-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="5da0e-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5da0e-119">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5da0e-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5da0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da0e-120">-DefaultProfile</span></span>
<span data-ttu-id="5da0e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5da0e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da0e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="5da0e-122">-Id</span></span>
<span data-ttu-id="5da0e-123">Especifica a ID do trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="5da0e-123">Specifies the ID of the job that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5da0e-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="5da0e-124">-TerminateReason</span></span>
<span data-ttu-id="5da0e-125">Especifica o motivo pelo qual você decidiu parar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="5da0e-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="5da0e-126">Esse cmdlet armazena esse texto como a propriedade **TerminateReason** do trabalho.</span><span class="sxs-lookup"><span data-stu-id="5da0e-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da0e-127">CommonParameters</span></span>
<span data-ttu-id="5da0e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da0e-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da0e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da0e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5da0e-130">INPUTS</span></span>

### <span data-ttu-id="5da0e-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5da0e-131">BatchAccountContext</span></span>
<span data-ttu-id="5da0e-132">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="5da0e-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5da0e-133">String</span><span class="sxs-lookup"><span data-stu-id="5da0e-133">String</span></span>
<span data-ttu-id="5da0e-134">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="5da0e-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5da0e-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5da0e-135">OUTPUTS</span></span>

## <span data-ttu-id="5da0e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5da0e-136">NOTES</span></span>

## <span data-ttu-id="5da0e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5da0e-137">RELATED LINKS</span></span>

[<span data-ttu-id="5da0e-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5da0e-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="5da0e-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5da0e-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5da0e-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5da0e-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5da0e-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5da0e-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="5da0e-142">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5da0e-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5da0e-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5da0e-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="5da0e-144">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="5da0e-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


