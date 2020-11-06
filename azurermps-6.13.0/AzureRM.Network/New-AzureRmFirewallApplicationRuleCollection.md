---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
ms.openlocfilehash: e5fbad2b63213af972260948439984754e9eaa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610557"
---
# <span data-ttu-id="aad43-101">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="aad43-101">New-AzureRmFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="aad43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aad43-102">SYNOPSIS</span></span>
<span data-ttu-id="aad43-103">Cria uma coleção de regras de aplicativos de firewall.</span><span class="sxs-lookup"><span data-stu-id="aad43-103">Creates a collection of Firewall application rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aad43-104">SYNTAX</span></span>

```
New-AzureRmFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad43-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aad43-105">DESCRIPTION</span></span>
<span data-ttu-id="aad43-106">O cmdlet **New-AzureRmFirewallApplicationRuleCollection** cria uma coleção de regras de aplicativos de firewall.</span><span class="sxs-lookup"><span data-stu-id="aad43-106">The **New-AzureRmFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="aad43-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aad43-107">EXAMPLES</span></span>

### <span data-ttu-id="aad43-108">1: criar uma coleção com uma regra</span><span class="sxs-lookup"><span data-stu-id="aad43-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="aad43-109">Este exemplo cria uma coleção com uma regra.</span><span class="sxs-lookup"><span data-stu-id="aad43-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="aad43-110">Todo o tráfego que corresponde às condições identificadas em $rule 1 será permitido.</span><span class="sxs-lookup"><span data-stu-id="aad43-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="aad43-111">A primeira regra é para todo o tráfego HTTPS na porta 443 de 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="aad43-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="aad43-112">Se houver outro conjunto de regras de aplicativo com prioridade mais alta (número menor) que também corresponda ao tráfego identificado no $rule 1, a ação da coleção de regras com prioridade mais alta terá efeito em vez disso.</span><span class="sxs-lookup"><span data-stu-id="aad43-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="aad43-113">2: adicionar uma regra a uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="aad43-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="aad43-114">Este exemplo cria uma nova coleção de regras de aplicativo com uma regra e, em seguida, adiciona uma segunda regra à coleção de regras usando addrule no objeto da coleção Rule.</span><span class="sxs-lookup"><span data-stu-id="aad43-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="aad43-115">Cada nome de regra em um determinado conjunto de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="aad43-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="aad43-116">3: obter uma regra a partir de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="aad43-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="aad43-117">Este exemplo cria um novo conjunto de regras de aplicativo com uma regra e, em seguida, obtém a regra por nome, método de chamada GetRuleByName no objeto da coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="aad43-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="aad43-118">O nome da regra para o método GetRuleByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="aad43-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="aad43-119">4: remover uma regra de uma coleção de regras</span><span class="sxs-lookup"><span data-stu-id="aad43-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="aad43-120">Este exemplo cria um novo conjunto de regras de aplicativo com duas regras e, em seguida, remove a primeira regra da coleção de regras chamando o método RemoveRuleByName no objeto da coleção Rule.</span><span class="sxs-lookup"><span data-stu-id="aad43-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="aad43-121">O nome da regra para o método RemoveRuleByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="aad43-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="aad43-122">OS</span><span class="sxs-lookup"><span data-stu-id="aad43-122">PARAMETERS</span></span>

### <span data-ttu-id="aad43-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="aad43-123">-ActionType</span></span>
<span data-ttu-id="aad43-124">A ação da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="aad43-124">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad43-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad43-125">-DefaultProfile</span></span>
<span data-ttu-id="aad43-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aad43-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad43-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="aad43-127">-Name</span></span>
<span data-ttu-id="aad43-128">Especifica o nome desta regra de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aad43-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="aad43-129">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="aad43-129">The name must be unique inside a rule collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad43-130">-Priority</span><span class="sxs-lookup"><span data-stu-id="aad43-130">-Priority</span></span>
<span data-ttu-id="aad43-131">Especifica a prioridade dessa regra.</span><span class="sxs-lookup"><span data-stu-id="aad43-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="aad43-132">Priority é um número entre 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="aad43-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="aad43-133">Quanto menor o número, maior a prioridade.</span><span class="sxs-lookup"><span data-stu-id="aad43-133">The smaller the number, the bigger the priority.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad43-134">-Regra</span><span class="sxs-lookup"><span data-stu-id="aad43-134">-Rule</span></span>
<span data-ttu-id="aad43-135">Especifica a lista de regras a serem agrupadas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="aad43-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad43-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aad43-136">-Confirm</span></span>
<span data-ttu-id="aad43-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad43-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad43-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad43-138">-WhatIf</span></span>
<span data-ttu-id="aad43-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aad43-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad43-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aad43-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad43-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad43-141">CommonParameters</span></span>
<span data-ttu-id="aad43-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad43-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad43-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad43-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad43-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aad43-144">INPUTS</span></span>

### <span data-ttu-id="aad43-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="aad43-145">None</span></span>
<span data-ttu-id="aad43-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="aad43-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aad43-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aad43-147">OUTPUTS</span></span>

### <span data-ttu-id="aad43-148">Microsoft. Azure. Commands. Network. Models. PSFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="aad43-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="aad43-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aad43-149">NOTES</span></span>

## <span data-ttu-id="aad43-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aad43-150">RELATED LINKS</span></span>

[<span data-ttu-id="aad43-151">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="aad43-151">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="aad43-152">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="aad43-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="aad43-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="aad43-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
