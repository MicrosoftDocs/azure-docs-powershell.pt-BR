---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 57c2a177b802ea7fbd152328bf57a81593c9b647
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601891"
---
# <span data-ttu-id="8f0e8-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0e8-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="8f0e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0e8-103">Obtém cronogramas de trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="8f0e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f0e8-104">SYNTAX</span></span>

### <span data-ttu-id="8f0e8-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f0e8-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f0e8-106">%</span><span class="sxs-lookup"><span data-stu-id="8f0e8-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f0e8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f0e8-107">DESCRIPTION</span></span>
<span data-ttu-id="8f0e8-108">O cmdlet **Get-AzBatchJobSchedule** Obtém cronogramas do trabalho em lotes do Azure para a conta em lotes especificada pelo parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="8f0e8-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="8f0e8-109">Especifique uma ID para obter um único cronograma de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="8f0e8-110">Especifique o parâmetro *Filter* para obter as agendas de trabalho correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8f0e8-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8f0e8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f0e8-111">EXAMPLES</span></span>

### <span data-ttu-id="8f0e8-112">Exemplo 1: obter um plano de trabalho especificando uma ID</span><span class="sxs-lookup"><span data-stu-id="8f0e8-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="8f0e8-113">Esse comando obtém o plano de trabalho que tem a ID JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="8f0e8-114">Use o cmdlet Get-AzBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-114">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8f0e8-115">Exemplo 2: obter cronogramas de trabalho usando um filtro</span><span class="sxs-lookup"><span data-stu-id="8f0e8-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="8f0e8-116">Esse comando obtém todas as agendas de trabalho que têm IDs que começam com o trabalho especificando o parâmetro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="8f0e8-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="8f0e8-117">OS</span><span class="sxs-lookup"><span data-stu-id="8f0e8-117">PARAMETERS</span></span>

### <span data-ttu-id="8f0e8-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8f0e8-118">-BatchContext</span></span>
<span data-ttu-id="8f0e8-119">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8f0e8-120">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8f0e8-121">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8f0e8-122">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8f0e8-123">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8f0e8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f0e8-124">-DefaultProfile</span></span>
<span data-ttu-id="8f0e8-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f0e8-126">-Expandir</span><span class="sxs-lookup"><span data-stu-id="8f0e8-126">-Expand</span></span>
<span data-ttu-id="8f0e8-127">Especifica uma cláusula de expansão do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8f0e8-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="8f0e8-128">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obtém.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="8f0e8-129">-Filtro</span><span class="sxs-lookup"><span data-stu-id="8f0e8-129">-Filter</span></span>
<span data-ttu-id="8f0e8-130">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="8f0e8-131">Esse cmdlet retorna as agendas de trabalho que correspondem ao filtro especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="8f0e8-132">Se você não especificar um filtro, esse cmdlet retornará todas as agendas de trabalho do contexto em lotes.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0e8-133">-ID</span><span class="sxs-lookup"><span data-stu-id="8f0e8-133">-Id</span></span>
<span data-ttu-id="8f0e8-134">Especifica a ID do agendamento de trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="8f0e8-135">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0e8-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8f0e8-136">-MaxCount</span></span>
<span data-ttu-id="8f0e8-137">Especifica o número máximo de cronogramas de trabalho a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="8f0e8-138">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8f0e8-139">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-139">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f0e8-140">-Selecione</span><span class="sxs-lookup"><span data-stu-id="8f0e8-140">-Select</span></span>
<span data-ttu-id="8f0e8-141">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="8f0e8-142">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="8f0e8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0e8-143">CommonParameters</span></span>
<span data-ttu-id="8f0e8-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f0e8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0e8-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f0e8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0e8-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f0e8-146">INPUTS</span></span>

### <span data-ttu-id="8f0e8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8f0e8-147">System.String</span></span>

### <span data-ttu-id="8f0e8-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8f0e8-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8f0e8-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f0e8-149">OUTPUTS</span></span>

### <span data-ttu-id="8f0e8-150">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0e8-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="8f0e8-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f0e8-151">NOTES</span></span>

## <span data-ttu-id="8f0e8-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f0e8-152">RELATED LINKS</span></span>

[<span data-ttu-id="8f0e8-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0e8-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="8f0e8-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0e8-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="8f0e8-155">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8f0e8-155">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8f0e8-156">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0e8-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="8f0e8-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0e8-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="8f0e8-158">Parar-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0e8-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="8f0e8-159">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="8f0e8-159">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


