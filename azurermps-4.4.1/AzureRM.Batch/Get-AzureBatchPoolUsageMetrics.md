---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: 4f985859cb26372a6ffc68b8521d08033fdc6670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441415"
---
# <span data-ttu-id="e84a1-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="e84a1-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="e84a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e84a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e84a1-103">Obtém métricas de uso de pool para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="e84a1-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e84a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e84a1-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e84a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e84a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e84a1-106">O cmdlet **Get-AzureBatchPoolUsageMetrics** Obtém as métricas de uso agregadas pelo pool em intervalos de tempo individuais para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="e84a1-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="e84a1-107">Você pode obter as estatísticas para um pool específico e para um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="e84a1-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="e84a1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e84a1-108">EXAMPLES</span></span>

### <span data-ttu-id="e84a1-109">Exemplo 1: obter métricas de uso de pool para um intervalo de tempo</span><span class="sxs-lookup"><span data-stu-id="e84a1-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
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

<span data-ttu-id="e84a1-110">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="e84a1-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="e84a1-111">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="e84a1-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="e84a1-112">Os próximos dois comandos criam objetos **DateTime** usando o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="e84a1-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="e84a1-113">Os comandos armazenam esses valores nas variáveis $StartTime e $EndTime para uso com o comando final.</span><span class="sxs-lookup"><span data-stu-id="e84a1-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>

<span data-ttu-id="e84a1-114">O comando final retorna todas as métricas de uso de pool agregadas por pool, em intervalo de tempo entre as horas de início e término especificadas.</span><span class="sxs-lookup"><span data-stu-id="e84a1-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="e84a1-115">Exemplo 2: obter métricas de uso de pool usando um filtro</span><span class="sxs-lookup"><span data-stu-id="e84a1-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="e84a1-116">Esse comando retorna as métricas de uso do pool chamado ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="e84a1-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="e84a1-117">O comando especifica uma cadeia de caracteres de filtro para especificar esse pool e usa o mesmo valor $Context que o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="e84a1-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="e84a1-118">OS</span><span class="sxs-lookup"><span data-stu-id="e84a1-118">PARAMETERS</span></span>

### <span data-ttu-id="e84a1-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e84a1-119">-BatchContext</span></span>
<span data-ttu-id="e84a1-120">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e84a1-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e84a1-121">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="e84a1-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="e84a1-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e84a1-122">-EndTime</span></span>
<span data-ttu-id="e84a1-123">Especifica o final de um intervalo de tempo para o qual esse cmdlet obtém métricas de uso.</span><span class="sxs-lookup"><span data-stu-id="e84a1-123">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="e84a1-124">Especifique uma hora pelo menos duas horas antes.</span><span class="sxs-lookup"><span data-stu-id="e84a1-124">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="e84a1-125">Se você não especificar uma hora de término, esse cmdlet usa o último intervalo de agregação disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="e84a1-125">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="e84a1-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e84a1-126">-Filter</span></span>
<span data-ttu-id="e84a1-127">Especifica uma cláusula de filtro OData a ser usada para filtrar as métricas que esse cmdlet retruns.</span><span class="sxs-lookup"><span data-stu-id="e84a1-127">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="e84a1-128">A única propriedade válida é **poolid** com um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e84a1-128">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="e84a1-129">As possíveis operações são as seguintes: EQ, GE, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="e84a1-129">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="e84a1-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e84a1-130">-StartTime</span></span>
<span data-ttu-id="e84a1-131">Especifica o início de um intervalo de tempo para o qual esse cmdlet obtém métricas de uso.</span><span class="sxs-lookup"><span data-stu-id="e84a1-131">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="e84a1-132">Especifique uma hora, pelo menos duas e meia a metade de horas anteriores.</span><span class="sxs-lookup"><span data-stu-id="e84a1-132">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="e84a1-133">Se você não especificar uma hora de início, este cmdlet usará o último intervalo de agregação disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="e84a1-133">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="e84a1-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84a1-134">-DefaultProfile</span></span>
<span data-ttu-id="e84a1-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e84a1-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e84a1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84a1-136">CommonParameters</span></span>
<span data-ttu-id="e84a1-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e84a1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84a1-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e84a1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84a1-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e84a1-139">INPUTS</span></span>

### <span data-ttu-id="e84a1-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e84a1-140">BatchAccountContext</span></span>
<span data-ttu-id="e84a1-141">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e84a1-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="e84a1-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e84a1-142">OUTPUTS</span></span>

### <span data-ttu-id="e84a1-143">PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="e84a1-143">PSPoolUsageMetrics</span></span>

## <span data-ttu-id="e84a1-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e84a1-144">NOTES</span></span>

## <span data-ttu-id="e84a1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e84a1-145">RELATED LINKS</span></span>

[<span data-ttu-id="e84a1-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e84a1-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e84a1-147">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="e84a1-147">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="e84a1-148">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="e84a1-148">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


