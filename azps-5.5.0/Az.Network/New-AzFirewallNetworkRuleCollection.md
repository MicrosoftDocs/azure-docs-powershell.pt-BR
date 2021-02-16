---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118317"
---
# <span data-ttu-id="f5030-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f5030-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="f5030-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5030-102">SYNOPSIS</span></span>
<span data-ttu-id="f5030-103">Cria um Conjunto de Regras de Rede de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="f5030-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="f5030-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5030-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5030-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5030-105">DESCRIPTION</span></span>
<span data-ttu-id="f5030-106">O **cmdlet New-AzFirewallNetworkRuleCollection** cria um conjunto de Regras de Rede de Firewall.</span><span class="sxs-lookup"><span data-stu-id="f5030-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="f5030-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5030-107">EXAMPLES</span></span>

### <span data-ttu-id="f5030-108">Exemplo 1: Criar um conjunto de rede com duas regras</span><span class="sxs-lookup"><span data-stu-id="f5030-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="f5030-109">Este exemplo cria uma coleção que permitirá todo o tráfego que corresponde a uma das duas regras.</span><span class="sxs-lookup"><span data-stu-id="f5030-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="f5030-110">A primeira regra é para todo o tráfego UDP.</span><span class="sxs-lookup"><span data-stu-id="f5030-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="f5030-111">A segunda regra é para o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="f5030-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="f5030-112">Se houver outra coleção de regras de rede com prioridade mais alta (número menor) que também corresponde ao tráfego identificado no $rule 1 ou $rule 2, a ação do conjunto de regras com prioridade mais alta terá efeito.</span><span class="sxs-lookup"><span data-stu-id="f5030-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="f5030-113">Exemplo 2: Adicionar uma regra a um conjunto de regras</span><span class="sxs-lookup"><span data-stu-id="f5030-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="f5030-114">Este exemplo cria uma nova coleção de regras de rede com uma regra e adiciona uma segunda regra à coleção de regras usando o método AddRule no objeto de coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="f5030-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="f5030-115">Cada nome de regra em uma determinada coleção de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f5030-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="f5030-116">Exemplo 3: Obter uma regra de um conjunto de regras</span><span class="sxs-lookup"><span data-stu-id="f5030-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="f5030-117">Este exemplo cria uma nova coleção de regras de rede com uma regra e obtém a regra por nome, método de chamada GetRuleByName no objeto de coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="f5030-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="f5030-118">O nome da regra para o método GetRuleByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f5030-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="f5030-119">Exemplo 4: Remover uma regra de um conjunto de regras</span><span class="sxs-lookup"><span data-stu-id="f5030-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="f5030-120">Este exemplo cria uma nova coleção de regras de rede com duas regras e remove a primeira regra da coleção de regras por meio do método de chamada RemoveRuleByName no objeto de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="f5030-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="f5030-121">O nome da regra para o método RemoveRuleByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f5030-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="f5030-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5030-122">PARAMETERS</span></span>

### <span data-ttu-id="f5030-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="f5030-123">-ActionType</span></span>
<span data-ttu-id="f5030-124">Especifica a ação a ser tomada para as condições de correspondência de tráfego desta regra.</span><span class="sxs-lookup"><span data-stu-id="f5030-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="f5030-125">As ações aceitas são "Permitir" ou "Negar".</span><span class="sxs-lookup"><span data-stu-id="f5030-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="f5030-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5030-126">-DefaultProfile</span></span>
<span data-ttu-id="f5030-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f5030-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5030-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5030-128">-Name</span></span>
<span data-ttu-id="f5030-129">Especifica o nome desta coleção de regras de rede.</span><span class="sxs-lookup"><span data-stu-id="f5030-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="f5030-130">O nome deve ser exclusivo em toda a coleção de regras de rede.</span><span class="sxs-lookup"><span data-stu-id="f5030-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="f5030-131">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="f5030-131">-Priority</span></span>
<span data-ttu-id="f5030-132">Especifica a prioridade desta coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="f5030-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="f5030-133">Prioridade é um número entre 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="f5030-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="f5030-134">Quanto menor o número, maior será a prioridade.</span><span class="sxs-lookup"><span data-stu-id="f5030-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="f5030-135">-Regra</span><span class="sxs-lookup"><span data-stu-id="f5030-135">-Rule</span></span>
<span data-ttu-id="f5030-136">Especifica a lista de regras a serem agrupadas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="f5030-136">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="f5030-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f5030-137">-Confirm</span></span>
<span data-ttu-id="f5030-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5030-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5030-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5030-139">-WhatIf</span></span>
<span data-ttu-id="f5030-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f5030-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5030-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5030-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5030-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5030-142">CommonParameters</span></span>
<span data-ttu-id="f5030-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5030-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5030-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5030-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5030-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="f5030-145">INPUTS</span></span>

### <span data-ttu-id="f5030-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f5030-146">None</span></span>

## <span data-ttu-id="f5030-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="f5030-147">OUTPUTS</span></span>

### <span data-ttu-id="f5030-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f5030-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="f5030-149">Notas</span><span class="sxs-lookup"><span data-stu-id="f5030-149">NOTES</span></span>

## <span data-ttu-id="f5030-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5030-150">RELATED LINKS</span></span>

[<span data-ttu-id="f5030-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5030-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="f5030-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f5030-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f5030-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f5030-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
