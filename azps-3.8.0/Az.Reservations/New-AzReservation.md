---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942759"
---
# <span data-ttu-id="d2243-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="d2243-101">New-AzReservation</span></span>

## <span data-ttu-id="d2243-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2243-102">SYNOPSIS</span></span>
<span data-ttu-id="d2243-103">Comprar uma reserva</span><span class="sxs-lookup"><span data-stu-id="d2243-103">Purchase a reservation</span></span>

## <span data-ttu-id="d2243-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2243-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2243-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2243-105">DESCRIPTION</span></span>
<span data-ttu-id="d2243-106">Comprar uma instância de reserva e obter benefícios</span><span class="sxs-lookup"><span data-stu-id="d2243-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="d2243-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2243-107">EXAMPLES</span></span>

### <span data-ttu-id="d2243-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2243-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="d2243-109">Depois do cálculo do preço, o cliente poderia purcahse-lo pela RI fornecido por calculatePrice</span><span class="sxs-lookup"><span data-stu-id="d2243-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="d2243-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2243-110">PARAMETERS</span></span>

### <span data-ttu-id="d2243-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="d2243-111">-AppliedScope</span></span>
<span data-ttu-id="d2243-112">Assinatura à qual o benefício será aplicado.</span><span class="sxs-lookup"><span data-stu-id="d2243-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="d2243-113">Obrigatório se--aplicado-Scope-Type for único.</span><span class="sxs-lookup"><span data-stu-id="d2243-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="d2243-114">Não especifique se--aplicado-Scope-Type seja compartilhado.</span><span class="sxs-lookup"><span data-stu-id="d2243-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="d2243-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="d2243-115">-AppliedScopeType</span></span>
<span data-ttu-id="d2243-116">Tipo do escopo aplicado para atualizar a reserva com "único" ou "compartilhado"</span><span class="sxs-lookup"><span data-stu-id="d2243-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="d2243-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="d2243-117">-BillingPlan</span></span>
<span data-ttu-id="d2243-118">As opções de plano de cobrança disponíveis para esta SKU.</span><span class="sxs-lookup"><span data-stu-id="d2243-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="d2243-119">"Mensal" ou "dianteiro"</span><span class="sxs-lookup"><span data-stu-id="d2243-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="d2243-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="d2243-120">-BillingScopeId</span></span>
<span data-ttu-id="d2243-121">Assinatura que será cobrada pela reserva de compras.</span><span class="sxs-lookup"><span data-stu-id="d2243-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="d2243-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2243-122">-DefaultProfile</span></span>
<span data-ttu-id="d2243-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2243-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2243-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d2243-124">-DisplayName</span></span>
<span data-ttu-id="d2243-125">Nome amigável para o usuário identificar facilmente a reserva.</span><span class="sxs-lookup"><span data-stu-id="d2243-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="d2243-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="d2243-126">-InstanceFlexibility</span></span>
<span data-ttu-id="d2243-127">{{Fill InstanceFlexibility descrição}}</span><span class="sxs-lookup"><span data-stu-id="d2243-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="d2243-128">-Local</span><span class="sxs-lookup"><span data-stu-id="d2243-128">-Location</span></span>
<span data-ttu-id="d2243-129">Local em que o SKU está disponível.</span><span class="sxs-lookup"><span data-stu-id="d2243-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="d2243-130">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="d2243-130">-Quantity</span></span>
<span data-ttu-id="d2243-131">Quantidade de produto para calcular o preço ou a compra.</span><span class="sxs-lookup"><span data-stu-id="d2243-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="d2243-132">-Renove</span><span class="sxs-lookup"><span data-stu-id="d2243-132">-Renew</span></span>
<span data-ttu-id="d2243-133">Defina como verdadeiro para comprar automaticamente uma nova reserva na hora da data de expiração.</span><span class="sxs-lookup"><span data-stu-id="d2243-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="d2243-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d2243-134">-ReservationOrderId</span></span>
<span data-ttu-id="d2243-135">ID da ordem de reserva a comprar, gerar por reserva de reservas do AZ-ordem calculada.</span><span class="sxs-lookup"><span data-stu-id="d2243-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="d2243-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="d2243-136">-ReservedResourceType</span></span>
<span data-ttu-id="d2243-137">Tipo do recurso para o qual as SKUs devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="d2243-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="d2243-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="d2243-138">-Sku</span></span>
<span data-ttu-id="d2243-139">Nome do SKU</span><span class="sxs-lookup"><span data-stu-id="d2243-139">Sku name</span></span>

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

### <span data-ttu-id="d2243-140">-Prazo</span><span class="sxs-lookup"><span data-stu-id="d2243-140">-Term</span></span>
<span data-ttu-id="d2243-141">Termos de reserva disponíveis para este recurso.</span><span class="sxs-lookup"><span data-stu-id="d2243-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="d2243-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2243-142">-Confirm</span></span>
<span data-ttu-id="d2243-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2243-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2243-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2243-144">-WhatIf</span></span>
<span data-ttu-id="d2243-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2243-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2243-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2243-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2243-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2243-147">CommonParameters</span></span>
<span data-ttu-id="d2243-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2243-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2243-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2243-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2243-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2243-150">INPUTS</span></span>

### <span data-ttu-id="d2243-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d2243-151">None</span></span>

## <span data-ttu-id="d2243-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2243-152">OUTPUTS</span></span>

### <span data-ttu-id="d2243-153">Microsoft. Azure. Management. reservas. Models. ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="d2243-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="d2243-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2243-154">NOTES</span></span>

## <span data-ttu-id="d2243-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2243-155">RELATED LINKS</span></span>
