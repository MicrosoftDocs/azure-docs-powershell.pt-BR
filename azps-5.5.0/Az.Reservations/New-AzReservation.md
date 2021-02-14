---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110824"
---
# <span data-ttu-id="75b45-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="75b45-101">New-AzReservation</span></span>

## <span data-ttu-id="75b45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75b45-102">SYNOPSIS</span></span>
<span data-ttu-id="75b45-103">Comprar uma reserva</span><span class="sxs-lookup"><span data-stu-id="75b45-103">Purchase a reservation</span></span>

## <span data-ttu-id="75b45-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75b45-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75b45-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="75b45-105">DESCRIPTION</span></span>
<span data-ttu-id="75b45-106">Comprar uma instância de reserva e obter benefícios</span><span class="sxs-lookup"><span data-stu-id="75b45-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="75b45-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75b45-107">EXAMPLES</span></span>

### <span data-ttu-id="75b45-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75b45-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="75b45-109">Depois de calcular o preço, o cliente pode calcular que o RI fornece pelo calculatePrice</span><span class="sxs-lookup"><span data-stu-id="75b45-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="75b45-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75b45-110">PARAMETERS</span></span>

### <span data-ttu-id="75b45-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="75b45-111">-AppliedScope</span></span>
<span data-ttu-id="75b45-112">Assinatura de que o benefício será aplicado.</span><span class="sxs-lookup"><span data-stu-id="75b45-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="75b45-113">Obrigatório se --tipo de escopo aplicado for Único.</span><span class="sxs-lookup"><span data-stu-id="75b45-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="75b45-114">Não especifique se --tipo de escopo aplicado é Compartilhado.</span><span class="sxs-lookup"><span data-stu-id="75b45-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="75b45-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="75b45-115">-AppliedScopeType</span></span>
<span data-ttu-id="75b45-116">Tipo do Escopo Aplicado para atualizar a reserva com "Único" ou "Compartilhado"</span><span class="sxs-lookup"><span data-stu-id="75b45-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="75b45-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="75b45-117">-BillingPlan</span></span>
<span data-ttu-id="75b45-118">As opções de plano de cobrança disponíveis para esta SKU.</span><span class="sxs-lookup"><span data-stu-id="75b45-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="75b45-119">"Mensal" ou "Upfront"</span><span class="sxs-lookup"><span data-stu-id="75b45-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="75b45-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="75b45-120">-BillingScopeId</span></span>
<span data-ttu-id="75b45-121">Assinatura que será cobrada pela compra de Reserva.</span><span class="sxs-lookup"><span data-stu-id="75b45-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="75b45-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b45-122">-DefaultProfile</span></span>
<span data-ttu-id="75b45-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75b45-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b45-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75b45-124">-DisplayName</span></span>
<span data-ttu-id="75b45-125">Nome amigável para o usuário identificar facilmente a reserva.</span><span class="sxs-lookup"><span data-stu-id="75b45-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="75b45-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="75b45-126">-InstanceFlexibility</span></span>
<span data-ttu-id="75b45-127">{{ Fill InstanceFlexibility Description }}</span><span class="sxs-lookup"><span data-stu-id="75b45-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="75b45-128">-Local</span><span class="sxs-lookup"><span data-stu-id="75b45-128">-Location</span></span>
<span data-ttu-id="75b45-129">Local em que a SKU está disponível.</span><span class="sxs-lookup"><span data-stu-id="75b45-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="75b45-130">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="75b45-130">-Quantity</span></span>
<span data-ttu-id="75b45-131">Quantidade de produto para calcular preço ou compra.</span><span class="sxs-lookup"><span data-stu-id="75b45-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="75b45-132">-Renovar</span><span class="sxs-lookup"><span data-stu-id="75b45-132">-Renew</span></span>
<span data-ttu-id="75b45-133">Definir isso como verdadeiro comprará automaticamente uma nova reserva na data de vencimento.</span><span class="sxs-lookup"><span data-stu-id="75b45-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="75b45-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="75b45-134">-ReservationOrderId</span></span>
<span data-ttu-id="75b45-135">ID do pedido de reserva para comprar, gerar pelo cálculo de ordem de reserva de reservas do Az.</span><span class="sxs-lookup"><span data-stu-id="75b45-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="75b45-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="75b45-136">-ReservedResourceType</span></span>
<span data-ttu-id="75b45-137">Tipo do recurso para o qual as sKIs devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="75b45-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="75b45-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="75b45-138">-Sku</span></span>
<span data-ttu-id="75b45-139">Nome da SKU</span><span class="sxs-lookup"><span data-stu-id="75b45-139">Sku name</span></span>

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

### <span data-ttu-id="75b45-140">-Termo</span><span class="sxs-lookup"><span data-stu-id="75b45-140">-Term</span></span>
<span data-ttu-id="75b45-141">Termos de reserva disponíveis para este recurso.</span><span class="sxs-lookup"><span data-stu-id="75b45-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="75b45-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="75b45-142">-Confirm</span></span>
<span data-ttu-id="75b45-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75b45-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b45-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b45-144">-WhatIf</span></span>
<span data-ttu-id="75b45-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="75b45-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75b45-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75b45-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b45-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b45-147">CommonParameters</span></span>
<span data-ttu-id="75b45-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b45-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b45-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75b45-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b45-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="75b45-150">INPUTS</span></span>

### <span data-ttu-id="75b45-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75b45-151">None</span></span>

## <span data-ttu-id="75b45-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="75b45-152">OUTPUTS</span></span>

### <span data-ttu-id="75b45-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="75b45-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="75b45-154">Notas</span><span class="sxs-lookup"><span data-stu-id="75b45-154">NOTES</span></span>

## <span data-ttu-id="75b45-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75b45-155">RELATED LINKS</span></span>
