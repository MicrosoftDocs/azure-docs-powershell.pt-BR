---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115914"
---
# <span data-ttu-id="7170a-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="7170a-101">New-AzReservation</span></span>

## <span data-ttu-id="7170a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7170a-102">SYNOPSIS</span></span>
<span data-ttu-id="7170a-103">Comprar uma reserva</span><span class="sxs-lookup"><span data-stu-id="7170a-103">Purchase a reservation</span></span>

## <span data-ttu-id="7170a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7170a-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7170a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7170a-105">DESCRIPTION</span></span>
<span data-ttu-id="7170a-106">Comprar uma instância de reserva e obter benefícios</span><span class="sxs-lookup"><span data-stu-id="7170a-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="7170a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7170a-107">EXAMPLES</span></span>

### <span data-ttu-id="7170a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7170a-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="7170a-109">Depois do cálculo do preço, o cliente poderia purcahse-lo pela RI fornecido por calculatePrice</span><span class="sxs-lookup"><span data-stu-id="7170a-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="7170a-110">OS</span><span class="sxs-lookup"><span data-stu-id="7170a-110">PARAMETERS</span></span>

### <span data-ttu-id="7170a-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="7170a-111">-AppliedScope</span></span>
<span data-ttu-id="7170a-112">Assinatura à qual o benefício será aplicado.</span><span class="sxs-lookup"><span data-stu-id="7170a-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="7170a-113">Obrigatório se--aplicado-Scope-Type for único.</span><span class="sxs-lookup"><span data-stu-id="7170a-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="7170a-114">Não especifique se--aplicado-Scope-Type seja compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7170a-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="7170a-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="7170a-115">-AppliedScopeType</span></span>
<span data-ttu-id="7170a-116">Tipo do escopo aplicado para atualizar a reserva com "único" ou "compartilhado"</span><span class="sxs-lookup"><span data-stu-id="7170a-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="7170a-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="7170a-117">-BillingPlan</span></span>
<span data-ttu-id="7170a-118">As opções de plano de cobrança disponíveis para esta SKU.</span><span class="sxs-lookup"><span data-stu-id="7170a-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="7170a-119">"Mensal" ou "dianteiro"</span><span class="sxs-lookup"><span data-stu-id="7170a-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="7170a-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="7170a-120">-BillingScopeId</span></span>
<span data-ttu-id="7170a-121">Assinatura que será cobrada pela reserva de compras.</span><span class="sxs-lookup"><span data-stu-id="7170a-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="7170a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7170a-122">-DefaultProfile</span></span>
<span data-ttu-id="7170a-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7170a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7170a-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7170a-124">-DisplayName</span></span>
<span data-ttu-id="7170a-125">Nome amigável para o usuário identificar facilmente a reserva.</span><span class="sxs-lookup"><span data-stu-id="7170a-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="7170a-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="7170a-126">-InstanceFlexibility</span></span>
<span data-ttu-id="7170a-127">{{Fill InstanceFlexibility descrição}}</span><span class="sxs-lookup"><span data-stu-id="7170a-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="7170a-128">-Local</span><span class="sxs-lookup"><span data-stu-id="7170a-128">-Location</span></span>
<span data-ttu-id="7170a-129">Local em que o SKU está disponível.</span><span class="sxs-lookup"><span data-stu-id="7170a-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="7170a-130">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="7170a-130">-Quantity</span></span>
<span data-ttu-id="7170a-131">Quantidade de produto para calcular o preço ou a compra.</span><span class="sxs-lookup"><span data-stu-id="7170a-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="7170a-132">-Renove</span><span class="sxs-lookup"><span data-stu-id="7170a-132">-Renew</span></span>
<span data-ttu-id="7170a-133">Defina como verdadeiro para comprar automaticamente uma nova reserva na hora da data de expiração.</span><span class="sxs-lookup"><span data-stu-id="7170a-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="7170a-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="7170a-134">-ReservationOrderId</span></span>
<span data-ttu-id="7170a-135">ID da ordem de reserva a comprar, gerar por reserva de reservas do AZ-ordem calculada.</span><span class="sxs-lookup"><span data-stu-id="7170a-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="7170a-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="7170a-136">-ReservedResourceType</span></span>
<span data-ttu-id="7170a-137">Tipo do recurso para o qual as SKUs devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="7170a-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="7170a-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="7170a-138">-Sku</span></span>
<span data-ttu-id="7170a-139">Nome do SKU</span><span class="sxs-lookup"><span data-stu-id="7170a-139">Sku name</span></span>

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

### <span data-ttu-id="7170a-140">-Prazo</span><span class="sxs-lookup"><span data-stu-id="7170a-140">-Term</span></span>
<span data-ttu-id="7170a-141">Termos de reserva disponíveis para este recurso.</span><span class="sxs-lookup"><span data-stu-id="7170a-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="7170a-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7170a-142">-Confirm</span></span>
<span data-ttu-id="7170a-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7170a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7170a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7170a-144">-WhatIf</span></span>
<span data-ttu-id="7170a-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7170a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7170a-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7170a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7170a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7170a-147">CommonParameters</span></span>
<span data-ttu-id="7170a-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7170a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7170a-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7170a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7170a-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7170a-150">INPUTS</span></span>

### <span data-ttu-id="7170a-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7170a-151">None</span></span>

## <span data-ttu-id="7170a-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7170a-152">OUTPUTS</span></span>

### <span data-ttu-id="7170a-153">Microsoft. Azure. Management. reservas. Models. ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="7170a-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="7170a-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7170a-154">NOTES</span></span>

## <span data-ttu-id="7170a-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7170a-155">RELATED LINKS</span></span>
