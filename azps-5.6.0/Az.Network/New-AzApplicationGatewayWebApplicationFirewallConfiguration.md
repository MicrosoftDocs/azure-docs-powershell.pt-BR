---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 7d13febefe06ed1c290a0f95cbfda39dea353426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888626"
---
# <span data-ttu-id="a71cf-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a71cf-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a71cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a71cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a71cf-103">Cria uma configuração WAF para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a71cf-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="a71cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a71cf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71cf-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a71cf-105">DESCRIPTION</span></span>
<span data-ttu-id="a71cf-106">O cmdlet **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cria uma configuração waf (firewall de aplicativo web) para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="a71cf-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a71cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a71cf-107">EXAMPLES</span></span>

### <span data-ttu-id="a71cf-108">Exemplo 1: Criar uma configuração de firewall de aplicativo Web para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a71cf-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="a71cf-109">O primeiro comando cria uma nova configuração de grupo de regras desabilitada para o grupo de regras chamado "REQUEST-942-APPLICATION-ATTACK-SQLI" com a regra 942130 e a regra 942140 sendo desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a71cf-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="a71cf-110">O segundo comando cria outra configuração de grupo de regras desabilitada para um grupo de regras chamado "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="a71cf-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="a71cf-111">Nenhuma regra é aprovada especificamente e, portanto, todas as regras do grupo de regras serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="a71cf-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="a71cf-112">Em seguida, o último comando cria uma configuração WAF com regras de firewall desabilitadas conforme configurado no $disabledRuleGroup 1 e $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="a71cf-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="a71cf-113">A nova configuração waf é armazenada na $firewallConfig variável.</span><span class="sxs-lookup"><span data-stu-id="a71cf-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="a71cf-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a71cf-114">PARAMETERS</span></span>

### <span data-ttu-id="a71cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71cf-115">-DefaultProfile</span></span>
<span data-ttu-id="a71cf-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a71cf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a71cf-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="a71cf-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="a71cf-118">Os grupos de regras desabilitados.</span><span class="sxs-lookup"><span data-stu-id="a71cf-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="a71cf-119">-Enabled</span></span>
<span data-ttu-id="a71cf-120">Indica se o WAF está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a71cf-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-121">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="a71cf-121">-Exclusion</span></span>
<span data-ttu-id="a71cf-122">As listas de exclusão.</span><span class="sxs-lookup"><span data-stu-id="a71cf-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="a71cf-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="a71cf-124">Limite máximo de carregamento de arquivo em MB.</span><span class="sxs-lookup"><span data-stu-id="a71cf-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="a71cf-125">-FirewallMode</span></span>
<span data-ttu-id="a71cf-126">Especifica o modo de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a71cf-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="a71cf-127">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a71cf-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a71cf-128">Detecção</span><span class="sxs-lookup"><span data-stu-id="a71cf-128">Detection</span></span>
- <span data-ttu-id="a71cf-129">Prevenção</span><span class="sxs-lookup"><span data-stu-id="a71cf-129">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="a71cf-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="a71cf-131">Tamanho máximo do corpo da solicitação em KB.</span><span class="sxs-lookup"><span data-stu-id="a71cf-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="a71cf-132">-RequestBodyCheck</span></span>
<span data-ttu-id="a71cf-133">Se o corpo da solicitação está marcado ou não.</span><span class="sxs-lookup"><span data-stu-id="a71cf-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="a71cf-134">-RuleSetType</span></span>
<span data-ttu-id="a71cf-135">O tipo do conjunto de regras de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a71cf-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="a71cf-136">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a71cf-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="a71cf-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="a71cf-137">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="a71cf-138">-RuleSetVersion</span></span>
<span data-ttu-id="a71cf-139">A versão do tipo de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="a71cf-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71cf-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a71cf-140">-Confirm</span></span>
<span data-ttu-id="a71cf-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71cf-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a71cf-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71cf-142">-WhatIf</span></span>
<span data-ttu-id="a71cf-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a71cf-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a71cf-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a71cf-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a71cf-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71cf-145">CommonParameters</span></span>
<span data-ttu-id="a71cf-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a71cf-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71cf-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a71cf-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71cf-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a71cf-148">INPUTS</span></span>

### <span data-ttu-id="a71cf-149">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a71cf-149">None</span></span>

## <span data-ttu-id="a71cf-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a71cf-150">OUTPUTS</span></span>

### <span data-ttu-id="a71cf-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a71cf-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a71cf-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="a71cf-152">NOTES</span></span>

## <span data-ttu-id="a71cf-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a71cf-153">RELATED LINKS</span></span>

[<span data-ttu-id="a71cf-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a71cf-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="a71cf-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a71cf-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


