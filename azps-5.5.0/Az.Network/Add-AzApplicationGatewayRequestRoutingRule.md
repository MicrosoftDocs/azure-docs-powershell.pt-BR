---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112915"
---
# <span data-ttu-id="7dc4d-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dc4d-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7dc4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc4d-103">Adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="7dc4d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7dc4d-104">SYNTAX</span></span>

### <span data-ttu-id="7dc4d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7dc4d-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dc4d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7dc4d-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dc4d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7dc4d-107">DESCRIPTION</span></span>
<span data-ttu-id="7dc4d-108">O **cmdlet Add-AzApplicationGatewayRequestRoutingRule** adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="7dc4d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7dc4d-109">EXAMPLES</span></span>

### <span data-ttu-id="7dc4d-110">Exemplo 1: Adicionar uma regra de roteamento de solicitação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7dc4d-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="7dc4d-111">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw usuário.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7dc4d-112">O segundo comando adiciona a regra de roteamento de solicitação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="7dc4d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dc4d-113">PARAMETERS</span></span>

### <span data-ttu-id="7dc4d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dc4d-114">-ApplicationGateway</span></span>
<span data-ttu-id="7dc4d-115">Especifica um gateway de aplicativo ao qual este cmdlet adiciona uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="7dc4d-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7dc4d-116">-BackendAddressPool</span></span>
<span data-ttu-id="7dc4d-117">Especifica um objeto de pool de endereços back-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="7dc4d-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7dc4d-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="7dc4d-119">Especifica uma ID do pool de endereços back-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="7dc4d-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7dc4d-120">-BackendHttpSettings</span></span>
<span data-ttu-id="7dc4d-121">Especifica um objeto de configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="7dc4d-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7dc4d-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="7dc4d-123">Especifica uma ID de configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="7dc4d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc4d-124">-DefaultProfile</span></span>
<span data-ttu-id="7dc4d-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc4d-126">-httpListener</span><span class="sxs-lookup"><span data-stu-id="7dc4d-126">-HttpListener</span></span>
<span data-ttu-id="7dc4d-127">Especifica o objeto de ouvinte HTTP do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="7dc4d-128">-httpListenerId</span><span class="sxs-lookup"><span data-stu-id="7dc4d-128">-HttpListenerId</span></span>
<span data-ttu-id="7dc4d-129">Especifica a ID de ouvinte HTTP do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="7dc4d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="7dc4d-130">-Name</span></span>
<span data-ttu-id="7dc4d-131">Especifica o nome da regra de roteamento de solicitação que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="7dc4d-132">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="7dc4d-132">-Priority</span></span>
<span data-ttu-id="7dc4d-133">A prioridade da regra</span><span class="sxs-lookup"><span data-stu-id="7dc4d-133">The priority of the rule</span></span>

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

### <span data-ttu-id="7dc4d-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7dc4d-134">-RedirectConfiguration</span></span>
<span data-ttu-id="7dc4d-135">Redirecionamento do gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7dc4d-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="7dc4d-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7dc4d-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="7dc4d-137">ID do gateway de aplicativo RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7dc4d-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="7dc4d-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7dc4d-138">-RewriteRuleSet</span></span>
<span data-ttu-id="7dc4d-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7dc4d-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="7dc4d-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="7dc4d-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="7dc4d-141">ID do gateway de aplicativo RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7dc4d-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="7dc4d-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="7dc4d-142">-RuleType</span></span>
<span data-ttu-id="7dc4d-143">Especifica o tipo de regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="7dc4d-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="7dc4d-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="7dc4d-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="7dc4d-145">-UrlPathMapId</span></span>
<span data-ttu-id="7dc4d-146">Especifica a ID do mapa de caminho da URL para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="7dc4d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc4d-147">CommonParameters</span></span>
<span data-ttu-id="7dc4d-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dc4d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc4d-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dc4d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc4d-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="7dc4d-150">INPUTS</span></span>

### <span data-ttu-id="7dc4d-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dc4d-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7dc4d-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="7dc4d-152">OUTPUTS</span></span>

### <span data-ttu-id="7dc4d-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dc4d-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7dc4d-154">Notas</span><span class="sxs-lookup"><span data-stu-id="7dc4d-154">NOTES</span></span>

## <span data-ttu-id="7dc4d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dc4d-155">RELATED LINKS</span></span>

[<span data-ttu-id="7dc4d-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dc4d-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7dc4d-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dc4d-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7dc4d-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dc4d-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7dc4d-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dc4d-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


