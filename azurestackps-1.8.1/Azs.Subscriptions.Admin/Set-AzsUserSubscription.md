---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774890"
---
# <span data-ttu-id="05b8f-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="05b8f-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="05b8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="05b8f-103">Atualiza a assinatura do usuário especificada</span><span class="sxs-lookup"><span data-stu-id="05b8f-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="05b8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05b8f-104">SYNTAX</span></span>

### <span data-ttu-id="05b8f-105">Definir (padrão)</span><span class="sxs-lookup"><span data-stu-id="05b8f-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b8f-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="05b8f-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b8f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="05b8f-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05b8f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05b8f-108">DESCRIPTION</span></span>
<span data-ttu-id="05b8f-109">Atualiza a assinatura do usuário especificada</span><span class="sxs-lookup"><span data-stu-id="05b8f-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="05b8f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="05b8f-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="05b8f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="05b8f-112">Atualiza uma assinatura</span><span class="sxs-lookup"><span data-stu-id="05b8f-112">Updates a subscription</span></span>

## <span data-ttu-id="05b8f-113">OS</span><span class="sxs-lookup"><span data-stu-id="05b8f-113">PARAMETERS</span></span>

### <span data-ttu-id="05b8f-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05b8f-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="05b8f-115">Identificador de assinatura do DelegatedProvider pai.</span><span class="sxs-lookup"><span data-stu-id="05b8f-115">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="05b8f-116">-DisplayName</span></span>
<span data-ttu-id="05b8f-117">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="05b8f-117">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="05b8f-118">-ExternalReferenceId</span></span>
<span data-ttu-id="05b8f-119">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="05b8f-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05b8f-120">-InputObject</span></span>
<span data-ttu-id="05b8f-121">O objeto de entrada do tipo Microsoft. AzureStack. Management. Network. admin. Models. quota.</span><span class="sxs-lookup"><span data-stu-id="05b8f-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-122">-Local</span><span class="sxs-lookup"><span data-stu-id="05b8f-122">-Location</span></span>
<span data-ttu-id="05b8f-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="05b8f-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="05b8f-124">-OfferId</span></span>
<span data-ttu-id="05b8f-125">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="05b8f-125">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-126">-Proprietário</span><span class="sxs-lookup"><span data-stu-id="05b8f-126">-Owner</span></span>
<span data-ttu-id="05b8f-127">Proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="05b8f-127">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05b8f-128">-ResourceId</span></span>
<span data-ttu-id="05b8f-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="05b8f-129">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="05b8f-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="05b8f-131">Tipo de Gerenciador de recursos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="05b8f-131">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-132">-Estado</span><span class="sxs-lookup"><span data-stu-id="05b8f-132">-State</span></span>
<span data-ttu-id="05b8f-133">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="05b8f-133">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05b8f-134">-SubscriptionId</span></span>
<span data-ttu-id="05b8f-135">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="05b8f-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-136">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="05b8f-136">-TenantId</span></span>
<span data-ttu-id="05b8f-137">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="05b8f-137">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b8f-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05b8f-138">-Confirm</span></span>
<span data-ttu-id="05b8f-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05b8f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b8f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b8f-140">-WhatIf</span></span>
<span data-ttu-id="05b8f-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05b8f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b8f-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05b8f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b8f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b8f-143">CommonParameters</span></span>
<span data-ttu-id="05b8f-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05b8f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b8f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b8f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b8f-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05b8f-146">INPUTS</span></span>

## <span data-ttu-id="05b8f-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05b8f-147">OUTPUTS</span></span>

### <span data-ttu-id="05b8f-148">Microsoft. AzureStack. Management. inscrições. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="05b8f-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="05b8f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05b8f-149">NOTES</span></span>

## <span data-ttu-id="05b8f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05b8f-150">RELATED LINKS</span></span>

