---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 33ae727ea31d533652943240cd9cd25014635533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432336"
---
# <span data-ttu-id="a1997-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1997-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="a1997-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1997-102">SYNOPSIS</span></span>
<span data-ttu-id="a1997-103">Interrompe um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="a1997-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1997-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1997-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1997-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1997-105">DESCRIPTION</span></span>
<span data-ttu-id="a1997-106">O cmdlet **Stop-AzureBatchJobSchedule** interrompe um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1997-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="a1997-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1997-107">EXAMPLES</span></span>

### <span data-ttu-id="a1997-108">Exemplo 1: interromper um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="a1997-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="a1997-109">Esse comando interrompe o agendamento de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="a1997-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="a1997-110">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="a1997-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a1997-111">OS</span><span class="sxs-lookup"><span data-stu-id="a1997-111">PARAMETERS</span></span>

### <span data-ttu-id="a1997-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a1997-112">-BatchContext</span></span>
<span data-ttu-id="a1997-113">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="a1997-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a1997-114">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="a1997-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a1997-115">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="a1997-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a1997-116">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="a1997-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a1997-117">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a1997-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a1997-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1997-118">-DefaultProfile</span></span>
<span data-ttu-id="a1997-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1997-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1997-120">-ID</span><span class="sxs-lookup"><span data-stu-id="a1997-120">-Id</span></span>
<span data-ttu-id="a1997-121">Especifica a ID do agendamento de trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="a1997-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a1997-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1997-122">CommonParameters</span></span>
<span data-ttu-id="a1997-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1997-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1997-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1997-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1997-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1997-125">INPUTS</span></span>

### <span data-ttu-id="a1997-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a1997-126">System.String</span></span>

### <span data-ttu-id="a1997-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a1997-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a1997-128">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1997-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a1997-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1997-129">OUTPUTS</span></span>

### <span data-ttu-id="a1997-130">System. void</span><span class="sxs-lookup"><span data-stu-id="a1997-130">System.Void</span></span>

## <span data-ttu-id="a1997-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1997-131">NOTES</span></span>

## <span data-ttu-id="a1997-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1997-132">RELATED LINKS</span></span>

[<span data-ttu-id="a1997-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1997-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1997-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1997-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1997-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a1997-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a1997-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1997-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1997-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1997-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1997-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a1997-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="a1997-139">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="a1997-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


