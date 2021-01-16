---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262962"
---
# <span data-ttu-id="07d96-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="07d96-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="07d96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07d96-102">SYNOPSIS</span></span>
<span data-ttu-id="07d96-103">Obtém as contagens de tarefas para o trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="07d96-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="07d96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07d96-104">SYNTAX</span></span>

### <span data-ttu-id="07d96-105">%</span><span class="sxs-lookup"><span data-stu-id="07d96-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d96-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="07d96-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d96-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07d96-107">DESCRIPTION</span></span>
<span data-ttu-id="07d96-108">O cmdlet **Get-AzBatchTaskCount** Obtém a contagem de tarefas em lotes do Azure para um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="07d96-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="07d96-109">Especifique um trabalho pelo parâmetro *JobID* ou por meio do parâmetro *Job* .</span><span class="sxs-lookup"><span data-stu-id="07d96-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="07d96-110">Contagens de tarefas fornecem uma contagem das tarefas por meio do estado de tarefa ativo, em execução ou concluído, e uma contagem de tarefas que tiveram êxito ou falharam.</span><span class="sxs-lookup"><span data-stu-id="07d96-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="07d96-111">As tarefas no estado preparação são contadas como em execução.</span><span class="sxs-lookup"><span data-stu-id="07d96-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="07d96-112">Se o validationStatus for Unvalidated, o serviço em lotes não poderá verificar contagens de estado em relação ao estado da tarefa como relatado na API de tarefas da lista.</span><span class="sxs-lookup"><span data-stu-id="07d96-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="07d96-113">A validationStatus pode ser desvalidada se o trabalho contiver mais de 200.000 tarefas.</span><span class="sxs-lookup"><span data-stu-id="07d96-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="07d96-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07d96-114">EXAMPLES</span></span>

### <span data-ttu-id="07d96-115">Exemplo 1: obter contagens de tarefas por ID</span><span class="sxs-lookup"><span data-stu-id="07d96-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="07d96-116">Esse comando obtém a contagem de tarefas para o job Job01.</span><span class="sxs-lookup"><span data-stu-id="07d96-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="07d96-117">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="07d96-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="07d96-118">OS</span><span class="sxs-lookup"><span data-stu-id="07d96-118">PARAMETERS</span></span>

### <span data-ttu-id="07d96-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="07d96-119">-BatchContext</span></span>
<span data-ttu-id="07d96-120">A instância BatchAccountContext a ser usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="07d96-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="07d96-121">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="07d96-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="07d96-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="07d96-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="07d96-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="07d96-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="07d96-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="07d96-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="07d96-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d96-125">-DefaultProfile</span></span>
<span data-ttu-id="07d96-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07d96-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d96-127">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="07d96-127">-Job</span></span>
<span data-ttu-id="07d96-128">Especifica o trabalho que contém as tarefas obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07d96-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="07d96-129">Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="07d96-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="07d96-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="07d96-130">-JobId</span></span>
<span data-ttu-id="07d96-131">A ID do trabalho para o qual obter contagens de tarefas.</span><span class="sxs-lookup"><span data-stu-id="07d96-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="07d96-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d96-132">CommonParameters</span></span>
<span data-ttu-id="07d96-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d96-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d96-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07d96-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d96-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07d96-135">INPUTS</span></span>

### <span data-ttu-id="07d96-136">System. String</span><span class="sxs-lookup"><span data-stu-id="07d96-136">System.String</span></span>

### <span data-ttu-id="07d96-137">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="07d96-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="07d96-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="07d96-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="07d96-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07d96-139">OUTPUTS</span></span>

### <span data-ttu-id="07d96-140">Microsoft.Azure.Commands.Batch. Modelos. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="07d96-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="07d96-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07d96-141">NOTES</span></span>

## <span data-ttu-id="07d96-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07d96-142">RELATED LINKS</span></span>

[<span data-ttu-id="07d96-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="07d96-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="07d96-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="07d96-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="07d96-145">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="07d96-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
