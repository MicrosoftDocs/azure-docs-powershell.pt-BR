---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: be73b757bf20a2f688d7f7293ac4022e7bc8f4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431423"
---
# <span data-ttu-id="71af4-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71af4-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="71af4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71af4-102">SYNOPSIS</span></span>
<span data-ttu-id="71af4-103">Habilita um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="71af4-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71af4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71af4-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71af4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71af4-105">DESCRIPTION</span></span>
<span data-ttu-id="71af4-106">O cmdlet **Enable-AzureBatchJob** habilita um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="71af4-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="71af4-107">Depois de habilitar um trabalho, novas tarefas podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="71af4-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="71af4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71af4-108">EXAMPLES</span></span>

### <span data-ttu-id="71af4-109">Exemplo 1: habilitar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="71af4-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="71af4-110">Esse comando habilita o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="71af4-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="71af4-111">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="71af4-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="71af4-112">OS</span><span class="sxs-lookup"><span data-stu-id="71af4-112">PARAMETERS</span></span>

### <span data-ttu-id="71af4-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="71af4-113">-BatchContext</span></span>
<span data-ttu-id="71af4-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="71af4-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="71af4-115">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="71af4-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="71af4-116">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="71af4-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="71af4-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="71af4-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="71af4-118">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="71af4-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="71af4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71af4-119">-DefaultProfile</span></span>
<span data-ttu-id="71af4-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71af4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71af4-121">-ID</span><span class="sxs-lookup"><span data-stu-id="71af4-121">-Id</span></span>
<span data-ttu-id="71af4-122">Especifica a ID do trabalho que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="71af4-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="71af4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71af4-123">CommonParameters</span></span>
<span data-ttu-id="71af4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71af4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71af4-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71af4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71af4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71af4-126">INPUTS</span></span>

### <span data-ttu-id="71af4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="71af4-127">System.String</span></span>

### <span data-ttu-id="71af4-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="71af4-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="71af4-129">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71af4-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="71af4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71af4-130">OUTPUTS</span></span>

### <span data-ttu-id="71af4-131">System. void</span><span class="sxs-lookup"><span data-stu-id="71af4-131">System.Void</span></span>

## <span data-ttu-id="71af4-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71af4-132">NOTES</span></span>

## <span data-ttu-id="71af4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71af4-133">RELATED LINKS</span></span>

[<span data-ttu-id="71af4-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71af4-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="71af4-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71af4-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="71af4-136">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71af4-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="71af4-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71af4-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="71af4-138">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71af4-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="71af4-139">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="71af4-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


