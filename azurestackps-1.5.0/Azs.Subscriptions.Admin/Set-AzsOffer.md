---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 285b9509241e9035c007f871ac6395008a1f9cde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426114"
---
# <span data-ttu-id="44122-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="44122-101">Set-AzsOffer</span></span>

## <span data-ttu-id="44122-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44122-102">SYNOPSIS</span></span>
<span data-ttu-id="44122-103">Atualize a oferta.</span><span class="sxs-lookup"><span data-stu-id="44122-103">Update the offer.</span></span>

## <span data-ttu-id="44122-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44122-104">SYNTAX</span></span>

### <span data-ttu-id="44122-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="44122-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44122-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="44122-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44122-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="44122-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44122-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44122-108">DESCRIPTION</span></span>
<span data-ttu-id="44122-109">Atualize a oferta.</span><span class="sxs-lookup"><span data-stu-id="44122-109">Update the offer.</span></span>

## <span data-ttu-id="44122-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44122-110">EXAMPLES</span></span>

### <span data-ttu-id="44122-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="44122-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="44122-112">Atualize a oferta.</span><span class="sxs-lookup"><span data-stu-id="44122-112">Update the offer.</span></span>

## <span data-ttu-id="44122-113">OS</span><span class="sxs-lookup"><span data-stu-id="44122-113">PARAMETERS</span></span>

### <span data-ttu-id="44122-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="44122-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="44122-115">Referências a planos de complemento que um locatário pode adquirir opcionalmente como parte da oferta.</span><span class="sxs-lookup"><span data-stu-id="44122-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="44122-116">-BasePlanIds</span></span>
<span data-ttu-id="44122-117">Identificadores dos planos base que se tornam disponíveis para o locatário imediatamente quando um locatário assina a oferta.</span><span class="sxs-lookup"><span data-stu-id="44122-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="44122-118">-Description</span></span>
<span data-ttu-id="44122-119">Descrição da oferta.</span><span class="sxs-lookup"><span data-stu-id="44122-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="44122-120">-DisplayName</span></span>
<span data-ttu-id="44122-121">Exibir o nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="44122-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="44122-122">-ExternalReferenceId</span></span>
<span data-ttu-id="44122-123">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="44122-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44122-124">-InputObject</span></span>
<span data-ttu-id="44122-125">O objeto de entrada do tipo Microsoft. AzureStack. Management. subscriptions. admin. Models. offer.</span><span class="sxs-lookup"><span data-stu-id="44122-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44122-126">-Local</span><span class="sxs-lookup"><span data-stu-id="44122-126">-Location</span></span>
<span data-ttu-id="44122-127">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="44122-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="44122-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="44122-129">Máximo de assinaturas por conta.</span><span class="sxs-lookup"><span data-stu-id="44122-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="44122-130">-Name</span></span>
<span data-ttu-id="44122-131">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="44122-131">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44122-132">-ResourceGroupName</span></span>
<span data-ttu-id="44122-133">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="44122-133">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44122-134">-ResourceId</span></span>
<span data-ttu-id="44122-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="44122-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44122-136">-Estado</span><span class="sxs-lookup"><span data-stu-id="44122-136">-State</span></span>
<span data-ttu-id="44122-137">Oferecer o estado de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="44122-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="44122-138">-SubscriptionCount</span></span>
<span data-ttu-id="44122-139">Contagem de assinaturas atual.</span><span class="sxs-lookup"><span data-stu-id="44122-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44122-140">-Confirm</span></span>
<span data-ttu-id="44122-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44122-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44122-142">-WhatIf</span></span>
<span data-ttu-id="44122-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44122-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44122-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44122-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44122-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44122-145">CommonParameters</span></span>
<span data-ttu-id="44122-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44122-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44122-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44122-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44122-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44122-148">INPUTS</span></span>

## <span data-ttu-id="44122-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44122-149">OUTPUTS</span></span>

### <span data-ttu-id="44122-150">Microsoft. AzureStack. Management. subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="44122-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="44122-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44122-151">NOTES</span></span>

## <span data-ttu-id="44122-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44122-152">RELATED LINKS</span></span>

