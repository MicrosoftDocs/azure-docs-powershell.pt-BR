---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cc2a30e5a5633dcda345184bef121befe710ad8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885403"
---
# <span data-ttu-id="26a23-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26a23-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="26a23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26a23-102">SYNOPSIS</span></span>
<span data-ttu-id="26a23-103">Define a configuração de uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="26a23-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="26a23-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="26a23-104">SYNTAX</span></span>

### <span data-ttu-id="26a23-105">BackendSetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="26a23-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26a23-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26a23-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26a23-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="26a23-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26a23-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26a23-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26a23-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="26a23-109">DESCRIPTION</span></span>
<span data-ttu-id="26a23-110">O cmdlet **Set-AzApplicationGatewayUrlPathMapConfig** define a configuração de uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="26a23-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="26a23-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26a23-111">EXAMPLES</span></span>

### <span data-ttu-id="26a23-112">Exemplo 1: atualizar um mapeamento de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="26a23-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="26a23-113">O primeiro comando obtém o gateway de aplicativo chamado appGwName e armazena o resultado na $appgw variável.</span><span class="sxs-lookup"><span data-stu-id="26a23-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="26a23-114">O segundo comando atualiza o mapeamento de caminho da URL chamado map01 no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26a23-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="26a23-115">O terceiro comando atualiza o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26a23-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="26a23-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="26a23-116">PARAMETERS</span></span>

### <span data-ttu-id="26a23-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26a23-117">-ApplicationGateway</span></span>
<span data-ttu-id="26a23-118">Especifica o gateway de aplicativo para o qual este cmdlet define uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="26a23-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="26a23-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="26a23-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="26a23-120">Especifica o pool de endereços de back-end padrão a ser roteado no caso de nenhuma das regras especificadas no *parâmetro pathRules* corresponder.</span><span class="sxs-lookup"><span data-stu-id="26a23-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="26a23-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="26a23-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="26a23-122">Especifica a ID padrão do pool de endereços de back-end.</span><span class="sxs-lookup"><span data-stu-id="26a23-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="26a23-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="26a23-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="26a23-124">Especifica as configurações HTTP de back-end padrão a ser usadas no caso de nenhuma das regras especificadas no *parâmetro pathRules* corresponder.</span><span class="sxs-lookup"><span data-stu-id="26a23-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="26a23-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="26a23-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="26a23-126">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="26a23-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="26a23-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a23-127">-DefaultProfile</span></span>
<span data-ttu-id="26a23-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="26a23-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26a23-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26a23-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="26a23-130">RedirectConfiguration padrão do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="26a23-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="26a23-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="26a23-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="26a23-132">ID do gateway de aplicativo RedirectConfiguration padrão</span><span class="sxs-lookup"><span data-stu-id="26a23-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="26a23-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26a23-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="26a23-134">Conjunto de regras de regra de regra padrão do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="26a23-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="26a23-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="26a23-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="26a23-136">ID do conjunto de regras de regra de regra padrão do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="26a23-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="26a23-137">-Name</span><span class="sxs-lookup"><span data-stu-id="26a23-137">-Name</span></span>
<span data-ttu-id="26a23-138">Especifica o nome do mapa do caminho da URL para o qual este cmdlet define a configuração.</span><span class="sxs-lookup"><span data-stu-id="26a23-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="26a23-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="26a23-139">-PathRules</span></span>
<span data-ttu-id="26a23-140">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="26a23-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="26a23-141">Observe que as regras de caminho são confidenciais de ordem, elas são aplicadas para que sejam especificadas.</span><span class="sxs-lookup"><span data-stu-id="26a23-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="26a23-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a23-142">CommonParameters</span></span>
<span data-ttu-id="26a23-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a23-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a23-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26a23-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a23-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26a23-145">INPUTS</span></span>

### <span data-ttu-id="26a23-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26a23-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26a23-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="26a23-147">OUTPUTS</span></span>

### <span data-ttu-id="26a23-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26a23-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26a23-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="26a23-149">NOTES</span></span>

## <span data-ttu-id="26a23-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26a23-150">RELATED LINKS</span></span>

[<span data-ttu-id="26a23-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26a23-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26a23-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26a23-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26a23-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26a23-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26a23-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26a23-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


