---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: d637767f21a34daf5afaf1f2a44e9ebc9b80934a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890999"
---
# <span data-ttu-id="a8efd-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a8efd-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="a8efd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8efd-102">SYNOPSIS</span></span>
<span data-ttu-id="a8efd-103">Cria uma coleção de regras NAT do Firewall.</span><span class="sxs-lookup"><span data-stu-id="a8efd-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="a8efd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a8efd-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8efd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a8efd-105">DESCRIPTION</span></span>
<span data-ttu-id="a8efd-106">O cmdlet **New-AzFirewallNatRuleCollection** cria uma coleção de Regras NAT do Firewall.</span><span class="sxs-lookup"><span data-stu-id="a8efd-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="a8efd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8efd-107">EXAMPLES</span></span>

### <span data-ttu-id="a8efd-108">Exemplo 1: Criar uma coleção com uma regra</span><span class="sxs-lookup"><span data-stu-id="a8efd-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="a8efd-109">Este exemplo cria uma coleção com uma regra.</span><span class="sxs-lookup"><span data-stu-id="a8efd-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="a8efd-110">Todo o tráfego que corresponde às condições identificadas $rule 1 será DNAT'ed para endereço e porta traduzidos.</span><span class="sxs-lookup"><span data-stu-id="a8efd-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="a8efd-111">Exemplo 2: Adicionar uma regra a uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="a8efd-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="a8efd-112">Este exemplo cria uma nova coleção de regras NAT com uma regra e adiciona uma segunda regra à coleção de regras usando o método AddRule no objeto da coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="a8efd-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="a8efd-113">Cada nome de regra em uma determinada coleção de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a8efd-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="a8efd-114">Exemplo 3: Obter uma regra de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="a8efd-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="a8efd-115">Este exemplo cria uma nova coleção de regras NAT com uma regra e obtém a regra por nome, o método de chamada GetRuleByName no objeto da coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="a8efd-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="a8efd-116">O nome da regra do método GetRuleByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a8efd-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="a8efd-117">Exemplo 4: Remover uma regra de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="a8efd-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="a8efd-118">Este exemplo cria uma nova coleção de regras NAT com duas regras e remove a primeira regra da coleção de regras chamando o método RemoveRuleByName no objeto da coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="a8efd-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="a8efd-119">O nome da regra do método RemoveRuleByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a8efd-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="a8efd-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a8efd-120">PARAMETERS</span></span>

### <span data-ttu-id="a8efd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8efd-121">-DefaultProfile</span></span>
<span data-ttu-id="a8efd-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a8efd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8efd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a8efd-123">-Name</span></span>
<span data-ttu-id="a8efd-124">Especifica o nome dessa regra NAT.</span><span class="sxs-lookup"><span data-stu-id="a8efd-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="a8efd-125">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="a8efd-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="a8efd-126">-Priority</span><span class="sxs-lookup"><span data-stu-id="a8efd-126">-Priority</span></span>
<span data-ttu-id="a8efd-127">Especifica a prioridade dessa regra.</span><span class="sxs-lookup"><span data-stu-id="a8efd-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="a8efd-128">Prioridade é um número entre 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="a8efd-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="a8efd-129">Quanto menor o número, maior será a prioridade.</span><span class="sxs-lookup"><span data-stu-id="a8efd-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="a8efd-130">-Rule</span><span class="sxs-lookup"><span data-stu-id="a8efd-130">-Rule</span></span>
<span data-ttu-id="a8efd-131">Especifica a lista de regras a serem agrupadas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="a8efd-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8efd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8efd-132">-Confirm</span></span>
<span data-ttu-id="a8efd-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8efd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8efd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8efd-134">-WhatIf</span></span>
<span data-ttu-id="a8efd-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8efd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8efd-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8efd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8efd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8efd-137">CommonParameters</span></span>
<span data-ttu-id="a8efd-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8efd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8efd-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8efd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8efd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8efd-140">INPUTS</span></span>

### <span data-ttu-id="a8efd-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8efd-141">None</span></span>

## <span data-ttu-id="a8efd-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a8efd-142">OUTPUTS</span></span>

### <span data-ttu-id="a8efd-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a8efd-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="a8efd-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="a8efd-144">NOTES</span></span>

## <span data-ttu-id="a8efd-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8efd-145">RELATED LINKS</span></span>

[<span data-ttu-id="a8efd-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="a8efd-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="a8efd-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a8efd-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a8efd-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a8efd-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
