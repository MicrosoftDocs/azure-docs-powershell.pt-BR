---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441447"
---
# <span data-ttu-id="f4e3b-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="f4e3b-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="f4e3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e3b-103">Obter `Reservation` histórico de revisão.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4e3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4e3b-104">SYNTAX</span></span>

### <span data-ttu-id="f4e3b-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4e3b-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="f4e3b-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4e3b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4e3b-107">DESCRIPTION</span></span>
<span data-ttu-id="f4e3b-108">Lista de todas as revisões para o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="f4e3b-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="f4e3b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4e3b-109">EXAMPLES</span></span>

### <span data-ttu-id="f4e3b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4e3b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="f4e3b-111">Obter o histórico de revisão da reserva específica</span><span class="sxs-lookup"><span data-stu-id="f4e3b-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="f4e3b-112">OS</span><span class="sxs-lookup"><span data-stu-id="f4e3b-112">PARAMETERS</span></span>

### <span data-ttu-id="f4e3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e3b-113">-DefaultProfile</span></span>
<span data-ttu-id="f4e3b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e3b-115">-Reserva</span><span class="sxs-lookup"><span data-stu-id="f4e3b-115">-Reservation</span></span>
<span data-ttu-id="f4e3b-116">Parâmetro do objeto pipe para `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="f4e3b-116">Pipe object parameter for `Reservation`s</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3b-117">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="f4e3b-117">-ReservationId</span></span>
<span data-ttu-id="f4e3b-118">Reservaid do `Reservation` do qual o histórico deve ser mostrado</span><span class="sxs-lookup"><span data-stu-id="f4e3b-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3b-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f4e3b-119">-ReservationOrderId</span></span>
<span data-ttu-id="f4e3b-120">ReservationOrderId para o `ReservationOrder` que contém o `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f4e3b-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e3b-121">CommonParameters</span></span>
<span data-ttu-id="f4e3b-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e3b-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e3b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e3b-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4e3b-124">INPUTS</span></span>

### <span data-ttu-id="f4e3b-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f4e3b-125">System.Guid</span></span>

### <span data-ttu-id="f4e3b-126">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="f4e3b-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="f4e3b-127">Parâmetros: Reserva (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="f4e3b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4e3b-128">OUTPUTS</span></span>

### <span data-ttu-id="f4e3b-129">Microsoft. Azure. Commands. reservas. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="f4e3b-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="f4e3b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4e3b-130">NOTES</span></span>

## <span data-ttu-id="f4e3b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4e3b-131">RELATED LINKS</span></span>
