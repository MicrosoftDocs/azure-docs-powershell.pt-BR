---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433505"
---
# <span data-ttu-id="5e18f-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e18f-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5e18f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e18f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e18f-103">Adiciona uma matriz de mapeamentos de caminho de URL a um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="5e18f-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5e18f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e18f-104">SYNTAX</span></span>

### <span data-ttu-id="5e18f-105">BackendSetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e18f-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e18f-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e18f-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e18f-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="5e18f-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e18f-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e18f-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e18f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e18f-109">DESCRIPTION</span></span>
<span data-ttu-id="5e18f-110">O cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** adiciona uma matriz de mapeamentos de caminho de URL a um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="5e18f-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="5e18f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e18f-111">EXAMPLES</span></span>

### <span data-ttu-id="5e18f-112">Exemplo 1: adicionar um mapeamento de caminho de URL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e18f-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="5e18f-113">O primeiro comando obtém um gateway do aplicativo chamado appGwName e o armazena em $appgw variável.</span><span class="sxs-lookup"><span data-stu-id="5e18f-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="5e18f-114">O segundo comando obtém o pool de endereços de back-end e o armazena em $pool variável.</span><span class="sxs-lookup"><span data-stu-id="5e18f-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="5e18f-115">O terceiro comando obtém as configurações de back-end http e as armazena em $poolSettings variável.</span><span class="sxs-lookup"><span data-stu-id="5e18f-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="5e18f-116">O quarto comando cria uma nova configuração de regra de caminho chamada rule01 e a armazena em $pathRule variável.</span><span class="sxs-lookup"><span data-stu-id="5e18f-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="5e18f-117">O quinto comando adiciona a configuração de mapeamento de caminho de URL chamada url01 ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e18f-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="5e18f-118">O sexto comando atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5e18f-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="5e18f-119">OS</span><span class="sxs-lookup"><span data-stu-id="5e18f-119">PARAMETERS</span></span>

### <span data-ttu-id="5e18f-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e18f-120">-ApplicationGateway</span></span>
<span data-ttu-id="5e18f-121">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="5e18f-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="5e18f-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5e18f-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5e18f-123">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="5e18f-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5e18f-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5e18f-125">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="5e18f-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5e18f-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5e18f-127">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="5e18f-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5e18f-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5e18f-129">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="5e18f-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e18f-130">-DefaultProfile</span></span>
<span data-ttu-id="5e18f-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e18f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e18f-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e18f-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5e18f-133">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5e18f-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5e18f-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5e18f-135">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5e18f-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5e18f-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="5e18f-137">Conjunto de regras de regravação padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5e18f-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="5e18f-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="5e18f-139">ID do conjunto de regras de regravação padrão do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5e18f-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e18f-140">-Name</span></span>
<span data-ttu-id="5e18f-141">Especifica o nome do mapa de caminho de URL que este cmdlet adiciona ao pool do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="5e18f-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="5e18f-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5e18f-142">-PathRules</span></span>
<span data-ttu-id="5e18f-143">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="5e18f-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="5e18f-144">As regras de caminho são sigilosas de ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="5e18f-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e18f-145">CommonParameters</span></span>
<span data-ttu-id="5e18f-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e18f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e18f-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e18f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e18f-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e18f-148">INPUTS</span></span>

### <span data-ttu-id="5e18f-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e18f-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e18f-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e18f-150">OUTPUTS</span></span>

### <span data-ttu-id="5e18f-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e18f-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e18f-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e18f-152">NOTES</span></span>

## <span data-ttu-id="5e18f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e18f-153">RELATED LINKS</span></span>

[<span data-ttu-id="5e18f-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e18f-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5e18f-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e18f-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5e18f-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e18f-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5e18f-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e18f-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


