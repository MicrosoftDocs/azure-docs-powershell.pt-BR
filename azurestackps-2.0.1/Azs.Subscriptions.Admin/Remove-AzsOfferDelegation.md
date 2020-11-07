---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: e9de73f68501071bceb87c115c2c9882fc5ea988
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945176"
---
# <span data-ttu-id="33aff-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="33aff-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="33aff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33aff-102">SYNOPSIS</span></span>
<span data-ttu-id="33aff-103">Exclua a delegação de oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="33aff-103">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="33aff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33aff-104">SYNTAX</span></span>

### <span data-ttu-id="33aff-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="33aff-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="33aff-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="33aff-106">DeleteViaIdentity</span></span>
```
Remove-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33aff-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33aff-107">DESCRIPTION</span></span>
<span data-ttu-id="33aff-108">Exclua a delegação de oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="33aff-108">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="33aff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33aff-109">EXAMPLES</span></span>

### <span data-ttu-id="33aff-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33aff-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1

{{ Add output here }}
```

<span data-ttu-id="33aff-111">Remove a delegação de oferta</span><span class="sxs-lookup"><span data-stu-id="33aff-111">Removes the offer delegation</span></span>

## <span data-ttu-id="33aff-112">OS</span><span class="sxs-lookup"><span data-stu-id="33aff-112">PARAMETERS</span></span>

### <span data-ttu-id="33aff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33aff-113">-DefaultProfile</span></span>
<span data-ttu-id="33aff-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33aff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33aff-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33aff-115">-InputObject</span></span>
<span data-ttu-id="33aff-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="33aff-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="33aff-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="33aff-117">-Name</span></span>
<span data-ttu-id="33aff-118">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="33aff-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="33aff-119">-Offername</span><span class="sxs-lookup"><span data-stu-id="33aff-119">-OfferName</span></span>
<span data-ttu-id="33aff-120">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="33aff-120">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="33aff-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33aff-121">-PassThru</span></span>
<span data-ttu-id="33aff-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="33aff-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="33aff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33aff-123">-ResourceGroupName</span></span>
<span data-ttu-id="33aff-124">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="33aff-124">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="33aff-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33aff-125">-SubscriptionId</span></span>
<span data-ttu-id="33aff-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="33aff-126">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="33aff-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33aff-127">-Confirm</span></span>
<span data-ttu-id="33aff-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33aff-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33aff-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33aff-129">-WhatIf</span></span>
<span data-ttu-id="33aff-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33aff-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33aff-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33aff-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33aff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33aff-132">CommonParameters</span></span>
<span data-ttu-id="33aff-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33aff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33aff-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33aff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33aff-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33aff-135">INPUTS</span></span>

### <span data-ttu-id="33aff-136">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="33aff-136">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="33aff-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33aff-137">OUTPUTS</span></span>

### <span data-ttu-id="33aff-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33aff-138">System.Boolean</span></span>

<span data-ttu-id="33aff-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="33aff-139">ALIASES</span></span>

## <span data-ttu-id="33aff-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33aff-140">NOTES</span></span>

<span data-ttu-id="33aff-141">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="33aff-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33aff-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33aff-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="33aff-143">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="33aff-143">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33aff-144">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="33aff-144">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="33aff-145">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="33aff-145">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="33aff-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="33aff-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33aff-147">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="33aff-147">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="33aff-148">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="33aff-148">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="33aff-149">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="33aff-149">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="33aff-150">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="33aff-150">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="33aff-151">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="33aff-151">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="33aff-152">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="33aff-152">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="33aff-153">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="33aff-153">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="33aff-154">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="33aff-154">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="33aff-155">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="33aff-155">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="33aff-156">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="33aff-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="33aff-157">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="33aff-157">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="33aff-158">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="33aff-158">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="33aff-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33aff-159">RELATED LINKS</span></span>

