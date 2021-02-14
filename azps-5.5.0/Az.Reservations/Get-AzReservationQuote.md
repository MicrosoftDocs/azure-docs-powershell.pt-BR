---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 073a059063198e91a1bbcc67814c01c1b786e7c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110829"
---
# <span data-ttu-id="7606c-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="7606c-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="7606c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7606c-102">SYNOPSIS</span></span>
<span data-ttu-id="7606c-103">Obter uma cotação para a reserva.</span><span class="sxs-lookup"><span data-stu-id="7606c-103">Get a quote for the reservation.</span></span> <span data-ttu-id="7606c-104">Isso é passado para `New-AzReservation` compra.</span><span class="sxs-lookup"><span data-stu-id="7606c-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="7606c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7606c-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7606c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7606c-106">DESCRIPTION</span></span>
<span data-ttu-id="7606c-107">Calcular o preço para fazer um pedido de reserva.</span><span class="sxs-lookup"><span data-stu-id="7606c-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="7606c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7606c-108">EXAMPLES</span></span>

### <span data-ttu-id="7606c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7606c-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="7606c-110">Depois de obter o catálogo, o cliente pode obter o produto diferente com base na localização.</span><span class="sxs-lookup"><span data-stu-id="7606c-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="7606c-111">Ao usar essas informações, verifique o preço corretamente</span><span class="sxs-lookup"><span data-stu-id="7606c-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="7606c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7606c-112">PARAMETERS</span></span>

### <span data-ttu-id="7606c-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="7606c-113">-AppliedScope</span></span>
<span data-ttu-id="7606c-114">Assinatura de que o benefício será aplicado.</span><span class="sxs-lookup"><span data-stu-id="7606c-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="7606c-115">Obrigatório se --tipo de escopo aplicado for Único.</span><span class="sxs-lookup"><span data-stu-id="7606c-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="7606c-116">Não especifique se --tipo de escopo aplicado é Compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7606c-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="7606c-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="7606c-117">-AppliedScopeType</span></span>
<span data-ttu-id="7606c-118">Tipo do Escopo Aplicado para atualizar a reserva com "Único" ou "Compartilhado"</span><span class="sxs-lookup"><span data-stu-id="7606c-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="7606c-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="7606c-119">-BillingPlan</span></span>
<span data-ttu-id="7606c-120">As opções de plano de cobrança disponíveis para esta SKU.</span><span class="sxs-lookup"><span data-stu-id="7606c-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="7606c-121">"Mensal" ou "Upfront"</span><span class="sxs-lookup"><span data-stu-id="7606c-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="7606c-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="7606c-122">-BillingScopeId</span></span>
<span data-ttu-id="7606c-123">Assinatura que será cobrada pela compra de Reserva.</span><span class="sxs-lookup"><span data-stu-id="7606c-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="7606c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7606c-124">-DefaultProfile</span></span>
<span data-ttu-id="7606c-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7606c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7606c-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7606c-126">-DisplayName</span></span>
<span data-ttu-id="7606c-127">Nome amigável para o usuário identificar facilmente a reserva.</span><span class="sxs-lookup"><span data-stu-id="7606c-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="7606c-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="7606c-128">-InstanceFlexibility</span></span>
<span data-ttu-id="7606c-129">Tipo de Flexibilidade de Instância para atualizar a reserva com.</span><span class="sxs-lookup"><span data-stu-id="7606c-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="7606c-130">-Local</span><span class="sxs-lookup"><span data-stu-id="7606c-130">-Location</span></span>
<span data-ttu-id="7606c-131">Local em que a SKU está disponível.</span><span class="sxs-lookup"><span data-stu-id="7606c-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="7606c-132">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="7606c-132">-Quantity</span></span>
<span data-ttu-id="7606c-133">Quantidade de produto para calcular preço ou compra.</span><span class="sxs-lookup"><span data-stu-id="7606c-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="7606c-134">-Renovar</span><span class="sxs-lookup"><span data-stu-id="7606c-134">-Renew</span></span>
<span data-ttu-id="7606c-135">Definir isso como verdadeiro comprará automaticamente uma nova reserva na data de vencimento.</span><span class="sxs-lookup"><span data-stu-id="7606c-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="7606c-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="7606c-136">-ReservedResourceType</span></span>
<span data-ttu-id="7606c-137">Tipo do recurso para o qual as sKIs devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="7606c-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="7606c-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="7606c-138">-Sku</span></span>
<span data-ttu-id="7606c-139">Nome da SKU, obter a lista de SKU usando a apresentação de catálogo de reservas de comando</span><span class="sxs-lookup"><span data-stu-id="7606c-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="7606c-140">-Termo</span><span class="sxs-lookup"><span data-stu-id="7606c-140">-Term</span></span>
<span data-ttu-id="7606c-141">Termos de reserva disponíveis para este recurso.</span><span class="sxs-lookup"><span data-stu-id="7606c-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="7606c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7606c-142">CommonParameters</span></span>
<span data-ttu-id="7606c-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7606c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7606c-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7606c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7606c-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="7606c-145">INPUTS</span></span>

### <span data-ttu-id="7606c-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7606c-146">None</span></span>

## <span data-ttu-id="7606c-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="7606c-147">OUTPUTS</span></span>

### <span data-ttu-id="7606c-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="7606c-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="7606c-149">Notas</span><span class="sxs-lookup"><span data-stu-id="7606c-149">NOTES</span></span>

## <span data-ttu-id="7606c-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7606c-150">RELATED LINKS</span></span>
