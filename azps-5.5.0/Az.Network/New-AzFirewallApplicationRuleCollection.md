---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118323"
---
# <span data-ttu-id="248f1-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="248f1-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="248f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="248f1-102">SYNOPSIS</span></span>
<span data-ttu-id="248f1-103">Cria um conjunto de regras do aplicativo Firewall.</span><span class="sxs-lookup"><span data-stu-id="248f1-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="248f1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="248f1-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="248f1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="248f1-105">DESCRIPTION</span></span>
<span data-ttu-id="248f1-106">O **cmdlet New-AzFirewallApplicationRuleCollection** cria um conjunto de Regras de Aplicativo de Firewall.</span><span class="sxs-lookup"><span data-stu-id="248f1-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="248f1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="248f1-107">EXAMPLES</span></span>

### <span data-ttu-id="248f1-108">Exemplo 1: Criar uma coleção com uma regra</span><span class="sxs-lookup"><span data-stu-id="248f1-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="248f1-109">Este exemplo cria uma coleção com uma regra.</span><span class="sxs-lookup"><span data-stu-id="248f1-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="248f1-110">Todo o tráfego que corresponde às condições identificadas no $rule 1 será permitido.</span><span class="sxs-lookup"><span data-stu-id="248f1-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="248f1-111">A primeira regra é para todo o tráfego HTTPS na porta 443 a partir de 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="248f1-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="248f1-112">Se houver outra coleção de regras de aplicativo com prioridade mais alta (número menor) que também corresponde ao tráfego identificado no $rule 1, a ação do conjunto de regras com prioridade mais alta terá efeito.</span><span class="sxs-lookup"><span data-stu-id="248f1-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="248f1-113">Exemplo 2: Adicionar uma regra a uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="248f1-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="248f1-114">Este exemplo cria uma nova coleção de regras de aplicativo com uma regra e adiciona uma segunda regra à coleção de regras usando o método AddRule no objeto de coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="248f1-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="248f1-115">Cada nome de regra em uma determinada coleção de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="248f1-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="248f1-116">Exemplo 3: Obter uma regra de um conjunto de regras</span><span class="sxs-lookup"><span data-stu-id="248f1-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="248f1-117">Este exemplo cria uma nova coleção de regras de aplicativo com uma regra e obtém a regra por nome, método de chamada GetRuleByName no objeto de coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="248f1-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="248f1-118">O nome da regra para o método GetRuleByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="248f1-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="248f1-119">Exemplo 4: Remover uma regra de um conjunto de regras</span><span class="sxs-lookup"><span data-stu-id="248f1-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="248f1-120">Este exemplo cria uma nova coleção de regras de aplicativo com duas regras e remove a primeira regra da coleção de regras por meio do método de chamada RemoveRuleByName no objeto de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="248f1-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="248f1-121">O nome da regra para o método RemoveRuleByName não tem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="248f1-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="248f1-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="248f1-122">PARAMETERS</span></span>

### <span data-ttu-id="248f1-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="248f1-123">-ActionType</span></span>
<span data-ttu-id="248f1-124">A ação da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="248f1-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="248f1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="248f1-125">-DefaultProfile</span></span>
<span data-ttu-id="248f1-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="248f1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="248f1-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="248f1-127">-Name</span></span>
<span data-ttu-id="248f1-128">Especifica o nome desta regra de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="248f1-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="248f1-129">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="248f1-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="248f1-130">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="248f1-130">-Priority</span></span>
<span data-ttu-id="248f1-131">Especifica a prioridade dessa regra.</span><span class="sxs-lookup"><span data-stu-id="248f1-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="248f1-132">Prioridade é um número entre 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="248f1-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="248f1-133">Quanto menor o número, maior será a prioridade.</span><span class="sxs-lookup"><span data-stu-id="248f1-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="248f1-134">-Regra</span><span class="sxs-lookup"><span data-stu-id="248f1-134">-Rule</span></span>
<span data-ttu-id="248f1-135">Especifica a lista de regras a serem agrupadas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="248f1-135">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="248f1-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="248f1-136">-Confirm</span></span>
<span data-ttu-id="248f1-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="248f1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="248f1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="248f1-138">-WhatIf</span></span>
<span data-ttu-id="248f1-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="248f1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="248f1-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="248f1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="248f1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248f1-141">CommonParameters</span></span>
<span data-ttu-id="248f1-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="248f1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248f1-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="248f1-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248f1-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="248f1-144">INPUTS</span></span>

### <span data-ttu-id="248f1-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="248f1-145">None</span></span>

## <span data-ttu-id="248f1-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="248f1-146">OUTPUTS</span></span>

### <span data-ttu-id="248f1-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="248f1-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="248f1-148">Notas</span><span class="sxs-lookup"><span data-stu-id="248f1-148">NOTES</span></span>

## <span data-ttu-id="248f1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="248f1-149">RELATED LINKS</span></span>

[<span data-ttu-id="248f1-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="248f1-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="248f1-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="248f1-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="248f1-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="248f1-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
