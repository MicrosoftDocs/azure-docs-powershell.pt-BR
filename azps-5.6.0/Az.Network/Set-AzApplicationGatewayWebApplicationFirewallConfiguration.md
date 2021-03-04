---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 95d0e82609c2cb8bfcbbfcf57d1354d219da9f9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890994"
---
# <span data-ttu-id="1291a-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1291a-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="1291a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1291a-102">SYNOPSIS</span></span>
<span data-ttu-id="1291a-103">Modifica a configuração WAF de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1291a-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="1291a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1291a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1291a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1291a-105">DESCRIPTION</span></span>
<span data-ttu-id="1291a-106">O cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica a configuração do waf (firewall de aplicativo web) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1291a-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="1291a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1291a-107">EXAMPLES</span></span>

### <span data-ttu-id="1291a-108">Exemplo 1: atualizar a configuração de firewall do aplicativo web gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1291a-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="1291a-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1291a-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1291a-110">O segundo comando habilita a configuração de firewall para o gateway de aplicativo armazenado no $AppGw e define o modo de firewall como "Detecção", RuleSetType como "OWASP" e RuleSetVersion como "3.0".</span><span class="sxs-lookup"><span data-stu-id="1291a-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="1291a-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1291a-111">PARAMETERS</span></span>

### <span data-ttu-id="1291a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1291a-112">-ApplicationGateway</span></span>
<span data-ttu-id="1291a-113">Especifica um objeto gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1291a-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="1291a-114">Você pode usar o cmdlet Get-AzApplicationGateway para obter um objeto gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1291a-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1291a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1291a-115">-DefaultProfile</span></span>
<span data-ttu-id="1291a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1291a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1291a-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="1291a-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="1291a-118">Os grupos de regras desabilitados.</span><span class="sxs-lookup"><span data-stu-id="1291a-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="1291a-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="1291a-119">-Enabled</span></span>
<span data-ttu-id="1291a-120">Indica se o firewall do aplicativo Web está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1291a-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="1291a-121">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="1291a-121">-Exclusion</span></span>
<span data-ttu-id="1291a-122">As listas de exclusão.</span><span class="sxs-lookup"><span data-stu-id="1291a-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="1291a-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="1291a-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="1291a-124">Limite máximo de carregamento de arquivo em MB.</span><span class="sxs-lookup"><span data-stu-id="1291a-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="1291a-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="1291a-125">-FirewallMode</span></span>
<span data-ttu-id="1291a-126">Especifica o modo de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1291a-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="1291a-127">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1291a-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1291a-128">Detecção</span><span class="sxs-lookup"><span data-stu-id="1291a-128">Detection</span></span>
- <span data-ttu-id="1291a-129">Prevenção</span><span class="sxs-lookup"><span data-stu-id="1291a-129">Prevention</span></span>

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

### <span data-ttu-id="1291a-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="1291a-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="1291a-131">Tamanho máximo do corpo da solicitação em KB.</span><span class="sxs-lookup"><span data-stu-id="1291a-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="1291a-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="1291a-132">-RequestBodyCheck</span></span>
<span data-ttu-id="1291a-133">Se o corpo da solicitação está marcado ou não.</span><span class="sxs-lookup"><span data-stu-id="1291a-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="1291a-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="1291a-134">-RuleSetType</span></span>
<span data-ttu-id="1291a-135">O tipo do conjunto de regras de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1291a-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="1291a-136">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1291a-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="1291a-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="1291a-137">OWASP</span></span>

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

### <span data-ttu-id="1291a-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="1291a-138">-RuleSetVersion</span></span>
<span data-ttu-id="1291a-139">A versão do tipo de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="1291a-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="1291a-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1291a-140">-Confirm</span></span>
<span data-ttu-id="1291a-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1291a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1291a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1291a-142">-WhatIf</span></span>
<span data-ttu-id="1291a-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1291a-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1291a-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1291a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1291a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1291a-145">CommonParameters</span></span>
<span data-ttu-id="1291a-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1291a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1291a-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1291a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1291a-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1291a-148">INPUTS</span></span>

### <span data-ttu-id="1291a-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1291a-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1291a-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1291a-150">OUTPUTS</span></span>

### <span data-ttu-id="1291a-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1291a-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1291a-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="1291a-152">NOTES</span></span>

## <span data-ttu-id="1291a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1291a-153">RELATED LINKS</span></span>

[<span data-ttu-id="1291a-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1291a-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="1291a-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1291a-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="1291a-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1291a-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


