---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 1700e20318a502f32386638f94a9c5c86c271d7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117947"
---
# <span data-ttu-id="0c842-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="0c842-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="0c842-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c842-102">SYNOPSIS</span></span>
<span data-ttu-id="0c842-103">Obtém métricas de uso de pool para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="0c842-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="0c842-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c842-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c842-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c842-105">DESCRIPTION</span></span>
<span data-ttu-id="0c842-106">O cmdlet **Get-AzBatchPoolUsageMetric** obtém as métricas de uso, agregadas por pool em intervalos de tempo individuais, para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="0c842-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="0c842-107">Você pode obter as estatísticas para um pool específico e para um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="0c842-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="0c842-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c842-108">EXAMPLES</span></span>

### <span data-ttu-id="0c842-109">Exemplo 1: Obter métricas de uso de pool para um intervalo de tempo</span><span class="sxs-lookup"><span data-stu-id="0c842-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
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

<span data-ttu-id="0c842-110">O primeiro comando cria uma referência de objeto às teclas de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="0c842-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="0c842-111">O comando armazena essa referência de objeto na variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="0c842-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="0c842-112">Os dois comandos a seguir criam **objetos DateTime** usando o cmdlet Get-Date dados.</span><span class="sxs-lookup"><span data-stu-id="0c842-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="0c842-113">Os comandos armazenam esses valores nas variáveis $StartTime e $EndTime para uso com o comando final.</span><span class="sxs-lookup"><span data-stu-id="0c842-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="0c842-114">O comando final retorna todas as métricas de uso do pool, agregadas por pool, no intervalo de tempo entre as horas de início e de término especificadas.</span><span class="sxs-lookup"><span data-stu-id="0c842-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="0c842-115">Exemplo 2: Obter métricas de uso de pool usando um filtro</span><span class="sxs-lookup"><span data-stu-id="0c842-115">Example 2: Get pool usage metrics by using a filter</span></span>
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

<span data-ttu-id="0c842-116">Esse comando retorna as métricas de uso do pool chamado ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="0c842-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="0c842-117">O comando especifica uma cadeia de caracteres de filtro para especificar esse pool e usa o mesmo $Context valor do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="0c842-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="0c842-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c842-118">PARAMETERS</span></span>

### <span data-ttu-id="0c842-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0c842-119">-BatchContext</span></span>
<span data-ttu-id="0c842-120">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="0c842-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0c842-121">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="0c842-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0c842-122">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="0c842-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0c842-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="0c842-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0c842-124">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0c842-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0c842-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c842-125">-DefaultProfile</span></span>
<span data-ttu-id="0c842-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0c842-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c842-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0c842-127">-EndTime</span></span>
<span data-ttu-id="0c842-128">Especifica o fim de um intervalo de tempo para o qual este cmdlet obtém métricas de uso.</span><span class="sxs-lookup"><span data-stu-id="0c842-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="0c842-129">Especifique uma hora pelo menos duas horas antes.</span><span class="sxs-lookup"><span data-stu-id="0c842-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="0c842-130">Se você não especificar uma hora de término, esse cmdlet usará o último intervalo de agregação disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="0c842-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="0c842-131">-Filtro</span><span class="sxs-lookup"><span data-stu-id="0c842-131">-Filter</span></span>
<span data-ttu-id="0c842-132">Especifica uma cláusula de filtro OData a ser usada para filtrar as métricas que esse cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="0c842-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="0c842-133">A única propriedade válida é **poolId** com um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0c842-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="0c842-134">Possíveis operações são as seguintes: eq, ge, gt, le, lt, startswith.</span><span class="sxs-lookup"><span data-stu-id="0c842-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="0c842-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0c842-135">-StartTime</span></span>
<span data-ttu-id="0c842-136">Especifica o início de um intervalo de tempo para o qual este cmdlet obtém métricas de uso.</span><span class="sxs-lookup"><span data-stu-id="0c842-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="0c842-137">Especifique uma hora pelo menos duas horas e meia antes.</span><span class="sxs-lookup"><span data-stu-id="0c842-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="0c842-138">Se você não especificar uma hora de início, esse cmdlet usará o último intervalo de agregação disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="0c842-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="0c842-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c842-139">CommonParameters</span></span>
<span data-ttu-id="0c842-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c842-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c842-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c842-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c842-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="0c842-142">INPUTS</span></span>

### <span data-ttu-id="0c842-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0c842-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0c842-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="0c842-144">OUTPUTS</span></span>

### <span data-ttu-id="0c842-145">Microsoft.Azure.Commands.Batch. Models.PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="0c842-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="0c842-146">Notas</span><span class="sxs-lookup"><span data-stu-id="0c842-146">NOTES</span></span>

## <span data-ttu-id="0c842-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c842-147">RELATED LINKS</span></span>

[<span data-ttu-id="0c842-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0c842-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0c842-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="0c842-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="0c842-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="0c842-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
