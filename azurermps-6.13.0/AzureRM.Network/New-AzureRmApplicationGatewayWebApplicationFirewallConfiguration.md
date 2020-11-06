---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 523381f4b8b5b214dc2549f52e3340adec4d9341
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441254"
---
# <span data-ttu-id="f6676-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6676-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f6676-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6676-102">SYNOPSIS</span></span>
<span data-ttu-id="f6676-103">Cria uma configuração WAF para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6676-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6676-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6676-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-RequestBodyCheck <Boolean>] [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6676-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6676-105">DESCRIPTION</span></span>
<span data-ttu-id="f6676-106">O cmdlet **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cria uma configuração WAF (firewall de aplicativo Web) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6676-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="f6676-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6676-107">EXAMPLES</span></span>

### <span data-ttu-id="f6676-108">Exemplo 1: criar uma configuração de firewall de aplicativo Web para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f6676-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="f6676-109">O primeiro comando cria uma nova configuração de grupo de regras desabilitada para o grupo de regras chamado "REQUEST-942-APPLICATION-ATTACK-SQLI" com a regra 942130 e a regra 942140 sendo desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f6676-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="f6676-110">O segundo comando cria outra configuração de grupo de regras desabilitada para um grupo de regras chamado "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="f6676-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="f6676-111">Nenhuma regra é passada especificamente e, portanto, todas as regras do grupo de regras serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="f6676-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="f6676-112">Em seguida, o último comando cria uma configuração WAF com regras de firewall desabilitadas conforme configurado no $disabledRuleGroup 1 e $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="f6676-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="f6676-113">A nova configuração de WAF é armazenada na variável $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="f6676-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="f6676-114">OS</span><span class="sxs-lookup"><span data-stu-id="f6676-114">PARAMETERS</span></span>

### <span data-ttu-id="f6676-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6676-115">-DefaultProfile</span></span>
<span data-ttu-id="f6676-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6676-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6676-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="f6676-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="f6676-118">Os grupos de regras desabilitados.</span><span class="sxs-lookup"><span data-stu-id="f6676-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6676-119">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="f6676-119">-Enabled</span></span>
<span data-ttu-id="f6676-120">Indica se o WAF está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6676-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="f6676-121">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="f6676-121">-Exclusion</span></span>
<span data-ttu-id="f6676-122">Listas de exclusão.</span><span class="sxs-lookup"><span data-stu-id="f6676-122">The exclusion lists.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6676-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="f6676-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="f6676-124">Limite máximo de carregamento de arquivos em MB.</span><span class="sxs-lookup"><span data-stu-id="f6676-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="f6676-125">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="f6676-125">-FirewallMode</span></span>
<span data-ttu-id="f6676-126">Especifica o modo de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="f6676-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="f6676-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f6676-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6676-128">Detenção</span><span class="sxs-lookup"><span data-stu-id="f6676-128">Detection</span></span>
- <span data-ttu-id="f6676-129">Abrangente</span><span class="sxs-lookup"><span data-stu-id="f6676-129">Prevention</span></span>

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

### <span data-ttu-id="f6676-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="f6676-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="f6676-131">Tamanho máximo do corpo da solicitação em KB.</span><span class="sxs-lookup"><span data-stu-id="f6676-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="f6676-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="f6676-132">-RequestBodyCheck</span></span>
<span data-ttu-id="f6676-133">Se o corpo da solicitação está ou não selecionado.</span><span class="sxs-lookup"><span data-stu-id="f6676-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="f6676-134">-RuleSettype</span><span class="sxs-lookup"><span data-stu-id="f6676-134">-RuleSetType</span></span>
<span data-ttu-id="f6676-135">O tipo de regra de firewall de aplicativo Web definido.</span><span class="sxs-lookup"><span data-stu-id="f6676-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="f6676-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f6676-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="f6676-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="f6676-137">OWASP</span></span>

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

### <span data-ttu-id="f6676-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="f6676-138">-RuleSetVersion</span></span>
<span data-ttu-id="f6676-139">A versão do tipo de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="f6676-139">The version of the rule set type.</span></span>
<span data-ttu-id="f6676-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f6676-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="f6676-141">3,0</span><span class="sxs-lookup"><span data-stu-id="f6676-141">3.0</span></span>
- <span data-ttu-id="f6676-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="f6676-142">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6676-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6676-143">-Confirm</span></span>
<span data-ttu-id="f6676-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6676-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6676-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6676-145">-WhatIf</span></span>
<span data-ttu-id="f6676-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6676-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6676-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6676-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6676-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6676-148">CommonParameters</span></span>
<span data-ttu-id="f6676-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6676-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6676-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6676-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6676-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6676-151">INPUTS</span></span>

### <span data-ttu-id="f6676-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f6676-152">None</span></span>

## <span data-ttu-id="f6676-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6676-153">OUTPUTS</span></span>

### <span data-ttu-id="f6676-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6676-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f6676-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6676-155">NOTES</span></span>

## <span data-ttu-id="f6676-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6676-156">RELATED LINKS</span></span>

[<span data-ttu-id="f6676-157">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6676-157">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f6676-158">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6676-158">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


