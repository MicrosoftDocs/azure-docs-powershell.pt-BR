---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 53963e7672881255cf23df99e53a1471c3c42250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892943"
---
# <span data-ttu-id="9c6de-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c6de-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="9c6de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c6de-102">SYNOPSIS</span></span>
<span data-ttu-id="9c6de-103">Cria uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c6de-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="9c6de-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9c6de-104">SYNTAX</span></span>

### <span data-ttu-id="9c6de-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c6de-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c6de-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9c6de-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c6de-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9c6de-107">DESCRIPTION</span></span>
<span data-ttu-id="9c6de-108">O cmdlet **Add-AzApplicationGatewayRequestRoutingRule** cria uma regra de roteamento de solicitação para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c6de-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="9c6de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c6de-109">EXAMPLES</span></span>

### <span data-ttu-id="9c6de-110">Exemplo 1: Criar uma regra de roteamento de solicitação para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9c6de-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="9c6de-111">Este comando cria uma regra básica de roteamento de solicitação chamada Rule01 e armazena o resultado na variável chamada $Rule.</span><span class="sxs-lookup"><span data-stu-id="9c6de-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="9c6de-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9c6de-112">PARAMETERS</span></span>

### <span data-ttu-id="9c6de-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c6de-113">-BackendAddressPool</span></span>
<span data-ttu-id="9c6de-114">Especifica o pool de endereços back-end, como um objeto, para que a regra de roteamento de solicitação seja criado.</span><span class="sxs-lookup"><span data-stu-id="9c6de-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="9c6de-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9c6de-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="9c6de-116">Especifica a ID do pool de endereços back-end da regra de roteamento de solicitação a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9c6de-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="9c6de-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9c6de-117">-BackendHttpSettings</span></span>
<span data-ttu-id="9c6de-118">Especifica as configurações HTTP de back-end, como um objeto, para que a regra de roteamento de solicitação seja criado.</span><span class="sxs-lookup"><span data-stu-id="9c6de-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="9c6de-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="9c6de-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="9c6de-120">Especifica a ID de configurações HTTP de back-end da regra de roteamento de solicitação a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9c6de-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="9c6de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c6de-121">-DefaultProfile</span></span>
<span data-ttu-id="9c6de-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9c6de-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c6de-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="9c6de-123">-HttpListener</span></span>
<span data-ttu-id="9c6de-124">Especifica o ouvinte HTTP de back-end para a regra de roteamento de solicitação a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9c6de-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="9c6de-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="9c6de-125">-HttpListenerId</span></span>
<span data-ttu-id="9c6de-126">Especifica a ID de ouvinte HTTP de back-end para a regra de roteamento de solicitação a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9c6de-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="9c6de-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9c6de-127">-Name</span></span>
<span data-ttu-id="9c6de-128">Especifica o nome da regra de roteamento de solicitação que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="9c6de-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9c6de-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="9c6de-129">-Priority</span></span>
<span data-ttu-id="9c6de-130">A prioridade da regra</span><span class="sxs-lookup"><span data-stu-id="9c6de-130">The priority of the rule</span></span>

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

### <span data-ttu-id="9c6de-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c6de-131">-RedirectConfiguration</span></span>
<span data-ttu-id="9c6de-132">RedirectConfiguration do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9c6de-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="9c6de-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9c6de-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="9c6de-134">ID do gateway de aplicativo RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c6de-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="9c6de-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c6de-135">-RewriteRuleSet</span></span>
<span data-ttu-id="9c6de-136">Reescrita do gateway de aplicativoRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c6de-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9c6de-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="9c6de-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="9c6de-138">ID do gateway de aplicativos RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c6de-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9c6de-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="9c6de-139">-RuleType</span></span>
<span data-ttu-id="9c6de-140">Especifica o tipo da regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c6de-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="9c6de-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="9c6de-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="9c6de-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="9c6de-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="9c6de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c6de-143">CommonParameters</span></span>
<span data-ttu-id="9c6de-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c6de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c6de-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c6de-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c6de-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c6de-146">INPUTS</span></span>

### <span data-ttu-id="9c6de-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9c6de-147">None</span></span>

## <span data-ttu-id="9c6de-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9c6de-148">OUTPUTS</span></span>

### <span data-ttu-id="9c6de-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c6de-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="9c6de-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="9c6de-150">NOTES</span></span>

## <span data-ttu-id="9c6de-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c6de-151">RELATED LINKS</span></span>

[<span data-ttu-id="9c6de-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c6de-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9c6de-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c6de-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9c6de-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c6de-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="9c6de-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c6de-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


