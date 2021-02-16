---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126978"
---
# <span data-ttu-id="7cf28-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7cf28-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="7cf28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cf28-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf28-103">Adicionar uma única VirtualNetworkRule ao NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="7cf28-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="7cf28-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cf28-104">SYNTAX</span></span>

### <span data-ttu-id="7cf28-105">VirtualNetworkRulePropertiesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7cf28-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cf28-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf28-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf28-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cf28-107">DESCRIPTION</span></span>
<span data-ttu-id="7cf28-108">Adicionar uma única VirtualNetworkRule ao NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="7cf28-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="7cf28-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7cf28-109">EXAMPLES</span></span>

### <span data-ttu-id="7cf28-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7cf28-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="7cf28-111">Nome : DefaultAction padrão: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="7cf28-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="7cf28-112">Adiciona a sub-rede e IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) ao NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="7cf28-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="7cf28-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7cf28-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="7cf28-114">Nome : DefaultAction padrão: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="7cf28-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="7cf28-115">Adiciona o $virtualruleset 1 ao NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="7cf28-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="7cf28-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cf28-116">PARAMETERS</span></span>

### <span data-ttu-id="7cf28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf28-117">-DefaultProfile</span></span>
<span data-ttu-id="7cf28-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf28-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cf28-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="7cf28-120">ID arm da Sub-rede</span><span class="sxs-lookup"><span data-stu-id="7cf28-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="7cf28-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cf28-121">-Name</span></span>
<span data-ttu-id="7cf28-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7cf28-122">Namespace Name</span></span>

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

### <span data-ttu-id="7cf28-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf28-123">-ResourceGroupName</span></span>
<span data-ttu-id="7cf28-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7cf28-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7cf28-125">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="7cf28-125">-SubnetId</span></span>
<span data-ttu-id="7cf28-126">ID do Recurso da Sub-rede</span><span class="sxs-lookup"><span data-stu-id="7cf28-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="7cf28-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="7cf28-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="7cf28-128">Objeto de configuração VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7cf28-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="7cf28-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7cf28-129">-Confirm</span></span>
<span data-ttu-id="7cf28-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf28-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf28-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf28-131">-WhatIf</span></span>
<span data-ttu-id="7cf28-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7cf28-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf28-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7cf28-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf28-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf28-134">CommonParameters</span></span>
<span data-ttu-id="7cf28-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf28-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7cf28-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf28-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf28-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="7cf28-137">INPUTS</span></span>

### <span data-ttu-id="7cf28-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7cf28-138">System.String</span></span>

### <span data-ttu-id="7cf28-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7cf28-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7cf28-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7cf28-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="7cf28-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="7cf28-141">OUTPUTS</span></span>

### <span data-ttu-id="7cf28-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="7cf28-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="7cf28-143">Notas</span><span class="sxs-lookup"><span data-stu-id="7cf28-143">NOTES</span></span>

## <span data-ttu-id="7cf28-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cf28-144">RELATED LINKS</span></span>
