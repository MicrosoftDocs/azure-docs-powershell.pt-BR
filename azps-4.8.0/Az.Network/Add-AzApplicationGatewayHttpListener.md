---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947723"
---
# <span data-ttu-id="c1b29-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c1b29-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c1b29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1b29-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b29-103">Adiciona um ouvinte HTTP a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="c1b29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1b29-104">SYNTAX</span></span>

### <span data-ttu-id="c1b29-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1b29-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1b29-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c1b29-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1b29-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1b29-107">DESCRIPTION</span></span>
<span data-ttu-id="c1b29-108">O cmdlet **Add-AzApplicationGatewayHttpListener** adiciona um ouvinte http a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="c1b29-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1b29-109">EXAMPLES</span></span>

### <span data-ttu-id="c1b29-110">Exemplo 1: adicionar um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="c1b29-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="c1b29-111">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw. O segundo comando adiciona o ouvinte HTTP ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="c1b29-112">Exemplo 2: adicionar um ouvinte HTTPS com SSL</span><span class="sxs-lookup"><span data-stu-id="c1b29-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="c1b29-113">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c1b29-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c1b29-114">O segundo comando adiciona o ouvinte, que usa o protocolo HTTPS ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="c1b29-115">Exemplo 3: adicionar um ouvinte HTTPS com SSL e nomes de host</span><span class="sxs-lookup"><span data-stu-id="c1b29-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="c1b29-116">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c1b29-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c1b29-117">O segundo comando adiciona o ouvinte, que usa o protocolo HTTPS, com certificados SSL e nomes de host, ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="c1b29-118">OS</span><span class="sxs-lookup"><span data-stu-id="c1b29-118">PARAMETERS</span></span>

### <span data-ttu-id="c1b29-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1b29-119">-ApplicationGateway</span></span>
<span data-ttu-id="c1b29-120">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona um ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1b29-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="c1b29-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1b29-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="c1b29-122">Erro de cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c1b29-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b29-123">-DefaultProfile</span></span>
<span data-ttu-id="c1b29-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b29-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b29-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c1b29-125">-FirewallPolicy</span></span>
<span data-ttu-id="c1b29-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c1b29-126">FirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c1b29-127">-FirewallPolicyId</span></span>
<span data-ttu-id="c1b29-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c1b29-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="c1b29-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1b29-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="c1b29-130">Especifica o objeto de recurso de IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-130">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c1b29-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="c1b29-132">Especifica a ID de IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="c1b29-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1b29-133">-FrontendPort</span></span>
<span data-ttu-id="c1b29-134">Especifica o objeto de porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-134">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="c1b29-135">-FrontendPortId</span></span>
<span data-ttu-id="c1b29-136">Especifica a ID da porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b29-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="c1b29-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="c1b29-137">-HostName</span></span>
<span data-ttu-id="c1b29-138">Especifica o nome do host para o qual esse cmdlet adiciona um ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1b29-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-139">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="c1b29-139">-HostNames</span></span>
<span data-ttu-id="c1b29-140">Nomes de host</span><span class="sxs-lookup"><span data-stu-id="c1b29-140">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1b29-141">-Name</span></span>
<span data-ttu-id="c1b29-142">Especifica o nome da porta de front-end que esse comando adiciona.</span><span class="sxs-lookup"><span data-stu-id="c1b29-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="c1b29-143">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="c1b29-143">-Protocol</span></span>
<span data-ttu-id="c1b29-144">Especifica o protocolo do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1b29-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="c1b29-145">Há suporte para HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c1b29-145">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="c1b29-146">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="c1b29-147">-SslCertificate</span></span>
<span data-ttu-id="c1b29-148">Especifica o certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1b29-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="c1b29-149">Deve ser especificado se HTTPS for escolhido como protocolo de escuta.</span><span class="sxs-lookup"><span data-stu-id="c1b29-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b29-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="c1b29-150">-SslCertificateId</span></span>
<span data-ttu-id="c1b29-151">Especifica a ID do certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1b29-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="c1b29-152">Deve ser especificado se HTTPS for escolhido como protocolo de escuta.</span><span class="sxs-lookup"><span data-stu-id="c1b29-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="c1b29-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b29-153">CommonParameters</span></span>
<span data-ttu-id="c1b29-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b29-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b29-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b29-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b29-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1b29-156">INPUTS</span></span>

### <span data-ttu-id="c1b29-157">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1b29-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1b29-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1b29-158">OUTPUTS</span></span>

### <span data-ttu-id="c1b29-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1b29-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1b29-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1b29-160">NOTES</span></span>

## <span data-ttu-id="c1b29-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1b29-161">RELATED LINKS</span></span>

[<span data-ttu-id="c1b29-162">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c1b29-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c1b29-163">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c1b29-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c1b29-164">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c1b29-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c1b29-165">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c1b29-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


