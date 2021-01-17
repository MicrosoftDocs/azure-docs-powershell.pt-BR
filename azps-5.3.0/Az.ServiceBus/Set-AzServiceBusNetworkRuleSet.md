---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 87f735a098057beb67b76fd4a0f763732c2e816a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433096"
---
# <span data-ttu-id="a15bd-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a15bd-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="a15bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a15bd-102">SYNOPSIS</span></span>
<span data-ttu-id="a15bd-103">Atualize o NetworkruleSet do namespace fornecido na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a15bd-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="a15bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a15bd-104">SYNTAX</span></span>

### <span data-ttu-id="a15bd-105">NetworkRuleSetPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a15bd-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a15bd-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a15bd-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a15bd-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a15bd-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a15bd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a15bd-108">DESCRIPTION</span></span>
<span data-ttu-id="a15bd-109">Atualize o NetwrokruleSet do namespace fornecido na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a15bd-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="a15bd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a15bd-110">EXAMPLES</span></span>

### <span data-ttu-id="a15bd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a15bd-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="a15bd-112">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default tipo: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="a15bd-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a15bd-113">Atualize os parâmetros NetworkRuleSet using-IPRule e-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a15bd-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="a15bd-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a15bd-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="a15bd-115">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default tipo: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="a15bd-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a15bd-116">Atualize o NetworkRuleSet usando-InputObject</span><span class="sxs-lookup"><span data-stu-id="a15bd-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="a15bd-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a15bd-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="a15bd-118">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default tipo: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="a15bd-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a15bd-119">Atualize o NetworkRuleSet using-ResourceId do outro namespace.</span><span class="sxs-lookup"><span data-stu-id="a15bd-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="a15bd-120">OS</span><span class="sxs-lookup"><span data-stu-id="a15bd-120">PARAMETERS</span></span>

### <span data-ttu-id="a15bd-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="a15bd-121">-DefaultAction</span></span>
<span data-ttu-id="a15bd-122">Ação padrão para NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a15bd-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="a15bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a15bd-123">-DefaultProfile</span></span>
<span data-ttu-id="a15bd-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a15bd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a15bd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a15bd-125">-InputObject</span></span>
<span data-ttu-id="a15bd-126">Objeto de configuração NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="a15bd-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a15bd-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="a15bd-127">-IPRule</span></span>
<span data-ttu-id="a15bd-128">Lista de IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="a15bd-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a15bd-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="a15bd-129">-Name</span></span>
<span data-ttu-id="a15bd-130">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="a15bd-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="a15bd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a15bd-131">-ResourceGroupName</span></span>
<span data-ttu-id="a15bd-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a15bd-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="a15bd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a15bd-133">-ResourceId</span></span>
<span data-ttu-id="a15bd-134">ID do recurso do namespace</span><span class="sxs-lookup"><span data-stu-id="a15bd-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="a15bd-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a15bd-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="a15bd-136">Lista de VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="a15bd-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a15bd-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a15bd-137">-Confirm</span></span>
<span data-ttu-id="a15bd-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a15bd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a15bd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a15bd-139">-WhatIf</span></span>
<span data-ttu-id="a15bd-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a15bd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a15bd-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a15bd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a15bd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a15bd-142">CommonParameters</span></span>
<span data-ttu-id="a15bd-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a15bd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a15bd-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a15bd-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a15bd-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a15bd-145">INPUTS</span></span>

### <span data-ttu-id="a15bd-146">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a15bd-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="a15bd-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a15bd-147">System.String</span></span>

## <span data-ttu-id="a15bd-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a15bd-148">OUTPUTS</span></span>

### <span data-ttu-id="a15bd-149">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a15bd-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a15bd-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a15bd-150">NOTES</span></span>

## <span data-ttu-id="a15bd-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a15bd-151">RELATED LINKS</span></span>