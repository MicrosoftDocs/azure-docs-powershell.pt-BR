---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 47794cc34f3d259a57f021a93c1b17250b3546f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771297"
---
# <span data-ttu-id="3402f-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="3402f-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="3402f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3402f-102">SYNOPSIS</span></span>
<span data-ttu-id="3402f-103">Obter detalhes de uso da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3402f-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="3402f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3402f-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3402f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3402f-105">DESCRIPTION</span></span>
<span data-ttu-id="3402f-106">O cmdlet **Get-AzConsumptionUsageDetail** Obtém detalhes de uso da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3402f-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="3402f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3402f-107">EXAMPLES</span></span>

### <span data-ttu-id="3402f-108">Exemplo 1: obter detalhes de uso com a expansão de MeterDetails</span><span class="sxs-lookup"><span data-stu-id="3402f-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -Expand MeterDetails -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
ConsumedService:  Microsoft.Compute
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/usageDetails/24b9dff0-f022-55a1-886b-17b330000db3
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/MAR-CCM/providers/Microsoft.Compute/disks/mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
InstanceLocation:  usnorthcentral
InstanceName:  mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
IsEstimated:  true
MeterDetails:  MeterCategory:  Data Management
               MeterLocation:  usnorthcentral
               MeterName:  Standard Managed Disk Operations (in 10,000s)
               MeterSubCategory:  Data Management
               Unit:  Operations
MeterId:  82cd70ab-1aee-4b30-bc04-8b71e1204dbc
Name:  24b9dff0-f022-55a1-886b-17b330000db3
PretaxCost:  0
Product:  Data Management Standard Managed Disk Operations
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  6/1/2018 11:59:59 PM
UsageQuantity:  3.8218
UsageStart:  6/1/2018 12:00:00 AM
```

### <span data-ttu-id="3402f-109">Exemplo 2: obter detalhes de uso com o intervalo de datas</span><span class="sxs-lookup"><span data-stu-id="3402f-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/732582e5-40ad-bb23-7a69-ca1ff7c8b004
InstanceId:  storsimplezc9q6r2t7f
InstanceLocation:  US West Central
InstanceName:  storsimplezc9q6r2t7f
IsEstimated:  false
MeterId:  ad22fac8-9da5-4577-8683-56ae94d39e42
Name:  732582e5-40ad-bb23-7a69-ca1ff7c8b004
PretaxCost:  0
Product:  Data Management Geo Redundant Standard IO - Table Write
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/2/2017 11:59:59 PM
UsageQuantity:  0.0006
UsageStart:  10/2/2017 12:00:00 AM
```

### <span data-ttu-id="3402f-110">Exemplo 3: obter detalhes de uso do BillingPeriodName com o filtro InstanceName</span><span class="sxs-lookup"><span data-stu-id="3402f-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Microsoft.Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/8abc8b65-e8f1-31e1-f02b-058a7572363f
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/securitydata/providers/Microsoft.Storage/storageAccounts/1c2052westus
InstanceLocation:  uswest
InstanceName:  1c2052westus
IsEstimated:  false
MeterId:  9995d93a-7d35-4d3f-9c69-7a7fea447ef4
Name:  8abc8b65-e8f1-31e1-f02b-058a7572363f
PretaxCost:  0.000000693016692
Product:  Data Transfer Out - Zone 1
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/1/2017 11:59:59 PM
UsageQuantity:  0.000009
UsageStart:  10/1/2017 12:00:00 AM
```

## <span data-ttu-id="3402f-111">OS</span><span class="sxs-lookup"><span data-stu-id="3402f-111">PARAMETERS</span></span>

### <span data-ttu-id="3402f-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="3402f-112">-BillingPeriodName</span></span>
<span data-ttu-id="3402f-113">Nome de um período de cobrança específico para obter os detalhes de uso associados.</span><span class="sxs-lookup"><span data-stu-id="3402f-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="3402f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3402f-114">-DefaultProfile</span></span>
<span data-ttu-id="3402f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3402f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3402f-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="3402f-116">-EndDate</span></span>
<span data-ttu-id="3402f-117">A data de término (em UTC) dos usos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="3402f-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="3402f-118">-Expandir</span><span class="sxs-lookup"><span data-stu-id="3402f-118">-Expand</span></span>
<span data-ttu-id="3402f-119">Expanda os usos com base em MeterDetails ou AdditionalInfo.</span><span class="sxs-lookup"><span data-stu-id="3402f-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="3402f-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="3402f-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="3402f-121">Inclua propriedades adicionais nos usos.</span><span class="sxs-lookup"><span data-stu-id="3402f-121">Include additional properties in the usages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3402f-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="3402f-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="3402f-123">Inclua detalhes do medidor nos usos.</span><span class="sxs-lookup"><span data-stu-id="3402f-123">Include meter details in the usages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3402f-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3402f-124">-InstanceId</span></span>
<span data-ttu-id="3402f-125">A ID da instância dos usos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="3402f-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="3402f-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3402f-126">-InstanceName</span></span>
<span data-ttu-id="3402f-127">O nome da instância dos usos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="3402f-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="3402f-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3402f-128">-MaxCount</span></span>
<span data-ttu-id="3402f-129">Determine o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="3402f-129">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3402f-130">-Resource</span><span class="sxs-lookup"><span data-stu-id="3402f-130">-ResourceGroup</span></span>
<span data-ttu-id="3402f-131">O grupo de recursos dos usos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="3402f-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="3402f-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="3402f-132">-StartDate</span></span>
<span data-ttu-id="3402f-133">A data de início (em UTC) dos usos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="3402f-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="3402f-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="3402f-134">-Tag</span></span>
<span data-ttu-id="3402f-135">A marca de usos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="3402f-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="3402f-136">-Início</span><span class="sxs-lookup"><span data-stu-id="3402f-136">-Top</span></span>
<span data-ttu-id="3402f-137">Determine o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="3402f-137">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3402f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3402f-138">CommonParameters</span></span>
<span data-ttu-id="3402f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3402f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3402f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3402f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3402f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3402f-141">INPUTS</span></span>

### <span data-ttu-id="3402f-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3402f-142">None</span></span>

## <span data-ttu-id="3402f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3402f-143">OUTPUTS</span></span>

### <span data-ttu-id="3402f-144">Microsoft. Azure. Commands. consumo. Models. PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="3402f-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="3402f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3402f-145">NOTES</span></span>

## <span data-ttu-id="3402f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3402f-146">RELATED LINKS</span></span>
