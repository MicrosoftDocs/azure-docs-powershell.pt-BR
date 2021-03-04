---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: c0016eed43fa315a7bb135153c8b00c47248f235
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891689"
---
# <span data-ttu-id="065e1-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="065e1-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="065e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="065e1-102">SYNOPSIS</span></span>
<span data-ttu-id="065e1-103">Obter `Reservation` histórico de revisão.</span><span class="sxs-lookup"><span data-stu-id="065e1-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="065e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="065e1-104">SYNTAX</span></span>

### <span data-ttu-id="065e1-105">CommandLine (Padrão)</span><span class="sxs-lookup"><span data-stu-id="065e1-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="065e1-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="065e1-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="065e1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="065e1-107">DESCRIPTION</span></span>
<span data-ttu-id="065e1-108">Lista de todas as revisões para `Reservation` o .</span><span class="sxs-lookup"><span data-stu-id="065e1-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="065e1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="065e1-109">EXAMPLES</span></span>

### <span data-ttu-id="065e1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="065e1-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="065e1-111">Obter o histórico de revisão da reserva específica</span><span class="sxs-lookup"><span data-stu-id="065e1-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="065e1-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="065e1-112">PARAMETERS</span></span>

### <span data-ttu-id="065e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="065e1-113">-DefaultProfile</span></span>
<span data-ttu-id="065e1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="065e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="065e1-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="065e1-115">-Reservation</span></span>
<span data-ttu-id="065e1-116">Parâmetro do objeto Pipe para `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="065e1-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="065e1-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="065e1-117">-ReservationId</span></span>
<span data-ttu-id="065e1-118">ReservationId do `Reservation` qual o histórico deve ser mostrado</span><span class="sxs-lookup"><span data-stu-id="065e1-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="065e1-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="065e1-119">-ReservationOrderId</span></span>
<span data-ttu-id="065e1-120">ReservationOrderId para o `ReservationOrder` que contém o `Reservation`</span><span class="sxs-lookup"><span data-stu-id="065e1-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="065e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065e1-121">CommonParameters</span></span>
<span data-ttu-id="065e1-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="065e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065e1-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="065e1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065e1-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="065e1-124">INPUTS</span></span>

### <span data-ttu-id="065e1-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="065e1-125">System.Guid</span></span>

### <span data-ttu-id="065e1-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="065e1-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="065e1-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="065e1-127">OUTPUTS</span></span>

### <span data-ttu-id="065e1-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="065e1-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="065e1-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="065e1-129">NOTES</span></span>

## <span data-ttu-id="065e1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="065e1-130">RELATED LINKS</span></span>
