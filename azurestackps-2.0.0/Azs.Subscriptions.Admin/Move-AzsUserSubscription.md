---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/move-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 51ad63ef1531e7494b3929b8508e88e988155081
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945147"
---
# <span data-ttu-id="78715-101">Move-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="78715-101">Move-AzsUserSubscription</span></span>

## <span data-ttu-id="78715-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78715-102">SYNOPSIS</span></span>
<span data-ttu-id="78715-103">Mover assinaturas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="78715-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="78715-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78715-104">SYNTAX</span></span>

### <span data-ttu-id="78715-105">MoveExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="78715-105">MoveExpanded (Default)</span></span>
```
Move-AzsUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="78715-106">Vida</span><span class="sxs-lookup"><span data-stu-id="78715-106">Move</span></span>
```
Move-AzsUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="78715-107">MoveViaIdentity</span><span class="sxs-lookup"><span data-stu-id="78715-107">MoveViaIdentity</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="78715-108">MoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="78715-108">MoveViaIdentityExpanded</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78715-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78715-109">DESCRIPTION</span></span>
<span data-ttu-id="78715-110">Mover assinaturas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="78715-110">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="78715-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78715-111">EXAMPLES</span></span>

### <span data-ttu-id="78715-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78715-112">Example 1</span></span>
```powershell
PS C:\> Move-AzsSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

{{ Add output here }}
```

<span data-ttu-id="78715-113">Mova assinaturas de usuários para uma oferta de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="78715-113">Move user subscriptions to a delegated provider offer.</span></span>

### <span data-ttu-id="78715-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="78715-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id
Move-AzsSubscription -ResourceId $resourceIds

{{ Add output here }}
```

<span data-ttu-id="78715-115">Mova assinaturas de usuários de um provedor delegado para o provedor padrão.</span><span class="sxs-lookup"><span data-stu-id="78715-115">Move user subscriptions from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="78715-116">OS</span><span class="sxs-lookup"><span data-stu-id="78715-116">PARAMETERS</span></span>

### <span data-ttu-id="78715-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78715-117">-AsJob</span></span>
<span data-ttu-id="78715-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="78715-118">Run the command as a job</span></span>

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

### <span data-ttu-id="78715-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78715-119">-DefaultProfile</span></span>
<span data-ttu-id="78715-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78715-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78715-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="78715-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="78715-122">O identificador da oferta do provedor delegado (do contexto de administração) para a qual as assinaturas serão movidas.</span><span class="sxs-lookup"><span data-stu-id="78715-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="78715-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78715-123">-InputObject</span></span>
<span data-ttu-id="78715-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="78715-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: MoveViaIdentity, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="78715-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="78715-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="78715-126">A definição da ação mover assinaturas para construir, consulte a seção notas para propriedades MOVESUBSCRIPTIONSDEFINITION e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="78715-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Move, MoveViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="78715-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="78715-127">-NoWait</span></span>
<span data-ttu-id="78715-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="78715-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="78715-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78715-129">-PassThru</span></span>
<span data-ttu-id="78715-130">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="78715-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="78715-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78715-131">-ResourceId</span></span>
<span data-ttu-id="78715-132">Uma coleção de assinaturas para mover para a oferta do provedor delegado de destino.</span><span class="sxs-lookup"><span data-stu-id="78715-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="78715-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78715-133">-SubscriptionId</span></span>
<span data-ttu-id="78715-134">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="78715-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Move, MoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="78715-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78715-135">-Confirm</span></span>
<span data-ttu-id="78715-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78715-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78715-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78715-137">-WhatIf</span></span>
<span data-ttu-id="78715-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78715-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78715-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78715-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78715-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78715-140">CommonParameters</span></span>
<span data-ttu-id="78715-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78715-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78715-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78715-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78715-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78715-143">INPUTS</span></span>

### <span data-ttu-id="78715-144">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="78715-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="78715-145">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="78715-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="78715-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78715-146">OUTPUTS</span></span>

### <span data-ttu-id="78715-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78715-147">System.Boolean</span></span>

<span data-ttu-id="78715-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="78715-148">ALIASES</span></span>

## <span data-ttu-id="78715-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78715-149">NOTES</span></span>

<span data-ttu-id="78715-150">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="78715-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78715-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="78715-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="78715-152">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="78715-152">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78715-153">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="78715-153">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="78715-154">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="78715-154">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="78715-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="78715-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78715-156">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="78715-156">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="78715-157">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="78715-157">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="78715-158">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="78715-158">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="78715-159">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="78715-159">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="78715-160">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="78715-160">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="78715-161">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="78715-161">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="78715-162">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="78715-162">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="78715-163">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="78715-163">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="78715-164">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="78715-164">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="78715-165">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="78715-165">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="78715-166">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="78715-166">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="78715-167">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="78715-167">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="78715-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : a definição da ação mover assinaturas</span><span class="sxs-lookup"><span data-stu-id="78715-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="78715-169">`Resources <String[]>`: Um conjunto de assinaturas para mover-se para a oferta do provedor delegado de destino.</span><span class="sxs-lookup"><span data-stu-id="78715-169">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="78715-170">`[TargetDelegatedProviderOffer <String>]`: O identificador da oferta do provedor delegado (do contexto de administração) para o qual as assinaturas serão movidas.</span><span class="sxs-lookup"><span data-stu-id="78715-170">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="78715-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78715-171">RELATED LINKS</span></span>

