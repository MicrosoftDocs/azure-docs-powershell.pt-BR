---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117940"
---
# <span data-ttu-id="3e1e8-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="3e1e8-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="3e1e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e1e8-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1e8-103">Obtém as contagens de tarefas para o trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="3e1e8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e1e8-104">SYNTAX</span></span>

### <span data-ttu-id="3e1e8-105">Id</span><span class="sxs-lookup"><span data-stu-id="3e1e8-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e1e8-106">Parentobject</span><span class="sxs-lookup"><span data-stu-id="3e1e8-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e1e8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e1e8-107">DESCRIPTION</span></span>
<span data-ttu-id="3e1e8-108">O **cmdlet Get-AzBatchTaskCount** obtém a contagem de tarefas do Lote do Azure para um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="3e1e8-109">Especifique um trabalho pelo parâmetro *JobId* ou pelo *parâmetro Trabalho.*</span><span class="sxs-lookup"><span data-stu-id="3e1e8-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="3e1e8-110">As contagens de tarefas fornecem uma contagem das tarefas por estado de tarefa ativa, executada ou concluída e uma contagem de tarefas que tiveram êxito ou falharam.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="3e1e8-111">As tarefas no estado de preparação são contadas como em execução.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="3e1e8-112">Se o validationStatus não forvalidado, o serviço Lote não poderá verificar contagens de estado em relação aos estados da tarefa conforme relatado na API de Tarefas de Lista.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="3e1e8-113">Ostatus de validação pode não servalidado se o trabalho contiver mais de 200.000 tarefas.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="3e1e8-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e1e8-114">EXAMPLES</span></span>

### <span data-ttu-id="3e1e8-115">Exemplo 1: Obter contagens de tarefas por ID</span><span class="sxs-lookup"><span data-stu-id="3e1e8-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="3e1e8-116">Esse comando obtém as contagens de tarefas para o trabalho Job01.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="3e1e8-117">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="3e1e8-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e1e8-118">PARAMETERS</span></span>

### <span data-ttu-id="3e1e8-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3e1e8-119">-BatchContext</span></span>
<span data-ttu-id="3e1e8-120">A instância BatchAccountContext a ser usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="3e1e8-121">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="3e1e8-122">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="3e1e8-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="3e1e8-124">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3e1e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1e8-125">-DefaultProfile</span></span>
<span data-ttu-id="3e1e8-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e1e8-127">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="3e1e8-127">-Job</span></span>
<span data-ttu-id="3e1e8-128">Especifica o trabalho que contém tarefas que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="3e1e8-129">Para obter um **objeto PSCloudCloud,** use Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="3e1e8-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="3e1e8-130">-JobId</span></span>
<span data-ttu-id="3e1e8-131">A ID do trabalho para o qual obter contagens de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="3e1e8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1e8-132">CommonParameters</span></span>
<span data-ttu-id="3e1e8-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1e8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1e8-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e1e8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1e8-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e1e8-135">INPUTS</span></span>

### <span data-ttu-id="3e1e8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3e1e8-136">System.String</span></span>

### <span data-ttu-id="3e1e8-137">Microsoft.Azure.Commands.Batch. Models.PSCloudCloud</span><span class="sxs-lookup"><span data-stu-id="3e1e8-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="3e1e8-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e1e8-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3e1e8-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e1e8-139">OUTPUTS</span></span>

### <span data-ttu-id="3e1e8-140">Microsoft.Azure.Commands.Batch. Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="3e1e8-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="3e1e8-141">Notas</span><span class="sxs-lookup"><span data-stu-id="3e1e8-141">NOTES</span></span>

## <span data-ttu-id="3e1e8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e1e8-142">RELATED LINKS</span></span>

[<span data-ttu-id="3e1e8-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3e1e8-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3e1e8-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3e1e8-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="3e1e8-145">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="3e1e8-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
