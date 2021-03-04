---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: 61ae392b3dbe8b73aaabd617b397e953f5caebec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891678"
---
# <span data-ttu-id="be630-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="be630-101">Merge-AzReservation</span></span>

## <span data-ttu-id="be630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be630-102">SYNOPSIS</span></span>
<span data-ttu-id="be630-103">Mescla dois `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="be630-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="be630-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="be630-104">SYNTAX</span></span>

### <span data-ttu-id="be630-105">CommandLine (Padrão)</span><span class="sxs-lookup"><span data-stu-id="be630-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be630-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="be630-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be630-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="be630-107">DESCRIPTION</span></span>
<span data-ttu-id="be630-108">Mesclar o `Reservation` s especificado em um novo `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="be630-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="be630-109">Os dois `Reservation` s que estão sendo mesclados devem ter as mesmas propriedades.</span><span class="sxs-lookup"><span data-stu-id="be630-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="be630-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be630-110">EXAMPLES</span></span>

### <span data-ttu-id="be630-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be630-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="be630-112">Mesclar os dois `Reservation` s especificados em um `Reservation`</span><span class="sxs-lookup"><span data-stu-id="be630-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="be630-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="be630-113">PARAMETERS</span></span>

### <span data-ttu-id="be630-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be630-114">-DefaultProfile</span></span>
<span data-ttu-id="be630-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be630-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be630-116">-Reservation</span><span class="sxs-lookup"><span data-stu-id="be630-116">-Reservation</span></span>
<span data-ttu-id="be630-117">Cadeias de caracteres separadas por vírgulas de duas ReservationIds para mesclar</span><span class="sxs-lookup"><span data-stu-id="be630-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be630-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="be630-118">-ReservationId</span></span>
<span data-ttu-id="be630-119">ReservationOrderId para `ReservationOrder` o que contém os dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="be630-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be630-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="be630-120">-ReservationOrderId</span></span>
<span data-ttu-id="be630-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="be630-121">{{Fill ReservationOrderId Description}}</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be630-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be630-122">-Confirm</span></span>
<span data-ttu-id="be630-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be630-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be630-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be630-124">-WhatIf</span></span>
<span data-ttu-id="be630-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be630-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be630-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be630-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be630-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be630-127">CommonParameters</span></span>
<span data-ttu-id="be630-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be630-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be630-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be630-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be630-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be630-130">INPUTS</span></span>

### <span data-ttu-id="be630-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="be630-131">None</span></span>

## <span data-ttu-id="be630-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="be630-132">OUTPUTS</span></span>

### <span data-ttu-id="be630-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="be630-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="be630-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="be630-134">NOTES</span></span>

## <span data-ttu-id="be630-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be630-135">RELATED LINKS</span></span>
