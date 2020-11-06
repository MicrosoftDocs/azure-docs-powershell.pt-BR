---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610848"
---
# <span data-ttu-id="940b0-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="940b0-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="940b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="940b0-102">SYNOPSIS</span></span>
<span data-ttu-id="940b0-103">Desabilita um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="940b0-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="940b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="940b0-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="940b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="940b0-105">DESCRIPTION</span></span>
<span data-ttu-id="940b0-106">O cmdlet **Disable-AzureBatchJob** desabilita um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="940b0-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="940b0-107">Depois de habilitar um trabalho, novas tarefas podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="940b0-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="940b0-108">Tarefas desabilitadas não executam novas tarefas.</span><span class="sxs-lookup"><span data-stu-id="940b0-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="940b0-109">Você pode habilitar um trabalho desabilitado mais tarde.</span><span class="sxs-lookup"><span data-stu-id="940b0-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="940b0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="940b0-110">EXAMPLES</span></span>

### <span data-ttu-id="940b0-111">Exemplo 1: desabilitar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="940b0-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="940b0-112">Esse comando desabilita o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="940b0-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="940b0-113">O comando encerra tarefas ativas para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="940b0-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="940b0-114">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="940b0-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="940b0-115">OS</span><span class="sxs-lookup"><span data-stu-id="940b0-115">PARAMETERS</span></span>

### <span data-ttu-id="940b0-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="940b0-116">-BatchContext</span></span>
<span data-ttu-id="940b0-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="940b0-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="940b0-118">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="940b0-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="940b0-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="940b0-119">-DisableJobOption</span></span>
<span data-ttu-id="940b0-120">Especifica o que fazer com as tarefas ativas associadas ao trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="940b0-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="940b0-121">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="940b0-121">Valid values are:</span></span> 

- <span data-ttu-id="940b0-122">Refilar</span><span class="sxs-lookup"><span data-stu-id="940b0-122">Requeue</span></span> 
- <span data-ttu-id="940b0-123">Inesperada</span><span class="sxs-lookup"><span data-stu-id="940b0-123">Terminate</span></span> 
- <span data-ttu-id="940b0-124">Esperar</span><span class="sxs-lookup"><span data-stu-id="940b0-124">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940b0-125">-ID</span><span class="sxs-lookup"><span data-stu-id="940b0-125">-Id</span></span>
<span data-ttu-id="940b0-126">Especifica a ID do trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="940b0-126">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="940b0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940b0-127">-DefaultProfile</span></span>
<span data-ttu-id="940b0-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="940b0-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="940b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940b0-129">CommonParameters</span></span>
<span data-ttu-id="940b0-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="940b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940b0-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940b0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940b0-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="940b0-132">INPUTS</span></span>

### <span data-ttu-id="940b0-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="940b0-133">BatchAccountContext</span></span>
<span data-ttu-id="940b0-134">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="940b0-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="940b0-135">String</span><span class="sxs-lookup"><span data-stu-id="940b0-135">String</span></span>
<span data-ttu-id="940b0-136">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="940b0-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="940b0-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="940b0-137">OUTPUTS</span></span>

## <span data-ttu-id="940b0-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="940b0-138">NOTES</span></span>

## <span data-ttu-id="940b0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="940b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="940b0-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="940b0-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="940b0-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="940b0-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="940b0-142">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="940b0-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="940b0-143">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="940b0-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="940b0-144">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="940b0-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="940b0-145">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="940b0-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="940b0-146">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="940b0-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


