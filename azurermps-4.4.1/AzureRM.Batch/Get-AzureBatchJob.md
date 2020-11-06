---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430770"
---
# <span data-ttu-id="a5895-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5895-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="a5895-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5895-102">SYNOPSIS</span></span>
<span data-ttu-id="a5895-103">Obtém trabalhos em lotes para uma conta em lotes ou um cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5895-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5895-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5895-104">SYNTAX</span></span>

### <span data-ttu-id="a5895-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5895-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5895-106">%</span><span class="sxs-lookup"><span data-stu-id="a5895-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5895-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="a5895-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5895-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5895-108">DESCRIPTION</span></span>
<span data-ttu-id="a5895-109">O cmdlet **Get-AzureBatchJob** Obtém os trabalhos em lotes do Azure para a conta em lotes especificada pelo parâmetro *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="a5895-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="a5895-110">Você pode usar o parâmetro *ID* para obter um único trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5895-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="a5895-111">Você pode usar o parâmetro *Filter* para obter os trabalhos correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="a5895-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="a5895-112">Se você fornecer uma ID de agendamento de trabalho ou uma instância de **PSCloudJobSchedule** , esse cmdlet retornará apenas os trabalhos desse agendamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5895-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="a5895-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5895-113">EXAMPLES</span></span>

### <span data-ttu-id="a5895-114">Exemplo 1: obter um trabalho em lotes por ID</span><span class="sxs-lookup"><span data-stu-id="a5895-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
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

<span data-ttu-id="a5895-115">Esse comando obtém o trabalho que tem a ID Job01.</span><span class="sxs-lookup"><span data-stu-id="a5895-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="a5895-116">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="a5895-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a5895-117">Exemplo 2: obter todos os trabalhos ativos para um plano de trabalho</span><span class="sxs-lookup"><span data-stu-id="a5895-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="a5895-118">Esse comando obtém os trabalhos ativos para o plano de trabalho que tem a ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="a5895-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="a5895-119">Exemplo 3: Obtém todos os trabalhos em um plano de trabalho usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="a5895-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
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

<span data-ttu-id="a5895-120">Esse comando obtém o agendamento de trabalho que tem a ID JobSchedule27 usando o cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="a5895-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="a5895-121">O comando passa o agendamento do trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5895-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a5895-122">O comando obtém todos os trabalhos desse agendamento de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5895-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="a5895-123">OS</span><span class="sxs-lookup"><span data-stu-id="a5895-123">PARAMETERS</span></span>

### <span data-ttu-id="a5895-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a5895-124">-BatchContext</span></span>
<span data-ttu-id="a5895-125">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="a5895-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a5895-126">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="a5895-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a5895-127">-Expandir</span><span class="sxs-lookup"><span data-stu-id="a5895-127">-Expand</span></span>
<span data-ttu-id="a5895-128">Especifica uma cláusula de expansão do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="a5895-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="a5895-129">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obtém.</span><span class="sxs-lookup"><span data-stu-id="a5895-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="a5895-130">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a5895-130">-Filter</span></span>
<span data-ttu-id="a5895-131">Especifica uma cláusula de filtro OData para trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a5895-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="a5895-132">Se você não especificar um filtro, esse cmdlet retornará todos os trabalhos para a conta em lotes ou o cronograma do trabalho.</span><span class="sxs-lookup"><span data-stu-id="a5895-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="a5895-133">-ID</span><span class="sxs-lookup"><span data-stu-id="a5895-133">-Id</span></span>
<span data-ttu-id="a5895-134">Especifica a ID do trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a5895-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="a5895-135">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="a5895-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="a5895-136">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="a5895-136">-JobSchedule</span></span>
<span data-ttu-id="a5895-137">Especifica um objeto **PSCloudJobSchedule** que representa o agendamento do trabalho que contém os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a5895-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="a5895-138">Para obter um objeto **PSCloudJobSchedule** , use o cmdlet Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="a5895-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="a5895-139">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="a5895-139">-JobScheduleId</span></span>
<span data-ttu-id="a5895-140">Especifica a ID do agendamento do trabalho que contém os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a5895-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="a5895-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a5895-141">-MaxCount</span></span>
<span data-ttu-id="a5895-142">Especifica o número máximo de trabalhos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="a5895-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="a5895-143">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="a5895-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="a5895-144">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="a5895-144">The default value is 1000.</span></span>

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

### <span data-ttu-id="a5895-145">-Selecione</span><span class="sxs-lookup"><span data-stu-id="a5895-145">-Select</span></span>
<span data-ttu-id="a5895-146">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="a5895-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="a5895-147">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="a5895-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="a5895-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5895-148">-DefaultProfile</span></span>
<span data-ttu-id="a5895-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5895-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5895-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5895-150">CommonParameters</span></span>
<span data-ttu-id="a5895-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5895-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5895-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5895-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5895-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5895-153">INPUTS</span></span>

### <span data-ttu-id="a5895-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a5895-154">BatchAccountContext</span></span>
<span data-ttu-id="a5895-155">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a5895-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a5895-156">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a5895-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="a5895-157">O parâmetro ' JobSchedule ' aceita o valor do tipo ' PSCloudJobSchedule ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a5895-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="a5895-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5895-158">OUTPUTS</span></span>

### <span data-ttu-id="a5895-159">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a5895-159">PSCloudJob</span></span>

## <span data-ttu-id="a5895-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5895-160">NOTES</span></span>

## <span data-ttu-id="a5895-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5895-161">RELATED LINKS</span></span>

[<span data-ttu-id="a5895-162">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5895-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a5895-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5895-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a5895-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a5895-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a5895-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a5895-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="a5895-166">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5895-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a5895-167">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5895-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a5895-168">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5895-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a5895-169">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="a5895-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


