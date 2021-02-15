---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 8ce5d01d78b8b434e062b0f33ee41a4cbbce20ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114105"
---
# <span data-ttu-id="31a42-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="31a42-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="31a42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31a42-102">SYNOPSIS</span></span>
<span data-ttu-id="31a42-103">Modifica um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31a42-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="31a42-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31a42-104">SYNTAX</span></span>

### <span data-ttu-id="31a42-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="31a42-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31a42-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="31a42-106">SetByResource</span></span>
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

## <span data-ttu-id="31a42-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="31a42-107">DESCRIPTION</span></span>
<span data-ttu-id="31a42-108">O cmdlet **Set-AzApplicationGatewayHttpListener** modifica um ouvinte HTTP para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="31a42-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="31a42-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31a42-109">EXAMPLES</span></span>

### <span data-ttu-id="31a42-110">Exemplo 1: Definir um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="31a42-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="31a42-111">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="31a42-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="31a42-112">O segundo comando define o ouvinte HTTP do gateway para usar a configuração front-end armazenada no $FIP 01 com o protocolo HTTP na porta 80.</span><span class="sxs-lookup"><span data-stu-id="31a42-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="31a42-113">Exemplo 2: Adicionar um ouvinte HTTPS com SSL e Nomes de Host</span><span class="sxs-lookup"><span data-stu-id="31a42-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="31a42-114">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31a42-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="31a42-115">O segundo comando adiciona o ouvinte, que usa o protocolo HTTPS, com Certificados SSL e Nomes de Host, ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31a42-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="31a42-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31a42-116">PARAMETERS</span></span>

### <span data-ttu-id="31a42-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31a42-117">-ApplicationGateway</span></span>
<span data-ttu-id="31a42-118">Especifica o gateway do aplicativo ao qual este cmdlet associa o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="31a42-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="31a42-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="31a42-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="31a42-120">Erro do cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="31a42-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="31a42-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a42-121">-DefaultProfile</span></span>
<span data-ttu-id="31a42-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="31a42-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a42-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="31a42-123">-FirewallPolicy</span></span>
<span data-ttu-id="31a42-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="31a42-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="31a42-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="31a42-125">-FirewallPolicyId</span></span>
<span data-ttu-id="31a42-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="31a42-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="31a42-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="31a42-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="31a42-128">Especifica o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31a42-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="31a42-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="31a42-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="31a42-130">Especifica a ID do endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31a42-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="31a42-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="31a42-131">-FrontendPort</span></span>
<span data-ttu-id="31a42-132">Especifica a porta front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31a42-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="31a42-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="31a42-133">-FrontendPortId</span></span>
<span data-ttu-id="31a42-134">Especifica a ID da porta front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31a42-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="31a42-135">-Nomedo Host</span><span class="sxs-lookup"><span data-stu-id="31a42-135">-HostName</span></span>
<span data-ttu-id="31a42-136">Especifica o nome do host para o que este cmdlet envia ao ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="31a42-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="31a42-137">-Nomes de Host</span><span class="sxs-lookup"><span data-stu-id="31a42-137">-HostNames</span></span>
<span data-ttu-id="31a42-138">Nomes de host</span><span class="sxs-lookup"><span data-stu-id="31a42-138">Host names</span></span>

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

### <span data-ttu-id="31a42-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="31a42-139">-Name</span></span>
<span data-ttu-id="31a42-140">Especifica o nome do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="31a42-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="31a42-141">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="31a42-141">-Protocol</span></span>
<span data-ttu-id="31a42-142">Especifica o protocolo que o ouvinte HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="31a42-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="31a42-143">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="31a42-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31a42-144">Http</span><span class="sxs-lookup"><span data-stu-id="31a42-144">Http</span></span>
- <span data-ttu-id="31a42-145">Https</span><span class="sxs-lookup"><span data-stu-id="31a42-145">Https</span></span>

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

### <span data-ttu-id="31a42-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="31a42-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="31a42-147">Especifica se o cmdlet requer uma indicação de nome de servidor.</span><span class="sxs-lookup"><span data-stu-id="31a42-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="31a42-148">Os valores aceitáveis para este parâmetro são: verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="31a42-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="31a42-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="31a42-149">-SslCertificate</span></span>
<span data-ttu-id="31a42-150">Especifica o certificado SSL do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="31a42-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="31a42-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="31a42-151">-SslCertificateId</span></span>
<span data-ttu-id="31a42-152">Especifica a ID de certificado SSL (Secure Socket Layer) do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="31a42-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="31a42-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="31a42-153">-SslProfile</span></span>
<span data-ttu-id="31a42-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="31a42-154">SslProfile</span></span>

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

### <span data-ttu-id="31a42-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="31a42-155">-SslProfileId</span></span>
<span data-ttu-id="31a42-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="31a42-156">SslProfileId</span></span>

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

### <span data-ttu-id="31a42-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a42-157">CommonParameters</span></span>
<span data-ttu-id="31a42-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a42-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a42-159">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31a42-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a42-160">Entradas</span><span class="sxs-lookup"><span data-stu-id="31a42-160">INPUTS</span></span>

### <span data-ttu-id="31a42-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31a42-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="31a42-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="31a42-162">OUTPUTS</span></span>

### <span data-ttu-id="31a42-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31a42-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="31a42-164">Notas</span><span class="sxs-lookup"><span data-stu-id="31a42-164">NOTES</span></span>

## <span data-ttu-id="31a42-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31a42-165">RELATED LINKS</span></span>

[<span data-ttu-id="31a42-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="31a42-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="31a42-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="31a42-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="31a42-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="31a42-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="31a42-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="31a42-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


