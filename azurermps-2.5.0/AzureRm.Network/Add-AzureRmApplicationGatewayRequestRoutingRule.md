---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: fdbbb28d69d5094b52d8ac7340839fa570bce55d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785341"
---
# <span data-ttu-id="2bd46-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2bd46-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2bd46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bd46-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd46-103">Adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bd46-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bd46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bd46-104">SYNTAX</span></span>

### <span data-ttu-id="2bd46-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd46-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bd46-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2bd46-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bd46-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bd46-107">DESCRIPTION</span></span>
<span data-ttu-id="2bd46-108">O cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bd46-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="2bd46-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bd46-109">EXAMPLES</span></span>

### <span data-ttu-id="2bd46-110">Exemplo 1: adicionar uma regra de roteamento de solicitação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2bd46-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="2bd46-111">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2bd46-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2bd46-112">O segundo comando adiciona a regra de roteamento de solicitação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bd46-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="2bd46-113">OS</span><span class="sxs-lookup"><span data-stu-id="2bd46-113">PARAMETERS</span></span>

### <span data-ttu-id="2bd46-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bd46-114">-ApplicationGateway</span></span>
<span data-ttu-id="2bd46-115">Especifica um gateway de aplicativo para o qual esse cmdlet adiciona uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="2bd46-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="2bd46-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2bd46-116">-BackendAddressPool</span></span>
<span data-ttu-id="2bd46-117">Especifica um objeto de pool de endereços back-end do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2bd46-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2bd46-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="2bd46-119">Especifica uma ID do pool de endereços back-end do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="2bd46-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2bd46-120">-BackendHttpSettings</span></span>
<span data-ttu-id="2bd46-121">Especifica um objeto de configurações HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bd46-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2bd46-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="2bd46-123">Especifica uma ID de configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bd46-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd46-124">-DefaultProfile</span></span>
<span data-ttu-id="2bd46-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd46-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bd46-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="2bd46-126">-HttpListener</span></span>
<span data-ttu-id="2bd46-127">Especifica o objeto ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2bd46-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-128">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="2bd46-128">-HttpListenerId</span></span>
<span data-ttu-id="2bd46-129">Especifica a ID do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2bd46-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bd46-130">-Name</span></span>
<span data-ttu-id="2bd46-131">Especifica o nome da regra de roteamento de solicitação que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="2bd46-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bd46-132">-RedirectConfiguration</span></span>
<span data-ttu-id="2bd46-133">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2bd46-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2bd46-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="2bd46-135">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bd46-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="2bd46-136">-RuleType</span></span>
<span data-ttu-id="2bd46-137">Especifica o tipo de regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="2bd46-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2bd46-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="2bd46-139">-UrlPathMapId</span></span>
<span data-ttu-id="2bd46-140">Especifica a ID do mapa de caminho da URL para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="2bd46-140">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd46-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd46-141">CommonParameters</span></span>
<span data-ttu-id="2bd46-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd46-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd46-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd46-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd46-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bd46-144">INPUTS</span></span>

### <span data-ttu-id="2bd46-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2bd46-145">System.String</span></span>

## <span data-ttu-id="2bd46-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bd46-146">OUTPUTS</span></span>

### <span data-ttu-id="2bd46-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bd46-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2bd46-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bd46-148">NOTES</span></span>

## <span data-ttu-id="2bd46-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bd46-149">RELATED LINKS</span></span>

[<span data-ttu-id="2bd46-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2bd46-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2bd46-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2bd46-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2bd46-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2bd46-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2bd46-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2bd46-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


