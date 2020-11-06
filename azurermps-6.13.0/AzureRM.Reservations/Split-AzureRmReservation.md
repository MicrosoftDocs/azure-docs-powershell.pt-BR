---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: bc1fba5c7fa7e01a3c2461907a214809e175f3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427175"
---
# <span data-ttu-id="95a88-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="95a88-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="95a88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95a88-102">SYNOPSIS</span></span>
<span data-ttu-id="95a88-103">Dividir a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="95a88-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95a88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95a88-104">SYNTAX</span></span>

### <span data-ttu-id="95a88-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="95a88-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95a88-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="95a88-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Int32[]> -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95a88-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95a88-107">DESCRIPTION</span></span>
<span data-ttu-id="95a88-108">Dividir um `Reservation` em dois `Reservation` s com distribuição de quantidade especificada.</span><span class="sxs-lookup"><span data-stu-id="95a88-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="95a88-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95a88-109">EXAMPLES</span></span>

### <span data-ttu-id="95a88-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95a88-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="95a88-111">Dividir o especificado `Reservation` em dois `Reservation` s com as quantidades correspondentes</span><span class="sxs-lookup"><span data-stu-id="95a88-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="95a88-112">OS</span><span class="sxs-lookup"><span data-stu-id="95a88-112">PARAMETERS</span></span>

### <span data-ttu-id="95a88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a88-113">-DefaultProfile</span></span>
<span data-ttu-id="95a88-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95a88-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95a88-115">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="95a88-115">-Quantity</span></span>
<span data-ttu-id="95a88-116">Inteiros separados por vírgula para o campo quantidade dos dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="95a88-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95a88-117">-Reserva</span><span class="sxs-lookup"><span data-stu-id="95a88-117">-Reservation</span></span>
<span data-ttu-id="95a88-118">Parâmetro do objeto pipe para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="95a88-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="95a88-119">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="95a88-119">-ReservationId</span></span>
<span data-ttu-id="95a88-120">ID do `Reservation` a ser dividida</span><span class="sxs-lookup"><span data-stu-id="95a88-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="95a88-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="95a88-121">-ReservationOrderId</span></span>
<span data-ttu-id="95a88-122">ID do `ReservationOrder` que contém o `Reservation` usuário que deseja dividir</span><span class="sxs-lookup"><span data-stu-id="95a88-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="95a88-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95a88-123">-Confirm</span></span>
<span data-ttu-id="95a88-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95a88-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a88-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a88-125">-WhatIf</span></span>
<span data-ttu-id="95a88-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95a88-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95a88-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95a88-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a88-128">CommonParameters</span></span>
<span data-ttu-id="95a88-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a88-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a88-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a88-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95a88-131">INPUTS</span></span>

### <span data-ttu-id="95a88-132">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="95a88-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="95a88-133">Parâmetros: Reserva (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95a88-133">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="95a88-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95a88-134">OUTPUTS</span></span>

### <span data-ttu-id="95a88-135">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="95a88-135">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="95a88-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95a88-136">NOTES</span></span>

## <span data-ttu-id="95a88-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95a88-137">RELATED LINKS</span></span>
