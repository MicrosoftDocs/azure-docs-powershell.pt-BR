---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplan
schema: 2.0.0
ms.openlocfilehash: 4aa59d41bc13d79e487465a6a0721ec19ed68bb8
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945086"
---
# <span data-ttu-id="0ae69-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="0ae69-101">Get-AzsPlan</span></span>

## <span data-ttu-id="0ae69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ae69-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae69-103">Obter o plano especificado.</span><span class="sxs-lookup"><span data-stu-id="0ae69-103">Get the specified plan.</span></span>

## <span data-ttu-id="0ae69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ae69-104">SYNTAX</span></span>

### <span data-ttu-id="0ae69-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="0ae69-105">List (Default)</span></span>
```
Get-AzsPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ae69-106">Obter</span><span class="sxs-lookup"><span data-stu-id="0ae69-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ae69-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ae69-107">GetViaIdentity</span></span>
```
Get-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ae69-108">List1</span><span class="sxs-lookup"><span data-stu-id="0ae69-108">List1</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ae69-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ae69-109">DESCRIPTION</span></span>
<span data-ttu-id="0ae69-110">Obter o plano especificado.</span><span class="sxs-lookup"><span data-stu-id="0ae69-110">Get the specified plan.</span></span>

## <span data-ttu-id="0ae69-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ae69-111">EXAMPLES</span></span>

### <span data-ttu-id="0ae69-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ae69-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 1
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="0ae69-113">Obtenha um plano do specifc sob estas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="0ae69-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="0ae69-114">OS</span><span class="sxs-lookup"><span data-stu-id="0ae69-114">PARAMETERS</span></span>

### <span data-ttu-id="0ae69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae69-115">-DefaultProfile</span></span>
<span data-ttu-id="0ae69-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ae69-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ae69-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ae69-117">-InputObject</span></span>
<span data-ttu-id="0ae69-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0ae69-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ae69-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ae69-119">-Name</span></span>
<span data-ttu-id="0ae69-120">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="0ae69-120">Name of the plan.</span></span>

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

### <span data-ttu-id="0ae69-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae69-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ae69-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="0ae69-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0ae69-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ae69-123">-SubscriptionId</span></span>
<span data-ttu-id="0ae69-124">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0ae69-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0ae69-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae69-125">CommonParameters</span></span>
<span data-ttu-id="0ae69-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ae69-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae69-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ae69-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae69-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ae69-128">INPUTS</span></span>

### <span data-ttu-id="0ae69-129">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0ae69-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="0ae69-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ae69-130">OUTPUTS</span></span>

### <span data-ttu-id="0ae69-131">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="0ae69-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="0ae69-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0ae69-132">ALIASES</span></span>

## <span data-ttu-id="0ae69-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ae69-133">NOTES</span></span>

<span data-ttu-id="0ae69-134">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="0ae69-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ae69-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ae69-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0ae69-136">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="0ae69-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ae69-137">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="0ae69-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="0ae69-138">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="0ae69-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="0ae69-139">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="0ae69-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ae69-140">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="0ae69-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="0ae69-141">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="0ae69-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="0ae69-142">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="0ae69-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="0ae69-143">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="0ae69-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="0ae69-144">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="0ae69-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="0ae69-145">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="0ae69-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="0ae69-146">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="0ae69-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="0ae69-147">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="0ae69-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="0ae69-148">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="0ae69-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="0ae69-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0ae69-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0ae69-150">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0ae69-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="0ae69-151">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="0ae69-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="0ae69-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ae69-152">RELATED LINKS</span></span>

