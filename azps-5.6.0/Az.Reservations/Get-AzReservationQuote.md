---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 3a06de95cedd0ea38fa38b2fb8784e553ae6f4d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891684"
---
# <span data-ttu-id="03281-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="03281-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="03281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03281-102">SYNOPSIS</span></span>
<span data-ttu-id="03281-103">Obter uma aspas para a reserva.</span><span class="sxs-lookup"><span data-stu-id="03281-103">Get a quote for the reservation.</span></span> <span data-ttu-id="03281-104">Isso é passado para `New-AzReservation` a compra.</span><span class="sxs-lookup"><span data-stu-id="03281-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="03281-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="03281-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03281-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="03281-106">DESCRIPTION</span></span>
<span data-ttu-id="03281-107">Calcule o preço para colocar uma ordem de reserva.</span><span class="sxs-lookup"><span data-stu-id="03281-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="03281-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03281-108">EXAMPLES</span></span>

### <span data-ttu-id="03281-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03281-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="03281-110">Depois de obter o catálogo, o cliente pode obter o produto diferente com base no local.</span><span class="sxs-lookup"><span data-stu-id="03281-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="03281-111">Ao usar essas informações, verifique o preço corretamente</span><span class="sxs-lookup"><span data-stu-id="03281-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="03281-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="03281-112">PARAMETERS</span></span>

### <span data-ttu-id="03281-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="03281-113">-AppliedScope</span></span>
<span data-ttu-id="03281-114">Assinatura que o benefício será aplicado.</span><span class="sxs-lookup"><span data-stu-id="03281-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="03281-115">Obrigatório se --applied-scope-type for Single.</span><span class="sxs-lookup"><span data-stu-id="03281-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="03281-116">Não especifique se --applied-scope-type é Shared.</span><span class="sxs-lookup"><span data-stu-id="03281-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="03281-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="03281-117">-AppliedScopeType</span></span>
<span data-ttu-id="03281-118">Tipo do Escopo Aplicado para atualizar a reserva com "Single" ou "Shared"</span><span class="sxs-lookup"><span data-stu-id="03281-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="03281-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="03281-119">-BillingPlan</span></span>
<span data-ttu-id="03281-120">As opções de plano de cobrança disponíveis para este SKU.</span><span class="sxs-lookup"><span data-stu-id="03281-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="03281-121">"Mensal" ou "Upfront"</span><span class="sxs-lookup"><span data-stu-id="03281-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="03281-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="03281-122">-BillingScopeId</span></span>
<span data-ttu-id="03281-123">Assinatura que será cobrada pela compra de Reserva.</span><span class="sxs-lookup"><span data-stu-id="03281-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="03281-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03281-124">-DefaultProfile</span></span>
<span data-ttu-id="03281-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03281-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03281-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="03281-126">-DisplayName</span></span>
<span data-ttu-id="03281-127">Nome amigável para o usuário identificar facilmente a reserva.</span><span class="sxs-lookup"><span data-stu-id="03281-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="03281-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="03281-128">-InstanceFlexibility</span></span>
<span data-ttu-id="03281-129">Tipo de Flexibilidade de Instância para atualizar a reserva com.</span><span class="sxs-lookup"><span data-stu-id="03281-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="03281-130">-Location</span><span class="sxs-lookup"><span data-stu-id="03281-130">-Location</span></span>
<span data-ttu-id="03281-131">Local em que o SKU está disponível.</span><span class="sxs-lookup"><span data-stu-id="03281-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="03281-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="03281-132">-Quantity</span></span>
<span data-ttu-id="03281-133">Quantidade de produto para calcular preço ou compra.</span><span class="sxs-lookup"><span data-stu-id="03281-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="03281-134">-Renew</span><span class="sxs-lookup"><span data-stu-id="03281-134">-Renew</span></span>
<span data-ttu-id="03281-135">Definir isso como true comprará automaticamente uma nova reserva na data de expiração.</span><span class="sxs-lookup"><span data-stu-id="03281-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="03281-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="03281-136">-ReservedResourceType</span></span>
<span data-ttu-id="03281-137">Tipo do recurso para o qual os skus devem ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="03281-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="03281-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="03281-138">-Sku</span></span>
<span data-ttu-id="03281-139">Sku name, get the sku list by using command az reservations catalog show</span><span class="sxs-lookup"><span data-stu-id="03281-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="03281-140">-Term</span><span class="sxs-lookup"><span data-stu-id="03281-140">-Term</span></span>
<span data-ttu-id="03281-141">Termos de reserva disponíveis para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="03281-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="03281-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03281-142">CommonParameters</span></span>
<span data-ttu-id="03281-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03281-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03281-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03281-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03281-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03281-145">INPUTS</span></span>

### <span data-ttu-id="03281-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="03281-146">None</span></span>

## <span data-ttu-id="03281-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="03281-147">OUTPUTS</span></span>

### <span data-ttu-id="03281-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="03281-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="03281-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="03281-149">NOTES</span></span>

## <span data-ttu-id="03281-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03281-150">RELATED LINKS</span></span>
