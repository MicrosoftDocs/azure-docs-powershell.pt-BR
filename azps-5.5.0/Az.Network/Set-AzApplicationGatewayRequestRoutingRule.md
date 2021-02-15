---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f815994a6f60490bd930a17748cd00167c2b52ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114103"
---
# <span data-ttu-id="22ff8-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="22ff8-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="22ff8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="22ff8-103">Modifica uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22ff8-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="22ff8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22ff8-104">SYNTAX</span></span>

### <span data-ttu-id="22ff8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="22ff8-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22ff8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="22ff8-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22ff8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="22ff8-107">DESCRIPTION</span></span>
<span data-ttu-id="22ff8-108">O cmdlet **Set-AzApplicationGatewayRequestRoutingRule** modifica uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="22ff8-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="22ff8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22ff8-109">EXAMPLES</span></span>

### <span data-ttu-id="22ff8-110">Exemplo 1: Atualizar uma regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="22ff8-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="22ff8-111">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22ff8-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="22ff8-112">O segundo comando modifica a regra de roteamento de solicitação para que o gateway de aplicativo use configurações HTTP de back-end especificadas na variável $Setting, um ouvinte HTTP especificado na variável $Listener e um pool de endereços back-end especificado na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="22ff8-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="22ff8-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22ff8-113">PARAMETERS</span></span>

### <span data-ttu-id="22ff8-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22ff8-114">-ApplicationGateway</span></span>
<span data-ttu-id="22ff8-115">Especifica o objeto do gateway de aplicativo com o qual este cmdlet associa uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="22ff8-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="22ff8-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="22ff8-116">-BackendAddressPool</span></span>
<span data-ttu-id="22ff8-117">Especifica o pool de endereços back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22ff8-117">Specifies the application gateway back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="22ff8-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="22ff8-119">Especifica a ID do pool de endereços back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22ff8-119">Specifies the application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="22ff8-120">-BackendHttpSettings</span></span>
<span data-ttu-id="22ff8-121">Especifica as configurações http do back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22ff8-121">Specifies the application gateway backend HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="22ff8-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="22ff8-123">Especifica a ID de configurações HTTP de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22ff8-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ff8-124">-DefaultProfile</span></span>
<span data-ttu-id="22ff8-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="22ff8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22ff8-126">-httpListener</span><span class="sxs-lookup"><span data-stu-id="22ff8-126">-HttpListener</span></span>
<span data-ttu-id="22ff8-127">Especifica o ouvinte HTTP do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22ff8-127">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-128">-httpListenerId</span><span class="sxs-lookup"><span data-stu-id="22ff8-128">-HttpListenerId</span></span>
<span data-ttu-id="22ff8-129">Especifica a ID de ouvinte HTTP do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22ff8-129">Specifies the application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="22ff8-130">-Name</span></span>
<span data-ttu-id="22ff8-131">Especifica o nome da regra de roteamento de solicitação que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="22ff8-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="22ff8-132">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="22ff8-132">-Priority</span></span>
<span data-ttu-id="22ff8-133">A prioridade da regra</span><span class="sxs-lookup"><span data-stu-id="22ff8-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="22ff8-134">-RedirectConfiguration</span></span>
<span data-ttu-id="22ff8-135">Redirecionamento do gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="22ff8-135">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="22ff8-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="22ff8-137">ID do gateway de aplicativo RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="22ff8-137">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="22ff8-138">-RewriteRuleSet</span></span>
<span data-ttu-id="22ff8-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="22ff8-139">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="22ff8-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="22ff8-141">ID do gateway de aplicativo RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="22ff8-141">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="22ff8-142">-RuleType</span></span>
<span data-ttu-id="22ff8-143">Especifica o tipo de regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="22ff8-143">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="22ff8-144">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="22ff8-145">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ff8-146">CommonParameters</span></span>
<span data-ttu-id="22ff8-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ff8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ff8-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22ff8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ff8-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="22ff8-149">INPUTS</span></span>

### <span data-ttu-id="22ff8-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22ff8-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22ff8-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="22ff8-151">OUTPUTS</span></span>

### <span data-ttu-id="22ff8-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22ff8-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22ff8-153">Notas</span><span class="sxs-lookup"><span data-stu-id="22ff8-153">NOTES</span></span>

## <span data-ttu-id="22ff8-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22ff8-154">RELATED LINKS</span></span>

[<span data-ttu-id="22ff8-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="22ff8-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="22ff8-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="22ff8-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="22ff8-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="22ff8-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="22ff8-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="22ff8-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


