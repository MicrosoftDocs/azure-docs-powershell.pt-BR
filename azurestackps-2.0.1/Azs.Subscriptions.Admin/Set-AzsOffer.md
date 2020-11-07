---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945281"
---
# <span data-ttu-id="afddb-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="afddb-101">Set-AzsOffer</span></span>

## <span data-ttu-id="afddb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afddb-102">SYNOPSIS</span></span>
<span data-ttu-id="afddb-103">Criar ou atualizar a oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-103">Create or update the offer.</span></span>

## <span data-ttu-id="afddb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afddb-104">SYNTAX</span></span>

### <span data-ttu-id="afddb-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="afddb-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="afddb-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="afddb-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="afddb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afddb-107">DESCRIPTION</span></span>
<span data-ttu-id="afddb-108">Criar ou atualizar a oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-108">Create or update the offer.</span></span>

## <span data-ttu-id="afddb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afddb-109">EXAMPLES</span></span>

### <span data-ttu-id="afddb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="afddb-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="afddb-111">Atualize uma oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-111">Update an offer.</span></span>

## <span data-ttu-id="afddb-112">OS</span><span class="sxs-lookup"><span data-stu-id="afddb-112">PARAMETERS</span></span>

### <span data-ttu-id="afddb-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="afddb-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="afddb-114">Referências a planos de complemento que um locatário pode adquirir opcionalmente como parte da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="afddb-115">Para construir, consulte a seção notas para propriedades ADDONPLANDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="afddb-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afddb-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="afddb-116">-BasePlanIds</span></span>
<span data-ttu-id="afddb-117">Identificadores dos planos base que se tornam disponíveis para o locatário imediatamente quando um locatário assina a oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afddb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afddb-118">-DefaultProfile</span></span>
<span data-ttu-id="afddb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afddb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afddb-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="afddb-120">-Description</span></span>
<span data-ttu-id="afddb-121">Descrição da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-121">Description of offer.</span></span>

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

### <span data-ttu-id="afddb-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="afddb-122">-DisplayName</span></span>
<span data-ttu-id="afddb-123">Exibir o nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-123">Display name of offer.</span></span>

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

### <span data-ttu-id="afddb-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="afddb-124">-ExternalReferenceId</span></span>
<span data-ttu-id="afddb-125">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="afddb-125">External reference identifier.</span></span>

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

### <span data-ttu-id="afddb-126">-Local</span><span class="sxs-lookup"><span data-stu-id="afddb-126">-Location</span></span>
<span data-ttu-id="afddb-127">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="afddb-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afddb-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="afddb-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="afddb-129">Máximo de assinaturas por conta.</span><span class="sxs-lookup"><span data-stu-id="afddb-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afddb-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="afddb-130">-Name</span></span>
<span data-ttu-id="afddb-131">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-131">Name of an offer.</span></span>

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

### <span data-ttu-id="afddb-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="afddb-132">-OfferDefinition</span></span>
<span data-ttu-id="afddb-133">Representa uma oferta de serviços em que uma assinatura pode ser criada.</span><span class="sxs-lookup"><span data-stu-id="afddb-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="afddb-134">Para construir, consulte a seção notas para propriedades OFFERDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="afddb-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="afddb-135">-Propertiesname</span><span class="sxs-lookup"><span data-stu-id="afddb-135">-PropertiesName</span></span>
<span data-ttu-id="afddb-136">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-136">Name of the Offer.</span></span>

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

### <span data-ttu-id="afddb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afddb-137">-ResourceGroupName</span></span>
<span data-ttu-id="afddb-138">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="afddb-138">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="afddb-139">-Estado</span><span class="sxs-lookup"><span data-stu-id="afddb-139">-State</span></span>
<span data-ttu-id="afddb-140">Oferecer o estado de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="afddb-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afddb-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="afddb-141">-SubscriptionCount</span></span>
<span data-ttu-id="afddb-142">Contagem de assinaturas atual.</span><span class="sxs-lookup"><span data-stu-id="afddb-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afddb-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afddb-143">-SubscriptionId</span></span>
<span data-ttu-id="afddb-144">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="afddb-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="afddb-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="afddb-145">-Confirm</span></span>
<span data-ttu-id="afddb-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afddb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afddb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afddb-147">-WhatIf</span></span>
<span data-ttu-id="afddb-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="afddb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afddb-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afddb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afddb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afddb-150">CommonParameters</span></span>
<span data-ttu-id="afddb-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afddb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afddb-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afddb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afddb-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afddb-153">INPUTS</span></span>

### <span data-ttu-id="afddb-154">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="afddb-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="afddb-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afddb-155">OUTPUTS</span></span>

### <span data-ttu-id="afddb-156">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="afddb-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="afddb-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="afddb-157">ALIASES</span></span>

## <span data-ttu-id="afddb-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afddb-158">NOTES</span></span>

<span data-ttu-id="afddb-159">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="afddb-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="afddb-160">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="afddb-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="afddb-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: referências a planos de complemento que um locatário pode adquirir opcionalmente como parte da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="afddb-162">`[MaxAcquisitionCount <Int32?>]`: Número máximo de instâncias que podem ser adquiridas por uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="afddb-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="afddb-163">Se não for especificado, o valor presumido será 1.</span><span class="sxs-lookup"><span data-stu-id="afddb-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="afddb-164">`[PlanId <String>]`: Identificador do plano.</span><span class="sxs-lookup"><span data-stu-id="afddb-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="afddb-165">OFFERDEFINITION <IOffer> : representa uma oferta de serviços em que uma assinatura pode ser criada.</span><span class="sxs-lookup"><span data-stu-id="afddb-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="afddb-166">`[Location <String>]`: Localização do recurso</span><span class="sxs-lookup"><span data-stu-id="afddb-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="afddb-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Referências a planos de complemento que um locatário pode adquirir opcionalmente como parte da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="afddb-168">`[MaxAcquisitionCount <Int32?>]`: Número máximo de instâncias que podem ser adquiridas por uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="afddb-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="afddb-169">Se não for especificado, o valor presumido será 1.</span><span class="sxs-lookup"><span data-stu-id="afddb-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="afddb-170">`[PlanId <String>]`: Identificador do plano.</span><span class="sxs-lookup"><span data-stu-id="afddb-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="afddb-171">`[BasePlanIds <String[]>]`: Identificadores dos planos base que se tornam disponíveis para o locatário imediatamente quando um locatário assina a oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="afddb-172">`[Description <String>]`: Descrição da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="afddb-173">`[DisplayName <String>]`: Exibir o nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="afddb-174">`[ExternalReferenceId <String>]`: Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="afddb-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="afddb-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Máximo de assinaturas por conta.</span><span class="sxs-lookup"><span data-stu-id="afddb-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="afddb-176">`[PropertiesName <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="afddb-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="afddb-177">`[State <AccessibilityState?>]`: Oferecer estado de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="afddb-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="afddb-178">`[SubscriptionCount <Int32?>]`: Contagem de assinaturas atual.</span><span class="sxs-lookup"><span data-stu-id="afddb-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="afddb-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afddb-179">RELATED LINKS</span></span>

