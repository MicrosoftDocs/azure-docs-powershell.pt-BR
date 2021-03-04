---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: 7c3aff3f69ae76765a80c7db1e66ee0a79990c9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885945"
---
# <span data-ttu-id="df1b8-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="df1b8-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="df1b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="df1b8-103">Obtém pools em lotes na conta Batch especificada.</span><span class="sxs-lookup"><span data-stu-id="df1b8-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="df1b8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="df1b8-104">SYNTAX</span></span>

### <span data-ttu-id="df1b8-105">ODataFilter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df1b8-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df1b8-106">Id</span><span class="sxs-lookup"><span data-stu-id="df1b8-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df1b8-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="df1b8-107">DESCRIPTION</span></span>
<span data-ttu-id="df1b8-108">O cmdlet **Get-AzBatchPool** obtém os pools do Lote do Azure na conta Batch especificada com o parâmetro *BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="df1b8-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="df1b8-109">Você pode usar o parâmetro *Id* para obter um único pool ou pode usar o parâmetro *Filter* para obter os pools que corresponderem a um filtro OData (Protocolo de Dados Abertos).</span><span class="sxs-lookup"><span data-stu-id="df1b8-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="df1b8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df1b8-110">EXAMPLES</span></span>

### <span data-ttu-id="df1b8-111">Exemplo 1: Obter um pool por ID</span><span class="sxs-lookup"><span data-stu-id="df1b8-111">Example 1: Get a pool by ID</span></span>
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
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="df1b8-112">Este comando obtém o pool com a ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="df1b8-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="df1b8-113">Exemplo 2: Obter todos os pools usando um filtro OData</span><span class="sxs-lookup"><span data-stu-id="df1b8-113">Example 2: Get all pools using an OData filter</span></span>
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
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="df1b8-114">Este comando obtém os pools cujas IDs começam com My usando o *parâmetro Filter.*</span><span class="sxs-lookup"><span data-stu-id="df1b8-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="df1b8-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="df1b8-115">PARAMETERS</span></span>

### <span data-ttu-id="df1b8-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="df1b8-116">-BatchContext</span></span>
<span data-ttu-id="df1b8-117">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="df1b8-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="df1b8-118">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="df1b8-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="df1b8-119">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="df1b8-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="df1b8-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="df1b8-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="df1b8-121">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="df1b8-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="df1b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1b8-122">-DefaultProfile</span></span>
<span data-ttu-id="df1b8-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="df1b8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df1b8-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="df1b8-124">-Expand</span></span>
<span data-ttu-id="df1b8-125">Especifica uma cláusula de expansão do Protocolo de Dados Abertos (OData).</span><span class="sxs-lookup"><span data-stu-id="df1b8-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="df1b8-126">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obter.</span><span class="sxs-lookup"><span data-stu-id="df1b8-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="df1b8-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="df1b8-127">-Filter</span></span>
<span data-ttu-id="df1b8-128">Especifica a cláusula de filtro OData a ser usada ao consultar pools.</span><span class="sxs-lookup"><span data-stu-id="df1b8-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="df1b8-129">Se você não especificar um filtro, todos os pools sob a conta Batch especificada com o *parâmetro BatchContext* serão retornados.</span><span class="sxs-lookup"><span data-stu-id="df1b8-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="df1b8-130">-Id</span><span class="sxs-lookup"><span data-stu-id="df1b8-130">-Id</span></span>
<span data-ttu-id="df1b8-131">Especifica a ID do pool a ser obter.</span><span class="sxs-lookup"><span data-stu-id="df1b8-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="df1b8-132">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="df1b8-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="df1b8-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="df1b8-133">-MaxCount</span></span>
<span data-ttu-id="df1b8-134">Especifica o número máximo de pools a retornar.</span><span class="sxs-lookup"><span data-stu-id="df1b8-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="df1b8-135">Se você especificar um valor zero (0) ou menor, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="df1b8-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="df1b8-136">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="df1b8-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="df1b8-137">-Select</span><span class="sxs-lookup"><span data-stu-id="df1b8-137">-Select</span></span>
<span data-ttu-id="df1b8-138">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="df1b8-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="df1b8-139">Especifique um valor para que esse parâmetro receba propriedades específicas, em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="df1b8-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="df1b8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1b8-140">CommonParameters</span></span>
<span data-ttu-id="df1b8-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1b8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1b8-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df1b8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1b8-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df1b8-143">INPUTS</span></span>

### <span data-ttu-id="df1b8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="df1b8-144">System.String</span></span>

### <span data-ttu-id="df1b8-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="df1b8-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="df1b8-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="df1b8-146">OUTPUTS</span></span>

### <span data-ttu-id="df1b8-147">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="df1b8-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="df1b8-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="df1b8-148">NOTES</span></span>

## <span data-ttu-id="df1b8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df1b8-149">RELATED LINKS</span></span>

[<span data-ttu-id="df1b8-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="df1b8-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="df1b8-151">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="df1b8-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="df1b8-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="df1b8-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="df1b8-153">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="df1b8-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
