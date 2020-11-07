---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945113"
---
# <span data-ttu-id="23538-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="23538-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="23538-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23538-102">SYNOPSIS</span></span>
<span data-ttu-id="23538-103">Exclui um plano adquirido.</span><span class="sxs-lookup"><span data-stu-id="23538-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="23538-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23538-104">SYNTAX</span></span>

### <span data-ttu-id="23538-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="23538-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="23538-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23538-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="23538-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23538-107">DESCRIPTION</span></span>
<span data-ttu-id="23538-108">Exclui um plano adquirido.</span><span class="sxs-lookup"><span data-stu-id="23538-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="23538-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23538-109">EXAMPLES</span></span>

### <span data-ttu-id="23538-110">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="23538-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="23538-111">Excluir um plano adquirido.</span><span class="sxs-lookup"><span data-stu-id="23538-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="23538-112">OS</span><span class="sxs-lookup"><span data-stu-id="23538-112">PARAMETERS</span></span>

### <span data-ttu-id="23538-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23538-113">-DefaultProfile</span></span>
<span data-ttu-id="23538-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23538-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23538-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23538-115">-InputObject</span></span>
<span data-ttu-id="23538-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="23538-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="23538-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23538-117">-PassThru</span></span>
<span data-ttu-id="23538-118">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="23538-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="23538-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="23538-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="23538-120">O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="23538-120">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="23538-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23538-121">-SubscriptionId</span></span>
<span data-ttu-id="23538-122">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="23538-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="23538-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23538-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="23538-124">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="23538-124">The target subscription ID.</span></span>

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

### <span data-ttu-id="23538-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23538-125">-Confirm</span></span>
<span data-ttu-id="23538-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23538-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23538-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23538-127">-WhatIf</span></span>
<span data-ttu-id="23538-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23538-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23538-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23538-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23538-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23538-130">CommonParameters</span></span>
<span data-ttu-id="23538-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23538-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23538-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23538-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23538-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23538-133">INPUTS</span></span>

### <span data-ttu-id="23538-134">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="23538-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="23538-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23538-135">OUTPUTS</span></span>

### <span data-ttu-id="23538-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23538-136">System.Boolean</span></span>

<span data-ttu-id="23538-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="23538-137">ALIASES</span></span>

### <span data-ttu-id="23538-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="23538-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="23538-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23538-139">NOTES</span></span>

<span data-ttu-id="23538-140">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="23538-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23538-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23538-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="23538-142">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="23538-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23538-143">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="23538-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="23538-144">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="23538-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="23538-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="23538-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23538-146">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="23538-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="23538-147">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="23538-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="23538-148">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="23538-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="23538-149">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="23538-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="23538-150">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="23538-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="23538-151">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="23538-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="23538-152">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="23538-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="23538-153">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="23538-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="23538-154">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="23538-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="23538-155">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="23538-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="23538-156">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="23538-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="23538-157">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="23538-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="23538-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23538-158">RELATED LINKS</span></span>

