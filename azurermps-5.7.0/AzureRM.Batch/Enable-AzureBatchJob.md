---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 81ace9fd18b916f8f4788cf5878af1a620a61882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609980"
---
# <span data-ttu-id="96147-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="96147-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="96147-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96147-102">SYNOPSIS</span></span>
<span data-ttu-id="96147-103">Habilita um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="96147-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96147-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96147-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96147-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96147-105">DESCRIPTION</span></span>
<span data-ttu-id="96147-106">O cmdlet **Enable-AzureBatchJob** habilita um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="96147-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="96147-107">Depois de habilitar um trabalho, novas tarefas podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="96147-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="96147-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96147-108">EXAMPLES</span></span>

### <span data-ttu-id="96147-109">Exemplo 1: habilitar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="96147-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="96147-110">Esse comando habilita o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="96147-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="96147-111">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="96147-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="96147-112">OS</span><span class="sxs-lookup"><span data-stu-id="96147-112">PARAMETERS</span></span>

### <span data-ttu-id="96147-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="96147-113">-BatchContext</span></span>
<span data-ttu-id="96147-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="96147-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="96147-115">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="96147-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="96147-116">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="96147-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="96147-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="96147-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="96147-118">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="96147-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="96147-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96147-119">-DefaultProfile</span></span>
<span data-ttu-id="96147-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96147-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96147-121">-ID</span><span class="sxs-lookup"><span data-stu-id="96147-121">-Id</span></span>
<span data-ttu-id="96147-122">Especifica a ID do trabalho que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="96147-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="96147-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96147-123">CommonParameters</span></span>
<span data-ttu-id="96147-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96147-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96147-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96147-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96147-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96147-126">INPUTS</span></span>

### <span data-ttu-id="96147-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="96147-127">BatchAccountContext</span></span>
<span data-ttu-id="96147-128">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="96147-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="96147-129">String</span><span class="sxs-lookup"><span data-stu-id="96147-129">String</span></span>
<span data-ttu-id="96147-130">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="96147-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="96147-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96147-131">OUTPUTS</span></span>

## <span data-ttu-id="96147-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96147-132">NOTES</span></span>

## <span data-ttu-id="96147-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96147-133">RELATED LINKS</span></span>

[<span data-ttu-id="96147-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="96147-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="96147-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="96147-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="96147-136">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="96147-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="96147-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="96147-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="96147-138">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="96147-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="96147-139">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="96147-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


