---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationDetail.md
ms.openlocfilehash: a7a4b50198a63329b0d45986f2bce60edb927777
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602113"
---
# <span data-ttu-id="acb1c-101">Get-AzureRmConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="acb1c-101">Get-AzureRmConsumptionReservationDetail</span></span>

## <span data-ttu-id="acb1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acb1c-102">SYNOPSIS</span></span>
<span data-ttu-id="acb1c-103">Obter detalhes das reservas para o intervalo de datas fornecido.</span><span class="sxs-lookup"><span data-stu-id="acb1c-103">Get reservations details for provided date range.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acb1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acb1c-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acb1c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acb1c-105">DESCRIPTION</span></span>
<span data-ttu-id="acb1c-106">O cmdlet **Get-AzureRmConsumptionReservationDetail** Obtém detalhes de reservas para o intervalo de datas fornecido.</span><span class="sxs-lookup"><span data-stu-id="acb1c-106">The **Get-AzureRmConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="acb1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acb1c-107">EXAMPLES</span></span>

### <span data-ttu-id="acb1c-108">Exemplo 1: obter detalhes de reserva com ID de ordem de reserva para o intervalo de datas fornecido</span><span class="sxs-lookup"><span data-stu-id="acb1c-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="acb1c-109">Exemplo 2: obter detalhes de reserva com ID de ordem de reserva e ID de reserva para o intervalo de datas fornecido</span><span class="sxs-lookup"><span data-stu-id="acb1c-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="acb1c-110">OS</span><span class="sxs-lookup"><span data-stu-id="acb1c-110">PARAMETERS</span></span>

### <span data-ttu-id="acb1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb1c-111">-DefaultProfile</span></span>
<span data-ttu-id="acb1c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acb1c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acb1c-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="acb1c-113">-EndDate</span></span>
<span data-ttu-id="acb1c-114">Os dados finais (AAAA-MM-DD em UTC) do detalhe da reserva.</span><span class="sxs-lookup"><span data-stu-id="acb1c-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb1c-115">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="acb1c-115">-ReservationId</span></span>
<span data-ttu-id="acb1c-116">O identificador de uma reserva em uma ordem de reserva.</span><span class="sxs-lookup"><span data-stu-id="acb1c-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="acb1c-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="acb1c-117">-ReservationOrderId</span></span>
<span data-ttu-id="acb1c-118">O identificador de uma compra de reserva.</span><span class="sxs-lookup"><span data-stu-id="acb1c-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="acb1c-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="acb1c-119">-StartDate</span></span>
<span data-ttu-id="acb1c-120">Os dados de início (AAAA-MM-DD em UTC) do detalhe da reserva.</span><span class="sxs-lookup"><span data-stu-id="acb1c-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb1c-121">CommonParameters</span></span>
<span data-ttu-id="acb1c-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acb1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb1c-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acb1c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb1c-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acb1c-124">INPUTS</span></span>

### <span data-ttu-id="acb1c-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="acb1c-125">None</span></span>

## <span data-ttu-id="acb1c-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acb1c-126">OUTPUTS</span></span>

### <span data-ttu-id="acb1c-127">Microsoft. Azure. Commands. consumo. Models. PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="acb1c-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="acb1c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acb1c-128">NOTES</span></span>

## <span data-ttu-id="acb1c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acb1c-129">RELATED LINKS</span></span>
