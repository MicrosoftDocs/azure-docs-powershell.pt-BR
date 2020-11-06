---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95e46bfc1f90f4e9760077b11f52d8020cb7f409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440314"
---
# <span data-ttu-id="6a14d-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a14d-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6a14d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a14d-102">SYNOPSIS</span></span>
<span data-ttu-id="6a14d-103">Modifica uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a14d-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a14d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a14d-104">SYNTAX</span></span>

### <span data-ttu-id="6a14d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a14d-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a14d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6a14d-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a14d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a14d-107">DESCRIPTION</span></span>
<span data-ttu-id="6a14d-108">O cmdlet **set-AzureRmApplicationGatewayRequestRoutingRule** modifica uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="6a14d-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="6a14d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a14d-109">EXAMPLES</span></span>

### <span data-ttu-id="6a14d-110">Exemplo 1: atualizar uma regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="6a14d-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6a14d-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6a14d-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6a14d-112">O segundo comando modifica a regra de roteamento de solicitação do Application Gateway para usar as configurações HTTP de back-end especificadas na variável $Setting, um ouvinte HTTP especificado na variável $Listener e um pool de endereços back-end especificado na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="6a14d-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="6a14d-113">OS</span><span class="sxs-lookup"><span data-stu-id="6a14d-113">PARAMETERS</span></span>

### <span data-ttu-id="6a14d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a14d-114">-ApplicationGateway</span></span>
<span data-ttu-id="6a14d-115">Especifica o objeto do gateway do aplicativo com o qual esse cmdlet associa uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="6a14d-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="6a14d-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a14d-116">-BackendAddressPool</span></span>
<span data-ttu-id="6a14d-117">Especifica o pool de endereços back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a14d-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="6a14d-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6a14d-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6a14d-119">Especifica a ID do pool de endereços de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a14d-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="6a14d-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6a14d-120">-BackendHttpSettings</span></span>
<span data-ttu-id="6a14d-121">Especifica as configurações HTTP de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a14d-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="6a14d-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6a14d-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6a14d-123">Especifica a ID de configurações HTTP de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a14d-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="6a14d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a14d-124">-DefaultProfile</span></span>
<span data-ttu-id="6a14d-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a14d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a14d-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="6a14d-126">-HttpListener</span></span>
<span data-ttu-id="6a14d-127">Especifica o ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6a14d-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="6a14d-128">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="6a14d-128">-HttpListenerId</span></span>
<span data-ttu-id="6a14d-129">Especifica a ID do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6a14d-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="6a14d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a14d-130">-Name</span></span>
<span data-ttu-id="6a14d-131">Especifica o nome da regra de roteamento de solicitação que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="6a14d-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6a14d-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a14d-132">-RedirectConfiguration</span></span>
<span data-ttu-id="6a14d-133">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="6a14d-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6a14d-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6a14d-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="6a14d-135">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a14d-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6a14d-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6a14d-136">-RuleType</span></span>
<span data-ttu-id="6a14d-137">Especifica o tipo de regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="6a14d-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="6a14d-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6a14d-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="6a14d-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6a14d-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6a14d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a14d-140">CommonParameters</span></span>
<span data-ttu-id="6a14d-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a14d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a14d-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a14d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a14d-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a14d-143">INPUTS</span></span>

### <span data-ttu-id="6a14d-144">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a14d-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="6a14d-145">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6a14d-145">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="6a14d-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a14d-146">OUTPUTS</span></span>

### <span data-ttu-id="6a14d-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a14d-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a14d-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a14d-148">NOTES</span></span>

## <span data-ttu-id="6a14d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a14d-149">RELATED LINKS</span></span>

[<span data-ttu-id="6a14d-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a14d-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6a14d-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a14d-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6a14d-152">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a14d-152">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6a14d-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a14d-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


