---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 6428e4df850d2806939f5d9f8d4e115698e91fb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602289"
---
# <span data-ttu-id="4fce2-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="4fce2-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="4fce2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fce2-102">SYNOPSIS</span></span>
<span data-ttu-id="4fce2-103">Combina dois `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="4fce2-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fce2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fce2-104">SYNTAX</span></span>

### <span data-ttu-id="4fce2-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fce2-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fce2-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="4fce2-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fce2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fce2-107">DESCRIPTION</span></span>
<span data-ttu-id="4fce2-108">Mescle o `Reservation` s especificado em um novo `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="4fce2-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="4fce2-109">Os dois `Reservation` s sendo mesclados devem ter as mesmas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4fce2-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="4fce2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fce2-110">EXAMPLES</span></span>

### <span data-ttu-id="4fce2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fce2-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="4fce2-112">Mesclar os dois `Reservation` s especificados em um `Reservation`</span><span class="sxs-lookup"><span data-stu-id="4fce2-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="4fce2-113">OS</span><span class="sxs-lookup"><span data-stu-id="4fce2-113">PARAMETERS</span></span>

### <span data-ttu-id="4fce2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fce2-114">-DefaultProfile</span></span>
<span data-ttu-id="4fce2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fce2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fce2-116">-Reserva</span><span class="sxs-lookup"><span data-stu-id="4fce2-116">-Reservation</span></span>
<span data-ttu-id="4fce2-117">Cadeias de caracteres separadas por vírgula de dois ReservationIds para mesclar</span><span class="sxs-lookup"><span data-stu-id="4fce2-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="4fce2-118">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="4fce2-118">-ReservationId</span></span>
<span data-ttu-id="4fce2-119">ReservationOrderId para o `ReservationOrder` que contém os dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="4fce2-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="4fce2-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="4fce2-120">-ReservationOrderId</span></span>
<span data-ttu-id="4fce2-121">{{Fill ReservationOrderId descrição}}</span><span class="sxs-lookup"><span data-stu-id="4fce2-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="4fce2-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4fce2-122">-Confirm</span></span>
<span data-ttu-id="4fce2-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fce2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fce2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fce2-124">-WhatIf</span></span>
<span data-ttu-id="4fce2-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4fce2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fce2-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fce2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fce2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fce2-127">CommonParameters</span></span>
<span data-ttu-id="4fce2-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fce2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fce2-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fce2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fce2-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fce2-130">INPUTS</span></span>

### <span data-ttu-id="4fce2-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4fce2-131">None</span></span>

## <span data-ttu-id="4fce2-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fce2-132">OUTPUTS</span></span>

### <span data-ttu-id="4fce2-133">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="4fce2-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="4fce2-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fce2-134">NOTES</span></span>

## <span data-ttu-id="4fce2-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fce2-135">RELATED LINKS</span></span>
