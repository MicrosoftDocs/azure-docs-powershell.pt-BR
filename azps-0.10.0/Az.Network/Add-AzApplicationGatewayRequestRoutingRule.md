---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 32695204a153d04643063f4d991b577e619edcea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775649"
---
# <span data-ttu-id="60829-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="60829-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="60829-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60829-102">SYNOPSIS</span></span>
<span data-ttu-id="60829-103">Adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60829-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="60829-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60829-104">SYNTAX</span></span>

### <span data-ttu-id="60829-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="60829-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60829-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="60829-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60829-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60829-107">DESCRIPTION</span></span>
<span data-ttu-id="60829-108">O cmdlet **Add-AzApplicationGatewayRequestRoutingRule** adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60829-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="60829-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60829-109">EXAMPLES</span></span>

### <span data-ttu-id="60829-110">Exemplo 1: adicionar uma regra de roteamento de solicitação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="60829-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="60829-111">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="60829-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="60829-112">O segundo comando adiciona a regra de roteamento de solicitação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60829-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="60829-113">OS</span><span class="sxs-lookup"><span data-stu-id="60829-113">PARAMETERS</span></span>

### <span data-ttu-id="60829-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60829-114">-ApplicationGateway</span></span>
<span data-ttu-id="60829-115">Especifica um gateway de aplicativo para o qual esse cmdlet adiciona uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="60829-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="60829-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="60829-116">-BackendAddressPool</span></span>
<span data-ttu-id="60829-117">Especifica um objeto de pool de endereços back-end do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="60829-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="60829-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="60829-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="60829-119">Especifica uma ID do pool de endereços back-end do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="60829-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="60829-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="60829-120">-BackendHttpSettings</span></span>
<span data-ttu-id="60829-121">Especifica um objeto de configurações HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60829-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="60829-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="60829-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="60829-123">Especifica uma ID de configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60829-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="60829-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60829-124">-DefaultProfile</span></span>
<span data-ttu-id="60829-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60829-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60829-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="60829-126">-HttpListener</span></span>
<span data-ttu-id="60829-127">Especifica o objeto ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="60829-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="60829-128">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="60829-128">-HttpListenerId</span></span>
<span data-ttu-id="60829-129">Especifica a ID do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="60829-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="60829-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="60829-130">-Name</span></span>
<span data-ttu-id="60829-131">Especifica o nome da regra de roteamento de solicitação que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="60829-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="60829-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="60829-132">-RedirectConfiguration</span></span>
<span data-ttu-id="60829-133">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="60829-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="60829-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="60829-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="60829-135">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="60829-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="60829-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="60829-136">-RuleType</span></span>
<span data-ttu-id="60829-137">Especifica o tipo de regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="60829-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="60829-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="60829-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="60829-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="60829-139">-UrlPathMapId</span></span>
<span data-ttu-id="60829-140">Especifica a ID do mapa de caminho da URL para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="60829-140">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="60829-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60829-141">CommonParameters</span></span>
<span data-ttu-id="60829-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60829-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60829-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60829-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60829-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60829-144">INPUTS</span></span>

### <span data-ttu-id="60829-145">System. String</span><span class="sxs-lookup"><span data-stu-id="60829-145">System.String</span></span>

## <span data-ttu-id="60829-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60829-146">OUTPUTS</span></span>

### <span data-ttu-id="60829-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60829-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="60829-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60829-148">NOTES</span></span>

## <span data-ttu-id="60829-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60829-149">RELATED LINKS</span></span>

[<span data-ttu-id="60829-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="60829-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="60829-151">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="60829-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="60829-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="60829-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="60829-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="60829-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

