---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: af0a81cf915cd853bfc8ca957d706cdb45d96180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771894"
---
# <span data-ttu-id="73ec2-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73ec2-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="73ec2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="73ec2-103">Cria um conjunto de regras de rede do firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="73ec2-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="73ec2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73ec2-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73ec2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73ec2-105">DESCRIPTION</span></span>
<span data-ttu-id="73ec2-106">O cmdlet **New-AzFirewallNetworkRuleCollection** cria um conjunto de regras de rede de firewall.</span><span class="sxs-lookup"><span data-stu-id="73ec2-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="73ec2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73ec2-107">EXAMPLES</span></span>

### <span data-ttu-id="73ec2-108">1: criar uma coleção de rede com duas regras</span><span class="sxs-lookup"><span data-stu-id="73ec2-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="73ec2-109">Este exemplo cria uma coleção que permitirá todo o tráfego que corresponda a qualquer uma das duas regras.</span><span class="sxs-lookup"><span data-stu-id="73ec2-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="73ec2-110">A primeira regra é para todo o tráfego UDP.</span><span class="sxs-lookup"><span data-stu-id="73ec2-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="73ec2-111">A segunda regra se refere ao tráfego de TCP de 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="73ec2-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="73ec2-112">Se houver outro conjunto de regras de rede com prioridade mais alta (número menor) que também corresponda ao tráfego identificado no $rule 1 ou $rule 2, a ação da coleção de regras com prioridade mais alta terá efeito em vez disso.</span><span class="sxs-lookup"><span data-stu-id="73ec2-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="73ec2-113">2: adicionar uma regra a uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="73ec2-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="73ec2-114">Este exemplo cria um novo conjunto de regras de rede com uma regra e, em seguida, adiciona uma segunda regra à coleção de regras usando addrule no objeto da coleção Rule.</span><span class="sxs-lookup"><span data-stu-id="73ec2-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="73ec2-115">Cada nome de regra em um determinado conjunto de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="73ec2-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="73ec2-116">3: obter uma regra a partir de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="73ec2-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="73ec2-117">Este exemplo cria um novo conjunto de regras de rede com uma regra e, em seguida, obtém a regra por nome, método de chamada GetRuleByName no objeto da coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="73ec2-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="73ec2-118">O nome da regra para o método GetRuleByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="73ec2-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="73ec2-119">4: remover uma regra de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="73ec2-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="73ec2-120">Este exemplo cria um novo conjunto de regras de rede com duas regras e, em seguida, remove a primeira regra da coleção de regras chamando o método RemoveRuleByName no objeto da coleção Rule.</span><span class="sxs-lookup"><span data-stu-id="73ec2-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="73ec2-121">O nome da regra para o método RemoveRuleByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="73ec2-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="73ec2-122">OS</span><span class="sxs-lookup"><span data-stu-id="73ec2-122">PARAMETERS</span></span>

### <span data-ttu-id="73ec2-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="73ec2-123">-ActionType</span></span>
<span data-ttu-id="73ec2-124">Especifica a ação a ser tomada para as condições de correspondência de tráfego dessa regra.</span><span class="sxs-lookup"><span data-stu-id="73ec2-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="73ec2-125">As ações aceitas são "Allow" ou "Deny".</span><span class="sxs-lookup"><span data-stu-id="73ec2-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ec2-126">-DefaultProfile</span></span>
<span data-ttu-id="73ec2-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73ec2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73ec2-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="73ec2-128">-Name</span></span>
<span data-ttu-id="73ec2-129">Especifica o nome da coleção de regras de rede.</span><span class="sxs-lookup"><span data-stu-id="73ec2-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="73ec2-130">O nome deve ser exclusivo em todas as coleções de regras de rede.</span><span class="sxs-lookup"><span data-stu-id="73ec2-130">The name must be unique across all network rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="73ec2-131">-Priority</span></span>
<span data-ttu-id="73ec2-132">Especifica a prioridade dessa coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="73ec2-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="73ec2-133">Priority é um número entre 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="73ec2-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="73ec2-134">Quanto menor o número, maior a prioridade.</span><span class="sxs-lookup"><span data-stu-id="73ec2-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-135">-Regra</span><span class="sxs-lookup"><span data-stu-id="73ec2-135">-Rule</span></span>
<span data-ttu-id="73ec2-136">Especifica a lista de regras a serem agrupadas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="73ec2-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73ec2-137">-Confirm</span></span>
<span data-ttu-id="73ec2-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73ec2-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ec2-139">-WhatIf</span></span>
<span data-ttu-id="73ec2-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73ec2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73ec2-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73ec2-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ec2-142">CommonParameters</span></span>
<span data-ttu-id="73ec2-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73ec2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ec2-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73ec2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ec2-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73ec2-145">INPUTS</span></span>

### <span data-ttu-id="73ec2-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="73ec2-146">None</span></span>

## <span data-ttu-id="73ec2-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73ec2-147">OUTPUTS</span></span>

### <span data-ttu-id="73ec2-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73ec2-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="73ec2-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73ec2-149">NOTES</span></span>

## <span data-ttu-id="73ec2-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73ec2-150">RELATED LINKS</span></span>

[<span data-ttu-id="73ec2-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73ec2-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="73ec2-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73ec2-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="73ec2-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73ec2-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
