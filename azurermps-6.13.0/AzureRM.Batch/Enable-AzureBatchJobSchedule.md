---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: e84bf86a3a784e47088ff1ed71047faac99239f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431421"
---
# <span data-ttu-id="613cd-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="613cd-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="613cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="613cd-102">SYNOPSIS</span></span>
<span data-ttu-id="613cd-103">Habilita um cronograma de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="613cd-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="613cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="613cd-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="613cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="613cd-105">DESCRIPTION</span></span>
<span data-ttu-id="613cd-106">O cmdlet **Enable-AzureBatchJobSchedule** habilita um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="613cd-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="613cd-107">Depois de habilitar um plano de trabalho, os trabalhos podem ser criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="613cd-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="613cd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="613cd-108">EXAMPLES</span></span>

### <span data-ttu-id="613cd-109">Exemplo 1: habilitar um plano de trabalho</span><span class="sxs-lookup"><span data-stu-id="613cd-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="613cd-110">Esse comando habilita o agendamento de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="613cd-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="613cd-111">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="613cd-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="613cd-112">OS</span><span class="sxs-lookup"><span data-stu-id="613cd-112">PARAMETERS</span></span>

### <span data-ttu-id="613cd-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="613cd-113">-BatchContext</span></span>
<span data-ttu-id="613cd-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="613cd-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="613cd-115">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="613cd-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="613cd-116">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="613cd-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="613cd-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="613cd-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="613cd-118">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="613cd-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="613cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="613cd-119">-DefaultProfile</span></span>
<span data-ttu-id="613cd-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="613cd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="613cd-121">-ID</span><span class="sxs-lookup"><span data-stu-id="613cd-121">-Id</span></span>
<span data-ttu-id="613cd-122">Especifica a ID do agendamento de trabalho que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="613cd-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="613cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="613cd-123">CommonParameters</span></span>
<span data-ttu-id="613cd-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="613cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="613cd-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="613cd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="613cd-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="613cd-126">INPUTS</span></span>

### <span data-ttu-id="613cd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="613cd-127">System.String</span></span>

### <span data-ttu-id="613cd-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="613cd-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="613cd-129">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="613cd-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="613cd-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="613cd-130">OUTPUTS</span></span>

### <span data-ttu-id="613cd-131">System. void</span><span class="sxs-lookup"><span data-stu-id="613cd-131">System.Void</span></span>

## <span data-ttu-id="613cd-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="613cd-132">NOTES</span></span>

## <span data-ttu-id="613cd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="613cd-133">RELATED LINKS</span></span>

[<span data-ttu-id="613cd-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="613cd-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="613cd-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="613cd-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="613cd-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="613cd-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="613cd-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="613cd-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="613cd-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="613cd-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="613cd-139">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="613cd-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="613cd-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="613cd-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

