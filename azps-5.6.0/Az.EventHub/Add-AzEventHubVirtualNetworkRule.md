---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 098fc29dd518f62b5b813e4698f5a111947eff3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886769"
---
# <span data-ttu-id="5bd34-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5bd34-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="5bd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd34-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd34-103">Adicionar um único VirtualNetworkRule a NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="5bd34-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="5bd34-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5bd34-104">SYNTAX</span></span>

### <span data-ttu-id="5bd34-105">VirtualNetworkRulePropertiesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5bd34-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bd34-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bd34-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bd34-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5bd34-107">DESCRIPTION</span></span>
<span data-ttu-id="5bd34-108">Adicionar um único VirtualNetworkRule a NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="5bd34-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="5bd34-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bd34-109">EXAMPLES</span></span>

### <span data-ttu-id="5bd34-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5bd34-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="5bd34-111">Nome : defaultAction padrão : Permitir Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft.. Eventhub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="5bd34-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="5bd34-112">Adiciona a sub-rede e IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) a NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="5bd34-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="5bd34-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5bd34-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="5bd34-114">Nome : defaultAction padrão : Permitir Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft.. Eventhub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="5bd34-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="5bd34-115">Adiciona o $virtualruleset 1 a NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="5bd34-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="5bd34-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5bd34-116">PARAMETERS</span></span>

### <span data-ttu-id="5bd34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd34-117">-DefaultProfile</span></span>
<span data-ttu-id="5bd34-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd34-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd34-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bd34-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="5bd34-120">ARM ID da Sub-rede</span><span class="sxs-lookup"><span data-stu-id="5bd34-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd34-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5bd34-121">-Name</span></span>
<span data-ttu-id="5bd34-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5bd34-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd34-123">-ResourceGroupName</span></span>
<span data-ttu-id="5bd34-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5bd34-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd34-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5bd34-125">-SubnetId</span></span>
<span data-ttu-id="5bd34-126">ID do Recurso de Sub-rede</span><span class="sxs-lookup"><span data-stu-id="5bd34-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd34-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5bd34-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="5bd34-128">Objeto de configuração VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5bd34-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd34-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bd34-129">-Confirm</span></span>
<span data-ttu-id="5bd34-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bd34-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd34-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd34-131">-WhatIf</span></span>
<span data-ttu-id="5bd34-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5bd34-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd34-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bd34-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd34-134">CommonParameters</span></span>
<span data-ttu-id="5bd34-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5bd34-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bd34-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd34-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bd34-137">INPUTS</span></span>

### <span data-ttu-id="5bd34-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5bd34-138">System.String</span></span>

### <span data-ttu-id="5bd34-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5bd34-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5bd34-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="5bd34-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="5bd34-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5bd34-141">OUTPUTS</span></span>

### <span data-ttu-id="5bd34-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5bd34-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="5bd34-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="5bd34-143">NOTES</span></span>

## <span data-ttu-id="5bd34-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bd34-144">RELATED LINKS</span></span>
