---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 3587c5aa977647a8eda5b9f74f5ef6be5f1dd5ee
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93785058"
---
# <span data-ttu-id="e59d3-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="e59d3-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="e59d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e59d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e59d3-103">Obtém métricas de uso de pool para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="e59d3-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="e59d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e59d3-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e59d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e59d3-105">DESCRIPTION</span></span>
<span data-ttu-id="e59d3-106">O cmdlet **Get-AzBatchPoolUsageMetric** Obtém as métricas de uso agregadas pelo pool em intervalos de tempo individuais para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="e59d3-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="e59d3-107">Você pode obter as estatísticas para um pool específico e para um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="e59d3-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="e59d3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e59d3-108">EXAMPLES</span></span>

### <span data-ttu-id="e59d3-109">Exemplo 1: obter métricas de uso de pool para um intervalo de tempo</span><span class="sxs-lookup"><span data-stu-id="e59d3-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="e59d3-110">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="e59d3-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="e59d3-111">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="e59d3-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="e59d3-112">Os próximos dois comandos criam objetos **DateTime** usando o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="e59d3-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="e59d3-113">Os comandos armazenam esses valores nas variáveis $StartTime e $EndTime para uso com o comando final.</span><span class="sxs-lookup"><span data-stu-id="e59d3-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="e59d3-114">O comando final retorna todas as métricas de uso de pool agregadas por pool, em intervalo de tempo entre as horas de início e término especificadas.</span><span class="sxs-lookup"><span data-stu-id="e59d3-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="e59d3-115">Exemplo 2: obter métricas de uso de pool usando um filtro</span><span class="sxs-lookup"><span data-stu-id="e59d3-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="e59d3-116">Esse comando retorna as métricas de uso do pool chamado ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="e59d3-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="e59d3-117">O comando especifica uma cadeia de caracteres de filtro para especificar esse pool e usa o mesmo valor $Context que o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="e59d3-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="e59d3-118">OS</span><span class="sxs-lookup"><span data-stu-id="e59d3-118">PARAMETERS</span></span>

### <span data-ttu-id="e59d3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e59d3-119">-BatchContext</span></span>
<span data-ttu-id="e59d3-120">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e59d3-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e59d3-121">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e59d3-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e59d3-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="e59d3-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e59d3-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e59d3-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e59d3-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e59d3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e59d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59d3-125">-DefaultProfile</span></span>
<span data-ttu-id="e59d3-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e59d3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e59d3-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e59d3-127">-EndTime</span></span>
<span data-ttu-id="e59d3-128">Especifica o final de um intervalo de tempo para o qual esse cmdlet obtém métricas de uso.</span><span class="sxs-lookup"><span data-stu-id="e59d3-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="e59d3-129">Especifique uma hora pelo menos duas horas antes.</span><span class="sxs-lookup"><span data-stu-id="e59d3-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="e59d3-130">Se você não especificar uma hora de término, esse cmdlet usa o último intervalo de agregação disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="e59d3-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e59d3-131">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e59d3-131">-Filter</span></span>
<span data-ttu-id="e59d3-132">Especifica uma cláusula de filtro OData a ser usada para filtrar as métricas que esse cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="e59d3-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="e59d3-133">A única propriedade válida é **poolid** com um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e59d3-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="e59d3-134">As possíveis operações são as seguintes: EQ, GE, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="e59d3-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="e59d3-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e59d3-135">-StartTime</span></span>
<span data-ttu-id="e59d3-136">Especifica o início de um intervalo de tempo para o qual esse cmdlet obtém métricas de uso.</span><span class="sxs-lookup"><span data-stu-id="e59d3-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="e59d3-137">Especifique uma hora, pelo menos duas e meia a metade de horas anteriores.</span><span class="sxs-lookup"><span data-stu-id="e59d3-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="e59d3-138">Se você não especificar uma hora de início, este cmdlet usará o último intervalo de agregação disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="e59d3-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e59d3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59d3-139">CommonParameters</span></span>
<span data-ttu-id="e59d3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59d3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59d3-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e59d3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59d3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e59d3-142">INPUTS</span></span>

### <span data-ttu-id="e59d3-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e59d3-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e59d3-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e59d3-144">OUTPUTS</span></span>

### <span data-ttu-id="e59d3-145">Microsoft.Azure.Commands.Batch. Modelos. PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="e59d3-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="e59d3-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e59d3-146">NOTES</span></span>

## <span data-ttu-id="e59d3-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e59d3-147">RELATED LINKS</span></span>

[<span data-ttu-id="e59d3-148">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e59d3-148">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e59d3-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="e59d3-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="e59d3-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="e59d3-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)


