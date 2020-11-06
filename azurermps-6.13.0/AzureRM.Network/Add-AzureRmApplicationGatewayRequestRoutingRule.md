---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 58ea4a4dc15a74f3f3e1f7360ec2be370b440a40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609774"
---
# <span data-ttu-id="e76af-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e76af-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e76af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e76af-102">SYNOPSIS</span></span>
<span data-ttu-id="e76af-103">Adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e76af-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e76af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e76af-104">SYNTAX</span></span>

### <span data-ttu-id="e76af-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e76af-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e76af-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e76af-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e76af-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e76af-107">DESCRIPTION</span></span>
<span data-ttu-id="e76af-108">O cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e76af-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="e76af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e76af-109">EXAMPLES</span></span>

### <span data-ttu-id="e76af-110">Exemplo 1: adicionar uma regra de roteamento de solicitação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e76af-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e76af-111">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e76af-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e76af-112">O segundo comando adiciona a regra de roteamento de solicitação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e76af-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="e76af-113">OS</span><span class="sxs-lookup"><span data-stu-id="e76af-113">PARAMETERS</span></span>

### <span data-ttu-id="e76af-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e76af-114">-ApplicationGateway</span></span>
<span data-ttu-id="e76af-115">Especifica um gateway de aplicativo para o qual esse cmdlet adiciona uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="e76af-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="e76af-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e76af-116">-BackendAddressPool</span></span>
<span data-ttu-id="e76af-117">Especifica um objeto de pool de endereços back-end do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e76af-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="e76af-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e76af-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="e76af-119">Especifica uma ID do pool de endereços back-end do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="e76af-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="e76af-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e76af-120">-BackendHttpSettings</span></span>
<span data-ttu-id="e76af-121">Especifica um objeto de configurações HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e76af-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="e76af-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e76af-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e76af-123">Especifica uma ID de configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e76af-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="e76af-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76af-124">-DefaultProfile</span></span>
<span data-ttu-id="e76af-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e76af-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76af-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e76af-126">-HttpListener</span></span>
<span data-ttu-id="e76af-127">Especifica o objeto ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e76af-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="e76af-128">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="e76af-128">-HttpListenerId</span></span>
<span data-ttu-id="e76af-129">Especifica a ID do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e76af-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="e76af-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="e76af-130">-Name</span></span>
<span data-ttu-id="e76af-131">Especifica o nome da regra de roteamento de solicitação que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="e76af-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="e76af-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e76af-132">-RedirectConfiguration</span></span>
<span data-ttu-id="e76af-133">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e76af-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e76af-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e76af-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="e76af-135">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e76af-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e76af-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e76af-136">-RuleType</span></span>
<span data-ttu-id="e76af-137">Especifica o tipo de regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="e76af-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="e76af-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e76af-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="e76af-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="e76af-139">-UrlPathMapId</span></span>
<span data-ttu-id="e76af-140">Especifica a ID do mapa de caminho da URL para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e76af-140">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="e76af-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76af-141">CommonParameters</span></span>
<span data-ttu-id="e76af-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e76af-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76af-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e76af-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76af-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e76af-144">INPUTS</span></span>

### <span data-ttu-id="e76af-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e76af-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e76af-146">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e76af-146">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e76af-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e76af-147">OUTPUTS</span></span>

### <span data-ttu-id="e76af-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e76af-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e76af-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e76af-149">NOTES</span></span>

## <span data-ttu-id="e76af-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e76af-150">RELATED LINKS</span></span>

[<span data-ttu-id="e76af-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e76af-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e76af-152">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e76af-152">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e76af-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e76af-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e76af-154">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e76af-154">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


