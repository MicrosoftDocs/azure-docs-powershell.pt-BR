---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: a94b4b8bee590fa31972d2b80c9c3f2d06c566e6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93785059"
---
# <span data-ttu-id="f46c8-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f46c8-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="f46c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f46c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f46c8-103">Obtém pools de lotes na conta em lotes especificada.</span><span class="sxs-lookup"><span data-stu-id="f46c8-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="f46c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f46c8-104">SYNTAX</span></span>

### <span data-ttu-id="f46c8-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="f46c8-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f46c8-106">%</span><span class="sxs-lookup"><span data-stu-id="f46c8-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f46c8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f46c8-107">DESCRIPTION</span></span>
<span data-ttu-id="f46c8-108">O cmdlet **Get-AzBatchPool** Obtém os pools de lotes do Azure sob a conta em lotes especificada com o parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="f46c8-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="f46c8-109">Você pode usar o parâmetro *ID* para obter um único pool ou pode usar o parâmetro *Filter* para obter os pools correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="f46c8-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="f46c8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f46c8-110">EXAMPLES</span></span>

### <span data-ttu-id="f46c8-111">Exemplo 1: obter um pool por ID</span><span class="sxs-lookup"><span data-stu-id="f46c8-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzBatchPool -Id "MyPool" -BatchContext $Context
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

<span data-ttu-id="f46c8-112">Esse comando obtém o pool com ID mypool.</span><span class="sxs-lookup"><span data-stu-id="f46c8-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="f46c8-113">Exemplo 2: obter todos os pools usando um filtro OData</span><span class="sxs-lookup"><span data-stu-id="f46c8-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
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

<span data-ttu-id="f46c8-114">Esse comando obtém os pools cujos IDs começam com My usando o parâmetro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="f46c8-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="f46c8-115">OS</span><span class="sxs-lookup"><span data-stu-id="f46c8-115">PARAMETERS</span></span>

### <span data-ttu-id="f46c8-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f46c8-116">-BatchContext</span></span>
<span data-ttu-id="f46c8-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f46c8-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f46c8-118">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f46c8-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f46c8-119">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="f46c8-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f46c8-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="f46c8-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f46c8-121">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f46c8-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f46c8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46c8-122">-DefaultProfile</span></span>
<span data-ttu-id="f46c8-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f46c8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f46c8-124">-Expandir</span><span class="sxs-lookup"><span data-stu-id="f46c8-124">-Expand</span></span>
<span data-ttu-id="f46c8-125">Especifica uma cláusula de expansão do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="f46c8-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="f46c8-126">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obtém.</span><span class="sxs-lookup"><span data-stu-id="f46c8-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="f46c8-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="f46c8-127">-Filter</span></span>
<span data-ttu-id="f46c8-128">Especifica a cláusula de filtro OData a ser usada ao consultar pools.</span><span class="sxs-lookup"><span data-stu-id="f46c8-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="f46c8-129">Se você não especificar um filtro, todos os pools abaixo da conta em lotes especificados com o parâmetro *BatchContext* serão retornados.</span><span class="sxs-lookup"><span data-stu-id="f46c8-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="f46c8-130">-ID</span><span class="sxs-lookup"><span data-stu-id="f46c8-130">-Id</span></span>
<span data-ttu-id="f46c8-131">Especifica a ID do pool a obter.</span><span class="sxs-lookup"><span data-stu-id="f46c8-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="f46c8-132">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="f46c8-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="f46c8-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f46c8-133">-MaxCount</span></span>
<span data-ttu-id="f46c8-134">Especifica o número máximo de pools a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="f46c8-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="f46c8-135">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="f46c8-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="f46c8-136">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="f46c8-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="f46c8-137">-Selecione</span><span class="sxs-lookup"><span data-stu-id="f46c8-137">-Select</span></span>
<span data-ttu-id="f46c8-138">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="f46c8-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="f46c8-139">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="f46c8-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="f46c8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46c8-140">CommonParameters</span></span>
<span data-ttu-id="f46c8-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46c8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46c8-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46c8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46c8-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f46c8-143">INPUTS</span></span>

### <span data-ttu-id="f46c8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f46c8-144">System.String</span></span>

### <span data-ttu-id="f46c8-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f46c8-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f46c8-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f46c8-146">OUTPUTS</span></span>

### <span data-ttu-id="f46c8-147">Microsoft.Azure.Commands.Batch. Modelos. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="f46c8-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="f46c8-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f46c8-148">NOTES</span></span>

## <span data-ttu-id="f46c8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f46c8-149">RELATED LINKS</span></span>

[<span data-ttu-id="f46c8-150">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f46c8-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f46c8-151">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f46c8-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="f46c8-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f46c8-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="f46c8-153">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="f46c8-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


