---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945133"
---
# <span data-ttu-id="52053-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="52053-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="52053-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52053-102">SYNOPSIS</span></span>
<span data-ttu-id="52053-103">Verifica a integridade da identidade</span><span class="sxs-lookup"><span data-stu-id="52053-103">Checks the identity health</span></span>

## <span data-ttu-id="52053-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52053-104">SYNTAX</span></span>

### <span data-ttu-id="52053-105">Verificar (padrão)</span><span class="sxs-lookup"><span data-stu-id="52053-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="52053-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52053-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52053-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52053-107">DESCRIPTION</span></span>
<span data-ttu-id="52053-108">Verifica a integridade da identidade</span><span class="sxs-lookup"><span data-stu-id="52053-108">Checks the identity health</span></span>

## <span data-ttu-id="52053-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52053-109">EXAMPLES</span></span>

### <span data-ttu-id="52053-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52053-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="52053-111">Obter o status da integridade da identidade.</span><span class="sxs-lookup"><span data-stu-id="52053-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="52053-112">OS</span><span class="sxs-lookup"><span data-stu-id="52053-112">PARAMETERS</span></span>

### <span data-ttu-id="52053-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52053-113">-DefaultProfile</span></span>
<span data-ttu-id="52053-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52053-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52053-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52053-115">-InputObject</span></span>
<span data-ttu-id="52053-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="52053-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="52053-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52053-117">-SubscriptionId</span></span>
<span data-ttu-id="52053-118">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="52053-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52053-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52053-119">-Confirm</span></span>
<span data-ttu-id="52053-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52053-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52053-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52053-121">-WhatIf</span></span>
<span data-ttu-id="52053-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52053-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52053-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52053-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52053-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52053-124">CommonParameters</span></span>
<span data-ttu-id="52053-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52053-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52053-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52053-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52053-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52053-127">INPUTS</span></span>

### <span data-ttu-id="52053-128">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="52053-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="52053-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52053-129">OUTPUTS</span></span>

### <span data-ttu-id="52053-130">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IIdentityHealthCheckReportDefinition</span><span class="sxs-lookup"><span data-stu-id="52053-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="52053-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="52053-131">ALIASES</span></span>

## <span data-ttu-id="52053-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52053-132">NOTES</span></span>

<span data-ttu-id="52053-133">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="52053-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52053-134">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52053-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="52053-135">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="52053-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52053-136">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="52053-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="52053-137">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="52053-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="52053-138">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="52053-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52053-139">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="52053-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="52053-140">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="52053-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="52053-141">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="52053-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="52053-142">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="52053-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="52053-143">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="52053-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="52053-144">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="52053-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="52053-145">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="52053-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="52053-146">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="52053-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="52053-147">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="52053-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="52053-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="52053-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="52053-149">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="52053-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="52053-150">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="52053-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="52053-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52053-151">RELATED LINKS</span></span>

