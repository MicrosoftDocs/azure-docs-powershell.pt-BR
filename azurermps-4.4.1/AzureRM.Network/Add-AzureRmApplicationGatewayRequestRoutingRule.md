---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f72fb4eb80475b421ca4a893a598d8686dde64c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433083"
---
# <span data-ttu-id="766fb-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="766fb-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="766fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="766fb-102">SYNOPSIS</span></span>
<span data-ttu-id="766fb-103">Adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="766fb-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="766fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="766fb-104">SYNTAX</span></span>

### <span data-ttu-id="766fb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="766fb-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="766fb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="766fb-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="766fb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="766fb-107">DESCRIPTION</span></span>
<span data-ttu-id="766fb-108">O cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="766fb-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="766fb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="766fb-109">EXAMPLES</span></span>

### <span data-ttu-id="766fb-110">Exemplo 1: adicionar uma regra de roteamento de solicitação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="766fb-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="766fb-111">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="766fb-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="766fb-112">O segundo comando adiciona a regra de roteamento de solicitação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="766fb-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="766fb-113">OS</span><span class="sxs-lookup"><span data-stu-id="766fb-113">PARAMETERS</span></span>

### <span data-ttu-id="766fb-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="766fb-114">-ApplicationGateway</span></span>
<span data-ttu-id="766fb-115">Especifica um gateway de aplicativo para o qual esse cmdlet adiciona uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="766fb-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="766fb-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="766fb-116">-BackendAddressPool</span></span>
<span data-ttu-id="766fb-117">Especifica um objeto de pool de endereços back-end do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="766fb-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="766fb-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="766fb-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="766fb-119">Especifica uma ID do pool de endereços back-end do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="766fb-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="766fb-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="766fb-120">-BackendHttpSettings</span></span>
<span data-ttu-id="766fb-121">Especifica um objeto de configurações HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="766fb-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="766fb-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="766fb-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="766fb-123">Especifica uma ID de configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="766fb-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="766fb-124">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="766fb-124">-HttpListener</span></span>
<span data-ttu-id="766fb-125">Especifica o objeto ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="766fb-125">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="766fb-126">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="766fb-126">-HttpListenerId</span></span>
<span data-ttu-id="766fb-127">Especifica a ID do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="766fb-127">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="766fb-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="766fb-128">-Name</span></span>
<span data-ttu-id="766fb-129">Especifica o nome da regra de roteamento de solicitação que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="766fb-129">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="766fb-130">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="766fb-130">-RedirectConfiguration</span></span>
<span data-ttu-id="766fb-131">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="766fb-131">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="766fb-132">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="766fb-132">-RedirectConfigurationId</span></span>
<span data-ttu-id="766fb-133">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="766fb-133">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="766fb-134">-RuleType</span><span class="sxs-lookup"><span data-stu-id="766fb-134">-RuleType</span></span>
<span data-ttu-id="766fb-135">Especifica o tipo de regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="766fb-135">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="766fb-136">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="766fb-136">-UrlPathMap</span></span>
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

### <span data-ttu-id="766fb-137">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="766fb-137">-UrlPathMapId</span></span>
<span data-ttu-id="766fb-138">Especifica a ID do mapa de caminho da URL para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="766fb-138">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="766fb-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766fb-139">-DefaultProfile</span></span>
<span data-ttu-id="766fb-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="766fb-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="766fb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766fb-141">CommonParameters</span></span>
<span data-ttu-id="766fb-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="766fb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766fb-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="766fb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766fb-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="766fb-144">INPUTS</span></span>

### <span data-ttu-id="766fb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="766fb-145">System.String</span></span>

## <span data-ttu-id="766fb-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="766fb-146">OUTPUTS</span></span>

### <span data-ttu-id="766fb-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="766fb-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="766fb-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="766fb-148">NOTES</span></span>

## <span data-ttu-id="766fb-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="766fb-149">RELATED LINKS</span></span>

[<span data-ttu-id="766fb-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="766fb-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="766fb-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="766fb-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="766fb-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="766fb-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="766fb-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="766fb-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


