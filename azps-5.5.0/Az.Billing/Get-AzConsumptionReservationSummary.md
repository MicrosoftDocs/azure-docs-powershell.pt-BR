---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115518"
---
# <span data-ttu-id="0d17b-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="0d17b-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="0d17b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d17b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d17b-103">Obter resumos de reserva para o trigo diário ou mensal.</span><span class="sxs-lookup"><span data-stu-id="0d17b-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="0d17b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d17b-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d17b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d17b-105">DESCRIPTION</span></span>
<span data-ttu-id="0d17b-106">O cmdlet **Get-AzConsumptionReservationSummary obtém** resumos de reserva para o trigo diário ou mensal.</span><span class="sxs-lookup"><span data-stu-id="0d17b-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="0d17b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d17b-107">EXAMPLES</span></span>

### <span data-ttu-id="0d17b-108">Exemplo 1: Obter resumos de reserva com ID do pedido de reserva para o trigo mensal</span><span class="sxs-lookup"><span data-stu-id="0d17b-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="0d17b-109">Exemplo 2: Obter resumos de reserva com ID do pedido de reserva e ID de reserva para o trigo mensal</span><span class="sxs-lookup"><span data-stu-id="0d17b-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="0d17b-110">Exemplo 3: Obter resumos de reserva com ID do pedido de reserva para intervalo de datas fornecidos diariamente</span><span class="sxs-lookup"><span data-stu-id="0d17b-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="0d17b-111">Exemplo 4: Obter resumos de reserva com ID do pedido de reserva e ID de reserva para intervalo de datas fornecidos diariamente</span><span class="sxs-lookup"><span data-stu-id="0d17b-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="0d17b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d17b-112">PARAMETERS</span></span>

### <span data-ttu-id="0d17b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d17b-113">-DefaultProfile</span></span>
<span data-ttu-id="0d17b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d17b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d17b-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0d17b-115">-EndDate</span></span>
<span data-ttu-id="0d17b-116">Os dados de término (AAAA-MM-DD em UTC) do resumo da reserva, necessários somente para os trigos diários.</span><span class="sxs-lookup"><span data-stu-id="0d17b-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="0d17b-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="0d17b-117">-Grain</span></span>
<span data-ttu-id="0d17b-118">O tempo do resumo da reserva pode ser diário ou mensal.</span><span class="sxs-lookup"><span data-stu-id="0d17b-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d17b-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="0d17b-119">-ReservationId</span></span>
<span data-ttu-id="0d17b-120">O identificador de uma reserva dentro de um pedido de reserva.</span><span class="sxs-lookup"><span data-stu-id="0d17b-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="0d17b-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0d17b-121">-ReservationOrderId</span></span>
<span data-ttu-id="0d17b-122">O identificador de uma compra de reserva.</span><span class="sxs-lookup"><span data-stu-id="0d17b-122">The identifier of a reservation purchase.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d17b-123">-Data Inicial</span><span class="sxs-lookup"><span data-stu-id="0d17b-123">-StartDate</span></span>
<span data-ttu-id="0d17b-124">Os dados de início (YYYYY-MM-DD em UTC) do resumo da reserva, necessários somente para os trigos diários.</span><span class="sxs-lookup"><span data-stu-id="0d17b-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="0d17b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d17b-125">CommonParameters</span></span>
<span data-ttu-id="0d17b-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d17b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d17b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d17b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d17b-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d17b-128">INPUTS</span></span>

### <span data-ttu-id="0d17b-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0d17b-129">None</span></span>

## <span data-ttu-id="0d17b-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d17b-130">OUTPUTS</span></span>

### <span data-ttu-id="0d17b-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="0d17b-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="0d17b-132">Notas</span><span class="sxs-lookup"><span data-stu-id="0d17b-132">NOTES</span></span>

## <span data-ttu-id="0d17b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d17b-133">RELATED LINKS</span></span>
