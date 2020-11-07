---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 171431e02627177bbb62f64c9a170c02234e0c61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771897"
---
# <span data-ttu-id="bf693-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bf693-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="bf693-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf693-102">SYNOPSIS</span></span>
<span data-ttu-id="bf693-103">Cria uma coleção de regras NAT de firewall.</span><span class="sxs-lookup"><span data-stu-id="bf693-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="bf693-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf693-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf693-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf693-105">DESCRIPTION</span></span>
<span data-ttu-id="bf693-106">O cmdlet **New-AzFirewallNatRuleCollection** cria uma coleção de regras NAT de firewall.</span><span class="sxs-lookup"><span data-stu-id="bf693-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="bf693-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf693-107">EXAMPLES</span></span>

### <span data-ttu-id="bf693-108">1: criar uma coleção com uma regra</span><span class="sxs-lookup"><span data-stu-id="bf693-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="bf693-109">Este exemplo cria uma coleção com uma regra.</span><span class="sxs-lookup"><span data-stu-id="bf693-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="bf693-110">Todo o tráfego que corresponde às condições identificadas em $rule 1 será DNAT'ed para o endereço e a porta traduzidos.</span><span class="sxs-lookup"><span data-stu-id="bf693-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="bf693-111">2: adicionar uma regra a uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="bf693-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="bf693-112">Este exemplo cria uma nova coleção de regras NAT com uma regra e, em seguida, adiciona uma segunda regra à coleção de regras usando addrule no objeto da coleção Rule.</span><span class="sxs-lookup"><span data-stu-id="bf693-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="bf693-113">Cada nome de regra em um determinado conjunto de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bf693-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="bf693-114">3: obter uma regra a partir de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="bf693-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="bf693-115">Este exemplo cria uma nova coleção de regras NAT com uma regra e, em seguida, obtém a regra por nome, método de chamada GetRuleByName no objeto da coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="bf693-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="bf693-116">O nome da regra para o método GetRuleByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bf693-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="bf693-117">4: remover uma regra de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="bf693-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="bf693-118">Este exemplo cria uma nova coleção de regras NAT com duas regras e, em seguida, remove a primeira regra da coleção Rule chamando o método RemoveRuleByName no objeto da coleção Rule.</span><span class="sxs-lookup"><span data-stu-id="bf693-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="bf693-119">O nome da regra para o método RemoveRuleByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bf693-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="bf693-120">OS</span><span class="sxs-lookup"><span data-stu-id="bf693-120">PARAMETERS</span></span>

### <span data-ttu-id="bf693-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf693-121">-DefaultProfile</span></span>
<span data-ttu-id="bf693-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf693-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf693-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf693-123">-Name</span></span>
<span data-ttu-id="bf693-124">Especifica o nome da regra NAT.</span><span class="sxs-lookup"><span data-stu-id="bf693-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="bf693-125">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="bf693-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="bf693-126">-Priority</span><span class="sxs-lookup"><span data-stu-id="bf693-126">-Priority</span></span>
<span data-ttu-id="bf693-127">Especifica a prioridade dessa regra.</span><span class="sxs-lookup"><span data-stu-id="bf693-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="bf693-128">Priority é um número entre 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="bf693-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="bf693-129">Quanto menor o número, maior a prioridade.</span><span class="sxs-lookup"><span data-stu-id="bf693-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="bf693-130">-Regra</span><span class="sxs-lookup"><span data-stu-id="bf693-130">-Rule</span></span>
<span data-ttu-id="bf693-131">Especifica a lista de regras a serem agrupadas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="bf693-131">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="bf693-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf693-132">-Confirm</span></span>
<span data-ttu-id="bf693-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf693-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf693-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf693-134">-WhatIf</span></span>
<span data-ttu-id="bf693-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf693-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf693-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf693-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf693-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf693-137">CommonParameters</span></span>
<span data-ttu-id="bf693-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf693-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf693-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf693-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf693-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf693-140">INPUTS</span></span>

### <span data-ttu-id="bf693-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bf693-141">None</span></span>

## <span data-ttu-id="bf693-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf693-142">OUTPUTS</span></span>

### <span data-ttu-id="bf693-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bf693-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="bf693-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf693-144">NOTES</span></span>

## <span data-ttu-id="bf693-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf693-145">RELATED LINKS</span></span>

[<span data-ttu-id="bf693-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="bf693-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="bf693-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bf693-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="bf693-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bf693-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)