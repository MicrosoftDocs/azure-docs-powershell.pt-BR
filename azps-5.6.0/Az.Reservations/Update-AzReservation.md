---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: b93dd1462bb019b12fe761e0bdd6cc4172c01b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891674"
---
# <span data-ttu-id="b347a-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="b347a-101">Update-AzReservation</span></span>

## <span data-ttu-id="b347a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b347a-102">SYNOPSIS</span></span>
<span data-ttu-id="b347a-103">Atualizar um `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="b347a-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="b347a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b347a-104">SYNTAX</span></span>

### <span data-ttu-id="b347a-105">CommandLine (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b347a-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b347a-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="b347a-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b347a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b347a-107">DESCRIPTION</span></span>
<span data-ttu-id="b347a-108">Atualiza os escopos aplicados do `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="b347a-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="b347a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b347a-109">EXAMPLES</span></span>

### <span data-ttu-id="b347a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b347a-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="b347a-111">Atualiza o AppliedScopeType do especificado `Reservation` para Single e InstanceFlexibility como On.</span><span class="sxs-lookup"><span data-stu-id="b347a-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="b347a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b347a-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="b347a-113">Atualiza o AppliedScopeType do especificado `Reservation` para Shared e InstanceFlexibility como Desligado.</span><span class="sxs-lookup"><span data-stu-id="b347a-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="b347a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b347a-114">PARAMETERS</span></span>

### <span data-ttu-id="b347a-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="b347a-115">-AppliedScope</span></span>
<span data-ttu-id="b347a-116">SubscriptionId para que `Reservation` isso seja aplicado</span><span class="sxs-lookup"><span data-stu-id="b347a-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="b347a-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="b347a-117">-AppliedScopeType</span></span>
<span data-ttu-id="b347a-118">Tipo do Escopo Aplicado</span><span class="sxs-lookup"><span data-stu-id="b347a-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="b347a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b347a-119">-DefaultProfile</span></span>
<span data-ttu-id="b347a-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b347a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b347a-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="b347a-121">-InstanceFlexibility</span></span>
<span data-ttu-id="b347a-122">Se presente, atualiza o valor InstanceFlexibility do `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="b347a-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="b347a-123">Se não for especificado, o valor existente permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="b347a-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="b347a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b347a-124">-Name</span></span>
<span data-ttu-id="b347a-125">Nome da Reserva</span><span class="sxs-lookup"><span data-stu-id="b347a-125">Name of Reservation</span></span>

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

### <span data-ttu-id="b347a-126">-Reservation</span><span class="sxs-lookup"><span data-stu-id="b347a-126">-Reservation</span></span>
<span data-ttu-id="b347a-127">Parâmetro do objeto Pipe para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="b347a-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="b347a-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="b347a-128">-ReservationId</span></span>
<span data-ttu-id="b347a-129">ID da `Reservation` atualização</span><span class="sxs-lookup"><span data-stu-id="b347a-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="b347a-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="b347a-130">-ReservationOrderId</span></span>
<span data-ttu-id="b347a-131">ID da `ReservationOrder` atualização</span><span class="sxs-lookup"><span data-stu-id="b347a-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="b347a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b347a-132">-Confirm</span></span>
<span data-ttu-id="b347a-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b347a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b347a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b347a-134">-WhatIf</span></span>
<span data-ttu-id="b347a-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b347a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b347a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b347a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b347a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b347a-137">CommonParameters</span></span>
<span data-ttu-id="b347a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b347a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b347a-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b347a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b347a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b347a-140">INPUTS</span></span>

### <span data-ttu-id="b347a-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="b347a-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="b347a-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b347a-142">OUTPUTS</span></span>

### <span data-ttu-id="b347a-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="b347a-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="b347a-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="b347a-144">NOTES</span></span>

## <span data-ttu-id="b347a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b347a-145">RELATED LINKS</span></span>
