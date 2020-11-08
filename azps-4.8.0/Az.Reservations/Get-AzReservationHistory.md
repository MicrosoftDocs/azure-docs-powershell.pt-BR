---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110994"
---
# <span data-ttu-id="e0418-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="e0418-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="e0418-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0418-102">SYNOPSIS</span></span>
<span data-ttu-id="e0418-103">Obter `Reservation` histórico de revisão.</span><span class="sxs-lookup"><span data-stu-id="e0418-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="e0418-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0418-104">SYNTAX</span></span>

### <span data-ttu-id="e0418-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0418-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0418-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="e0418-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0418-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0418-107">DESCRIPTION</span></span>
<span data-ttu-id="e0418-108">Lista de todas as revisões para o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e0418-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="e0418-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0418-109">EXAMPLES</span></span>

### <span data-ttu-id="e0418-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0418-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="e0418-111">Obter o histórico de revisão da reserva específica</span><span class="sxs-lookup"><span data-stu-id="e0418-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="e0418-112">OS</span><span class="sxs-lookup"><span data-stu-id="e0418-112">PARAMETERS</span></span>

### <span data-ttu-id="e0418-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0418-113">-DefaultProfile</span></span>
<span data-ttu-id="e0418-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0418-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0418-115">-Reserva</span><span class="sxs-lookup"><span data-stu-id="e0418-115">-Reservation</span></span>
<span data-ttu-id="e0418-116">Parâmetro do objeto pipe para `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="e0418-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="e0418-117">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="e0418-117">-ReservationId</span></span>
<span data-ttu-id="e0418-118">Reservaid do `Reservation` do qual o histórico deve ser mostrado</span><span class="sxs-lookup"><span data-stu-id="e0418-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="e0418-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e0418-119">-ReservationOrderId</span></span>
<span data-ttu-id="e0418-120">ReservationOrderId para o `ReservationOrder` que contém o `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e0418-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="e0418-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0418-121">CommonParameters</span></span>
<span data-ttu-id="e0418-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0418-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0418-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0418-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0418-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0418-124">INPUTS</span></span>

### <span data-ttu-id="e0418-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e0418-125">System.Guid</span></span>

### <span data-ttu-id="e0418-126">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="e0418-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e0418-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0418-127">OUTPUTS</span></span>

### <span data-ttu-id="e0418-128">Microsoft. Azure. Commands. reservas. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="e0418-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="e0418-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0418-129">NOTES</span></span>

## <span data-ttu-id="e0418-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0418-130">RELATED LINKS</span></span>
