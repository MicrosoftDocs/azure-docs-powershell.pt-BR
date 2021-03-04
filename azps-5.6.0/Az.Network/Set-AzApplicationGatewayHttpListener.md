---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91e8aef2e5d12a13648132a1c8d6ece9dc4d21cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890595"
---
# <span data-ttu-id="87345-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="87345-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="87345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87345-102">SYNOPSIS</span></span>
<span data-ttu-id="87345-103">Modifica um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87345-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="87345-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="87345-104">SYNTAX</span></span>

### <span data-ttu-id="87345-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="87345-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87345-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="87345-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87345-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="87345-107">DESCRIPTION</span></span>
<span data-ttu-id="87345-108">O cmdlet **Set-AzApplicationGatewayHttpListener** modifica um ouvinte HTTP para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="87345-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="87345-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87345-109">EXAMPLES</span></span>

### <span data-ttu-id="87345-110">Exemplo 1: Definir um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="87345-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="87345-111">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="87345-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="87345-112">O segundo comando define o ouvinte HTTP do gateway para usar a configuração front-end armazenada em $FIP 01 com o protocolo HTTP na porta 80.</span><span class="sxs-lookup"><span data-stu-id="87345-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="87345-113">Exemplo 2: Adicionar um ouvinte HTTPS com SSL e HostNames</span><span class="sxs-lookup"><span data-stu-id="87345-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="87345-114">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="87345-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="87345-115">O segundo comando adiciona o ouvinte, que usa o protocolo HTTPS, com Certificados SSL e HostNames, ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87345-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="87345-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="87345-116">PARAMETERS</span></span>

### <span data-ttu-id="87345-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87345-117">-ApplicationGateway</span></span>
<span data-ttu-id="87345-118">Especifica o gateway de aplicativo com o qual esse cmdlet associa o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="87345-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="87345-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="87345-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="87345-120">Erro do cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="87345-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="87345-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87345-121">-DefaultProfile</span></span>
<span data-ttu-id="87345-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="87345-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87345-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="87345-123">-FirewallPolicy</span></span>
<span data-ttu-id="87345-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="87345-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="87345-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="87345-125">-FirewallPolicyId</span></span>
<span data-ttu-id="87345-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="87345-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="87345-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="87345-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="87345-128">Especifica o endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87345-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="87345-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="87345-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="87345-130">Especifica a ID do endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87345-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="87345-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="87345-131">-FrontendPort</span></span>
<span data-ttu-id="87345-132">Especifica a porta front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87345-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="87345-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="87345-133">-FrontendPortId</span></span>
<span data-ttu-id="87345-134">Especifica a ID da porta front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87345-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="87345-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="87345-135">-HostName</span></span>
<span data-ttu-id="87345-136">Especifica o nome do host para o que este cmdlet envia o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="87345-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="87345-137">-HostNames</span><span class="sxs-lookup"><span data-stu-id="87345-137">-HostNames</span></span>
<span data-ttu-id="87345-138">Nomes de host</span><span class="sxs-lookup"><span data-stu-id="87345-138">Host names</span></span>

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

### <span data-ttu-id="87345-139">-Name</span><span class="sxs-lookup"><span data-stu-id="87345-139">-Name</span></span>
<span data-ttu-id="87345-140">Especifica o nome do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="87345-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="87345-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="87345-141">-Protocol</span></span>
<span data-ttu-id="87345-142">Especifica o protocolo que o ouvinte HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="87345-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="87345-143">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="87345-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87345-144">Http</span><span class="sxs-lookup"><span data-stu-id="87345-144">Http</span></span>
- <span data-ttu-id="87345-145">Https</span><span class="sxs-lookup"><span data-stu-id="87345-145">Https</span></span>

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

### <span data-ttu-id="87345-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="87345-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="87345-147">Especifica se o cmdlet requer uma indicação de nome de servidor.</span><span class="sxs-lookup"><span data-stu-id="87345-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="87345-148">Os valores aceitáveis para este parâmetro são: true ou false.</span><span class="sxs-lookup"><span data-stu-id="87345-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="87345-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="87345-149">-SslCertificate</span></span>
<span data-ttu-id="87345-150">Especifica o certificado SSL do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="87345-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="87345-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="87345-151">-SslCertificateId</span></span>
<span data-ttu-id="87345-152">Especifica a ID de certificado SSL do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="87345-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="87345-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="87345-153">-SslProfile</span></span>
<span data-ttu-id="87345-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="87345-154">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87345-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="87345-155">-SslProfileId</span></span>
<span data-ttu-id="87345-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="87345-156">SslProfileId</span></span>

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

### <span data-ttu-id="87345-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87345-157">CommonParameters</span></span>
<span data-ttu-id="87345-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87345-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87345-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87345-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87345-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87345-160">INPUTS</span></span>

### <span data-ttu-id="87345-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87345-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="87345-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="87345-162">OUTPUTS</span></span>

### <span data-ttu-id="87345-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87345-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="87345-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="87345-164">NOTES</span></span>

## <span data-ttu-id="87345-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87345-165">RELATED LINKS</span></span>

[<span data-ttu-id="87345-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="87345-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="87345-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="87345-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="87345-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="87345-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="87345-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="87345-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


