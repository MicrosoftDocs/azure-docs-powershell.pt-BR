---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945179"
---
# <span data-ttu-id="fee08-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="fee08-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="fee08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fee08-102">SYNOPSIS</span></span>
<span data-ttu-id="fee08-103">Cria ou atualiza a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="fee08-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="fee08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fee08-104">SYNTAX</span></span>

### <span data-ttu-id="fee08-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="fee08-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fee08-106">Criados</span><span class="sxs-lookup"><span data-stu-id="fee08-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fee08-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fee08-107">DESCRIPTION</span></span>
<span data-ttu-id="fee08-108">Cria ou atualiza a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="fee08-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="fee08-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fee08-109">EXAMPLES</span></span>

### <span data-ttu-id="fee08-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fee08-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="fee08-111">Cria uma nova assinatura de usuário</span><span class="sxs-lookup"><span data-stu-id="fee08-111">Creates a new user subscription</span></span>

## <span data-ttu-id="fee08-112">OS</span><span class="sxs-lookup"><span data-stu-id="fee08-112">PARAMETERS</span></span>

### <span data-ttu-id="fee08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee08-113">-DefaultProfile</span></span>
<span data-ttu-id="fee08-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fee08-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee08-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fee08-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="fee08-116">Identificador de assinatura do DelegatedProvider pai.</span><span class="sxs-lookup"><span data-stu-id="fee08-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fee08-117">-DisplayName</span></span>
<span data-ttu-id="fee08-118">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="fee08-119">-ExternalReferenceId</span></span>
<span data-ttu-id="fee08-120">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="fee08-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-121">-ID</span><span class="sxs-lookup"><span data-stu-id="fee08-121">-Id</span></span>
<span data-ttu-id="fee08-122">Identificador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="fee08-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="fee08-123">-OfferId</span></span>
<span data-ttu-id="fee08-124">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="fee08-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-125">-Proprietário</span><span class="sxs-lookup"><span data-stu-id="fee08-125">-Owner</span></span>
<span data-ttu-id="fee08-126">Proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="fee08-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="fee08-128">Tipo de Gerenciador de recursos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="fee08-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="fee08-129">-State</span></span>
<span data-ttu-id="fee08-130">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="fee08-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="fee08-132">Propriedades do objeto de assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-132">Subscription object properties.</span></span>
<span data-ttu-id="fee08-133">Para construir, consulte a seção notas para propriedades SUBSCRIPTIONDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fee08-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fee08-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="fee08-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fee08-135">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-136">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="fee08-136">-TenantId</span></span>
<span data-ttu-id="fee08-137">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="fee08-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fee08-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fee08-138">-Confirm</span></span>
<span data-ttu-id="fee08-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee08-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee08-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee08-140">-WhatIf</span></span>
<span data-ttu-id="fee08-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fee08-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee08-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fee08-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee08-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee08-143">CommonParameters</span></span>
<span data-ttu-id="fee08-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee08-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee08-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fee08-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee08-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fee08-146">INPUTS</span></span>

### <span data-ttu-id="fee08-147">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="fee08-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="fee08-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fee08-148">OUTPUTS</span></span>

### <span data-ttu-id="fee08-149">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="fee08-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="fee08-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fee08-150">ALIASES</span></span>

## <span data-ttu-id="fee08-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fee08-151">NOTES</span></span>

<span data-ttu-id="fee08-152">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="fee08-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fee08-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fee08-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fee08-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : propriedades do objeto de assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="fee08-155">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura do DelegatedProvider pai.</span><span class="sxs-lookup"><span data-stu-id="fee08-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="fee08-156">`[DisplayName <String>]`: Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="fee08-157">`[ExternalReferenceId <String>]`: Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="fee08-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="fee08-158">`[Id <String>]`: Identificador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="fee08-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="fee08-159">`[OfferId <String>]`: Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="fee08-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="fee08-160">`[Owner <String>]`: Proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="fee08-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Tipo de Gerenciador de recursos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="fee08-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="fee08-162">`[State <SubscriptionState?>]`: Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="fee08-163">`[SubscriptionId <String>]`: Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="fee08-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="fee08-164">`[TenantId <String>]`: Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="fee08-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="fee08-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fee08-165">RELATED LINKS</span></span>

