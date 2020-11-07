---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945101"
---
# <span data-ttu-id="e90e1-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e90e1-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="e90e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e90e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e90e1-103">Cria ou atualiza a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e90e1-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="e90e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e90e1-104">SYNTAX</span></span>

### <span data-ttu-id="e90e1-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="e90e1-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e90e1-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="e90e1-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e90e1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e90e1-107">DESCRIPTION</span></span>
<span data-ttu-id="e90e1-108">Cria ou atualiza a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e90e1-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="e90e1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e90e1-109">EXAMPLES</span></span>

### <span data-ttu-id="e90e1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e90e1-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="e90e1-111">Atualiza uma assinatura</span><span class="sxs-lookup"><span data-stu-id="e90e1-111">Updates a subscription</span></span>

## <span data-ttu-id="e90e1-112">OS</span><span class="sxs-lookup"><span data-stu-id="e90e1-112">PARAMETERS</span></span>

### <span data-ttu-id="e90e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90e1-113">-DefaultProfile</span></span>
<span data-ttu-id="e90e1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e90e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e90e1-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="e90e1-116">Identificador de assinatura do DelegatedProvider pai.</span><span class="sxs-lookup"><span data-stu-id="e90e1-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e90e1-117">-DisplayName</span></span>
<span data-ttu-id="e90e1-118">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e90e1-119">-ExternalReferenceId</span></span>
<span data-ttu-id="e90e1-120">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="e90e1-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e90e1-121">-Id</span></span>
<span data-ttu-id="e90e1-122">Identificador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="e90e1-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e90e1-123">-OfferId</span></span>
<span data-ttu-id="e90e1-124">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="e90e1-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-125">-Proprietário</span><span class="sxs-lookup"><span data-stu-id="e90e1-125">-Owner</span></span>
<span data-ttu-id="e90e1-126">Proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="e90e1-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="e90e1-128">Tipo de Gerenciador de recursos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e90e1-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="e90e1-129">-State</span></span>
<span data-ttu-id="e90e1-130">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e90e1-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="e90e1-132">Propriedades do objeto de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-132">Subscription object properties.</span></span>
<span data-ttu-id="e90e1-133">Para construir, consulte a seção notas para propriedades SUBSCRIPTIONDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e90e1-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e90e1-134">-SubscriptionId</span></span>
<span data-ttu-id="e90e1-135">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e90e1-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="e90e1-136">-SubscriptionId1</span></span>
<span data-ttu-id="e90e1-137">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-137">Subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e90e1-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="e90e1-139">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e90e1-139">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-140">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="e90e1-140">-TenantId</span></span>
<span data-ttu-id="e90e1-141">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="e90e1-141">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e90e1-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e90e1-142">-Confirm</span></span>
<span data-ttu-id="e90e1-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e90e1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e90e1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e90e1-144">-WhatIf</span></span>
<span data-ttu-id="e90e1-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e90e1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e90e1-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e90e1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e90e1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90e1-147">CommonParameters</span></span>
<span data-ttu-id="e90e1-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e90e1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90e1-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e90e1-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90e1-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e90e1-150">INPUTS</span></span>

### <span data-ttu-id="e90e1-151">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e90e1-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="e90e1-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e90e1-152">OUTPUTS</span></span>

### <span data-ttu-id="e90e1-153">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e90e1-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="e90e1-154">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e90e1-154">ALIASES</span></span>

## <span data-ttu-id="e90e1-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e90e1-155">NOTES</span></span>

<span data-ttu-id="e90e1-156">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e90e1-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e90e1-157">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e90e1-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e90e1-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : propriedades do objeto de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="e90e1-159">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura do DelegatedProvider pai.</span><span class="sxs-lookup"><span data-stu-id="e90e1-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="e90e1-160">`[DisplayName <String>]`: Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="e90e1-161">`[ExternalReferenceId <String>]`: Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="e90e1-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="e90e1-162">`[Id <String>]`: Identificador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="e90e1-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="e90e1-163">`[OfferId <String>]`: Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="e90e1-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="e90e1-164">`[Owner <String>]`: Proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="e90e1-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Tipo de Gerenciador de recursos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e90e1-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="e90e1-166">`[State <SubscriptionState?>]`: Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="e90e1-167">`[SubscriptionId <String>]`: Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e90e1-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="e90e1-168">`[TenantId <String>]`: Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="e90e1-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="e90e1-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e90e1-169">RELATED LINKS</span></span>

