---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946849"
---
# <span data-ttu-id="b7298-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="b7298-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="b7298-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7298-102">SYNOPSIS</span></span>
<span data-ttu-id="b7298-103">Obter a delegação de oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="b7298-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="b7298-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7298-104">SYNTAX</span></span>

### <span data-ttu-id="b7298-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b7298-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7298-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b7298-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7298-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7298-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7298-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7298-108">DESCRIPTION</span></span>
<span data-ttu-id="b7298-109">Obter a delegação de oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="b7298-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="b7298-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7298-110">EXAMPLES</span></span>

### <span data-ttu-id="b7298-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7298-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="b7298-112">Obter a lista de ofertas delegadas.</span><span class="sxs-lookup"><span data-stu-id="b7298-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="b7298-113">OS</span><span class="sxs-lookup"><span data-stu-id="b7298-113">PARAMETERS</span></span>

### <span data-ttu-id="b7298-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7298-114">-DefaultProfile</span></span>
<span data-ttu-id="b7298-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7298-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7298-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7298-116">-InputObject</span></span>
<span data-ttu-id="b7298-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b7298-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7298-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7298-118">-Name</span></span>
<span data-ttu-id="b7298-119">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="b7298-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="b7298-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="b7298-120">-OfferName</span></span>
<span data-ttu-id="b7298-121">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="b7298-121">Name of an offer.</span></span>

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

### <span data-ttu-id="b7298-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7298-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7298-123">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="b7298-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b7298-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7298-124">-SubscriptionId</span></span>
<span data-ttu-id="b7298-125">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7298-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7298-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7298-126">CommonParameters</span></span>
<span data-ttu-id="b7298-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7298-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7298-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7298-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7298-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7298-129">INPUTS</span></span>

### <span data-ttu-id="b7298-130">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b7298-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b7298-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7298-131">OUTPUTS</span></span>

### <span data-ttu-id="b7298-132">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="b7298-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="b7298-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b7298-133">ALIASES</span></span>

## <span data-ttu-id="b7298-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7298-134">NOTES</span></span>

<span data-ttu-id="b7298-135">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b7298-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7298-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7298-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b7298-137">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b7298-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7298-138">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="b7298-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b7298-139">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="b7298-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b7298-140">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b7298-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7298-141">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="b7298-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b7298-142">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="b7298-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b7298-143">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="b7298-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b7298-144">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="b7298-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b7298-145">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="b7298-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b7298-146">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="b7298-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b7298-147">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="b7298-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b7298-148">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="b7298-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b7298-149">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="b7298-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b7298-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7298-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b7298-151">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b7298-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b7298-152">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="b7298-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b7298-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7298-153">RELATED LINKS</span></span>

