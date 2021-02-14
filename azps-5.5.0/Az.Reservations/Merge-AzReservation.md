---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110828"
---
# <span data-ttu-id="313f5-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="313f5-101">Merge-AzReservation</span></span>

## <span data-ttu-id="313f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="313f5-102">SYNOPSIS</span></span>
<span data-ttu-id="313f5-103">Mescla dois `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="313f5-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="313f5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="313f5-104">SYNTAX</span></span>

### <span data-ttu-id="313f5-105">CommandLine (Padrão)</span><span class="sxs-lookup"><span data-stu-id="313f5-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="313f5-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="313f5-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313f5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="313f5-107">DESCRIPTION</span></span>
<span data-ttu-id="313f5-108">Mesclar os `Reservation` s especificados em um `Reservation` novo.</span><span class="sxs-lookup"><span data-stu-id="313f5-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="313f5-109">Os dois `Reservation` que estão sendo mesclados devem ter as mesmas propriedades.</span><span class="sxs-lookup"><span data-stu-id="313f5-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="313f5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="313f5-110">EXAMPLES</span></span>

### <span data-ttu-id="313f5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="313f5-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="313f5-112">Mesclar os dois `Reservation` s especificados em um `Reservation`</span><span class="sxs-lookup"><span data-stu-id="313f5-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="313f5-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="313f5-113">PARAMETERS</span></span>

### <span data-ttu-id="313f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313f5-114">-DefaultProfile</span></span>
<span data-ttu-id="313f5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="313f5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="313f5-116">-Reserva</span><span class="sxs-lookup"><span data-stu-id="313f5-116">-Reservation</span></span>
<span data-ttu-id="313f5-117">Cadeias de caracteres separadas por vírgula de duas ReservationIds para mesclar</span><span class="sxs-lookup"><span data-stu-id="313f5-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="313f5-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="313f5-118">-ReservationId</span></span>
<span data-ttu-id="313f5-119">ReservationOrderId para o `ReservationOrder` que contém os dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="313f5-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="313f5-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="313f5-120">-ReservationOrderId</span></span>
<span data-ttu-id="313f5-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="313f5-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="313f5-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="313f5-122">-Confirm</span></span>
<span data-ttu-id="313f5-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="313f5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="313f5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313f5-124">-WhatIf</span></span>
<span data-ttu-id="313f5-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="313f5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="313f5-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="313f5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="313f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313f5-127">CommonParameters</span></span>
<span data-ttu-id="313f5-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="313f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313f5-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="313f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313f5-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="313f5-130">INPUTS</span></span>

### <span data-ttu-id="313f5-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="313f5-131">None</span></span>

## <span data-ttu-id="313f5-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="313f5-132">OUTPUTS</span></span>

### <span data-ttu-id="313f5-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="313f5-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="313f5-134">Notas</span><span class="sxs-lookup"><span data-stu-id="313f5-134">NOTES</span></span>

## <span data-ttu-id="313f5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="313f5-135">RELATED LINKS</span></span>
