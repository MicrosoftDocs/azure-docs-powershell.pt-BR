---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: df7cf094482f849782d6570b0df1af8cbadb7077
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599218"
---
# <span data-ttu-id="00811-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="00811-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="00811-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00811-102">SYNOPSIS</span></span>
<span data-ttu-id="00811-103">Adicionar um único IPrule ao NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="00811-103">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="00811-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00811-104">SYNTAX</span></span>

### <span data-ttu-id="00811-105">IPRulePropertiesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="00811-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00811-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00811-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00811-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00811-107">DESCRIPTION</span></span>
<span data-ttu-id="00811-108">Adicionar um único IPrule ao NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="00811-108">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="00811-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00811-109">EXAMPLES</span></span>

### <span data-ttu-id="00811-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00811-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="00811-111">Nome: DefaultAction padrão: allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="00811-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="00811-112">Adicione o IPRule com IpMask "11.22.33.44" e a ação permita para o namesapce fornecido.</span><span class="sxs-lookup"><span data-stu-id="00811-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namesapce.</span></span>

### <span data-ttu-id="00811-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="00811-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="00811-114">Nome: DefaultAction padrão: allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="00811-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="00811-115">Adicione o IPRule com IpMask "11.22.33.44" e a ação permita para o namesapce fornecido.</span><span class="sxs-lookup"><span data-stu-id="00811-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namesapce.</span></span>

## <span data-ttu-id="00811-116">OS</span><span class="sxs-lookup"><span data-stu-id="00811-116">PARAMETERS</span></span>

### <span data-ttu-id="00811-117">-Ação</span><span class="sxs-lookup"><span data-stu-id="00811-117">-Action</span></span>
<span data-ttu-id="00811-118">A ação de filtro IP</span><span class="sxs-lookup"><span data-stu-id="00811-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="00811-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00811-119">-DefaultProfile</span></span>
<span data-ttu-id="00811-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00811-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00811-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="00811-121">-IpMask</span></span>
<span data-ttu-id="00811-122">ID do recurso de sub-rede</span><span class="sxs-lookup"><span data-stu-id="00811-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="00811-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="00811-123">-IpRuleObject</span></span>
<span data-ttu-id="00811-124">Objeto de configuração IPRule a ser adicionado</span><span class="sxs-lookup"><span data-stu-id="00811-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="00811-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="00811-125">-Name</span></span>
<span data-ttu-id="00811-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="00811-126">Namespace Name</span></span>

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

### <span data-ttu-id="00811-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00811-127">-ResourceGroupName</span></span>
<span data-ttu-id="00811-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="00811-128">Resource Group Name</span></span>

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

### <span data-ttu-id="00811-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00811-129">-Confirm</span></span>
<span data-ttu-id="00811-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00811-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00811-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00811-131">-WhatIf</span></span>
<span data-ttu-id="00811-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00811-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00811-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00811-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00811-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00811-134">CommonParameters</span></span>
<span data-ttu-id="00811-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00811-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="00811-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00811-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00811-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00811-137">INPUTS</span></span>

### <span data-ttu-id="00811-138">System. String</span><span class="sxs-lookup"><span data-stu-id="00811-138">System.String</span></span>

### <span data-ttu-id="00811-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="00811-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="00811-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00811-140">OUTPUTS</span></span>

### <span data-ttu-id="00811-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="00811-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="00811-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00811-142">NOTES</span></span>

## <span data-ttu-id="00811-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00811-143">RELATED LINKS</span></span>