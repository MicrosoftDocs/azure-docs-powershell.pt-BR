---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432416"
---
# <span data-ttu-id="da2e1-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="da2e1-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="da2e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da2e1-102">SYNOPSIS</span></span>
<span data-ttu-id="da2e1-103">Obter `Reservation` histórico de revisão.</span><span class="sxs-lookup"><span data-stu-id="da2e1-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da2e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da2e1-104">SYNTAX</span></span>

### <span data-ttu-id="da2e1-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="da2e1-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="da2e1-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="da2e1-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="da2e1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da2e1-107">DESCRIPTION</span></span>
<span data-ttu-id="da2e1-108">Lista de todas as revisões para o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="da2e1-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="da2e1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da2e1-109">EXAMPLES</span></span>

### <span data-ttu-id="da2e1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da2e1-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="da2e1-111">Obter o histórico de revisão da reserva específica</span><span class="sxs-lookup"><span data-stu-id="da2e1-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="da2e1-112">OS</span><span class="sxs-lookup"><span data-stu-id="da2e1-112">PARAMETERS</span></span>

### <span data-ttu-id="da2e1-113">-Reserva</span><span class="sxs-lookup"><span data-stu-id="da2e1-113">-Reservation</span></span>
<span data-ttu-id="da2e1-114">Parâmetro do objeto pipe para `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="da2e1-114">Pipe object parameter for `Reservation`s</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da2e1-115">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="da2e1-115">-ReservationId</span></span>
<span data-ttu-id="da2e1-116">Reservaid do `Reservation` do qual o histórico deve ser mostrado</span><span class="sxs-lookup"><span data-stu-id="da2e1-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da2e1-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="da2e1-117">-ReservationOrderId</span></span>
<span data-ttu-id="da2e1-118">ReservationOrderId para o `ReservationOrder` que contém o `Reservation`</span><span class="sxs-lookup"><span data-stu-id="da2e1-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da2e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da2e1-119">CommonParameters</span></span>
<span data-ttu-id="da2e1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da2e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da2e1-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da2e1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da2e1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da2e1-122">INPUTS</span></span>

### <span data-ttu-id="da2e1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="da2e1-123">System.String</span></span>
<span data-ttu-id="da2e1-124">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="da2e1-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="da2e1-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da2e1-125">OUTPUTS</span></span>

### <span data-ttu-id="da2e1-126">Microsoft. Azure. Commands. reservas. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="da2e1-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="da2e1-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da2e1-127">NOTES</span></span>

## <span data-ttu-id="da2e1-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da2e1-128">RELATED LINKS</span></span>

