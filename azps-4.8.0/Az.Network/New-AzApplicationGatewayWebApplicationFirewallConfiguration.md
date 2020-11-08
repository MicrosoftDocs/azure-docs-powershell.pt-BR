---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114865"
---
# <span data-ttu-id="4856b-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4856b-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="4856b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4856b-102">SYNOPSIS</span></span>
<span data-ttu-id="4856b-103">Cria uma configuração WAF para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4856b-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="4856b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4856b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4856b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4856b-105">DESCRIPTION</span></span>
<span data-ttu-id="4856b-106">O cmdlet **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cria uma configuração WAF (firewall de aplicativo Web) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="4856b-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="4856b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4856b-107">EXAMPLES</span></span>

### <span data-ttu-id="4856b-108">Exemplo 1: criar uma configuração de firewall de aplicativo Web para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="4856b-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="4856b-109">O primeiro comando cria uma nova configuração de grupo de regras desabilitada para o grupo de regras chamado "REQUEST-942-APPLICATION-ATTACK-SQLI" com a regra 942130 e a regra 942140 sendo desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4856b-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="4856b-110">O segundo comando cria outra configuração de grupo de regras desabilitada para um grupo de regras chamado "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="4856b-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="4856b-111">Nenhuma regra é passada especificamente e, portanto, todas as regras do grupo de regras serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="4856b-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="4856b-112">Em seguida, o último comando cria uma configuração WAF com regras de firewall desabilitadas conforme configurado no $disabledRuleGroup 1 e $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="4856b-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="4856b-113">A nova configuração de WAF é armazenada na variável $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="4856b-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="4856b-114">OS</span><span class="sxs-lookup"><span data-stu-id="4856b-114">PARAMETERS</span></span>

### <span data-ttu-id="4856b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4856b-115">-DefaultProfile</span></span>
<span data-ttu-id="4856b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4856b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4856b-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="4856b-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="4856b-118">Os grupos de regras desabilitados.</span><span class="sxs-lookup"><span data-stu-id="4856b-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="4856b-119">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="4856b-119">-Enabled</span></span>
<span data-ttu-id="4856b-120">Indica se o WAF está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4856b-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="4856b-121">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="4856b-121">-Exclusion</span></span>
<span data-ttu-id="4856b-122">Listas de exclusão.</span><span class="sxs-lookup"><span data-stu-id="4856b-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="4856b-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="4856b-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="4856b-124">Limite máximo de carregamento de arquivos em MB.</span><span class="sxs-lookup"><span data-stu-id="4856b-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="4856b-125">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="4856b-125">-FirewallMode</span></span>
<span data-ttu-id="4856b-126">Especifica o modo de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="4856b-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="4856b-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4856b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4856b-128">Detenção</span><span class="sxs-lookup"><span data-stu-id="4856b-128">Detection</span></span>
- <span data-ttu-id="4856b-129">Abrangente</span><span class="sxs-lookup"><span data-stu-id="4856b-129">Prevention</span></span>

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

### <span data-ttu-id="4856b-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="4856b-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="4856b-131">Tamanho máximo do corpo da solicitação em KB.</span><span class="sxs-lookup"><span data-stu-id="4856b-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="4856b-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="4856b-132">-RequestBodyCheck</span></span>
<span data-ttu-id="4856b-133">Se o corpo da solicitação está ou não selecionado.</span><span class="sxs-lookup"><span data-stu-id="4856b-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="4856b-134">-RuleSettype</span><span class="sxs-lookup"><span data-stu-id="4856b-134">-RuleSetType</span></span>
<span data-ttu-id="4856b-135">O tipo de regra de firewall de aplicativo Web definido.</span><span class="sxs-lookup"><span data-stu-id="4856b-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="4856b-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4856b-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="4856b-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="4856b-137">OWASP</span></span>

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

### <span data-ttu-id="4856b-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="4856b-138">-RuleSetVersion</span></span>
<span data-ttu-id="4856b-139">A versão do tipo de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="4856b-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="4856b-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4856b-140">-Confirm</span></span>
<span data-ttu-id="4856b-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4856b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4856b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4856b-142">-WhatIf</span></span>
<span data-ttu-id="4856b-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4856b-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4856b-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4856b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4856b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4856b-145">CommonParameters</span></span>
<span data-ttu-id="4856b-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4856b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4856b-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4856b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4856b-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4856b-148">INPUTS</span></span>

### <span data-ttu-id="4856b-149">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4856b-149">None</span></span>

## <span data-ttu-id="4856b-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4856b-150">OUTPUTS</span></span>

### <span data-ttu-id="4856b-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4856b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="4856b-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4856b-152">NOTES</span></span>

## <span data-ttu-id="4856b-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4856b-153">RELATED LINKS</span></span>

[<span data-ttu-id="4856b-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4856b-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="4856b-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4856b-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


