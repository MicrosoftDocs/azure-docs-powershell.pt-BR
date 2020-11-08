---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118476"
---
# <span data-ttu-id="5cbfc-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="5cbfc-101">Update-AzReservation</span></span>

## <span data-ttu-id="5cbfc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5cbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbfc-103">Atualizar um `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5cbfc-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="5cbfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cbfc-104">SYNTAX</span></span>

### <span data-ttu-id="5cbfc-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="5cbfc-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbfc-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="5cbfc-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cbfc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5cbfc-107">DESCRIPTION</span></span>
<span data-ttu-id="5cbfc-108">Atualiza os escopos aplicados do `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5cbfc-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="5cbfc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5cbfc-109">EXAMPLES</span></span>

### <span data-ttu-id="5cbfc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5cbfc-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="5cbfc-111">Atualiza o AppliedScopeType do especificado `Reservation` para Single e InstanceFlexibility para on.</span><span class="sxs-lookup"><span data-stu-id="5cbfc-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="5cbfc-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5cbfc-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="5cbfc-113">Atualiza o AppliedScopeType do especificado `Reservation` para compartilhado e o InstanceFlexibility para off.</span><span class="sxs-lookup"><span data-stu-id="5cbfc-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="5cbfc-114">OS</span><span class="sxs-lookup"><span data-stu-id="5cbfc-114">PARAMETERS</span></span>

### <span data-ttu-id="5cbfc-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="5cbfc-115">-AppliedScope</span></span>
<span data-ttu-id="5cbfc-116">SubscriptionId para `Reservation` ser aplicada</span><span class="sxs-lookup"><span data-stu-id="5cbfc-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="5cbfc-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="5cbfc-117">-AppliedScopeType</span></span>
<span data-ttu-id="5cbfc-118">Tipo do escopo aplicado</span><span class="sxs-lookup"><span data-stu-id="5cbfc-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="5cbfc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbfc-119">-DefaultProfile</span></span>
<span data-ttu-id="5cbfc-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbfc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cbfc-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="5cbfc-121">-InstanceFlexibility</span></span>
<span data-ttu-id="5cbfc-122">Se presente, atualiza o valor InstanceFlexibility do `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5cbfc-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="5cbfc-123">Se não for especificado, o valor existente permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="5cbfc-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="5cbfc-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cbfc-124">-Name</span></span>
<span data-ttu-id="5cbfc-125">Nome da reserva</span><span class="sxs-lookup"><span data-stu-id="5cbfc-125">Name of Reservation</span></span>

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

### <span data-ttu-id="5cbfc-126">-Reserva</span><span class="sxs-lookup"><span data-stu-id="5cbfc-126">-Reservation</span></span>
<span data-ttu-id="5cbfc-127">Parâmetro do objeto pipe para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="5cbfc-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="5cbfc-128">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="5cbfc-128">-ReservationId</span></span>
<span data-ttu-id="5cbfc-129">ID do `Reservation` a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="5cbfc-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="5cbfc-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5cbfc-130">-ReservationOrderId</span></span>
<span data-ttu-id="5cbfc-131">ID do `ReservationOrder` a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="5cbfc-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="5cbfc-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5cbfc-132">-Confirm</span></span>
<span data-ttu-id="5cbfc-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbfc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbfc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbfc-134">-WhatIf</span></span>
<span data-ttu-id="5cbfc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5cbfc-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cbfc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cbfc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbfc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbfc-137">CommonParameters</span></span>
<span data-ttu-id="5cbfc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbfc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbfc-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cbfc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbfc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5cbfc-140">INPUTS</span></span>

### <span data-ttu-id="5cbfc-141">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5cbfc-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5cbfc-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5cbfc-142">OUTPUTS</span></span>

### <span data-ttu-id="5cbfc-143">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5cbfc-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5cbfc-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5cbfc-144">NOTES</span></span>

## <span data-ttu-id="5cbfc-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cbfc-145">RELATED LINKS</span></span>
