---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: b0709c7b839ca992d415cd5ba9fff58e769120fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124703"
---
# <span data-ttu-id="5793e-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5793e-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="5793e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5793e-102">SYNOPSIS</span></span>
<span data-ttu-id="5793e-103">Obtém trabalhos em lotes para uma conta em lotes ou um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5793e-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="5793e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5793e-104">SYNTAX</span></span>

### <span data-ttu-id="5793e-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="5793e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5793e-106">%</span><span class="sxs-lookup"><span data-stu-id="5793e-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5793e-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5793e-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5793e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5793e-108">DESCRIPTION</span></span>
<span data-ttu-id="5793e-109">O cmdlet **Get-AzBatchJob** Obtém os trabalhos em lotes do Azure para a conta em lotes especificada pelo parâmetro *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="5793e-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="5793e-110">Você pode usar o parâmetro *ID* para obter um único trabalho.</span><span class="sxs-lookup"><span data-stu-id="5793e-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="5793e-111">Você pode usar o parâmetro *Filter* para obter os trabalhos correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="5793e-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="5793e-112">Se você fornecer uma ID de agendamento de trabalho ou uma instância de **PSCloudJobSchedule** , esse cmdlet retornará apenas os trabalhos desse agendamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5793e-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="5793e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5793e-113">EXAMPLES</span></span>

### <span data-ttu-id="5793e-114">Exemplo 1: obter um trabalho em lotes por ID</span><span class="sxs-lookup"><span data-stu-id="5793e-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 :
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="5793e-115">Esse comando obtém o trabalho que tem a ID Job01.</span><span class="sxs-lookup"><span data-stu-id="5793e-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="5793e-116">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="5793e-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5793e-117">Exemplo 2: obter todos os trabalhos ativos para um plano de trabalho</span><span class="sxs-lookup"><span data-stu-id="5793e-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="5793e-118">Esse comando obtém os trabalhos ativos para o plano de trabalho que tem a ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="5793e-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="5793e-119">Exemplo 3: Obtém todos os trabalhos em um plano de trabalho usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="5793e-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="5793e-120">Esse comando obtém o agendamento de trabalho que tem a ID JobSchedule27 usando o cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="5793e-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="5793e-121">O comando passa o agendamento do trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="5793e-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5793e-122">O comando obtém todos os trabalhos desse agendamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5793e-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="5793e-123">OS</span><span class="sxs-lookup"><span data-stu-id="5793e-123">PARAMETERS</span></span>

### <span data-ttu-id="5793e-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5793e-124">-BatchContext</span></span>
<span data-ttu-id="5793e-125">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="5793e-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5793e-126">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="5793e-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5793e-127">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="5793e-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5793e-128">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="5793e-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5793e-129">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5793e-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5793e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5793e-130">-DefaultProfile</span></span>
<span data-ttu-id="5793e-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5793e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5793e-132">-Expandir</span><span class="sxs-lookup"><span data-stu-id="5793e-132">-Expand</span></span>
<span data-ttu-id="5793e-133">Especifica uma cláusula de expansão do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="5793e-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="5793e-134">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obtém.</span><span class="sxs-lookup"><span data-stu-id="5793e-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5793e-135">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5793e-135">-Filter</span></span>
<span data-ttu-id="5793e-136">Especifica uma cláusula de filtro OData para trabalhos.</span><span class="sxs-lookup"><span data-stu-id="5793e-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="5793e-137">Se você não especificar um filtro, esse cmdlet retornará todos os trabalhos para a conta em lotes ou o cronograma do trabalho.</span><span class="sxs-lookup"><span data-stu-id="5793e-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5793e-138">-ID</span><span class="sxs-lookup"><span data-stu-id="5793e-138">-Id</span></span>
<span data-ttu-id="5793e-139">Especifica a ID do trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5793e-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="5793e-140">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="5793e-140">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5793e-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="5793e-141">-JobSchedule</span></span>
<span data-ttu-id="5793e-142">Especifica um objeto **PSCloudJobSchedule** que representa o agendamento do trabalho que contém os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="5793e-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="5793e-143">Para obter um objeto **PSCloudJobSchedule** , use o cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="5793e-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5793e-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="5793e-144">-JobScheduleId</span></span>
<span data-ttu-id="5793e-145">Especifica a ID do agendamento do trabalho que contém os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="5793e-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5793e-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5793e-146">-MaxCount</span></span>
<span data-ttu-id="5793e-147">Especifica o número máximo de trabalhos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="5793e-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="5793e-148">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="5793e-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="5793e-149">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="5793e-149">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5793e-150">-Selecione</span><span class="sxs-lookup"><span data-stu-id="5793e-150">-Select</span></span>
<span data-ttu-id="5793e-151">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="5793e-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="5793e-152">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="5793e-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5793e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5793e-153">CommonParameters</span></span>
<span data-ttu-id="5793e-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5793e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5793e-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5793e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5793e-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5793e-156">INPUTS</span></span>

### <span data-ttu-id="5793e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5793e-157">System.String</span></span>

### <span data-ttu-id="5793e-158">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5793e-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="5793e-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5793e-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5793e-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5793e-160">OUTPUTS</span></span>

### <span data-ttu-id="5793e-161">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="5793e-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="5793e-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5793e-162">NOTES</span></span>

## <span data-ttu-id="5793e-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5793e-163">RELATED LINKS</span></span>

[<span data-ttu-id="5793e-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5793e-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="5793e-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5793e-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="5793e-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5793e-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5793e-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5793e-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="5793e-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5793e-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="5793e-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5793e-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="5793e-170">Parar-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5793e-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="5793e-171">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="5793e-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
