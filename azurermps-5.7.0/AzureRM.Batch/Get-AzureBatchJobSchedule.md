---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 3c53a81952b204f08911b11accf6feb6bd55a3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602874"
---
# <span data-ttu-id="fadb6-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fadb6-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="fadb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fadb6-102">SYNOPSIS</span></span>
<span data-ttu-id="fadb6-103">Obtém cronogramas de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="fadb6-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fadb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fadb6-104">SYNTAX</span></span>

### <span data-ttu-id="fadb6-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="fadb6-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fadb6-106">%</span><span class="sxs-lookup"><span data-stu-id="fadb6-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fadb6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fadb6-107">DESCRIPTION</span></span>
<span data-ttu-id="fadb6-108">O cmdlet **Get-AzureBatchJobSchedule** Obtém cronogramas do trabalho em lotes do Azure para a conta em lotes especificada pelo parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="fadb6-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="fadb6-109">Especifique uma ID para obter um único cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fadb6-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="fadb6-110">Especifique o parâmetro *Filter* para obter as agendas de trabalho correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="fadb6-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="fadb6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fadb6-111">EXAMPLES</span></span>

### <span data-ttu-id="fadb6-112">Exemplo 1: obter um plano de trabalho especificando uma ID</span><span class="sxs-lookup"><span data-stu-id="fadb6-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="fadb6-113">Esse comando obtém o plano de trabalho que tem a ID JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="fadb6-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="fadb6-114">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="fadb6-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fadb6-115">Exemplo 2: obter cronogramas de trabalho usando um filtro</span><span class="sxs-lookup"><span data-stu-id="fadb6-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 : 
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="fadb6-116">Esse comando obtém todas as agendas de trabalho que têm IDs que começam com o trabalho especificando o parâmetro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="fadb6-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="fadb6-117">OS</span><span class="sxs-lookup"><span data-stu-id="fadb6-117">PARAMETERS</span></span>

### <span data-ttu-id="fadb6-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fadb6-118">-BatchContext</span></span>
<span data-ttu-id="fadb6-119">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="fadb6-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fadb6-120">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="fadb6-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fadb6-121">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="fadb6-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fadb6-122">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="fadb6-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fadb6-123">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fadb6-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fadb6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadb6-124">-DefaultProfile</span></span>
<span data-ttu-id="fadb6-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fadb6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fadb6-126">-Expandir</span><span class="sxs-lookup"><span data-stu-id="fadb6-126">-Expand</span></span>
<span data-ttu-id="fadb6-127">Especifica uma cláusula de expansão do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="fadb6-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="fadb6-128">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obtém.</span><span class="sxs-lookup"><span data-stu-id="fadb6-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadb6-129">-Filtro</span><span class="sxs-lookup"><span data-stu-id="fadb6-129">-Filter</span></span>
<span data-ttu-id="fadb6-130">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="fadb6-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="fadb6-131">Esse cmdlet retorna as agendas de trabalho que correspondem ao filtro especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fadb6-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="fadb6-132">Se você não especificar um filtro, esse cmdlet retornará todas as agendas de trabalho do contexto em lotes.</span><span class="sxs-lookup"><span data-stu-id="fadb6-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadb6-133">-ID</span><span class="sxs-lookup"><span data-stu-id="fadb6-133">-Id</span></span>
<span data-ttu-id="fadb6-134">Especifica a ID do agendamento de trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fadb6-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="fadb6-135">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="fadb6-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fadb6-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fadb6-136">-MaxCount</span></span>
<span data-ttu-id="fadb6-137">Especifica o número máximo de cronogramas de trabalho a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="fadb6-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="fadb6-138">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="fadb6-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="fadb6-139">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="fadb6-139">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadb6-140">-Selecione</span><span class="sxs-lookup"><span data-stu-id="fadb6-140">-Select</span></span>
<span data-ttu-id="fadb6-141">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="fadb6-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="fadb6-142">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="fadb6-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fadb6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadb6-143">CommonParameters</span></span>
<span data-ttu-id="fadb6-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fadb6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadb6-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fadb6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadb6-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fadb6-146">INPUTS</span></span>

### <span data-ttu-id="fadb6-147">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fadb6-147">BatchAccountContext</span></span>
<span data-ttu-id="fadb6-148">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fadb6-148">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fadb6-149">String</span><span class="sxs-lookup"><span data-stu-id="fadb6-149">String</span></span>
<span data-ttu-id="fadb6-150">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fadb6-150">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="fadb6-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fadb6-151">OUTPUTS</span></span>

### <span data-ttu-id="fadb6-152">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fadb6-152">PSCloudJobSchedule</span></span>

## <span data-ttu-id="fadb6-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fadb6-153">NOTES</span></span>

## <span data-ttu-id="fadb6-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fadb6-154">RELATED LINKS</span></span>

[<span data-ttu-id="fadb6-155">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fadb6-155">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="fadb6-156">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fadb6-156">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="fadb6-157">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fadb6-157">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fadb6-158">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fadb6-158">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="fadb6-159">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fadb6-159">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="fadb6-160">Parar-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fadb6-160">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="fadb6-161">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="fadb6-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


