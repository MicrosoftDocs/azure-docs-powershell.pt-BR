---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117410"
---
# <span data-ttu-id="90ca1-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90ca1-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="90ca1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="90ca1-103">Cria uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="90ca1-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="90ca1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90ca1-104">SYNTAX</span></span>

### <span data-ttu-id="90ca1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="90ca1-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90ca1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="90ca1-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90ca1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="90ca1-107">DESCRIPTION</span></span>
<span data-ttu-id="90ca1-108">O cmdlet **Add-AzApplicationGatewayRequestRoutingRule** cria uma regra de roteamento de solicitação para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="90ca1-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="90ca1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="90ca1-109">EXAMPLES</span></span>

### <span data-ttu-id="90ca1-110">Exemplo 1: Criar uma regra de roteamento de solicitação para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="90ca1-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="90ca1-111">Esse comando cria uma regra de roteamento de solicitação básica chamada Rule01 e armazena o resultado na variável chamada $Rule.</span><span class="sxs-lookup"><span data-stu-id="90ca1-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="90ca1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90ca1-112">PARAMETERS</span></span>

### <span data-ttu-id="90ca1-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="90ca1-113">-BackendAddressPool</span></span>
<span data-ttu-id="90ca1-114">Especifica o pool de endereços back-end, como um objeto, para que a regra de roteamento de solicitação seja criar.</span><span class="sxs-lookup"><span data-stu-id="90ca1-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="90ca1-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="90ca1-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="90ca1-116">Especifica a ID do pool de endereços back-end da regra de roteamento de solicitação para criar.</span><span class="sxs-lookup"><span data-stu-id="90ca1-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="90ca1-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="90ca1-117">-BackendHttpSettings</span></span>
<span data-ttu-id="90ca1-118">Especifica as configurações HTTP de back-end, como um objeto, para que a regra de roteamento de solicitação seja criar.</span><span class="sxs-lookup"><span data-stu-id="90ca1-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="90ca1-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="90ca1-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="90ca1-120">Especifica a ID de configurações HTTP de back-end da regra de roteamento de solicitação para criar.</span><span class="sxs-lookup"><span data-stu-id="90ca1-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="90ca1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ca1-121">-DefaultProfile</span></span>
<span data-ttu-id="90ca1-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="90ca1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90ca1-123">-httpListener</span><span class="sxs-lookup"><span data-stu-id="90ca1-123">-HttpListener</span></span>
<span data-ttu-id="90ca1-124">Especifica o ouvinte HTTP de back-end para a regra de roteamento de solicitação a ser criado.</span><span class="sxs-lookup"><span data-stu-id="90ca1-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="90ca1-125">-httpListenerId</span><span class="sxs-lookup"><span data-stu-id="90ca1-125">-HttpListenerId</span></span>
<span data-ttu-id="90ca1-126">Especifica a ID de ouvinte HTTP de back-end para que a regra de roteamento de solicitação seja criar.</span><span class="sxs-lookup"><span data-stu-id="90ca1-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="90ca1-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="90ca1-127">-Name</span></span>
<span data-ttu-id="90ca1-128">Especifica o nome da regra de roteamento de solicitação que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="90ca1-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="90ca1-129">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="90ca1-129">-Priority</span></span>
<span data-ttu-id="90ca1-130">A prioridade da regra</span><span class="sxs-lookup"><span data-stu-id="90ca1-130">The priority of the rule</span></span>

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

### <span data-ttu-id="90ca1-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ca1-131">-RedirectConfiguration</span></span>
<span data-ttu-id="90ca1-132">Redirecionamento do gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="90ca1-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="90ca1-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="90ca1-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="90ca1-134">ID do gateway de aplicativo RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ca1-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="90ca1-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="90ca1-135">-RewriteRuleSet</span></span>
<span data-ttu-id="90ca1-136">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="90ca1-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="90ca1-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="90ca1-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="90ca1-138">ID do gateway de aplicativo RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="90ca1-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="90ca1-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="90ca1-139">-RuleType</span></span>
<span data-ttu-id="90ca1-140">Especifica o tipo da regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="90ca1-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="90ca1-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="90ca1-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="90ca1-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="90ca1-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="90ca1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ca1-143">CommonParameters</span></span>
<span data-ttu-id="90ca1-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ca1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ca1-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90ca1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ca1-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="90ca1-146">INPUTS</span></span>

### <span data-ttu-id="90ca1-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="90ca1-147">None</span></span>

## <span data-ttu-id="90ca1-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="90ca1-148">OUTPUTS</span></span>

### <span data-ttu-id="90ca1-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90ca1-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="90ca1-150">Notas</span><span class="sxs-lookup"><span data-stu-id="90ca1-150">NOTES</span></span>

## <span data-ttu-id="90ca1-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90ca1-151">RELATED LINKS</span></span>

[<span data-ttu-id="90ca1-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90ca1-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90ca1-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90ca1-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90ca1-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90ca1-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90ca1-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90ca1-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


