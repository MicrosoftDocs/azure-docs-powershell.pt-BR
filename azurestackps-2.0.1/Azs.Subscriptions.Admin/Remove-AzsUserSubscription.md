---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945198"
---
# <span data-ttu-id="e12ff-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e12ff-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="e12ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e12ff-102">SYNOPSIS</span></span>


## <span data-ttu-id="e12ff-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e12ff-103">SYNTAX</span></span>

### <span data-ttu-id="e12ff-104">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="e12ff-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e12ff-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e12ff-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e12ff-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e12ff-106">DESCRIPTION</span></span>


## <span data-ttu-id="e12ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e12ff-107">EXAMPLES</span></span>

### <span data-ttu-id="e12ff-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e12ff-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="e12ff-109">Exclua a assinatura de locatário especificada.</span><span class="sxs-lookup"><span data-stu-id="e12ff-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="e12ff-110">OS</span><span class="sxs-lookup"><span data-stu-id="e12ff-110">PARAMETERS</span></span>

### <span data-ttu-id="e12ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12ff-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="e12ff-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e12ff-112">-Force</span></span>


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

### <span data-ttu-id="e12ff-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e12ff-113">-InputObject</span></span>
<span data-ttu-id="e12ff-114">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e12ff-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e12ff-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e12ff-115">-PassThru</span></span>


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

### <span data-ttu-id="e12ff-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e12ff-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="e12ff-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e12ff-117">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="e12ff-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e12ff-118">-Confirm</span></span>
<span data-ttu-id="e12ff-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e12ff-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e12ff-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12ff-120">-WhatIf</span></span>
<span data-ttu-id="e12ff-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e12ff-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e12ff-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e12ff-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e12ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12ff-123">CommonParameters</span></span>
<span data-ttu-id="e12ff-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12ff-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e12ff-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12ff-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e12ff-126">INPUTS</span></span>

### <span data-ttu-id="e12ff-127">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e12ff-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e12ff-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e12ff-128">OUTPUTS</span></span>

### <span data-ttu-id="e12ff-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e12ff-129">System.Boolean</span></span>

<span data-ttu-id="e12ff-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e12ff-130">ALIASES</span></span>

## <span data-ttu-id="e12ff-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e12ff-131">NOTES</span></span>

<span data-ttu-id="e12ff-132">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e12ff-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e12ff-133">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e12ff-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e12ff-134">INPUTobject <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="e12ff-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="e12ff-135">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="e12ff-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e12ff-136">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="e12ff-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e12ff-137">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e12ff-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e12ff-138">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="e12ff-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e12ff-139">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="e12ff-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e12ff-140">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="e12ff-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e12ff-141">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="e12ff-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e12ff-142">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="e12ff-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e12ff-143">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="e12ff-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e12ff-144">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="e12ff-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e12ff-145">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="e12ff-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e12ff-146">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="e12ff-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e12ff-147">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e12ff-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e12ff-148">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e12ff-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e12ff-149">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="e12ff-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e12ff-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e12ff-150">RELATED LINKS</span></span>

