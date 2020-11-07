---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsmanifest
schema: 2.0.0
ms.openlocfilehash: 4e5ccedc67af31c19d35e5a91fad62ba46535ed7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945374"
---
# <span data-ttu-id="f5d3f-101">Get-AzsManifest</span><span class="sxs-lookup"><span data-stu-id="f5d3f-101">Get-AzsManifest</span></span>

## <span data-ttu-id="f5d3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d3f-103">Obter o manifesto especificado.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-103">Get the specified manifest.</span></span>

## <span data-ttu-id="f5d3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5d3f-104">SYNTAX</span></span>

### <span data-ttu-id="f5d3f-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5d3f-105">List (Default)</span></span>
```
Get-AzsManifest [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5d3f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f5d3f-106">Get</span></span>
```
Get-AzsManifest -ManifestName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5d3f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f5d3f-107">GetViaIdentity</span></span>
```
Get-AzsManifest -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f5d3f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5d3f-108">DESCRIPTION</span></span>
<span data-ttu-id="f5d3f-109">Obter o manifesto especificado.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-109">Get the specified manifest.</span></span>

## <span data-ttu-id="f5d3f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5d3f-110">EXAMPLES</span></span>

### <span data-ttu-id="f5d3f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5d3f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsManifest

Name     : Microsoft-Authorization-Admin--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata

Name     : Microsoft-Authorization--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata
```

<span data-ttu-id="f5d3f-112">Lista todos os manifestos sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-112">Lists all the manifests under the current subscription.</span></span>

## <span data-ttu-id="f5d3f-113">OS</span><span class="sxs-lookup"><span data-stu-id="f5d3f-113">PARAMETERS</span></span>

### <span data-ttu-id="f5d3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d3f-114">-DefaultProfile</span></span>
<span data-ttu-id="f5d3f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5d3f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5d3f-116">-InputObject</span></span>
<span data-ttu-id="f5d3f-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f5d3f-118">-ManifestName</span><span class="sxs-lookup"><span data-stu-id="f5d3f-118">-ManifestName</span></span>
<span data-ttu-id="f5d3f-119">O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-119">The manifest name.</span></span>

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

### <span data-ttu-id="f5d3f-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5d3f-120">-SubscriptionId</span></span>
<span data-ttu-id="f5d3f-121">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f5d3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d3f-122">CommonParameters</span></span>
<span data-ttu-id="f5d3f-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d3f-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5d3f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d3f-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5d3f-125">INPUTS</span></span>

### <span data-ttu-id="f5d3f-126">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f5d3f-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="f5d3f-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5d3f-127">OUTPUTS</span></span>

### <span data-ttu-id="f5d3f-128">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IManifest</span><span class="sxs-lookup"><span data-stu-id="f5d3f-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IManifest</span></span>

<span data-ttu-id="f5d3f-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f5d3f-129">ALIASES</span></span>

## <span data-ttu-id="f5d3f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5d3f-130">NOTES</span></span>

<span data-ttu-id="f5d3f-131">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5d3f-132">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f5d3f-133">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f5d3f-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5d3f-134">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="f5d3f-135">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="f5d3f-136">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f5d3f-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5d3f-137">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="f5d3f-138">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="f5d3f-139">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="f5d3f-140">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="f5d3f-141">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="f5d3f-142">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="f5d3f-143">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="f5d3f-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="f5d3f-144">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="f5d3f-145">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="f5d3f-146">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f5d3f-147">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="f5d3f-148">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="f5d3f-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="f5d3f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5d3f-149">RELATED LINKS</span></span>

