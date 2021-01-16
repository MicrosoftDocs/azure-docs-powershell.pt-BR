---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: 0dfdec27fe53aaf40ebd46a2c623047381faa554
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430401"
---
# <span data-ttu-id="168d6-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="168d6-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="168d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="168d6-102">SYNOPSIS</span></span>
<span data-ttu-id="168d6-103">Obter Marketplaces da assinatura.</span><span class="sxs-lookup"><span data-stu-id="168d6-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="168d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="168d6-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="168d6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="168d6-105">DESCRIPTION</span></span>
<span data-ttu-id="168d6-106">O cmdlet **Get-AzConsumptionMarketplace** Obtém Marketplaces da assinatura.</span><span class="sxs-lookup"><span data-stu-id="168d6-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="168d6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="168d6-107">EXAMPLES</span></span>

### <span data-ttu-id="168d6-108">Exemplo 1: obter uso do Marketplace</span><span class="sxs-lookup"><span data-stu-id="168d6-108">Example 1: Get marketplaces usage</span></span>
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

### <span data-ttu-id="168d6-109">Exemplo 2: obter uso do Marketplace com o intervalo de datas</span><span class="sxs-lookup"><span data-stu-id="168d6-109">Example 2: Get marketplace usage with date range</span></span>
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

### <span data-ttu-id="168d6-110">Exemplo 3: obter o uso do Marketplace de BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="168d6-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
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

### <span data-ttu-id="168d6-111">Exemplo 4: obter uso do Marketplace com o filtro InstanceName</span><span class="sxs-lookup"><span data-stu-id="168d6-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
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

## <span data-ttu-id="168d6-112">OS</span><span class="sxs-lookup"><span data-stu-id="168d6-112">PARAMETERS</span></span>

### <span data-ttu-id="168d6-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="168d6-113">-BillingPeriodName</span></span>
<span data-ttu-id="168d6-114">Nome de um período de cobrança específico para obter o Marketplace associado.</span><span class="sxs-lookup"><span data-stu-id="168d6-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="168d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168d6-115">-DefaultProfile</span></span>
<span data-ttu-id="168d6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="168d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="168d6-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="168d6-117">-EndDate</span></span>
<span data-ttu-id="168d6-118">A data de término (em UTC) dos Marketplaces a serem filtrados.</span><span class="sxs-lookup"><span data-stu-id="168d6-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="168d6-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="168d6-119">-InstanceId</span></span>
<span data-ttu-id="168d6-120">A ID da instância dos Marketplaces a serem filtradas.</span><span class="sxs-lookup"><span data-stu-id="168d6-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="168d6-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="168d6-121">-InstanceName</span></span>
<span data-ttu-id="168d6-122">O nome da instância dos Marketplaces a serem filtrados.</span><span class="sxs-lookup"><span data-stu-id="168d6-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="168d6-123">-Resource</span><span class="sxs-lookup"><span data-stu-id="168d6-123">-ResourceGroup</span></span>
<span data-ttu-id="168d6-124">O grupo de recursos dos Marketplaces para filtrar.</span><span class="sxs-lookup"><span data-stu-id="168d6-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="168d6-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="168d6-125">-StartDate</span></span>
<span data-ttu-id="168d6-126">A data de início (em UTC) dos Marketplaces para filtrar.</span><span class="sxs-lookup"><span data-stu-id="168d6-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="168d6-127">-Início</span><span class="sxs-lookup"><span data-stu-id="168d6-127">-Top</span></span>
<span data-ttu-id="168d6-128">Determine o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="168d6-128">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="168d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168d6-129">CommonParameters</span></span>
<span data-ttu-id="168d6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="168d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168d6-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="168d6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168d6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="168d6-132">INPUTS</span></span>

### <span data-ttu-id="168d6-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="168d6-133">None</span></span>

## <span data-ttu-id="168d6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="168d6-134">OUTPUTS</span></span>

### <span data-ttu-id="168d6-135">Microsoft. Azure. Commands. consumo. Models. PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="168d6-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="168d6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="168d6-136">NOTES</span></span>

## <span data-ttu-id="168d6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="168d6-137">RELATED LINKS</span></span>
