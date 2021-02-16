---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: 0dfdec27fe53aaf40ebd46a2c623047381faa554
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117927"
---
# <span data-ttu-id="d4281-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="d4281-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="d4281-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4281-102">SYNOPSIS</span></span>
<span data-ttu-id="d4281-103">Obter marketplaces da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4281-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="d4281-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4281-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4281-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4281-105">DESCRIPTION</span></span>
<span data-ttu-id="d4281-106">O cmdlet **Get-AzConsumptionMarketplace** obtém marketplaces da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4281-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="d4281-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d4281-107">EXAMPLES</span></span>

### <span data-ttu-id="d4281-108">Exemplo 1: Obter uso de marketplaces</span><span class="sxs-lookup"><span data-stu-id="d4281-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

### <span data-ttu-id="d4281-109">Exemplo 2: Obter uso do marketplace com intervalo de datas</span><span class="sxs-lookup"><span data-stu-id="d4281-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1/providers/Microsoft.Consumption/marketplaces/0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-01-04T00:00:00Z
UsageStart:  2018-01-03T00:00:00Z
```

### <span data-ttu-id="d4281-110">Exemplo 3: Obter uso do marketplace de BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="d4281-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1/providers/Microsoft.Consumption/marketplaces/ea82233a-9f76-7eaa-4478-42bd61cf6287
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  ea82233a-9f76-7eaa-4478-42bd61cf6287
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2017-10-29T00:00:00Z
UsageStart:  2017-10-28T00:00:00Z
```

### <span data-ttu-id="d4281-111">Exemplo 4: Obter o uso do marketplace com filtro Nomeda Instância</span><span class="sxs-lookup"><span data-stu-id="d4281-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -InstanceName TestVM -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

## <span data-ttu-id="d4281-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4281-112">PARAMETERS</span></span>

### <span data-ttu-id="d4281-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="d4281-113">-BillingPeriodName</span></span>
<span data-ttu-id="d4281-114">Nome de um período de cobrança específico para obter o marketplace associado.</span><span class="sxs-lookup"><span data-stu-id="d4281-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="d4281-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4281-115">-DefaultProfile</span></span>
<span data-ttu-id="d4281-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4281-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4281-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d4281-117">-EndDate</span></span>
<span data-ttu-id="d4281-118">A data de término (em UTC) dos marketplaces a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="d4281-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="d4281-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d4281-119">-InstanceId</span></span>
<span data-ttu-id="d4281-120">A ID de instância dos marketplaces a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="d4281-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="d4281-121">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="d4281-121">-InstanceName</span></span>
<span data-ttu-id="d4281-122">O nome da instância dos marketplaces a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="d4281-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="d4281-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d4281-123">-ResourceGroup</span></span>
<span data-ttu-id="d4281-124">O grupo de recursos dos marketplaces a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="d4281-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="d4281-125">-Data Inicial</span><span class="sxs-lookup"><span data-stu-id="d4281-125">-StartDate</span></span>
<span data-ttu-id="d4281-126">A data de início (em UTC) dos marketplaces a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="d4281-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="d4281-127">-Superior</span><span class="sxs-lookup"><span data-stu-id="d4281-127">-Top</span></span>
<span data-ttu-id="d4281-128">Determine o número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="d4281-128">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="d4281-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4281-129">CommonParameters</span></span>
<span data-ttu-id="d4281-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4281-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4281-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4281-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4281-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="d4281-132">INPUTS</span></span>

### <span data-ttu-id="d4281-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d4281-133">None</span></span>

## <span data-ttu-id="d4281-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="d4281-134">OUTPUTS</span></span>

### <span data-ttu-id="d4281-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="d4281-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="d4281-136">Notas</span><span class="sxs-lookup"><span data-stu-id="d4281-136">NOTES</span></span>

## <span data-ttu-id="d4281-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4281-137">RELATED LINKS</span></span>
