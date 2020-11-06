---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611010"
---
# <span data-ttu-id="cba3d-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cba3d-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="cba3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cba3d-102">SYNOPSIS</span></span>
<span data-ttu-id="cba3d-103">Obtém pools de lotes na conta em lotes especificada.</span><span class="sxs-lookup"><span data-stu-id="cba3d-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cba3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cba3d-104">SYNTAX</span></span>

### <span data-ttu-id="cba3d-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="cba3d-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cba3d-106">%</span><span class="sxs-lookup"><span data-stu-id="cba3d-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba3d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cba3d-107">DESCRIPTION</span></span>
<span data-ttu-id="cba3d-108">O cmdlet **Get-AzureBatchPool** Obtém os pools de lotes do Azure sob a conta em lotes especificada com o parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="cba3d-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="cba3d-109">Você pode usar o parâmetro *ID* para obter um único pool ou pode usar o parâmetro *Filter* para obter os pools correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="cba3d-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="cba3d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cba3d-110">EXAMPLES</span></span>

### <span data-ttu-id="cba3d-111">Exemplo 1: obter um pool por ID</span><span class="sxs-lookup"><span data-stu-id="cba3d-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="cba3d-112">Esse comando obtém o pool com ID mypool.</span><span class="sxs-lookup"><span data-stu-id="cba3d-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="cba3d-113">Exemplo 2: obter todos os pools usando um filtro OData</span><span class="sxs-lookup"><span data-stu-id="cba3d-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="cba3d-114">Esse comando obtém os pools cujos IDs começam com My usando o parâmetro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="cba3d-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="cba3d-115">OS</span><span class="sxs-lookup"><span data-stu-id="cba3d-115">PARAMETERS</span></span>

### <span data-ttu-id="cba3d-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cba3d-116">-BatchContext</span></span>
<span data-ttu-id="cba3d-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="cba3d-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cba3d-118">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="cba3d-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="cba3d-119">-Expandir</span><span class="sxs-lookup"><span data-stu-id="cba3d-119">-Expand</span></span>
<span data-ttu-id="cba3d-120">Especifica uma cláusula de expansão do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="cba3d-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="cba3d-121">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obtém.</span><span class="sxs-lookup"><span data-stu-id="cba3d-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="cba3d-122">-Filtro</span><span class="sxs-lookup"><span data-stu-id="cba3d-122">-Filter</span></span>
<span data-ttu-id="cba3d-123">Especifica a cláusula de filtro OData a ser usada ao consultar pools.</span><span class="sxs-lookup"><span data-stu-id="cba3d-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="cba3d-124">Se você não especificar um filtro, todos os pools abaixo da conta em lotes especificados com o parâmetro *BatchContext* serão retornados.</span><span class="sxs-lookup"><span data-stu-id="cba3d-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="cba3d-125">-ID</span><span class="sxs-lookup"><span data-stu-id="cba3d-125">-Id</span></span>
<span data-ttu-id="cba3d-126">Especifica a ID do pool a obter.</span><span class="sxs-lookup"><span data-stu-id="cba3d-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="cba3d-127">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="cba3d-127">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="cba3d-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cba3d-128">-MaxCount</span></span>
<span data-ttu-id="cba3d-129">Especifica o número máximo de pools a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="cba3d-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="cba3d-130">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="cba3d-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="cba3d-131">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="cba3d-131">The default value is 1000.</span></span>

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

### <span data-ttu-id="cba3d-132">-Selecione</span><span class="sxs-lookup"><span data-stu-id="cba3d-132">-Select</span></span>
<span data-ttu-id="cba3d-133">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="cba3d-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="cba3d-134">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="cba3d-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="cba3d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba3d-135">-DefaultProfile</span></span>
<span data-ttu-id="cba3d-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cba3d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cba3d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba3d-137">CommonParameters</span></span>
<span data-ttu-id="cba3d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba3d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba3d-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba3d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba3d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cba3d-140">INPUTS</span></span>

### <span data-ttu-id="cba3d-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cba3d-141">BatchAccountContext</span></span>
<span data-ttu-id="cba3d-142">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cba3d-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cba3d-143">String</span><span class="sxs-lookup"><span data-stu-id="cba3d-143">String</span></span>
<span data-ttu-id="cba3d-144">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cba3d-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cba3d-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cba3d-145">OUTPUTS</span></span>

### <span data-ttu-id="cba3d-146">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="cba3d-146">PSCloudPool</span></span>

## <span data-ttu-id="cba3d-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cba3d-147">NOTES</span></span>

## <span data-ttu-id="cba3d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cba3d-148">RELATED LINKS</span></span>

[<span data-ttu-id="cba3d-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cba3d-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cba3d-150">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cba3d-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="cba3d-151">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cba3d-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="cba3d-152">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="cba3d-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


