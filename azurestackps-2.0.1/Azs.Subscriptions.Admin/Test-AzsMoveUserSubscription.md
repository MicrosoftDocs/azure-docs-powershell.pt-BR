---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsmoveusersubscription
schema: 2.0.0
ms.openlocfilehash: c0e80b7d0f17bf505c0b3bb8d22539afffea851a
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945280"
---
# <span data-ttu-id="df1ce-101">Test-AzsMoveUserSubscription</span><span class="sxs-lookup"><span data-stu-id="df1ce-101">Test-AzsMoveUserSubscription</span></span>

## <span data-ttu-id="df1ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="df1ce-103">Valide se as assinaturas do usuário podem ser movidas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="df1ce-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="df1ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df1ce-104">SYNTAX</span></span>

### <span data-ttu-id="df1ce-105">ValidateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="df1ce-105">ValidateExpanded (Default)</span></span>
```
Test-AzsMoveUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df1ce-106">Válida</span><span class="sxs-lookup"><span data-stu-id="df1ce-106">Validate</span></span>
```
Test-AzsMoveUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="df1ce-107">ValidateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="df1ce-107">ValidateViaIdentity</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df1ce-108">ValidateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="df1ce-108">ValidateViaIdentityExpanded</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df1ce-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df1ce-109">DESCRIPTION</span></span>
<span data-ttu-id="df1ce-110">Valide se as assinaturas do usuário podem ser movidas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="df1ce-110">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="df1ce-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df1ce-111">EXAMPLES</span></span>

### <span data-ttu-id="df1ce-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df1ce-112">Example 1</span></span>
```powershell
PS C:\> Test-MoveUserSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

```

<span data-ttu-id="df1ce-113">Teste se as assinaturas do usuário podem ser movidas para uma oferta de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="df1ce-113">Test that user subscriptions can be moved to a delegated provider offer.</span></span>

### <span data-ttu-id="df1ce-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="df1ce-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where Displayname -eq "testsubscription" | Select -ExpandProperty Id
Test-MoveUserSubscription -ResourceId $resourceIds

```

<span data-ttu-id="df1ce-115">Teste se as assinaturas do usuário podem ser movidas de um provedor delegado para o provedor padrão.</span><span class="sxs-lookup"><span data-stu-id="df1ce-115">Test that user subscriptions can be moved from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="df1ce-116">OS</span><span class="sxs-lookup"><span data-stu-id="df1ce-116">PARAMETERS</span></span>

### <span data-ttu-id="df1ce-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df1ce-117">-AsJob</span></span>
<span data-ttu-id="df1ce-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="df1ce-118">Run the command as a job</span></span>

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

### <span data-ttu-id="df1ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1ce-119">-DefaultProfile</span></span>
<span data-ttu-id="df1ce-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df1ce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df1ce-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="df1ce-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="df1ce-122">O identificador da oferta do provedor delegado (do contexto de administração) para a qual as assinaturas serão movidas.</span><span class="sxs-lookup"><span data-stu-id="df1ce-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="df1ce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df1ce-123">-InputObject</span></span>
<span data-ttu-id="df1ce-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="df1ce-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: ValidateViaIdentity, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="df1ce-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="df1ce-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="df1ce-126">A definição da ação mover assinaturas para construir, consulte a seção notas para propriedades MOVESUBSCRIPTIONSDEFINITION e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="df1ce-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Validate, ValidateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="df1ce-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="df1ce-127">-NoWait</span></span>
<span data-ttu-id="df1ce-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="df1ce-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df1ce-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df1ce-129">-PassThru</span></span>
<span data-ttu-id="df1ce-130">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="df1ce-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="df1ce-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df1ce-131">-ResourceId</span></span>
<span data-ttu-id="df1ce-132">Uma coleção de assinaturas para mover para a oferta do provedor delegado de destino.</span><span class="sxs-lookup"><span data-stu-id="df1ce-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="df1ce-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df1ce-133">-SubscriptionId</span></span>
<span data-ttu-id="df1ce-134">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="df1ce-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Validate, ValidateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="df1ce-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df1ce-135">-Confirm</span></span>
<span data-ttu-id="df1ce-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1ce-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df1ce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df1ce-137">-WhatIf</span></span>
<span data-ttu-id="df1ce-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df1ce-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df1ce-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df1ce-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df1ce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1ce-140">CommonParameters</span></span>
<span data-ttu-id="df1ce-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1ce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1ce-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df1ce-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1ce-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df1ce-143">INPUTS</span></span>

### <span data-ttu-id="df1ce-144">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="df1ce-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="df1ce-145">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="df1ce-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="df1ce-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df1ce-146">OUTPUTS</span></span>

### <span data-ttu-id="df1ce-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df1ce-147">System.Boolean</span></span>

<span data-ttu-id="df1ce-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="df1ce-148">ALIASES</span></span>

### <span data-ttu-id="df1ce-149">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="df1ce-149">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="df1ce-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df1ce-150">NOTES</span></span>

<span data-ttu-id="df1ce-151">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="df1ce-151">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df1ce-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df1ce-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="df1ce-153">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="df1ce-153">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df1ce-154">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="df1ce-154">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="df1ce-155">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="df1ce-155">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="df1ce-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="df1ce-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df1ce-157">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="df1ce-157">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="df1ce-158">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="df1ce-158">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="df1ce-159">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="df1ce-159">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="df1ce-160">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="df1ce-160">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="df1ce-161">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="df1ce-161">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="df1ce-162">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="df1ce-162">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="df1ce-163">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="df1ce-163">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="df1ce-164">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="df1ce-164">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="df1ce-165">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="df1ce-165">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="df1ce-166">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="df1ce-166">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="df1ce-167">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="df1ce-167">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="df1ce-168">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="df1ce-168">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="df1ce-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : a definição da ação mover assinaturas</span><span class="sxs-lookup"><span data-stu-id="df1ce-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="df1ce-170">`Resources <String[]>`: Um conjunto de assinaturas para mover-se para a oferta do provedor delegado de destino.</span><span class="sxs-lookup"><span data-stu-id="df1ce-170">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="df1ce-171">`[TargetDelegatedProviderOffer <String>]`: O identificador da oferta do provedor delegado (do contexto de administração) para o qual as assinaturas serão movidas.</span><span class="sxs-lookup"><span data-stu-id="df1ce-171">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="df1ce-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df1ce-172">RELATED LINKS</span></span>

