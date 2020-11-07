---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cce59bbbef69f10f39478d784d688a4f1de312fb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774928"
---
# <span data-ttu-id="320de-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="320de-101">New-AzsOffer</span></span>

## <span data-ttu-id="320de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="320de-102">SYNOPSIS</span></span>
<span data-ttu-id="320de-103">Cria uma nova oferta.</span><span class="sxs-lookup"><span data-stu-id="320de-103">Creates a new offer.</span></span>

## <span data-ttu-id="320de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="320de-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320de-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="320de-105">DESCRIPTION</span></span>
<span data-ttu-id="320de-106">Criar ou atualizar a oferta.</span><span class="sxs-lookup"><span data-stu-id="320de-106">Create or update the offer.</span></span>

## <span data-ttu-id="320de-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="320de-107">EXAMPLES</span></span>

### <span data-ttu-id="320de-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="320de-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="320de-109">Cria uma nova oferta.</span><span class="sxs-lookup"><span data-stu-id="320de-109">Creates a new offer.</span></span>

## <span data-ttu-id="320de-110">OS</span><span class="sxs-lookup"><span data-stu-id="320de-110">PARAMETERS</span></span>

### <span data-ttu-id="320de-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="320de-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="320de-112">Referências a planos de complemento que um locatário pode adquirir opcionalmente como parte da oferta.</span><span class="sxs-lookup"><span data-stu-id="320de-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="320de-113">-BasePlanIds</span></span>
<span data-ttu-id="320de-114">Identificadores dos planos base que se tornam disponíveis para o locatário imediatamente quando um locatário assina a oferta.</span><span class="sxs-lookup"><span data-stu-id="320de-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="320de-115">-Description</span></span>
<span data-ttu-id="320de-116">Descrição da oferta.</span><span class="sxs-lookup"><span data-stu-id="320de-116">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="320de-117">-DisplayName</span></span>
<span data-ttu-id="320de-118">Exibir o nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="320de-118">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="320de-119">-ExternalReferenceId</span></span>
<span data-ttu-id="320de-120">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="320de-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-121">-Local</span><span class="sxs-lookup"><span data-stu-id="320de-121">-Location</span></span>
<span data-ttu-id="320de-122">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="320de-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="320de-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="320de-124">Máximo de assinaturas por conta.</span><span class="sxs-lookup"><span data-stu-id="320de-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="320de-125">-Name</span></span>
<span data-ttu-id="320de-126">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="320de-126">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320de-127">-ResourceGroupName</span></span>
<span data-ttu-id="320de-128">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="320de-128">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="320de-129">-State</span></span>
<span data-ttu-id="320de-130">Oferecer o estado de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="320de-130">Offer accessibility state.</span></span>
<span data-ttu-id="320de-131">O valor padrão é particular.</span><span class="sxs-lookup"><span data-stu-id="320de-131">Default value is Private.</span></span>
<span data-ttu-id="320de-132">Esse parâmetro será preterido em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="320de-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="320de-133">-SubscriptionCount</span></span>
<span data-ttu-id="320de-134">Contagem de assinaturas atual.</span><span class="sxs-lookup"><span data-stu-id="320de-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320de-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="320de-135">-Confirm</span></span>
<span data-ttu-id="320de-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320de-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320de-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320de-137">-WhatIf</span></span>
<span data-ttu-id="320de-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="320de-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320de-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="320de-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320de-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320de-140">CommonParameters</span></span>
<span data-ttu-id="320de-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320de-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320de-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320de-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320de-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="320de-143">INPUTS</span></span>

## <span data-ttu-id="320de-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="320de-144">OUTPUTS</span></span>

### <span data-ttu-id="320de-145">Microsoft. AzureStack. Management. subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="320de-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="320de-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="320de-146">NOTES</span></span>

## <span data-ttu-id="320de-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="320de-147">RELATED LINKS</span></span>

