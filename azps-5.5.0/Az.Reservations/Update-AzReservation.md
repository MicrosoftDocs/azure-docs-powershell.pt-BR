---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110823"
---
# <span data-ttu-id="e18a3-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="e18a3-101">Update-AzReservation</span></span>

## <span data-ttu-id="e18a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e18a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e18a3-103">Atualizar um `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e18a3-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="e18a3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e18a3-104">SYNTAX</span></span>

### <span data-ttu-id="e18a3-105">CommandLine (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e18a3-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e18a3-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e18a3-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e18a3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e18a3-107">DESCRIPTION</span></span>
<span data-ttu-id="e18a3-108">Atualiza os escopos aplicados do `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e18a3-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="e18a3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e18a3-109">EXAMPLES</span></span>

### <span data-ttu-id="e18a3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e18a3-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="e18a3-111">Atualiza o AppliedScopeType do especificado como Único e `Reservation` InstanceFlexibility para Ligado.</span><span class="sxs-lookup"><span data-stu-id="e18a3-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="e18a3-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e18a3-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="e18a3-113">Atualiza o AppliedScopeType do especificado como Compartilhado e `Reservation` InstanceFlexibility para Desligado.</span><span class="sxs-lookup"><span data-stu-id="e18a3-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="e18a3-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e18a3-114">PARAMETERS</span></span>

### <span data-ttu-id="e18a3-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="e18a3-115">-AppliedScope</span></span>
<span data-ttu-id="e18a3-116">SubscriptionId para que `Reservation` isso seja aplicado</span><span class="sxs-lookup"><span data-stu-id="e18a3-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="e18a3-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="e18a3-117">-AppliedScopeType</span></span>
<span data-ttu-id="e18a3-118">Tipo do Escopo Aplicado</span><span class="sxs-lookup"><span data-stu-id="e18a3-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="e18a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18a3-119">-DefaultProfile</span></span>
<span data-ttu-id="e18a3-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e18a3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e18a3-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="e18a3-121">-InstanceFlexibility</span></span>
<span data-ttu-id="e18a3-122">Se estiver presente, atualizará o valor InstanceFlexibility do `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e18a3-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="e18a3-123">Se não especificado, o valor existente permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="e18a3-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="e18a3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e18a3-124">-Name</span></span>
<span data-ttu-id="e18a3-125">Nome da Reserva</span><span class="sxs-lookup"><span data-stu-id="e18a3-125">Name of Reservation</span></span>

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

### <span data-ttu-id="e18a3-126">-Reserva</span><span class="sxs-lookup"><span data-stu-id="e18a3-126">-Reservation</span></span>
<span data-ttu-id="e18a3-127">Parâmetro de objeto de cano para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e18a3-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="e18a3-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="e18a3-128">-ReservationId</span></span>
<span data-ttu-id="e18a3-129">ID da `Reservation` atualização</span><span class="sxs-lookup"><span data-stu-id="e18a3-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="e18a3-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e18a3-130">-ReservationOrderId</span></span>
<span data-ttu-id="e18a3-131">ID da `ReservationOrder` atualização</span><span class="sxs-lookup"><span data-stu-id="e18a3-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="e18a3-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e18a3-132">-Confirm</span></span>
<span data-ttu-id="e18a3-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e18a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e18a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e18a3-134">-WhatIf</span></span>
<span data-ttu-id="e18a3-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e18a3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e18a3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e18a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e18a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18a3-137">CommonParameters</span></span>
<span data-ttu-id="e18a3-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e18a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18a3-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e18a3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18a3-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="e18a3-140">INPUTS</span></span>

### <span data-ttu-id="e18a3-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="e18a3-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e18a3-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="e18a3-142">OUTPUTS</span></span>

### <span data-ttu-id="e18a3-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="e18a3-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e18a3-144">Notas</span><span class="sxs-lookup"><span data-stu-id="e18a3-144">NOTES</span></span>

## <span data-ttu-id="e18a3-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e18a3-145">RELATED LINKS</span></span>
