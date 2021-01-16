---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9b5e618fc4b4be02614d872bfa5bcdabd2b0fec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259969"
---
# <span data-ttu-id="88514-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="88514-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="88514-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88514-102">SYNOPSIS</span></span>
<span data-ttu-id="88514-103">Modifica a configuração do WAF de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="88514-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="88514-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88514-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88514-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88514-105">DESCRIPTION</span></span>
<span data-ttu-id="88514-106">O cmdlet **set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica a configuração do WAF (firewall de aplicativo Web) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="88514-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="88514-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88514-107">EXAMPLES</span></span>

### <span data-ttu-id="88514-108">Exemplo 1: atualizar a configuração de firewall do aplicativo Web do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="88514-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="88514-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e, em seguida, armazena-o na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="88514-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="88514-110">O segundo comando habilita a configuração do firewall para o gateway do aplicativo armazenado no $AppGw e define o modo de firewall como "detecção", RuleSettype para "OWASP" e o RuleSetVersion para "3,0".</span><span class="sxs-lookup"><span data-stu-id="88514-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="88514-111">OS</span><span class="sxs-lookup"><span data-stu-id="88514-111">PARAMETERS</span></span>

### <span data-ttu-id="88514-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88514-112">-ApplicationGateway</span></span>
<span data-ttu-id="88514-113">Especifica um objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="88514-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="88514-114">Você pode usar o cmdlet Get-AzApplicationGateway para obter um objeto de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="88514-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="88514-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88514-115">-DefaultProfile</span></span>
<span data-ttu-id="88514-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88514-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88514-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="88514-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="88514-118">Os grupos de regras desabilitados.</span><span class="sxs-lookup"><span data-stu-id="88514-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="88514-119">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="88514-119">-Enabled</span></span>
<span data-ttu-id="88514-120">Indica se o Firewall do aplicativo Web está habilitado.</span><span class="sxs-lookup"><span data-stu-id="88514-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="88514-121">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="88514-121">-Exclusion</span></span>
<span data-ttu-id="88514-122">Listas de exclusão.</span><span class="sxs-lookup"><span data-stu-id="88514-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="88514-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="88514-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="88514-124">Limite máximo de carregamento de arquivos em MB.</span><span class="sxs-lookup"><span data-stu-id="88514-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="88514-125">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="88514-125">-FirewallMode</span></span>
<span data-ttu-id="88514-126">Especifica o modo de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="88514-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="88514-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="88514-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88514-128">Detenção</span><span class="sxs-lookup"><span data-stu-id="88514-128">Detection</span></span>
- <span data-ttu-id="88514-129">Abrangente</span><span class="sxs-lookup"><span data-stu-id="88514-129">Prevention</span></span>

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

### <span data-ttu-id="88514-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="88514-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="88514-131">Tamanho máximo do corpo da solicitação em KB.</span><span class="sxs-lookup"><span data-stu-id="88514-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="88514-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="88514-132">-RequestBodyCheck</span></span>
<span data-ttu-id="88514-133">Se o corpo da solicitação está ou não selecionado.</span><span class="sxs-lookup"><span data-stu-id="88514-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="88514-134">-RuleSettype</span><span class="sxs-lookup"><span data-stu-id="88514-134">-RuleSetType</span></span>
<span data-ttu-id="88514-135">O tipo de regra de firewall de aplicativo Web definido.</span><span class="sxs-lookup"><span data-stu-id="88514-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="88514-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="88514-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="88514-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="88514-137">OWASP</span></span>

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

### <span data-ttu-id="88514-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="88514-138">-RuleSetVersion</span></span>
<span data-ttu-id="88514-139">A versão do tipo de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="88514-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="88514-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88514-140">-Confirm</span></span>
<span data-ttu-id="88514-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88514-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88514-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88514-142">-WhatIf</span></span>
<span data-ttu-id="88514-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88514-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88514-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88514-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88514-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88514-145">CommonParameters</span></span>
<span data-ttu-id="88514-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88514-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88514-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88514-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88514-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88514-148">INPUTS</span></span>

### <span data-ttu-id="88514-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88514-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="88514-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88514-150">OUTPUTS</span></span>

### <span data-ttu-id="88514-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88514-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="88514-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88514-152">NOTES</span></span>

## <span data-ttu-id="88514-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88514-153">RELATED LINKS</span></span>

[<span data-ttu-id="88514-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88514-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="88514-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="88514-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="88514-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="88514-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


