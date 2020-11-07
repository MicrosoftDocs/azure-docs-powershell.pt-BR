---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsoffer
schema: 2.0.0
ms.openlocfilehash: d38c7493e49888fe638cae4fbb5cb937ec41ccba
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946604"
---
# <span data-ttu-id="7ed19-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="7ed19-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="7ed19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ed19-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed19-103">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="7ed19-103">Delete the specified offer.</span></span>

## <span data-ttu-id="7ed19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ed19-104">SYNTAX</span></span>

### <span data-ttu-id="7ed19-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ed19-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ed19-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ed19-106">DeleteViaIdentity</span></span>
```
Remove-AzsOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ed19-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ed19-107">DESCRIPTION</span></span>
<span data-ttu-id="7ed19-108">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="7ed19-108">Delete the specified offer.</span></span>

## <span data-ttu-id="7ed19-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ed19-109">EXAMPLES</span></span>

### <span data-ttu-id="7ed19-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ed19-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOffer -Name "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="7ed19-111">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="7ed19-111">Delete the specified offer.</span></span>

## <span data-ttu-id="7ed19-112">OS</span><span class="sxs-lookup"><span data-stu-id="7ed19-112">PARAMETERS</span></span>

### <span data-ttu-id="7ed19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed19-113">-DefaultProfile</span></span>
<span data-ttu-id="7ed19-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed19-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ed19-115">-InputObject</span></span>
<span data-ttu-id="7ed19-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7ed19-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ed19-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ed19-117">-Name</span></span>
<span data-ttu-id="7ed19-118">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="7ed19-118">Name of an offer.</span></span>

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

### <span data-ttu-id="7ed19-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ed19-119">-PassThru</span></span>
<span data-ttu-id="7ed19-120">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7ed19-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7ed19-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed19-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ed19-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="7ed19-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="7ed19-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ed19-123">-SubscriptionId</span></span>
<span data-ttu-id="7ed19-124">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7ed19-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7ed19-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ed19-125">-Confirm</span></span>
<span data-ttu-id="7ed19-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed19-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed19-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed19-127">-WhatIf</span></span>
<span data-ttu-id="7ed19-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ed19-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed19-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ed19-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed19-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed19-130">CommonParameters</span></span>
<span data-ttu-id="7ed19-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed19-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed19-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ed19-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed19-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ed19-133">INPUTS</span></span>

### <span data-ttu-id="7ed19-134">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7ed19-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="7ed19-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ed19-135">OUTPUTS</span></span>

### <span data-ttu-id="7ed19-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ed19-136">System.Boolean</span></span>

<span data-ttu-id="7ed19-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7ed19-137">ALIASES</span></span>

## <span data-ttu-id="7ed19-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ed19-138">NOTES</span></span>

<span data-ttu-id="7ed19-139">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="7ed19-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ed19-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ed19-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7ed19-141">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="7ed19-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ed19-142">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="7ed19-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="7ed19-143">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="7ed19-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="7ed19-144">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7ed19-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ed19-145">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="7ed19-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="7ed19-146">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="7ed19-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="7ed19-147">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="7ed19-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="7ed19-148">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="7ed19-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="7ed19-149">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="7ed19-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="7ed19-150">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="7ed19-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="7ed19-151">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="7ed19-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="7ed19-152">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="7ed19-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="7ed19-153">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="7ed19-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="7ed19-154">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7ed19-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7ed19-155">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="7ed19-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="7ed19-156">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="7ed19-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="7ed19-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ed19-157">RELATED LINKS</span></span>

