---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945339"
---
# <span data-ttu-id="2c740-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="2c740-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="2c740-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c740-102">SYNOPSIS</span></span>
<span data-ttu-id="2c740-103">Obter uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="2c740-103">Get a specified subscription.</span></span>

## <span data-ttu-id="2c740-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c740-104">SYNTAX</span></span>

### <span data-ttu-id="2c740-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c740-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c740-106">Obter</span><span class="sxs-lookup"><span data-stu-id="2c740-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c740-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2c740-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c740-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c740-108">DESCRIPTION</span></span>
<span data-ttu-id="2c740-109">Obter uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="2c740-109">Get a specified subscription.</span></span>

## <span data-ttu-id="2c740-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c740-110">EXAMPLES</span></span>

### <span data-ttu-id="2c740-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c740-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="2c740-112">Obtenha a lista de assinaturas de usuários como operadora.</span><span class="sxs-lookup"><span data-stu-id="2c740-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="2c740-113">OS</span><span class="sxs-lookup"><span data-stu-id="2c740-113">PARAMETERS</span></span>

### <span data-ttu-id="2c740-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c740-114">-DefaultProfile</span></span>
<span data-ttu-id="2c740-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c740-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c740-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2c740-116">-Filter</span></span>
<span data-ttu-id="2c740-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="2c740-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c740-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c740-118">-InputObject</span></span>
<span data-ttu-id="2c740-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2c740-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2c740-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c740-120">-SubscriptionId</span></span>
<span data-ttu-id="2c740-121">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c740-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2c740-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c740-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="2c740-123">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2c740-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="2c740-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c740-124">CommonParameters</span></span>
<span data-ttu-id="2c740-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c740-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c740-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c740-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c740-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c740-127">INPUTS</span></span>

### <span data-ttu-id="2c740-128">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2c740-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="2c740-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c740-129">OUTPUTS</span></span>

### <span data-ttu-id="2c740-130">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="2c740-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="2c740-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2c740-131">ALIASES</span></span>

## <span data-ttu-id="2c740-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c740-132">NOTES</span></span>

<span data-ttu-id="2c740-133">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="2c740-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c740-134">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2c740-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2c740-135">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="2c740-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c740-136">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="2c740-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="2c740-137">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="2c740-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="2c740-138">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2c740-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c740-139">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="2c740-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="2c740-140">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="2c740-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="2c740-141">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="2c740-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="2c740-142">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="2c740-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="2c740-143">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="2c740-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="2c740-144">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="2c740-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="2c740-145">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="2c740-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="2c740-146">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="2c740-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2c740-147">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="2c740-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="2c740-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c740-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2c740-149">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2c740-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="2c740-150">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="2c740-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="2c740-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c740-151">RELATED LINKS</span></span>

