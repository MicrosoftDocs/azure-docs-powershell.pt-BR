---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: f0117a7fa89f5e392009a9df814996ee66cc8bcd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785315"
---
# <span data-ttu-id="9980a-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9980a-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="9980a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9980a-102">SYNOPSIS</span></span>
<span data-ttu-id="9980a-103">Cria uma configuração WAF para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9980a-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9980a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9980a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9980a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9980a-105">DESCRIPTION</span></span>
<span data-ttu-id="9980a-106">O cmdlet **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cria uma configuração WAF (firewall de aplicativo Web) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9980a-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="9980a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9980a-107">EXAMPLES</span></span>

### <span data-ttu-id="9980a-108">Exemplo 1: criar uma configuração de firewall de aplicativo Web para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9980a-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="9980a-109">O primeiro comando cria uma nova configuração de grupo de regras desabilitada para o grupo de regras chamado "REQUEST-942-APPLICATION-ATTACK-SQLI" com a regra 942130 e a regra 942140 sendo desabilitada.</span><span class="sxs-lookup"><span data-stu-id="9980a-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="9980a-110">O segundo comando cria outra configuração de grupo de regras desabilitada para um grupo de regras chamado "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="9980a-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="9980a-111">Nenhuma regra é passada especificamente e, portanto, todas as regras do grupo de regras serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="9980a-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="9980a-112">Em seguida, o último comando cria uma configuração WAF com regras de firewall desabilitadas conforme configurado no $disabledRuleGroup 1 e $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="9980a-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="9980a-113">A nova configuração de WAF é armazenada na variável $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="9980a-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="9980a-114">OS</span><span class="sxs-lookup"><span data-stu-id="9980a-114">PARAMETERS</span></span>

### <span data-ttu-id="9980a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9980a-115">-DefaultProfile</span></span>
<span data-ttu-id="9980a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9980a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9980a-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="9980a-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="9980a-118">Os grupos de regras desabilitados.</span><span class="sxs-lookup"><span data-stu-id="9980a-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9980a-119">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="9980a-119">-Enabled</span></span>
<span data-ttu-id="9980a-120">Indica se o WAF está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9980a-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9980a-121">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="9980a-121">-FirewallMode</span></span>
<span data-ttu-id="9980a-122">Especifica o modo de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="9980a-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="9980a-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9980a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9980a-124">Detenção</span><span class="sxs-lookup"><span data-stu-id="9980a-124">Detection</span></span>
- <span data-ttu-id="9980a-125">Abrangente</span><span class="sxs-lookup"><span data-stu-id="9980a-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9980a-126">-RuleSettype</span><span class="sxs-lookup"><span data-stu-id="9980a-126">-RuleSetType</span></span>
<span data-ttu-id="9980a-127">O tipo de regra de firewall de aplicativo Web definido.</span><span class="sxs-lookup"><span data-stu-id="9980a-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="9980a-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9980a-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="9980a-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="9980a-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9980a-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="9980a-130">-RuleSetVersion</span></span>
<span data-ttu-id="9980a-131">A versão do tipo de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="9980a-131">The version of the rule set type.</span></span>
<span data-ttu-id="9980a-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9980a-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="9980a-133">3,0</span><span class="sxs-lookup"><span data-stu-id="9980a-133">3.0</span></span>
- <span data-ttu-id="9980a-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="9980a-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9980a-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9980a-135">-Confirm</span></span>
<span data-ttu-id="9980a-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9980a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9980a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9980a-137">-WhatIf</span></span>
<span data-ttu-id="9980a-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9980a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9980a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9980a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9980a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9980a-140">CommonParameters</span></span>
<span data-ttu-id="9980a-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9980a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9980a-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9980a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9980a-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9980a-143">INPUTS</span></span>

## <span data-ttu-id="9980a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9980a-144">OUTPUTS</span></span>

### <span data-ttu-id="9980a-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9980a-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="9980a-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9980a-146">NOTES</span></span>

## <span data-ttu-id="9980a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9980a-147">RELATED LINKS</span></span>

[<span data-ttu-id="9980a-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9980a-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="9980a-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9980a-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


