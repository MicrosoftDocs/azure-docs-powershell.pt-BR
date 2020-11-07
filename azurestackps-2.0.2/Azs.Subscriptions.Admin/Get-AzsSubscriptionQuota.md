---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947065"
---
# <span data-ttu-id="b8ad6-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="b8ad6-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="b8ad6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ad6-103">Obtém uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-103">Gets a quota by name.</span></span>

## <span data-ttu-id="b8ad6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8ad6-104">SYNTAX</span></span>

### <span data-ttu-id="b8ad6-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8ad6-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8ad6-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b8ad6-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b8ad6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8ad6-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8ad6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8ad6-108">DESCRIPTION</span></span>
<span data-ttu-id="b8ad6-109">Obtém uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-109">Gets a quota by name.</span></span>

## <span data-ttu-id="b8ad6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8ad6-110">EXAMPLES</span></span>

### <span data-ttu-id="b8ad6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8ad6-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="b8ad6-112">Obtenha a lista de cotas do provedor de recursos de assinatura.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="b8ad6-113">OS</span><span class="sxs-lookup"><span data-stu-id="b8ad6-113">PARAMETERS</span></span>

### <span data-ttu-id="b8ad6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ad6-114">-DefaultProfile</span></span>
<span data-ttu-id="b8ad6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8ad6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8ad6-116">-InputObject</span></span>
<span data-ttu-id="b8ad6-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8ad6-118">-Local</span><span class="sxs-lookup"><span data-stu-id="b8ad6-118">-Location</span></span>
<span data-ttu-id="b8ad6-119">O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b8ad6-120">-Quota</span><span class="sxs-lookup"><span data-stu-id="b8ad6-120">-Quota</span></span>
<span data-ttu-id="b8ad6-121">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-121">Name of the quota.</span></span>

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

### <span data-ttu-id="b8ad6-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8ad6-122">-SubscriptionId</span></span>
<span data-ttu-id="b8ad6-123">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b8ad6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ad6-124">CommonParameters</span></span>
<span data-ttu-id="b8ad6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ad6-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8ad6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ad6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8ad6-127">INPUTS</span></span>

### <span data-ttu-id="b8ad6-128">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b8ad6-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b8ad6-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8ad6-129">OUTPUTS</span></span>

### <span data-ttu-id="b8ad6-130">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IQuota</span><span class="sxs-lookup"><span data-stu-id="b8ad6-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="b8ad6-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b8ad6-131">ALIASES</span></span>

<span data-ttu-id="b8ad6-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="b8ad6-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="b8ad6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8ad6-133">NOTES</span></span>

<span data-ttu-id="b8ad6-134">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8ad6-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b8ad6-136">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b8ad6-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8ad6-137">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b8ad6-138">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b8ad6-139">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b8ad6-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8ad6-140">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b8ad6-141">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b8ad6-142">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b8ad6-143">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b8ad6-144">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b8ad6-145">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b8ad6-146">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="b8ad6-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b8ad6-147">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b8ad6-148">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b8ad6-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b8ad6-150">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b8ad6-151">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="b8ad6-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b8ad6-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8ad6-152">RELATED LINKS</span></span>

