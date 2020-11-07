---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945279"
---
# <span data-ttu-id="c3d3b-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c3d3b-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="c3d3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d3b-103">Obter a lista de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="c3d3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3d3b-104">SYNTAX</span></span>

### <span data-ttu-id="c3d3b-105">CheckExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3d3b-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3d3b-106">Selecionar</span><span class="sxs-lookup"><span data-stu-id="c3d3b-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3d3b-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c3d3b-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3d3b-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c3d3b-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3d3b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3d3b-109">DESCRIPTION</span></span>
<span data-ttu-id="c3d3b-110">Obter a lista de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="c3d3b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3d3b-111">EXAMPLES</span></span>

### <span data-ttu-id="c3d3b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3d3b-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="c3d3b-113">Retorna a disponibilidade do tipo e do nome do recurso de assinatura especificado</span><span class="sxs-lookup"><span data-stu-id="c3d3b-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="c3d3b-114">OS</span><span class="sxs-lookup"><span data-stu-id="c3d3b-114">PARAMETERS</span></span>

### <span data-ttu-id="c3d3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d3b-115">-DefaultProfile</span></span>
<span data-ttu-id="c3d3b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d3b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d3b-117">-InputObject</span></span>
<span data-ttu-id="c3d3b-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c3d3b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3d3b-119">-Name</span></span>
<span data-ttu-id="c3d3b-120">O nome do recurso a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c3d3b-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="c3d3b-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="c3d3b-122">A definição da ação verificar disponibilidade do nome.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-122">The check name availability action definition.</span></span>
<span data-ttu-id="c3d3b-123">Para construir, consulte a seção notas para propriedades NAMEAVAILABILITYDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c3d3b-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c3d3b-124">-ResourceType</span></span>
<span data-ttu-id="c3d3b-125">O tipo de recurso a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c3d3b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3d3b-126">-SubscriptionId</span></span>
<span data-ttu-id="c3d3b-127">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c3d3b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3d3b-128">-Confirm</span></span>
<span data-ttu-id="c3d3b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d3b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d3b-130">-WhatIf</span></span>
<span data-ttu-id="c3d3b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d3b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d3b-133">CommonParameters</span></span>
<span data-ttu-id="c3d3b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d3b-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3d3b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d3b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3d3b-136">INPUTS</span></span>

### <span data-ttu-id="c3d3b-137">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="c3d3b-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="c3d3b-138">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c3d3b-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="c3d3b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3d3b-139">OUTPUTS</span></span>

### <span data-ttu-id="c3d3b-140">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c3d3b-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="c3d3b-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c3d3b-141">ALIASES</span></span>

## <span data-ttu-id="c3d3b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3d3b-142">NOTES</span></span>

<span data-ttu-id="c3d3b-143">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3d3b-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c3d3b-145">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c3d3b-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3d3b-146">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="c3d3b-147">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="c3d3b-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c3d3b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3d3b-149">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="c3d3b-150">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="c3d3b-151">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="c3d3b-152">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="c3d3b-153">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="c3d3b-154">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="c3d3b-155">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="c3d3b-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="c3d3b-156">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c3d3b-157">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="c3d3b-158">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c3d3b-159">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="c3d3b-160">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="c3d3b-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : a definição da ação verificar disponibilidade do nome.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="c3d3b-162">`[Name <String>]`: O nome do recurso a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="c3d3b-163">`[ResourceType <String>]`: O tipo de recurso a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="c3d3b-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="c3d3b-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3d3b-164">RELATED LINKS</span></span>

