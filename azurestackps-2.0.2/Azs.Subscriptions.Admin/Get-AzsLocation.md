---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946733"
---
# <span data-ttu-id="5c42c-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="5c42c-101">Get-AzsLocation</span></span>

## <span data-ttu-id="5c42c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c42c-102">SYNOPSIS</span></span>
<span data-ttu-id="5c42c-103">Obter o local especificado.</span><span class="sxs-lookup"><span data-stu-id="5c42c-103">Get the specified location.</span></span>

## <span data-ttu-id="5c42c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c42c-104">SYNTAX</span></span>

### <span data-ttu-id="5c42c-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="5c42c-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5c42c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="5c42c-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5c42c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5c42c-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5c42c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c42c-108">DESCRIPTION</span></span>
<span data-ttu-id="5c42c-109">Obter o local especificado.</span><span class="sxs-lookup"><span data-stu-id="5c42c-109">Get the specified location.</span></span>

## <span data-ttu-id="5c42c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c42c-110">EXAMPLES</span></span>

### <span data-ttu-id="5c42c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c42c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="5c42c-112">Obtenha uma lista de todos os locais do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="5c42c-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="5c42c-113">OS</span><span class="sxs-lookup"><span data-stu-id="5c42c-113">PARAMETERS</span></span>

### <span data-ttu-id="5c42c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c42c-114">-DefaultProfile</span></span>
<span data-ttu-id="5c42c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c42c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c42c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c42c-116">-InputObject</span></span>
<span data-ttu-id="5c42c-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5c42c-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5c42c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c42c-118">-Name</span></span>
<span data-ttu-id="5c42c-119">O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="5c42c-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5c42c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c42c-120">-SubscriptionId</span></span>
<span data-ttu-id="5c42c-121">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5c42c-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5c42c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c42c-122">CommonParameters</span></span>
<span data-ttu-id="5c42c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c42c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c42c-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c42c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c42c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c42c-125">INPUTS</span></span>

### <span data-ttu-id="5c42c-126">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5c42c-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="5c42c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c42c-127">OUTPUTS</span></span>

### <span data-ttu-id="5c42c-128">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. ILocation</span><span class="sxs-lookup"><span data-stu-id="5c42c-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="5c42c-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5c42c-129">ALIASES</span></span>

## <span data-ttu-id="5c42c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c42c-130">NOTES</span></span>

<span data-ttu-id="5c42c-131">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5c42c-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c42c-132">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5c42c-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5c42c-133">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="5c42c-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c42c-134">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="5c42c-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="5c42c-135">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="5c42c-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="5c42c-136">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5c42c-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c42c-137">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="5c42c-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="5c42c-138">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="5c42c-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="5c42c-139">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="5c42c-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="5c42c-140">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="5c42c-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="5c42c-141">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="5c42c-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="5c42c-142">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="5c42c-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="5c42c-143">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="5c42c-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="5c42c-144">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="5c42c-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="5c42c-145">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="5c42c-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="5c42c-146">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5c42c-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5c42c-147">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5c42c-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="5c42c-148">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="5c42c-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="5c42c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c42c-149">RELATED LINKS</span></span>

