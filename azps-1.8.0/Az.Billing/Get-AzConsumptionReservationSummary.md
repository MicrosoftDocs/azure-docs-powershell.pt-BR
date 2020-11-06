---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a224157fb8a0740b49cd2b3576e57da9b45c993b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601446"
---
# <span data-ttu-id="e9c23-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="e9c23-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="e9c23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9c23-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c23-103">Obter resumos de reserva para grãos diários ou mensais.</span><span class="sxs-lookup"><span data-stu-id="e9c23-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="e9c23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9c23-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9c23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9c23-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c23-106">O cmdlet **Get-AzConsumptionReservationSummay** tem resumos de reserva para grãos diários ou mensais.</span><span class="sxs-lookup"><span data-stu-id="e9c23-106">The **Get-AzConsumptionReservationSummay** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="e9c23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9c23-107">EXAMPLES</span></span>

### <span data-ttu-id="e9c23-108">Exemplo 1: obter resumos de reserva com ID de ordem de reserva para detalhamento mensal</span><span class="sxs-lookup"><span data-stu-id="e9c23-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
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

### <span data-ttu-id="e9c23-109">Exemplo 2: obter resumos de reserva com ID de ordem de reserva e ID de reserva para detalhamento mensal</span><span class="sxs-lookup"><span data-stu-id="e9c23-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
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

### <span data-ttu-id="e9c23-110">Exemplo 3: obter resumos de reserva com a ID do pedido de reserva para o intervalo de datas fornecido do detalhamento diário</span><span class="sxs-lookup"><span data-stu-id="e9c23-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
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

### <span data-ttu-id="e9c23-111">Exemplo 4: obter resumos de reserva com ID de ordem de reserva e ID de reserva para intervalo de datas fornecido em detalhamento diário</span><span class="sxs-lookup"><span data-stu-id="e9c23-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
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

## <span data-ttu-id="e9c23-112">OS</span><span class="sxs-lookup"><span data-stu-id="e9c23-112">PARAMETERS</span></span>

### <span data-ttu-id="e9c23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c23-113">-DefaultProfile</span></span>
<span data-ttu-id="e9c23-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c23-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e9c23-115">-EndDate</span></span>
<span data-ttu-id="e9c23-116">Os dados finais (AAAA-MM-DD em UTC) do Resumo de reserva, necessários somente para o detalhamento diário.</span><span class="sxs-lookup"><span data-stu-id="e9c23-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="e9c23-117">-Granular</span><span class="sxs-lookup"><span data-stu-id="e9c23-117">-Grain</span></span>
<span data-ttu-id="e9c23-118">O intervalo de tempo do resumo da reserva pode ser diária ou mensalmente.</span><span class="sxs-lookup"><span data-stu-id="e9c23-118">The time grain of the reservation summaryy, can be daily or monthly.</span></span>

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

### <span data-ttu-id="e9c23-119">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="e9c23-119">-ReservationId</span></span>
<span data-ttu-id="e9c23-120">O identificador de uma reserva em uma ordem de reserva.</span><span class="sxs-lookup"><span data-stu-id="e9c23-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="e9c23-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e9c23-121">-ReservationOrderId</span></span>
<span data-ttu-id="e9c23-122">O identificador de uma compra de reserva.</span><span class="sxs-lookup"><span data-stu-id="e9c23-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="e9c23-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e9c23-123">-StartDate</span></span>
<span data-ttu-id="e9c23-124">Os dados de início (AAAA-MM-DD em UTC) do Resumo de reserva são necessários somente para o detalhamento diário.</span><span class="sxs-lookup"><span data-stu-id="e9c23-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="e9c23-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c23-125">CommonParameters</span></span>
<span data-ttu-id="e9c23-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c23-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c23-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c23-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c23-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9c23-128">INPUTS</span></span>

### <span data-ttu-id="e9c23-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e9c23-129">None</span></span>

## <span data-ttu-id="e9c23-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9c23-130">OUTPUTS</span></span>

### <span data-ttu-id="e9c23-131">Microsoft. Azure. Commands. consumo. Models. PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="e9c23-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="e9c23-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9c23-132">NOTES</span></span>

## <span data-ttu-id="e9c23-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9c23-133">RELATED LINKS</span></span>
