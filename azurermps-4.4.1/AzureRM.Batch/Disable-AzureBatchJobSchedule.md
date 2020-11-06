---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441215"
---
# <span data-ttu-id="aaf3f-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aaf3f-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="aaf3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aaf3f-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf3f-103">Desabilita o cronograma de um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaf3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aaf3f-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaf3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aaf3f-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf3f-106">O cmdlet **Disable-AzureBatchJobSchedule** desabilita um cronograma de trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="aaf3f-107">Se você desabilitar um cronograma, os trabalhos não serão criados de acordo com esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="aaf3f-108">Você pode habilitar um cronograma desabilitado mais tarde.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="aaf3f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aaf3f-109">EXAMPLES</span></span>

### <span data-ttu-id="aaf3f-110">Exemplo 1: desabilitar um cronograma de trabalho</span><span class="sxs-lookup"><span data-stu-id="aaf3f-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="aaf3f-111">Esse comando desabilita o plano de trabalho que tem a ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="aaf3f-112">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="aaf3f-113">OS</span><span class="sxs-lookup"><span data-stu-id="aaf3f-113">PARAMETERS</span></span>

### <span data-ttu-id="aaf3f-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aaf3f-114">-BatchContext</span></span>
<span data-ttu-id="aaf3f-115">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aaf3f-116">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="aaf3f-117">-ID</span><span class="sxs-lookup"><span data-stu-id="aaf3f-117">-Id</span></span>
<span data-ttu-id="aaf3f-118">Especifica a ID do agendamento de trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="aaf3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf3f-119">-DefaultProfile</span></span>
<span data-ttu-id="aaf3f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaf3f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf3f-121">CommonParameters</span></span>
<span data-ttu-id="aaf3f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf3f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf3f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf3f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf3f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aaf3f-124">INPUTS</span></span>

### <span data-ttu-id="aaf3f-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aaf3f-125">BatchAccountContext</span></span>
<span data-ttu-id="aaf3f-126">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="aaf3f-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="aaf3f-127">String</span><span class="sxs-lookup"><span data-stu-id="aaf3f-127">String</span></span>
<span data-ttu-id="aaf3f-128">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="aaf3f-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="aaf3f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aaf3f-129">OUTPUTS</span></span>

## <span data-ttu-id="aaf3f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aaf3f-130">NOTES</span></span>

## <span data-ttu-id="aaf3f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aaf3f-131">RELATED LINKS</span></span>

[<span data-ttu-id="aaf3f-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aaf3f-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="aaf3f-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aaf3f-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="aaf3f-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aaf3f-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="aaf3f-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aaf3f-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="aaf3f-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aaf3f-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="aaf3f-137">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aaf3f-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="aaf3f-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="aaf3f-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


