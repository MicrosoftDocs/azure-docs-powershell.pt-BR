---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: d384d1b0db463253052ab7efa53233bdd302f496
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772212"
---
# <span data-ttu-id="5908e-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5908e-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5908e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5908e-102">SYNOPSIS</span></span>
<span data-ttu-id="5908e-103">Define a configuração de uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="5908e-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5908e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5908e-104">SYNTAX</span></span>

### <span data-ttu-id="5908e-105">BackendSetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="5908e-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5908e-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5908e-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5908e-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="5908e-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5908e-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5908e-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5908e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5908e-109">DESCRIPTION</span></span>
<span data-ttu-id="5908e-110">O cmdlet **set-AzApplicationGatewayUrlPathMapConfig** define a configuração de uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="5908e-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5908e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5908e-111">EXAMPLES</span></span>

### <span data-ttu-id="5908e-112">Exemplo 1: atualizar um mapeamento de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="5908e-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="5908e-113">O primeiro comando obtém o gateway do aplicativo chamado appGwName e armazena o resultado na variável $appgw.</span><span class="sxs-lookup"><span data-stu-id="5908e-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="5908e-114">O segundo comando atualiza o mapeamento de caminho de URL chamado map01 no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5908e-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="5908e-115">O terceiro comando atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5908e-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="5908e-116">OS</span><span class="sxs-lookup"><span data-stu-id="5908e-116">PARAMETERS</span></span>

### <span data-ttu-id="5908e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5908e-117">-ApplicationGateway</span></span>
<span data-ttu-id="5908e-118">Especifica o gateway do aplicativo para o qual esse cmdlet define uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="5908e-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="5908e-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5908e-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5908e-120">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="5908e-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5908e-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5908e-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5908e-122">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="5908e-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5908e-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5908e-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5908e-124">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="5908e-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5908e-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5908e-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5908e-126">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="5908e-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5908e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5908e-127">-DefaultProfile</span></span>
<span data-ttu-id="5908e-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5908e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5908e-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5908e-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5908e-130">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5908e-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5908e-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5908e-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5908e-132">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5908e-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5908e-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5908e-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="5908e-134">Conjunto de regras de regravação padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5908e-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="5908e-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="5908e-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="5908e-136">ID do conjunto de regras de regravação padrão do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5908e-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="5908e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="5908e-137">-Name</span></span>
<span data-ttu-id="5908e-138">Especifica o nome do mapa de caminho de URL no qual este cmdlet define a configuração.</span><span class="sxs-lookup"><span data-stu-id="5908e-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="5908e-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5908e-139">-PathRules</span></span>
<span data-ttu-id="5908e-140">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="5908e-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="5908e-141">Observe que as regras de caminho são confidenciais da ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="5908e-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="5908e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5908e-142">CommonParameters</span></span>
<span data-ttu-id="5908e-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5908e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5908e-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5908e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5908e-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5908e-145">INPUTS</span></span>

### <span data-ttu-id="5908e-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5908e-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5908e-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5908e-147">OUTPUTS</span></span>

### <span data-ttu-id="5908e-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5908e-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5908e-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5908e-149">NOTES</span></span>

## <span data-ttu-id="5908e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5908e-150">RELATED LINKS</span></span>

[<span data-ttu-id="5908e-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5908e-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5908e-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5908e-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5908e-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5908e-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5908e-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5908e-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


