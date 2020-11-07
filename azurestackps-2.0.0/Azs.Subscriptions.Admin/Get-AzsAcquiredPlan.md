---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945144"
---
# <span data-ttu-id="e70c4-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="e70c4-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="e70c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e70c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e70c4-103">Obtém o plano especificado adquirido por uma assinatura que está consumindo a oferta.</span><span class="sxs-lookup"><span data-stu-id="e70c4-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="e70c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e70c4-104">SYNTAX</span></span>

### <span data-ttu-id="e70c4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="e70c4-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e70c4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e70c4-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e70c4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e70c4-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e70c4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e70c4-108">DESCRIPTION</span></span>
<span data-ttu-id="e70c4-109">Obtém o plano especificado adquirido por uma assinatura que está consumindo a oferta.</span><span class="sxs-lookup"><span data-stu-id="e70c4-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="e70c4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e70c4-110">EXAMPLES</span></span>

### <span data-ttu-id="e70c4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e70c4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="e70c4-112">Obtenha uma coleção de todos os planos adquiridos com acesso à assinatura.</span><span class="sxs-lookup"><span data-stu-id="e70c4-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="e70c4-113">OS</span><span class="sxs-lookup"><span data-stu-id="e70c4-113">PARAMETERS</span></span>

### <span data-ttu-id="e70c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70c4-114">-DefaultProfile</span></span>
<span data-ttu-id="e70c4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e70c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e70c4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e70c4-116">-InputObject</span></span>
<span data-ttu-id="e70c4-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e70c4-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e70c4-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="e70c4-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="e70c4-119">O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="e70c4-119">The plan acquisition Identifier</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e70c4-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e70c4-120">-SubscriptionId</span></span>
<span data-ttu-id="e70c4-121">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e70c4-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e70c4-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e70c4-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="e70c4-123">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e70c4-123">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e70c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70c4-124">CommonParameters</span></span>
<span data-ttu-id="e70c4-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e70c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70c4-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e70c4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70c4-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e70c4-127">INPUTS</span></span>

### <span data-ttu-id="e70c4-128">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e70c4-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e70c4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e70c4-129">OUTPUTS</span></span>

### <span data-ttu-id="e70c4-130">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="e70c4-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="e70c4-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e70c4-131">ALIASES</span></span>

<span data-ttu-id="e70c4-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="e70c4-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="e70c4-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e70c4-133">NOTES</span></span>

<span data-ttu-id="e70c4-134">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e70c4-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e70c4-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e70c4-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e70c4-136">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e70c4-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e70c4-137">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="e70c4-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e70c4-138">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="e70c4-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e70c4-139">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e70c4-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e70c4-140">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="e70c4-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e70c4-141">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="e70c4-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e70c4-142">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="e70c4-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e70c4-143">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="e70c4-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e70c4-144">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="e70c4-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e70c4-145">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="e70c4-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e70c4-146">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="e70c4-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e70c4-147">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="e70c4-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e70c4-148">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="e70c4-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e70c4-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e70c4-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e70c4-150">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e70c4-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e70c4-151">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="e70c4-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e70c4-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e70c4-152">RELATED LINKS</span></span>

