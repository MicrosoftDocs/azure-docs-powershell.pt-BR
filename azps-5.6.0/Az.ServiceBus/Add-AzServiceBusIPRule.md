---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: e0450df003b474cae57319d5450423af58f4d3eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887335"
---
# <span data-ttu-id="c6451-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="c6451-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="c6451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6451-102">SYNOPSIS</span></span>
<span data-ttu-id="c6451-103">Adicionar uma única regra IP ao NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="c6451-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="c6451-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c6451-104">SYNTAX</span></span>

### <span data-ttu-id="c6451-105">IPRulePropertiesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c6451-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6451-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6451-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6451-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c6451-107">DESCRIPTION</span></span>
<span data-ttu-id="c6451-108">Adicionar uma única regra IP ao NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="c6451-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="c6451-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6451-109">EXAMPLES</span></span>

### <span data-ttu-id="c6451-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6451-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="c6451-111">Nome : defaultAction padrão : Permitir Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="c6451-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="c6451-112">adicione o IPRule com IpMask "11.22.33.44" e Action Allow no namespace determinado.</span><span class="sxs-lookup"><span data-stu-id="c6451-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="c6451-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c6451-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="c6451-114">Nome : defaultAction padrão : Permitir Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="c6451-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="c6451-115">adicione o IPRule com IpMask "11.22.33.44" e Action Allow no namespace determinado.</span><span class="sxs-lookup"><span data-stu-id="c6451-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="c6451-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c6451-116">PARAMETERS</span></span>

### <span data-ttu-id="c6451-117">-Action</span><span class="sxs-lookup"><span data-stu-id="c6451-117">-Action</span></span>
<span data-ttu-id="c6451-118">A ação de filtro IP</span><span class="sxs-lookup"><span data-stu-id="c6451-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6451-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6451-119">-DefaultProfile</span></span>
<span data-ttu-id="c6451-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6451-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6451-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="c6451-121">-IpMask</span></span>
<span data-ttu-id="c6451-122">ID do Recurso de Sub-rede</span><span class="sxs-lookup"><span data-stu-id="c6451-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6451-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="c6451-123">-IpRuleObject</span></span>
<span data-ttu-id="c6451-124">Objeto de configuração IPRule a ser adicionado</span><span class="sxs-lookup"><span data-stu-id="c6451-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6451-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c6451-125">-Name</span></span>
<span data-ttu-id="c6451-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c6451-126">Namespace Name</span></span>

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

### <span data-ttu-id="c6451-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6451-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6451-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c6451-128">Resource Group Name</span></span>

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

### <span data-ttu-id="c6451-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6451-129">-Confirm</span></span>
<span data-ttu-id="c6451-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6451-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6451-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6451-131">-WhatIf</span></span>
<span data-ttu-id="c6451-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6451-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6451-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6451-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6451-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6451-134">CommonParameters</span></span>
<span data-ttu-id="c6451-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6451-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c6451-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6451-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6451-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6451-137">INPUTS</span></span>

### <span data-ttu-id="c6451-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c6451-138">System.String</span></span>

### <span data-ttu-id="c6451-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="c6451-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="c6451-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c6451-140">OUTPUTS</span></span>

### <span data-ttu-id="c6451-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="c6451-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="c6451-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="c6451-142">NOTES</span></span>

## <span data-ttu-id="c6451-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6451-143">RELATED LINKS</span></span>