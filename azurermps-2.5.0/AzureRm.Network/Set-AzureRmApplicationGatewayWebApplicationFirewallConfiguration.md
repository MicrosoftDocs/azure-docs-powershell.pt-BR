---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: fd925829248c7f11f047de90ddc2bc0b57f51b71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785882"
---
# <span data-ttu-id="c89c6-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c89c6-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="c89c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c89c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c89c6-103">Modifica a configuração do WAF de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c89c6-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c89c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c89c6-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c89c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c89c6-105">DESCRIPTION</span></span>
<span data-ttu-id="c89c6-106">O cmdlet **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** modifica a configuração do WAF (firewall de aplicativo Web) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c89c6-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="c89c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c89c6-107">EXAMPLES</span></span>

### <span data-ttu-id="c89c6-108">Exemplo 1: atualizar a configuração de firewall do aplicativo Web do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c89c6-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="c89c6-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e, em seguida, armazena-o na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c89c6-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c89c6-110">O segundo comando habilita a configuração do firewall para o gateway do aplicativo armazenado no $AppGw e define o modo de firewall como "detecção", RuleSettype para "OWASP" e o RuleSetVersion para "3,0".</span><span class="sxs-lookup"><span data-stu-id="c89c6-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="c89c6-111">OS</span><span class="sxs-lookup"><span data-stu-id="c89c6-111">PARAMETERS</span></span>

### <span data-ttu-id="c89c6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c89c6-112">-ApplicationGateway</span></span>
<span data-ttu-id="c89c6-113">Especifica um objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c89c6-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="c89c6-114">Você pode usar o cmdlet Get-AzureRmApplicationGateway para obter um objeto de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c89c6-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c89c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c89c6-115">-DefaultProfile</span></span>
<span data-ttu-id="c89c6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c89c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c89c6-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="c89c6-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="c89c6-118">Os grupos de regras desabilitados.</span><span class="sxs-lookup"><span data-stu-id="c89c6-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="c89c6-119">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="c89c6-119">-Enabled</span></span>
<span data-ttu-id="c89c6-120">Indica se o Firewall do aplicativo Web está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c89c6-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="c89c6-121">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="c89c6-121">-FirewallMode</span></span>
<span data-ttu-id="c89c6-122">Especifica o modo de firewall do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="c89c6-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="c89c6-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c89c6-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c89c6-124">Detenção</span><span class="sxs-lookup"><span data-stu-id="c89c6-124">Detection</span></span>
- <span data-ttu-id="c89c6-125">Abrangente</span><span class="sxs-lookup"><span data-stu-id="c89c6-125">Prevention</span></span>

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

### <span data-ttu-id="c89c6-126">-RuleSettype</span><span class="sxs-lookup"><span data-stu-id="c89c6-126">-RuleSetType</span></span>
<span data-ttu-id="c89c6-127">O tipo de regra de firewall de aplicativo Web definido.</span><span class="sxs-lookup"><span data-stu-id="c89c6-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="c89c6-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c89c6-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="c89c6-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="c89c6-129">OWASP</span></span>

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

### <span data-ttu-id="c89c6-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="c89c6-130">-RuleSetVersion</span></span>
<span data-ttu-id="c89c6-131">A versão do tipo de conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="c89c6-131">The version of the rule set type.</span></span>
<span data-ttu-id="c89c6-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c89c6-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="c89c6-133">3,0</span><span class="sxs-lookup"><span data-stu-id="c89c6-133">3.0</span></span>
- <span data-ttu-id="c89c6-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="c89c6-134">2.2.9</span></span>

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

### <span data-ttu-id="c89c6-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c89c6-135">-Confirm</span></span>
<span data-ttu-id="c89c6-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c89c6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c89c6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c89c6-137">-WhatIf</span></span>
<span data-ttu-id="c89c6-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c89c6-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c89c6-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c89c6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c89c6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89c6-140">CommonParameters</span></span>
<span data-ttu-id="c89c6-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c89c6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89c6-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c89c6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89c6-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c89c6-143">INPUTS</span></span>

### <span data-ttu-id="c89c6-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c89c6-144">PSApplicationGateway</span></span>
<span data-ttu-id="c89c6-145">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c89c6-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="c89c6-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c89c6-146">OUTPUTS</span></span>

### <span data-ttu-id="c89c6-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c89c6-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c89c6-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c89c6-148">NOTES</span></span>

## <span data-ttu-id="c89c6-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c89c6-149">RELATED LINKS</span></span>

[<span data-ttu-id="c89c6-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c89c6-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="c89c6-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c89c6-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="c89c6-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c89c6-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


