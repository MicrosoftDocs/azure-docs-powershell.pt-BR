---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112702"
---
# <span data-ttu-id="9f613-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="9f613-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="9f613-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f613-102">SYNOPSIS</span></span>
<span data-ttu-id="9f613-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="9f613-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="9f613-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f613-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f613-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f613-105">DESCRIPTION</span></span>
<span data-ttu-id="9f613-106">Calcular o preço para a inserção de uma ordem de reserva.</span><span class="sxs-lookup"><span data-stu-id="9f613-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="9f613-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f613-107">EXAMPLES</span></span>

### <span data-ttu-id="9f613-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f613-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="9f613-109">Depois de obter o catálogo, o cliente pode obter o produto diferente com base no local.</span><span class="sxs-lookup"><span data-stu-id="9f613-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="9f613-110">Ao usar essas informações, verifique o preço corretamente</span><span class="sxs-lookup"><span data-stu-id="9f613-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="9f613-111">OS</span><span class="sxs-lookup"><span data-stu-id="9f613-111">PARAMETERS</span></span>

### <span data-ttu-id="9f613-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="9f613-112">-AppliedScope</span></span>
<span data-ttu-id="9f613-113">Assinatura à qual o benefício será aplicado.</span><span class="sxs-lookup"><span data-stu-id="9f613-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="9f613-114">Obrigatório se--aplicado-Scope-Type for único.</span><span class="sxs-lookup"><span data-stu-id="9f613-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="9f613-115">Não especifique se--aplicado-Scope-Type seja compartilhado.</span><span class="sxs-lookup"><span data-stu-id="9f613-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="9f613-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="9f613-116">-AppliedScopeType</span></span>
<span data-ttu-id="9f613-117">Tipo do escopo aplicado para atualizar a reserva com "único" ou "compartilhado"</span><span class="sxs-lookup"><span data-stu-id="9f613-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="9f613-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="9f613-118">-BillingPlan</span></span>
<span data-ttu-id="9f613-119">As opções de plano de cobrança disponíveis para esta SKU.</span><span class="sxs-lookup"><span data-stu-id="9f613-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="9f613-120">"Mensal" ou "dianteiro"</span><span class="sxs-lookup"><span data-stu-id="9f613-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="9f613-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="9f613-121">-BillingScopeId</span></span>
<span data-ttu-id="9f613-122">Assinatura que será cobrada pela reserva de compras.</span><span class="sxs-lookup"><span data-stu-id="9f613-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="9f613-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f613-123">-DefaultProfile</span></span>
<span data-ttu-id="9f613-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f613-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f613-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9f613-125">-DisplayName</span></span>
<span data-ttu-id="9f613-126">Nome amigável para o usuário identificar facilmente a reserva.</span><span class="sxs-lookup"><span data-stu-id="9f613-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="9f613-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="9f613-127">-InstanceFlexibility</span></span>
<span data-ttu-id="9f613-128">Tipo de flexibilidade de instância para atualizar a reserva.</span><span class="sxs-lookup"><span data-stu-id="9f613-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="9f613-129">-Local</span><span class="sxs-lookup"><span data-stu-id="9f613-129">-Location</span></span>
<span data-ttu-id="9f613-130">Local em que o SKU está disponível.</span><span class="sxs-lookup"><span data-stu-id="9f613-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="9f613-131">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="9f613-131">-Quantity</span></span>
<span data-ttu-id="9f613-132">Quantidade de produto para calcular o preço ou a compra.</span><span class="sxs-lookup"><span data-stu-id="9f613-132">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="9f613-133">-Renove</span><span class="sxs-lookup"><span data-stu-id="9f613-133">-Renew</span></span>
<span data-ttu-id="9f613-134">Defina como verdadeiro para comprar automaticamente uma nova reserva na hora da data de expiração.</span><span class="sxs-lookup"><span data-stu-id="9f613-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="9f613-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="9f613-135">-ReservedResourceType</span></span>
<span data-ttu-id="9f613-136">Tipo do recurso para o qual as SKUs devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="9f613-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="9f613-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="9f613-137">-Sku</span></span>
<span data-ttu-id="9f613-138">Nome do SKU, obter a lista de SKU usando o comando AZ reservas programa de catálogo</span><span class="sxs-lookup"><span data-stu-id="9f613-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="9f613-139">-Prazo</span><span class="sxs-lookup"><span data-stu-id="9f613-139">-Term</span></span>
<span data-ttu-id="9f613-140">Termos de reserva disponíveis para este recurso.</span><span class="sxs-lookup"><span data-stu-id="9f613-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="9f613-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f613-141">CommonParameters</span></span>
<span data-ttu-id="9f613-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f613-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f613-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f613-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f613-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f613-144">INPUTS</span></span>

### <span data-ttu-id="9f613-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9f613-145">None</span></span>

## <span data-ttu-id="9f613-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f613-146">OUTPUTS</span></span>

### <span data-ttu-id="9f613-147">Microsoft. Azure. Management. reservas. Models. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="9f613-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="9f613-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f613-148">NOTES</span></span>

## <span data-ttu-id="9f613-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f613-149">RELATED LINKS</span></span>
