---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948280"
---
# <span data-ttu-id="205ce-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="205ce-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="205ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="205ce-102">SYNOPSIS</span></span>
<span data-ttu-id="205ce-103">Atualize o NetworkruleSet do namespace fornecido na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="205ce-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="205ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="205ce-104">SYNTAX</span></span>

### <span data-ttu-id="205ce-105">NetworkRuleSetPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="205ce-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205ce-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="205ce-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="205ce-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="205ce-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205ce-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="205ce-108">DESCRIPTION</span></span>
<span data-ttu-id="205ce-109">Atualize o NetworkruleSet do namespace fornecido na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="205ce-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="205ce-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="205ce-110">EXAMPLES</span></span>

### <span data-ttu-id="205ce-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="205ce-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="205ce-112">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="205ce-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="205ce-113">Atualize os parâmetros NetworkRuleSet using-IPRule e-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="205ce-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="205ce-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="205ce-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="205ce-115">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="205ce-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="205ce-116">Atualize o NetworkRuleSet usando-InputObject</span><span class="sxs-lookup"><span data-stu-id="205ce-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="205ce-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="205ce-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="205ce-118">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="205ce-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="205ce-119">Atualize o NetworkRuleSet using-ResourceId do outro namespace.</span><span class="sxs-lookup"><span data-stu-id="205ce-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="205ce-120">OS</span><span class="sxs-lookup"><span data-stu-id="205ce-120">PARAMETERS</span></span>

### <span data-ttu-id="205ce-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="205ce-121">-DefaultAction</span></span>
<span data-ttu-id="205ce-122">Ação padrão para NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="205ce-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="205ce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205ce-123">-DefaultProfile</span></span>
<span data-ttu-id="205ce-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="205ce-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205ce-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="205ce-125">-InputObject</span></span>
<span data-ttu-id="205ce-126">Objeto de configuração NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="205ce-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="205ce-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="205ce-127">-IPRule</span></span>
<span data-ttu-id="205ce-128">Lista de IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="205ce-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="205ce-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="205ce-129">-Name</span></span>
<span data-ttu-id="205ce-130">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="205ce-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="205ce-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205ce-131">-ResourceGroupName</span></span>
<span data-ttu-id="205ce-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="205ce-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="205ce-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="205ce-133">-ResourceId</span></span>
<span data-ttu-id="205ce-134">ID do recurso do namespace</span><span class="sxs-lookup"><span data-stu-id="205ce-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="205ce-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="205ce-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="205ce-136">Indica se o TrustedServiceAccessEnabled está habilitado</span><span class="sxs-lookup"><span data-stu-id="205ce-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

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

### <span data-ttu-id="205ce-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="205ce-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="205ce-138">Lista de VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="205ce-138">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="205ce-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="205ce-139">-Confirm</span></span>
<span data-ttu-id="205ce-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="205ce-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205ce-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205ce-141">-WhatIf</span></span>
<span data-ttu-id="205ce-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="205ce-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205ce-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="205ce-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205ce-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205ce-144">CommonParameters</span></span>
<span data-ttu-id="205ce-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205ce-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="205ce-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205ce-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205ce-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="205ce-147">INPUTS</span></span>

### <span data-ttu-id="205ce-148">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="205ce-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="205ce-149">System. String</span><span class="sxs-lookup"><span data-stu-id="205ce-149">System.String</span></span>

## <span data-ttu-id="205ce-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="205ce-150">OUTPUTS</span></span>

### <span data-ttu-id="205ce-151">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="205ce-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="205ce-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="205ce-152">NOTES</span></span>

## <span data-ttu-id="205ce-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="205ce-153">RELATED LINKS</span></span>