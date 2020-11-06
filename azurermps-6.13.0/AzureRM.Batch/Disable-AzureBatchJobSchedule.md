---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: e1eb586ff23f5f56cd9fc117f5039d3ccc841367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431432"
---
# <span data-ttu-id="6ac2b-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac2b-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="6ac2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ac2b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac2b-103">Desabilita o cronograma de um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ac2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ac2b-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ac2b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ac2b-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac2b-106">O cmdlet **Disable-AzureBatchJobSchedule** desabilita um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="6ac2b-107">Se você desabilitar um cronograma, os trabalhos não serão criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="6ac2b-108">Você pode habilitar um cronograma desabilitado mais tarde.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="6ac2b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ac2b-109">EXAMPLES</span></span>

### <span data-ttu-id="6ac2b-110">Exemplo 1: desabilitar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="6ac2b-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="6ac2b-111">Esse comando desabilita o plano de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="6ac2b-112">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6ac2b-113">OS</span><span class="sxs-lookup"><span data-stu-id="6ac2b-113">PARAMETERS</span></span>

### <span data-ttu-id="6ac2b-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6ac2b-114">-BatchContext</span></span>
<span data-ttu-id="6ac2b-115">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6ac2b-116">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6ac2b-117">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6ac2b-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6ac2b-119">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6ac2b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac2b-120">-DefaultProfile</span></span>
<span data-ttu-id="6ac2b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ac2b-122">-ID</span><span class="sxs-lookup"><span data-stu-id="6ac2b-122">-Id</span></span>
<span data-ttu-id="6ac2b-123">Especifica a ID do agendamento de trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="6ac2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac2b-124">CommonParameters</span></span>
<span data-ttu-id="6ac2b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac2b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac2b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac2b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ac2b-127">INPUTS</span></span>

### <span data-ttu-id="6ac2b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6ac2b-128">System.String</span></span>

### <span data-ttu-id="6ac2b-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6ac2b-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6ac2b-130">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6ac2b-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6ac2b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ac2b-131">OUTPUTS</span></span>

### <span data-ttu-id="6ac2b-132">System. void</span><span class="sxs-lookup"><span data-stu-id="6ac2b-132">System.Void</span></span>

## <span data-ttu-id="6ac2b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ac2b-133">NOTES</span></span>

## <span data-ttu-id="6ac2b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ac2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="6ac2b-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac2b-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6ac2b-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6ac2b-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6ac2b-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac2b-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="6ac2b-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac2b-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="6ac2b-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac2b-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="6ac2b-140">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6ac2b-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="6ac2b-141">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="6ac2b-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


