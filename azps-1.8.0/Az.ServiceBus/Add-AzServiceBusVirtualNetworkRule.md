---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 22389580fba26f977226452037a42d948f957440
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599217"
---
# <span data-ttu-id="931aa-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="931aa-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="931aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="931aa-102">SYNOPSIS</span></span>
<span data-ttu-id="931aa-103">Adicionar um único VirtualNetworkRule ao NetworkRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="931aa-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="931aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="931aa-104">SYNTAX</span></span>

### <span data-ttu-id="931aa-105">VirtualNetworkRulePropertiesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="931aa-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="931aa-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="931aa-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="931aa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="931aa-107">DESCRIPTION</span></span>
<span data-ttu-id="931aa-108">Adicionar um único VirtualNetworkRule ao NetworkRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="931aa-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="931aa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="931aa-109">EXAMPLES</span></span>

### <span data-ttu-id="931aa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="931aa-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="931aa-111">Nome: DefaultAction padrão: allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="931aa-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="931aa-112">Adiciona a sub-rede e IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) determinada ao NetworkRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="931aa-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="931aa-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="931aa-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="931aa-114">Nome: DefaultAction padrão: allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="931aa-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="931aa-115">Adiciona o $virtualruleset 1 a NetworkRuleSet para o namespace fornecido</span><span class="sxs-lookup"><span data-stu-id="931aa-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="931aa-116">OS</span><span class="sxs-lookup"><span data-stu-id="931aa-116">PARAMETERS</span></span>

### <span data-ttu-id="931aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931aa-117">-DefaultProfile</span></span>
<span data-ttu-id="931aa-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="931aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="931aa-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="931aa-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="931aa-120">ID do braço da sub-rede</span><span class="sxs-lookup"><span data-stu-id="931aa-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="931aa-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="931aa-121">-Name</span></span>
<span data-ttu-id="931aa-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="931aa-122">Namespace Name</span></span>

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

### <span data-ttu-id="931aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="931aa-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="931aa-124">Resource Group Name</span></span>

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

### <span data-ttu-id="931aa-125">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="931aa-125">-SubnetId</span></span>
<span data-ttu-id="931aa-126">ID do recurso de sub-rede</span><span class="sxs-lookup"><span data-stu-id="931aa-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="931aa-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="931aa-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="931aa-128">Objeto de configuração VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="931aa-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="931aa-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="931aa-129">-Confirm</span></span>
<span data-ttu-id="931aa-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="931aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="931aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="931aa-131">-WhatIf</span></span>
<span data-ttu-id="931aa-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="931aa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="931aa-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="931aa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="931aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931aa-134">CommonParameters</span></span>
<span data-ttu-id="931aa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="931aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="931aa-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="931aa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931aa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="931aa-137">INPUTS</span></span>

### <span data-ttu-id="931aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="931aa-138">System.String</span></span>

### <span data-ttu-id="931aa-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="931aa-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="931aa-140">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="931aa-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="931aa-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="931aa-141">OUTPUTS</span></span>

### <span data-ttu-id="931aa-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="931aa-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="931aa-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="931aa-143">NOTES</span></span>

## <span data-ttu-id="931aa-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="931aa-144">RELATED LINKS</span></span>