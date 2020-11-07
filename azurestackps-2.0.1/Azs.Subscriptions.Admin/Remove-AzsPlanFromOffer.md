---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplanfromoffer
schema: 2.0.0
ms.openlocfilehash: c3a68c028abc9033cef9d9fd7e8fbd39e4066d2d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945200"
---
# <span data-ttu-id="67ada-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="67ada-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="67ada-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67ada-102">SYNOPSIS</span></span>
<span data-ttu-id="67ada-103">Desvincular um plano de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="67ada-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="67ada-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67ada-104">SYNTAX</span></span>

### <span data-ttu-id="67ada-105">UnlinkExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="67ada-105">UnlinkExpanded (Default)</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67ada-106">Desvincular</span><span class="sxs-lookup"><span data-stu-id="67ada-106">Unlink</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67ada-107">UnlinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67ada-107">UnlinkViaIdentity</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67ada-108">UnlinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="67ada-108">UnlinkViaIdentityExpanded</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="67ada-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67ada-109">DESCRIPTION</span></span>
<span data-ttu-id="67ada-110">Desvincular um plano de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="67ada-110">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="67ada-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67ada-111">EXAMPLES</span></span>

### <span data-ttu-id="67ada-112">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="67ada-112">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsPlanFromOffer -PlanName "testplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="67ada-113">Desvincular um plano de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="67ada-113">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="67ada-114">OS</span><span class="sxs-lookup"><span data-stu-id="67ada-114">PARAMETERS</span></span>

### <span data-ttu-id="67ada-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ada-115">-DefaultProfile</span></span>
<span data-ttu-id="67ada-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67ada-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ada-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67ada-117">-InputObject</span></span>
<span data-ttu-id="67ada-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="67ada-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: UnlinkViaIdentity, UnlinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="67ada-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="67ada-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="67ada-120">A contagem máxima de aquisições por assinantes</span><span class="sxs-lookup"><span data-stu-id="67ada-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67ada-121">-Offername</span><span class="sxs-lookup"><span data-stu-id="67ada-121">-OfferName</span></span>
<span data-ttu-id="67ada-122">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="67ada-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67ada-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="67ada-123">-PlanLink</span></span>
<span data-ttu-id="67ada-124">Definição para vincular e desvincular planos a ofertas.</span><span class="sxs-lookup"><span data-stu-id="67ada-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="67ada-125">Para construir, consulte a seção notas para propriedades PLANLINK e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="67ada-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Unlink, UnlinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="67ada-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="67ada-126">-PlanLinkType</span></span>
<span data-ttu-id="67ada-127">Tipo do link do plano.</span><span class="sxs-lookup"><span data-stu-id="67ada-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67ada-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="67ada-128">-PlanName</span></span>
<span data-ttu-id="67ada-129">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="67ada-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67ada-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ada-130">-ResourceGroupName</span></span>
<span data-ttu-id="67ada-131">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="67ada-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67ada-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67ada-132">-SubscriptionId</span></span>
<span data-ttu-id="67ada-133">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="67ada-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67ada-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67ada-134">-Confirm</span></span>
<span data-ttu-id="67ada-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67ada-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ada-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ada-136">-WhatIf</span></span>
<span data-ttu-id="67ada-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67ada-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ada-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67ada-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ada-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ada-139">CommonParameters</span></span>
<span data-ttu-id="67ada-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ada-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ada-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67ada-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ada-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67ada-142">INPUTS</span></span>

### <span data-ttu-id="67ada-143">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="67ada-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="67ada-144">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="67ada-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="67ada-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67ada-145">OUTPUTS</span></span>

### <span data-ttu-id="67ada-146">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="67ada-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="67ada-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="67ada-147">ALIASES</span></span>

## <span data-ttu-id="67ada-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67ada-148">NOTES</span></span>

<span data-ttu-id="67ada-149">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="67ada-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67ada-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67ada-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="67ada-151">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="67ada-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67ada-152">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="67ada-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="67ada-153">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="67ada-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="67ada-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="67ada-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67ada-155">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="67ada-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="67ada-156">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="67ada-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="67ada-157">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="67ada-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="67ada-158">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="67ada-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="67ada-159">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="67ada-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="67ada-160">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="67ada-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="67ada-161">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="67ada-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="67ada-162">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="67ada-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="67ada-163">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="67ada-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="67ada-164">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="67ada-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="67ada-165">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="67ada-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="67ada-166">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="67ada-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="67ada-167">PLANLINK <IPlanLinkDefinition> : definição para vincular e desvincular planos a ofertas.</span><span class="sxs-lookup"><span data-stu-id="67ada-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="67ada-168">`[MaxAcquisitionCount <Int32?>]`: A contagem de aquisições máxima por assinantes</span><span class="sxs-lookup"><span data-stu-id="67ada-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="67ada-169">`[PlanLinkType <PlanLinkType?>]`: Tipo do link do plano.</span><span class="sxs-lookup"><span data-stu-id="67ada-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="67ada-170">`[PlanName <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="67ada-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="67ada-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67ada-171">RELATED LINKS</span></span>

