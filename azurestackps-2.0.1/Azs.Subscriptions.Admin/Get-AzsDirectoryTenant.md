---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945156"
---
# <span data-ttu-id="4921f-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="4921f-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="4921f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4921f-102">SYNOPSIS</span></span>
<span data-ttu-id="4921f-103">Obter um locatário de diretório por nome.</span><span class="sxs-lookup"><span data-stu-id="4921f-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="4921f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4921f-104">SYNTAX</span></span>

### <span data-ttu-id="4921f-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="4921f-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4921f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="4921f-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4921f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4921f-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4921f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4921f-108">DESCRIPTION</span></span>
<span data-ttu-id="4921f-109">Obter um locatário de diretório por nome.</span><span class="sxs-lookup"><span data-stu-id="4921f-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="4921f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4921f-110">EXAMPLES</span></span>

### <span data-ttu-id="4921f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4921f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="4921f-112">Lista todos os locatários de diretório na assinatura atual e o nome do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="4921f-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="4921f-113">OS</span><span class="sxs-lookup"><span data-stu-id="4921f-113">PARAMETERS</span></span>

### <span data-ttu-id="4921f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4921f-114">-DefaultProfile</span></span>
<span data-ttu-id="4921f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4921f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4921f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4921f-116">-InputObject</span></span>
<span data-ttu-id="4921f-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4921f-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4921f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4921f-118">-Name</span></span>
<span data-ttu-id="4921f-119">Nome do locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="4921f-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="4921f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4921f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4921f-121">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="4921f-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4921f-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4921f-122">-SubscriptionId</span></span>
<span data-ttu-id="4921f-123">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4921f-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4921f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4921f-124">CommonParameters</span></span>
<span data-ttu-id="4921f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4921f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4921f-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4921f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4921f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4921f-127">INPUTS</span></span>

### <span data-ttu-id="4921f-128">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4921f-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="4921f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4921f-129">OUTPUTS</span></span>

### <span data-ttu-id="4921f-130">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="4921f-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="4921f-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4921f-131">ALIASES</span></span>

## <span data-ttu-id="4921f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4921f-132">NOTES</span></span>

<span data-ttu-id="4921f-133">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="4921f-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4921f-134">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4921f-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4921f-135">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="4921f-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4921f-136">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="4921f-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="4921f-137">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="4921f-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="4921f-138">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="4921f-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4921f-139">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="4921f-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="4921f-140">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="4921f-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="4921f-141">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="4921f-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="4921f-142">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="4921f-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="4921f-143">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="4921f-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="4921f-144">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="4921f-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="4921f-145">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="4921f-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="4921f-146">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="4921f-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="4921f-147">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="4921f-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="4921f-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4921f-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4921f-149">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4921f-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="4921f-150">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="4921f-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="4921f-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4921f-151">RELATED LINKS</span></span>

