---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116805"
---
# <span data-ttu-id="f7955-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7955-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="f7955-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7955-102">SYNOPSIS</span></span>
<span data-ttu-id="f7955-103">Atualize o NetworkruleSet do namespace determinado na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7955-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f7955-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7955-104">SYNTAX</span></span>

### <span data-ttu-id="f7955-105">NetworkRuleSetPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f7955-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7955-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f7955-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7955-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7955-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7955-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7955-108">DESCRIPTION</span></span>
<span data-ttu-id="f7955-109">Atualize o NetworkruleSet do namespace determinado na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7955-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f7955-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7955-110">EXAMPLES</span></span>

### <span data-ttu-id="f7955-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7955-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="f7955-112">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvgroupst1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="f7955-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="f7955-113">Atualizar o NetworkRuleSet usando os parâmetros -IPRule e -VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f7955-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="f7955-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f7955-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="f7955-115">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvgroupst1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="f7955-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="f7955-116">Atualizar o NetworkRuleSet usando -InputObject</span><span class="sxs-lookup"><span data-stu-id="f7955-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="f7955-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f7955-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="f7955-118">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvgroupst1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="f7955-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="f7955-119">Atualize o NetworkRuleSet usando -ResourceId do outro namespace.</span><span class="sxs-lookup"><span data-stu-id="f7955-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="f7955-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7955-120">PARAMETERS</span></span>

### <span data-ttu-id="f7955-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="f7955-121">-DefaultAction</span></span>
<span data-ttu-id="f7955-122">Ação padrão para NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7955-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7955-123">-DefaultProfile</span></span>
<span data-ttu-id="f7955-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7955-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7955-125">-InputObject</span></span>
<span data-ttu-id="f7955-126">Objeto de configuração networkruleSet</span><span class="sxs-lookup"><span data-stu-id="f7955-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="f7955-127">-IPRule</span></span>
<span data-ttu-id="f7955-128">Lista de IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7955-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7955-129">-Name</span></span>
<span data-ttu-id="f7955-130">Nome do Namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="f7955-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7955-131">-ResourceGroupName</span></span>
<span data-ttu-id="f7955-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7955-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7955-133">-ResourceId</span></span>
<span data-ttu-id="f7955-134">ID do Recurso do Namespace</span><span class="sxs-lookup"><span data-stu-id="f7955-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="f7955-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="f7955-136">Indica se TrustedServiceAccessEnabled está habilitado</span><span class="sxs-lookup"><span data-stu-id="f7955-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f7955-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="f7955-138">Lista de VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="f7955-138">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f7955-139">-Confirm</span></span>
<span data-ttu-id="f7955-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7955-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7955-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7955-141">-WhatIf</span></span>
<span data-ttu-id="f7955-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f7955-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7955-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7955-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7955-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7955-144">CommonParameters</span></span>
<span data-ttu-id="f7955-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7955-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f7955-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7955-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7955-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="f7955-147">INPUTS</span></span>

### <span data-ttu-id="f7955-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f7955-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="f7955-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f7955-149">System.String</span></span>

## <span data-ttu-id="f7955-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="f7955-150">OUTPUTS</span></span>

### <span data-ttu-id="f7955-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f7955-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f7955-152">Notas</span><span class="sxs-lookup"><span data-stu-id="f7955-152">NOTES</span></span>

## <span data-ttu-id="f7955-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7955-153">RELATED LINKS</span></span>