---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 073a059063198e91a1bbcc67814c01c1b786e7c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264066"
---
# <span data-ttu-id="796c6-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="796c6-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="796c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="796c6-102">SYNOPSIS</span></span>
<span data-ttu-id="796c6-103">Obtenha uma cotação para a reserva.</span><span class="sxs-lookup"><span data-stu-id="796c6-103">Get a quote for the reservation.</span></span> <span data-ttu-id="796c6-104">Isso é passado para `New-AzReservation` a compra.</span><span class="sxs-lookup"><span data-stu-id="796c6-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="796c6-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="796c6-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="796c6-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="796c6-106">DESCRIPTION</span></span>
<span data-ttu-id="796c6-107">Calcular o preço para a inserção de uma ordem de reserva.</span><span class="sxs-lookup"><span data-stu-id="796c6-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="796c6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="796c6-108">EXAMPLES</span></span>

### <span data-ttu-id="796c6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="796c6-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="796c6-110">Depois de obter o catálogo, o cliente pode obter o produto diferente com base no local.</span><span class="sxs-lookup"><span data-stu-id="796c6-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="796c6-111">Ao usar essas informações, verifique o preço corretamente</span><span class="sxs-lookup"><span data-stu-id="796c6-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="796c6-112">OS</span><span class="sxs-lookup"><span data-stu-id="796c6-112">PARAMETERS</span></span>

### <span data-ttu-id="796c6-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="796c6-113">-AppliedScope</span></span>
<span data-ttu-id="796c6-114">Assinatura à qual o benefício será aplicado.</span><span class="sxs-lookup"><span data-stu-id="796c6-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="796c6-115">Obrigatório se--aplicado-Scope-Type for único.</span><span class="sxs-lookup"><span data-stu-id="796c6-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="796c6-116">Não especifique se--aplicado-Scope-Type seja compartilhado.</span><span class="sxs-lookup"><span data-stu-id="796c6-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="796c6-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="796c6-117">-AppliedScopeType</span></span>
<span data-ttu-id="796c6-118">Tipo do escopo aplicado para atualizar a reserva com "único" ou "compartilhado"</span><span class="sxs-lookup"><span data-stu-id="796c6-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="796c6-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="796c6-119">-BillingPlan</span></span>
<span data-ttu-id="796c6-120">As opções de plano de cobrança disponíveis para esta SKU.</span><span class="sxs-lookup"><span data-stu-id="796c6-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="796c6-121">"Mensal" ou "dianteiro"</span><span class="sxs-lookup"><span data-stu-id="796c6-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="796c6-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="796c6-122">-BillingScopeId</span></span>
<span data-ttu-id="796c6-123">Assinatura que será cobrada pela reserva de compras.</span><span class="sxs-lookup"><span data-stu-id="796c6-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="796c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796c6-124">-DefaultProfile</span></span>
<span data-ttu-id="796c6-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="796c6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="796c6-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="796c6-126">-DisplayName</span></span>
<span data-ttu-id="796c6-127">Nome amigável para o usuário identificar facilmente a reserva.</span><span class="sxs-lookup"><span data-stu-id="796c6-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="796c6-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="796c6-128">-InstanceFlexibility</span></span>
<span data-ttu-id="796c6-129">Tipo de flexibilidade de instância para atualizar a reserva.</span><span class="sxs-lookup"><span data-stu-id="796c6-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="796c6-130">-Local</span><span class="sxs-lookup"><span data-stu-id="796c6-130">-Location</span></span>
<span data-ttu-id="796c6-131">Local em que o SKU está disponível.</span><span class="sxs-lookup"><span data-stu-id="796c6-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="796c6-132">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="796c6-132">-Quantity</span></span>
<span data-ttu-id="796c6-133">Quantidade de produto para calcular o preço ou a compra.</span><span class="sxs-lookup"><span data-stu-id="796c6-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="796c6-134">-Renove</span><span class="sxs-lookup"><span data-stu-id="796c6-134">-Renew</span></span>
<span data-ttu-id="796c6-135">Defina como verdadeiro para comprar automaticamente uma nova reserva na hora da data de expiração.</span><span class="sxs-lookup"><span data-stu-id="796c6-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="796c6-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="796c6-136">-ReservedResourceType</span></span>
<span data-ttu-id="796c6-137">Tipo do recurso para o qual as SKUs devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="796c6-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="796c6-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="796c6-138">-Sku</span></span>
<span data-ttu-id="796c6-139">Nome do SKU, obter a lista de SKU usando o comando AZ reservas programa de catálogo</span><span class="sxs-lookup"><span data-stu-id="796c6-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="796c6-140">-Prazo</span><span class="sxs-lookup"><span data-stu-id="796c6-140">-Term</span></span>
<span data-ttu-id="796c6-141">Termos de reserva disponíveis para este recurso.</span><span class="sxs-lookup"><span data-stu-id="796c6-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="796c6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796c6-142">CommonParameters</span></span>
<span data-ttu-id="796c6-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="796c6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796c6-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="796c6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796c6-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="796c6-145">INPUTS</span></span>

### <span data-ttu-id="796c6-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="796c6-146">None</span></span>

## <span data-ttu-id="796c6-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="796c6-147">OUTPUTS</span></span>

### <span data-ttu-id="796c6-148">Microsoft. Azure. Management. reservas. Models. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="796c6-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="796c6-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="796c6-149">NOTES</span></span>

## <span data-ttu-id="796c6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="796c6-150">RELATED LINKS</span></span>
