---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: fcb3586d1c27fd95c6bf386943830b92635162e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441478"
---
# <span data-ttu-id="8fd5d-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8fd5d-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="8fd5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fd5d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd5d-103">Desabilita um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fd5d-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fd5d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fd5d-105">DESCRIPTION</span></span>
<span data-ttu-id="8fd5d-106">O cmdlet **Disable-AzureBatchJob** desabilita um trabalho em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="8fd5d-107">Depois de habilitar um trabalho, novas tarefas podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="8fd5d-108">Tarefas desabilitadas não executam novas tarefas.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="8fd5d-109">Você pode habilitar um trabalho desabilitado mais tarde.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="8fd5d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fd5d-110">EXAMPLES</span></span>

### <span data-ttu-id="8fd5d-111">Exemplo 1: desabilitar um trabalho em lotes</span><span class="sxs-lookup"><span data-stu-id="8fd5d-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="8fd5d-112">Esse comando desabilita o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="8fd5d-113">O comando encerra tarefas ativas para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="8fd5d-114">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8fd5d-115">OS</span><span class="sxs-lookup"><span data-stu-id="8fd5d-115">PARAMETERS</span></span>

### <span data-ttu-id="8fd5d-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8fd5d-116">-BatchContext</span></span>
<span data-ttu-id="8fd5d-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8fd5d-118">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8fd5d-119">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8fd5d-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8fd5d-121">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8fd5d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd5d-122">-DefaultProfile</span></span>
<span data-ttu-id="8fd5d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fd5d-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="8fd5d-124">-DisableJobOption</span></span>
<span data-ttu-id="8fd5d-125">Especifica o que fazer com as tarefas ativas associadas ao trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="8fd5d-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="8fd5d-126">Valid values are:</span></span> 

- <span data-ttu-id="8fd5d-127">Refilar</span><span class="sxs-lookup"><span data-stu-id="8fd5d-127">Requeue</span></span> 
- <span data-ttu-id="8fd5d-128">Inesperada</span><span class="sxs-lookup"><span data-stu-id="8fd5d-128">Terminate</span></span> 
- <span data-ttu-id="8fd5d-129">Esperar</span><span class="sxs-lookup"><span data-stu-id="8fd5d-129">Wait</span></span>

```yaml
Type: DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd5d-130">-ID</span><span class="sxs-lookup"><span data-stu-id="8fd5d-130">-Id</span></span>
<span data-ttu-id="8fd5d-131">Especifica a ID do trabalho que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="8fd5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd5d-132">CommonParameters</span></span>
<span data-ttu-id="8fd5d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd5d-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd5d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd5d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fd5d-135">INPUTS</span></span>

### <span data-ttu-id="8fd5d-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8fd5d-136">BatchAccountContext</span></span>
<span data-ttu-id="8fd5d-137">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8fd5d-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8fd5d-138">String</span><span class="sxs-lookup"><span data-stu-id="8fd5d-138">String</span></span>
<span data-ttu-id="8fd5d-139">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8fd5d-139">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8fd5d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fd5d-140">OUTPUTS</span></span>

## <span data-ttu-id="8fd5d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fd5d-141">NOTES</span></span>

## <span data-ttu-id="8fd5d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fd5d-142">RELATED LINKS</span></span>

[<span data-ttu-id="8fd5d-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8fd5d-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="8fd5d-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8fd5d-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8fd5d-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8fd5d-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="8fd5d-146">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8fd5d-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="8fd5d-147">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8fd5d-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="8fd5d-148">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8fd5d-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="8fd5d-149">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="8fd5d-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


