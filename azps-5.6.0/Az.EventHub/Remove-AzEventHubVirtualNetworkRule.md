---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 3d8221d36cdd6ec0845f3f26dfe1526f796c2213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890278"
---
# <span data-ttu-id="ded53-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ded53-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="ded53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ded53-102">SYNOPSIS</span></span>
<span data-ttu-id="ded53-103">Remove a única VirtualNetworkRule determinada para NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="ded53-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="ded53-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ded53-104">SYNTAX</span></span>

### <span data-ttu-id="ded53-105">VirtualNetworkRulePropertiesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ded53-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ded53-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ded53-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ded53-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ded53-107">DESCRIPTION</span></span>
<span data-ttu-id="ded53-108">Remove a única VirtualNetworkRule determinada para NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="ded53-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="ded53-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ded53-109">EXAMPLES</span></span>

### <span data-ttu-id="ded53-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ded53-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="ded53-111">Remove a única VirtualNetworkRule determinada para NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="ded53-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="ded53-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ded53-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="ded53-113">Remover o $virtualruleset 1 de NetworkRuleSet para o namespace determinado</span><span class="sxs-lookup"><span data-stu-id="ded53-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="ded53-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ded53-114">PARAMETERS</span></span>

### <span data-ttu-id="ded53-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ded53-115">-AsJob</span></span>
<span data-ttu-id="ded53-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ded53-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ded53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded53-117">-DefaultProfile</span></span>
<span data-ttu-id="ded53-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ded53-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ded53-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ded53-119">-Name</span></span>
<span data-ttu-id="ded53-120">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ded53-120">Namespace Name</span></span>

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

### <span data-ttu-id="ded53-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ded53-121">-PassThru</span></span>
<span data-ttu-id="ded53-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ded53-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ded53-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded53-123">-ResourceGroupName</span></span>
<span data-ttu-id="ded53-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ded53-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ded53-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ded53-125">-SubnetId</span></span>
<span data-ttu-id="ded53-126">ID do Recurso de Sub-rede</span><span class="sxs-lookup"><span data-stu-id="ded53-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="ded53-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ded53-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="ded53-128">Objeto de configuração IPRule</span><span class="sxs-lookup"><span data-stu-id="ded53-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="ded53-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ded53-129">-Confirm</span></span>
<span data-ttu-id="ded53-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ded53-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ded53-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ded53-131">-WhatIf</span></span>
<span data-ttu-id="ded53-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ded53-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ded53-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ded53-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ded53-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded53-134">CommonParameters</span></span>
<span data-ttu-id="ded53-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded53-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ded53-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded53-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded53-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ded53-137">INPUTS</span></span>

### <span data-ttu-id="ded53-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ded53-138">System.String</span></span>

### <span data-ttu-id="ded53-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ded53-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="ded53-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ded53-140">OUTPUTS</span></span>

### <span data-ttu-id="ded53-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ded53-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ded53-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="ded53-142">NOTES</span></span>

## <span data-ttu-id="ded53-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ded53-143">RELATED LINKS</span></span>