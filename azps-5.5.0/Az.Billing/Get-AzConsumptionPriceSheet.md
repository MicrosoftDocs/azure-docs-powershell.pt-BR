---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: 999466a754fdeeb98a3d8aaefd91f0b65a2810f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117924"
---
# <span data-ttu-id="2e371-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="2e371-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="2e371-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e371-102">SYNOPSIS</span></span>
<span data-ttu-id="2e371-103">Obter folhas de preços da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2e371-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="2e371-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e371-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e371-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e371-105">DESCRIPTION</span></span>
<span data-ttu-id="2e371-106">O cmdlet **Get-AzConsumptionPriceSheet obtém** folhas de preços da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2e371-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="2e371-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e371-107">EXAMPLES</span></span>

### <span data-ttu-id="2e371-108">Exemplo 1: Obter folhas de preços</span><span class="sxs-lookup"><span data-stu-id="2e371-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="2e371-109">Exemplo 2: Obter planilhas de preços com a expansão de MeterDetails</span><span class="sxs-lookup"><span data-stu-id="2e371-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="2e371-110">Exemplo 3: Obter folhas de preços de BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="2e371-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### <span data-ttu-id="2e371-111">Exemplo 4: Obter os 5 principais registros de folhas de preços</span><span class="sxs-lookup"><span data-stu-id="2e371-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## <span data-ttu-id="2e371-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e371-112">PARAMETERS</span></span>

### <span data-ttu-id="2e371-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="2e371-113">-BillingPeriodName</span></span>
<span data-ttu-id="2e371-114">Nome de um período de cobrança específico para obter as folhas de preços associadas.</span><span class="sxs-lookup"><span data-stu-id="2e371-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="2e371-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e371-115">-DefaultProfile</span></span>
<span data-ttu-id="2e371-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e371-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e371-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="2e371-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="2e371-118">Expanda as planilhas de preços com base em MeterDetails.</span><span class="sxs-lookup"><span data-stu-id="2e371-118">Expand the price sheets based on MeterDetails.</span></span>

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

### <span data-ttu-id="2e371-119">-Superior</span><span class="sxs-lookup"><span data-stu-id="2e371-119">-Top</span></span>
<span data-ttu-id="2e371-120">Determine o número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="2e371-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="2e371-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e371-121">CommonParameters</span></span>
<span data-ttu-id="2e371-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e371-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e371-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e371-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e371-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="2e371-124">INPUTS</span></span>

### <span data-ttu-id="2e371-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e371-125">None</span></span>

## <span data-ttu-id="2e371-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="2e371-126">OUTPUTS</span></span>

### <span data-ttu-id="2e371-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="2e371-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="2e371-128">Notas</span><span class="sxs-lookup"><span data-stu-id="2e371-128">NOTES</span></span>

## <span data-ttu-id="2e371-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e371-129">RELATED LINKS</span></span>
