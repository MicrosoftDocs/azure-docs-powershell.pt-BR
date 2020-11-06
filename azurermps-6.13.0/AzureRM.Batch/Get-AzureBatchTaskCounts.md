---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: 9010ec1d15958f5198c25fd0ef9e8a5ecfe6a39e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433316"
---
# <span data-ttu-id="294fd-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="294fd-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="294fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="294fd-102">SYNOPSIS</span></span>
<span data-ttu-id="294fd-103">Obtém as contagens de tarefas para o trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="294fd-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="294fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="294fd-104">SYNTAX</span></span>

### <span data-ttu-id="294fd-105">%</span><span class="sxs-lookup"><span data-stu-id="294fd-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="294fd-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="294fd-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="294fd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="294fd-107">DESCRIPTION</span></span>
<span data-ttu-id="294fd-108">O cmdlet **Get-AzureBatchTaskCounts** Obtém a contagem de tarefas em lotes do Azure para um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="294fd-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="294fd-109">Especifique um trabalho pelo parâmetro *JobID* ou por meio do parâmetro *Job* .</span><span class="sxs-lookup"><span data-stu-id="294fd-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="294fd-110">Contagens de tarefas fornecem uma contagem das tarefas por meio do estado de tarefa ativo, em execução ou concluído, e uma contagem de tarefas que tiveram êxito ou falharam.</span><span class="sxs-lookup"><span data-stu-id="294fd-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="294fd-111">As tarefas no estado preparação são contadas como em execução.</span><span class="sxs-lookup"><span data-stu-id="294fd-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="294fd-112">Se o validationStatus for Unvalidated, o serviço em lotes não poderá verificar contagens de estado em relação ao estado da tarefa como relatado na API de tarefas da lista.</span><span class="sxs-lookup"><span data-stu-id="294fd-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="294fd-113">A validationStatus pode ser desvalidada se o trabalho contiver mais de 200.000 tarefas.</span><span class="sxs-lookup"><span data-stu-id="294fd-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="294fd-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="294fd-114">EXAMPLES</span></span>

### <span data-ttu-id="294fd-115">Exemplo 1: obter contagens de tarefas por ID</span><span class="sxs-lookup"><span data-stu-id="294fd-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="294fd-116">Esse comando obtém a contagem de tarefas para o job Job01.</span><span class="sxs-lookup"><span data-stu-id="294fd-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="294fd-117">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="294fd-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="294fd-118">OS</span><span class="sxs-lookup"><span data-stu-id="294fd-118">PARAMETERS</span></span>

### <span data-ttu-id="294fd-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="294fd-119">-BatchContext</span></span>
<span data-ttu-id="294fd-120">A instância BatchAccountContext a ser usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="294fd-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="294fd-121">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="294fd-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="294fd-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="294fd-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="294fd-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="294fd-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="294fd-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="294fd-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="294fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294fd-125">-DefaultProfile</span></span>
<span data-ttu-id="294fd-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="294fd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="294fd-127">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="294fd-127">-Job</span></span>
<span data-ttu-id="294fd-128">Especifica o trabalho que contém as tarefas obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="294fd-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="294fd-129">Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="294fd-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="294fd-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="294fd-130">-JobId</span></span>
<span data-ttu-id="294fd-131">A ID do trabalho para o qual obter contagens de tarefas.</span><span class="sxs-lookup"><span data-stu-id="294fd-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294fd-132">CommonParameters</span></span>
<span data-ttu-id="294fd-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="294fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294fd-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="294fd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294fd-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="294fd-135">INPUTS</span></span>

### <span data-ttu-id="294fd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="294fd-136">System.String</span></span>

### <span data-ttu-id="294fd-137">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="294fd-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="294fd-138">Parâmetros: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="294fd-138">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="294fd-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="294fd-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="294fd-140">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="294fd-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="294fd-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="294fd-141">OUTPUTS</span></span>

### <span data-ttu-id="294fd-142">Microsoft.Azure.Commands.Batch. Modelos. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="294fd-142">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="294fd-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="294fd-143">NOTES</span></span>

## <span data-ttu-id="294fd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="294fd-144">RELATED LINKS</span></span>

[<span data-ttu-id="294fd-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="294fd-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="294fd-146">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="294fd-146">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="294fd-147">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="294fd-147">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)