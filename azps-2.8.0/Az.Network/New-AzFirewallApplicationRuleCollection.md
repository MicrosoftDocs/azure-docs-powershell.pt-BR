---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 2c88e38bba0b4242ff0b268936fbe246214d1921
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771896"
---
# <span data-ttu-id="b1d9e-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1d9e-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="b1d9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d9e-103">Cria uma coleção de regras de aplicativos de firewall.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="b1d9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1d9e-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1d9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d9e-106">O cmdlet **New-AzFirewallApplicationRuleCollection** cria uma coleção de regras de aplicativos de firewall.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="b1d9e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d9e-108">1: criar uma coleção com uma regra</span><span class="sxs-lookup"><span data-stu-id="b1d9e-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="b1d9e-109">Este exemplo cria uma coleção com uma regra.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="b1d9e-110">Todo o tráfego que corresponde às condições identificadas em $rule 1 será permitido.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="b1d9e-111">A primeira regra é para todo o tráfego HTTPS na porta 443 de 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="b1d9e-112">Se houver outro conjunto de regras de aplicativo com prioridade mais alta (número menor) que também corresponda ao tráfego identificado no $rule 1, a ação da coleção de regras com prioridade mais alta terá efeito em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="b1d9e-113">2: adicionar uma regra a uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="b1d9e-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="b1d9e-114">Este exemplo cria uma nova coleção de regras de aplicativo com uma regra e, em seguida, adiciona uma segunda regra à coleção de regras usando addrule no objeto da coleção Rule.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="b1d9e-115">Cada nome de regra em um determinado conjunto de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="b1d9e-116">3: obter uma regra a partir de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="b1d9e-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="b1d9e-117">Este exemplo cria um novo conjunto de regras de aplicativo com uma regra e, em seguida, obtém a regra por nome, método de chamada GetRuleByName no objeto da coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="b1d9e-118">O nome da regra para o método GetRuleByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="b1d9e-119">4: remover uma regra de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="b1d9e-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="b1d9e-120">Este exemplo cria um novo conjunto de regras de aplicativo com duas regras e, em seguida, remove a primeira regra da coleção de regras chamando o método RemoveRuleByName no objeto da coleção Rule.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="b1d9e-121">O nome da regra para o método RemoveRuleByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="b1d9e-122">OS</span><span class="sxs-lookup"><span data-stu-id="b1d9e-122">PARAMETERS</span></span>

### <span data-ttu-id="b1d9e-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="b1d9e-123">-ActionType</span></span>
<span data-ttu-id="b1d9e-124">A ação da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="b1d9e-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="b1d9e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d9e-125">-DefaultProfile</span></span>
<span data-ttu-id="b1d9e-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1d9e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1d9e-127">-Name</span></span>
<span data-ttu-id="b1d9e-128">Especifica o nome desta regra de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="b1d9e-129">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="b1d9e-130">-Priority</span><span class="sxs-lookup"><span data-stu-id="b1d9e-130">-Priority</span></span>
<span data-ttu-id="b1d9e-131">Especifica a prioridade dessa regra.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="b1d9e-132">Priority é um número entre 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="b1d9e-133">Quanto menor o número, maior a prioridade.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="b1d9e-134">-Regra</span><span class="sxs-lookup"><span data-stu-id="b1d9e-134">-Rule</span></span>
<span data-ttu-id="b1d9e-135">Especifica a lista de regras a serem agrupadas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d9e-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1d9e-136">-Confirm</span></span>
<span data-ttu-id="b1d9e-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1d9e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1d9e-138">-WhatIf</span></span>
<span data-ttu-id="b1d9e-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1d9e-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1d9e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d9e-141">CommonParameters</span></span>
<span data-ttu-id="b1d9e-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d9e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d9e-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d9e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d9e-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1d9e-144">INPUTS</span></span>

### <span data-ttu-id="b1d9e-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b1d9e-145">None</span></span>

## <span data-ttu-id="b1d9e-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1d9e-146">OUTPUTS</span></span>

### <span data-ttu-id="b1d9e-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1d9e-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="b1d9e-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1d9e-148">NOTES</span></span>

## <span data-ttu-id="b1d9e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1d9e-149">RELATED LINKS</span></span>

[<span data-ttu-id="b1d9e-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b1d9e-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="b1d9e-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1d9e-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b1d9e-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1d9e-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
