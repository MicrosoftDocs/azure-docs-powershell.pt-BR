---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 37be462c2af2c33987e6acd0118c3169b1e062d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891677"
---
# <span data-ttu-id="8f96b-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="8f96b-101">New-AzReservation</span></span>

## <span data-ttu-id="8f96b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f96b-102">SYNOPSIS</span></span>
<span data-ttu-id="8f96b-103">Comprar uma reserva</span><span class="sxs-lookup"><span data-stu-id="8f96b-103">Purchase a reservation</span></span>

## <span data-ttu-id="8f96b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8f96b-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f96b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8f96b-105">DESCRIPTION</span></span>
<span data-ttu-id="8f96b-106">Comprar uma instância de reserva e obter benefícios</span><span class="sxs-lookup"><span data-stu-id="8f96b-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="8f96b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f96b-107">EXAMPLES</span></span>

### <span data-ttu-id="8f96b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f96b-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="8f96b-109">Depois de calcular o preço, o cliente pode purcahse que a RI fornece por calculatePrice</span><span class="sxs-lookup"><span data-stu-id="8f96b-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="8f96b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8f96b-110">PARAMETERS</span></span>

### <span data-ttu-id="8f96b-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="8f96b-111">-AppliedScope</span></span>
<span data-ttu-id="8f96b-112">Assinatura que o benefício será aplicado.</span><span class="sxs-lookup"><span data-stu-id="8f96b-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="8f96b-113">Obrigatório se --applied-scope-type for Single.</span><span class="sxs-lookup"><span data-stu-id="8f96b-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="8f96b-114">Não especifique se --applied-scope-type é Shared.</span><span class="sxs-lookup"><span data-stu-id="8f96b-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="8f96b-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="8f96b-115">-AppliedScopeType</span></span>
<span data-ttu-id="8f96b-116">Tipo do Escopo Aplicado para atualizar a reserva com "Single" ou "Shared"</span><span class="sxs-lookup"><span data-stu-id="8f96b-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="8f96b-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="8f96b-117">-BillingPlan</span></span>
<span data-ttu-id="8f96b-118">As opções de plano de cobrança disponíveis para este SKU.</span><span class="sxs-lookup"><span data-stu-id="8f96b-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="8f96b-119">"Mensal" ou "Upfront"</span><span class="sxs-lookup"><span data-stu-id="8f96b-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="8f96b-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="8f96b-120">-BillingScopeId</span></span>
<span data-ttu-id="8f96b-121">Assinatura que será cobrada pela compra de Reserva.</span><span class="sxs-lookup"><span data-stu-id="8f96b-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="8f96b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f96b-122">-DefaultProfile</span></span>
<span data-ttu-id="8f96b-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f96b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f96b-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f96b-124">-DisplayName</span></span>
<span data-ttu-id="8f96b-125">Nome amigável para o usuário identificar facilmente a reserva.</span><span class="sxs-lookup"><span data-stu-id="8f96b-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="8f96b-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="8f96b-126">-InstanceFlexibility</span></span>
<span data-ttu-id="8f96b-127">{{ Fill InstanceFlexibility Description }}</span><span class="sxs-lookup"><span data-stu-id="8f96b-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="8f96b-128">-Location</span><span class="sxs-lookup"><span data-stu-id="8f96b-128">-Location</span></span>
<span data-ttu-id="8f96b-129">Local em que o SKU está disponível.</span><span class="sxs-lookup"><span data-stu-id="8f96b-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="8f96b-130">-Quantity</span><span class="sxs-lookup"><span data-stu-id="8f96b-130">-Quantity</span></span>
<span data-ttu-id="8f96b-131">Quantidade de produto para calcular preço ou compra.</span><span class="sxs-lookup"><span data-stu-id="8f96b-131">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f96b-132">-Renew</span><span class="sxs-lookup"><span data-stu-id="8f96b-132">-Renew</span></span>
<span data-ttu-id="8f96b-133">Definir isso como true comprará automaticamente uma nova reserva na data de expiração.</span><span class="sxs-lookup"><span data-stu-id="8f96b-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f96b-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8f96b-134">-ReservationOrderId</span></span>
<span data-ttu-id="8f96b-135">ID da ordem de reserva para compra, gerado pelo cálculo de ordem de reserva de reservas do az.</span><span class="sxs-lookup"><span data-stu-id="8f96b-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="8f96b-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="8f96b-136">-ReservedResourceType</span></span>
<span data-ttu-id="8f96b-137">Tipo do recurso para o qual os skus devem ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="8f96b-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="8f96b-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="8f96b-138">-Sku</span></span>
<span data-ttu-id="8f96b-139">Nome Sku</span><span class="sxs-lookup"><span data-stu-id="8f96b-139">Sku name</span></span>

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

### <span data-ttu-id="8f96b-140">-Term</span><span class="sxs-lookup"><span data-stu-id="8f96b-140">-Term</span></span>
<span data-ttu-id="8f96b-141">Termos de reserva disponíveis para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="8f96b-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="8f96b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f96b-142">-Confirm</span></span>
<span data-ttu-id="8f96b-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f96b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f96b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f96b-144">-WhatIf</span></span>
<span data-ttu-id="8f96b-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f96b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f96b-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f96b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f96b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f96b-147">CommonParameters</span></span>
<span data-ttu-id="8f96b-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f96b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f96b-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f96b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f96b-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f96b-150">INPUTS</span></span>

### <span data-ttu-id="8f96b-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8f96b-151">None</span></span>

## <span data-ttu-id="8f96b-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8f96b-152">OUTPUTS</span></span>

### <span data-ttu-id="8f96b-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="8f96b-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="8f96b-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="8f96b-154">NOTES</span></span>

## <span data-ttu-id="8f96b-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f96b-155">RELATED LINKS</span></span>
