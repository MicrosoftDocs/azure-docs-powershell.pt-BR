---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplan
schema: 2.0.0
ms.openlocfilehash: fca0ab39b587bea05228da3a053fd1575b3e7e98
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945253"
---
# <span data-ttu-id="02753-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="02753-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="02753-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02753-102">SYNOPSIS</span></span>
<span data-ttu-id="02753-103">Excluir o plano especificado.</span><span class="sxs-lookup"><span data-stu-id="02753-103">Delete the specified plan.</span></span>

## <span data-ttu-id="02753-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02753-104">SYNTAX</span></span>

### <span data-ttu-id="02753-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="02753-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02753-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="02753-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02753-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02753-107">DESCRIPTION</span></span>
<span data-ttu-id="02753-108">Excluir o plano especificado.</span><span class="sxs-lookup"><span data-stu-id="02753-108">Delete the specified plan.</span></span>

## <span data-ttu-id="02753-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02753-109">EXAMPLES</span></span>

### <span data-ttu-id="02753-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02753-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

```

<span data-ttu-id="02753-111">Excluir o plano especificado</span><span class="sxs-lookup"><span data-stu-id="02753-111">Delete the specified plan</span></span>

## <span data-ttu-id="02753-112">OS</span><span class="sxs-lookup"><span data-stu-id="02753-112">PARAMETERS</span></span>

### <span data-ttu-id="02753-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02753-113">-DefaultProfile</span></span>
<span data-ttu-id="02753-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02753-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02753-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02753-115">-InputObject</span></span>
<span data-ttu-id="02753-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="02753-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="02753-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="02753-117">-Name</span></span>
<span data-ttu-id="02753-118">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="02753-118">Name of the plan.</span></span>

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

### <span data-ttu-id="02753-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02753-119">-PassThru</span></span>
<span data-ttu-id="02753-120">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="02753-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="02753-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02753-121">-ResourceGroupName</span></span>
<span data-ttu-id="02753-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="02753-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="02753-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02753-123">-SubscriptionId</span></span>
<span data-ttu-id="02753-124">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="02753-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="02753-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02753-125">-Confirm</span></span>
<span data-ttu-id="02753-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02753-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02753-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02753-127">-WhatIf</span></span>
<span data-ttu-id="02753-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02753-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02753-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02753-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02753-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02753-130">CommonParameters</span></span>
<span data-ttu-id="02753-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02753-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02753-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02753-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02753-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02753-133">INPUTS</span></span>

### <span data-ttu-id="02753-134">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="02753-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="02753-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02753-135">OUTPUTS</span></span>

### <span data-ttu-id="02753-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02753-136">System.Boolean</span></span>

<span data-ttu-id="02753-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="02753-137">ALIASES</span></span>

## <span data-ttu-id="02753-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02753-138">NOTES</span></span>

<span data-ttu-id="02753-139">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="02753-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02753-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02753-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="02753-141">INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="02753-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02753-142">`[DelegatedProvider <String>]`: Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="02753-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="02753-143">`[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="02753-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="02753-144">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="02753-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02753-145">`[Location <String>]`: O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="02753-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="02753-146">`[ManifestName <String>]`: O nome do manifesto.</span><span class="sxs-lookup"><span data-stu-id="02753-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="02753-147">`[Offer <String>]`: Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="02753-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="02753-148">`[OfferDelegationName <String>]`: Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="02753-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="02753-149">`[OperationsStatusName <String>]`: O nome do status da operação.</span><span class="sxs-lookup"><span data-stu-id="02753-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="02753-150">`[Plan <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="02753-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="02753-151">`[PlanAcquisitionId <String>]`: O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="02753-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="02753-152">`[Quota <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="02753-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="02753-153">`[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="02753-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="02753-154">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="02753-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="02753-155">`[TargetSubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="02753-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="02753-156">`[Tenant <String>]`: Nome do locatário do diretório.</span><span class="sxs-lookup"><span data-stu-id="02753-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="02753-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02753-157">RELATED LINKS</span></span>

