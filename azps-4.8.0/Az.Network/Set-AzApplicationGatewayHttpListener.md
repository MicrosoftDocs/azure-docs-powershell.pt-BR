---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 3cc9af0865ca47099f5617cc1e94f3232ed9bdb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114330"
---
# <span data-ttu-id="a152a-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a152a-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a152a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a152a-102">SYNOPSIS</span></span>
<span data-ttu-id="a152a-103">Modifica um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a152a-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="a152a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a152a-104">SYNTAX</span></span>

### <span data-ttu-id="a152a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a152a-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a152a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a152a-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a152a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a152a-107">DESCRIPTION</span></span>
<span data-ttu-id="a152a-108">O cmdlet **set-AzApplicationGatewayHttpListener** modifica um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="a152a-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a152a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a152a-109">EXAMPLES</span></span>

### <span data-ttu-id="a152a-110">Exemplo 1: definir um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="a152a-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="a152a-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a152a-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a152a-112">O segundo comando define o ouvinte HTTP do gateway para usar a configuração de front-end armazenada em $FIP 01 com o protocolo HTTP na porta 80.</span><span class="sxs-lookup"><span data-stu-id="a152a-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="a152a-113">Exemplo 2: adicionar um ouvinte HTTPS com SSL e nomes de host</span><span class="sxs-lookup"><span data-stu-id="a152a-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="a152a-114">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a152a-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a152a-115">O segundo comando adiciona o ouvinte, que usa o protocolo HTTPS, com certificados SSL e nomes de host, ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a152a-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="a152a-116">OS</span><span class="sxs-lookup"><span data-stu-id="a152a-116">PARAMETERS</span></span>

### <span data-ttu-id="a152a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a152a-117">-ApplicationGateway</span></span>
<span data-ttu-id="a152a-118">Especifica o gateway do aplicativo com o qual esse cmdlet associa o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="a152a-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="a152a-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="a152a-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="a152a-120">Erro de cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a152a-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="a152a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a152a-121">-DefaultProfile</span></span>
<span data-ttu-id="a152a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a152a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a152a-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a152a-123">-FirewallPolicy</span></span>
<span data-ttu-id="a152a-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a152a-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="a152a-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="a152a-125">-FirewallPolicyId</span></span>
<span data-ttu-id="a152a-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="a152a-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="a152a-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a152a-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a152a-128">Especifica o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a152a-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a152a-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a152a-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a152a-130">Especifica a ID do endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a152a-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a152a-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a152a-131">-FrontendPort</span></span>
<span data-ttu-id="a152a-132">Especifica a porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a152a-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="a152a-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a152a-133">-FrontendPortId</span></span>
<span data-ttu-id="a152a-134">Especifica a ID da porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a152a-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="a152a-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="a152a-135">-HostName</span></span>
<span data-ttu-id="a152a-136">Especifica o nome do host para o qual esse cmdlet envia o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="a152a-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="a152a-137">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="a152a-137">-HostNames</span></span>
<span data-ttu-id="a152a-138">Nomes de host</span><span class="sxs-lookup"><span data-stu-id="a152a-138">Host names</span></span>

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

### <span data-ttu-id="a152a-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="a152a-139">-Name</span></span>
<span data-ttu-id="a152a-140">Especifica o nome do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="a152a-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="a152a-141">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="a152a-141">-Protocol</span></span>
<span data-ttu-id="a152a-142">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="a152a-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="a152a-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a152a-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a152a-144">Http</span><span class="sxs-lookup"><span data-stu-id="a152a-144">Http</span></span>
- <span data-ttu-id="a152a-145">Https</span><span class="sxs-lookup"><span data-stu-id="a152a-145">Https</span></span>

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

### <span data-ttu-id="a152a-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a152a-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="a152a-147">Especifica se o cmdlet requer uma indicação de nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a152a-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="a152a-148">Os valores aceitáveis para esse parâmetro são: true ou false.</span><span class="sxs-lookup"><span data-stu-id="a152a-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="a152a-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a152a-149">-SslCertificate</span></span>
<span data-ttu-id="a152a-150">Especifica o certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a152a-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="a152a-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a152a-151">-SslCertificateId</span></span>
<span data-ttu-id="a152a-152">Especifica a ID do certificado SSL (Secure Socket Layer) da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a152a-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="a152a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a152a-153">CommonParameters</span></span>
<span data-ttu-id="a152a-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a152a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a152a-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a152a-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a152a-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a152a-156">INPUTS</span></span>

### <span data-ttu-id="a152a-157">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a152a-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a152a-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a152a-158">OUTPUTS</span></span>

### <span data-ttu-id="a152a-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a152a-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a152a-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a152a-160">NOTES</span></span>

## <span data-ttu-id="a152a-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a152a-161">RELATED LINKS</span></span>

[<span data-ttu-id="a152a-162">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a152a-162">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a152a-163">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a152a-163">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a152a-164">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a152a-164">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a152a-165">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a152a-165">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


