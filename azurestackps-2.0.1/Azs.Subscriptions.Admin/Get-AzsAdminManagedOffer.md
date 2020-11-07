---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945159"
---
# <span data-ttu-id="25d71-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="25d71-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="25d71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25d71-102">SYNOPSIS</span></span>
<span data-ttu-id="25d71-103">Obter a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="25d71-103">Get the specified offer.</span></span>

## <span data-ttu-id="25d71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25d71-104">SYNTAX</span></span>

### <span data-ttu-id="25d71-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="25d71-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="25d71-106">Obter</span><span class="sxs-lookup"><span data-stu-id="25d71-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="25d71-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25d71-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="25d71-108">List1</span><span class="sxs-lookup"><span data-stu-id="25d71-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="25d71-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25d71-109">DESCRIPTION</span></span>
<span data-ttu-id="25d71-110">Obter a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="25d71-110">Get the specified offer.</span></span>

## <span data-ttu-id="25d71-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25d71-111">EXAMPLES</span></span>

### <span data-ttu-id="25d71-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25d71-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="25d71-113">Obter oferta por nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d71-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="25d71-114">OS</span><span class="sxs-lookup"><span data-stu-id="25d71-114">PARAMETERS</span></span>

### <span data-ttu-id="25d71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d71-115">-DefaultProfile</span></span>
<span data-ttu-id="25d71-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25d71-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d71-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25d71-117">-InputObject</span></span>
<span data-ttu-id="25d71-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="25d71-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="25d71-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="25d71-119">-Name</span></span>
<span data-ttu-id="25d71-120">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="25d71-120">Name of an offer.</span></span>

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

### <span data-ttu-id="25d71-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d71-121">-ResourceGroupName</span></span>
<span data-ttu-id="25d71-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="25d71-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25d71-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25d71-123">-SubscriptionId</span></span>
<span data-ttu-id="25d71-124">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="25d71-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25d71-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d71-125">CommonParameters</span></span>
<span data-ttu-id="25d71-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d71-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d71-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25d71-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d71-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25d71-128">INPUTS</span></span>

### <span data-ttu-id="25d71-129">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="25d71-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="25d71-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25d71-130">OUTPUTS</span></span>

### <span data-ttu-id="25d71-131">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="25d71-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="25d71-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="25d71-132">ALIASES</span></span>

<span data-ttu-id="25d71-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="25d71-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="25d71-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25d71-134">NOTES</span></span>

<span data-ttu-id="25d71-135">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="25d71-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25d71-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25d71-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="25d71-137">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="25d71-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25d71-138">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="25d71-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="25d71-139">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="25d71-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="25d71-140">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="25d71-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25d71-141">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="25d71-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="25d71-142">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="25d71-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="25d71-143">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="25d71-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="25d71-144">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="25d71-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="25d71-145">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="25d71-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="25d71-146">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="25d71-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="25d71-147">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="25d71-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="25d71-148">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="25d71-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="25d71-149">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="25d71-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="25d71-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="25d71-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="25d71-151">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="25d71-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="25d71-152">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="25d71-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="25d71-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25d71-153">RELATED LINKS</span></span>

