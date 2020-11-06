---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 5648bb1cb7497517afb5ff461674294e426c0131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600745"
---
# <span data-ttu-id="6bfba-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6bfba-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6bfba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bfba-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfba-103">Adiciona um ouvinte HTTP a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bfba-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="6bfba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bfba-104">SYNTAX</span></span>

### <span data-ttu-id="6bfba-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bfba-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6bfba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6bfba-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bfba-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6bfba-107">DESCRIPTION</span></span>
<span data-ttu-id="6bfba-108">O cmdlet **Add-AzApplicationGatewayHttpListener** adiciona um ouvinte http a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bfba-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="6bfba-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bfba-109">EXAMPLES</span></span>

### <span data-ttu-id="6bfba-110">Exemplo 1: adicionar um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="6bfba-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="6bfba-111">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw. O segundo comando adiciona o ouvinte HTTP ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bfba-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="6bfba-112">Exemplo 2: adicionar um ouvinte HTTPS com SSL</span><span class="sxs-lookup"><span data-stu-id="6bfba-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="6bfba-113">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6bfba-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6bfba-114">O segundo comando adiciona o ouvinte, que usa o protocolo HTTPS ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bfba-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="6bfba-115">OS</span><span class="sxs-lookup"><span data-stu-id="6bfba-115">PARAMETERS</span></span>

### <span data-ttu-id="6bfba-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bfba-116">-ApplicationGateway</span></span>
<span data-ttu-id="6bfba-117">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona um ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="6bfba-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="6bfba-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bfba-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="6bfba-119">Erro de cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6bfba-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="6bfba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfba-120">-DefaultProfile</span></span>
<span data-ttu-id="6bfba-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bfba-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bfba-122">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bfba-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="6bfba-123">Especifica o objeto de recurso de IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bfba-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="6bfba-124">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6bfba-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="6bfba-125">Especifica a ID de IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bfba-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="6bfba-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6bfba-126">-FrontendPort</span></span>
<span data-ttu-id="6bfba-127">Especifica o objeto de porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bfba-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="6bfba-128">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="6bfba-128">-FrontendPortId</span></span>
<span data-ttu-id="6bfba-129">Especifica a ID da porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bfba-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="6bfba-130">-HostName</span><span class="sxs-lookup"><span data-stu-id="6bfba-130">-HostName</span></span>
<span data-ttu-id="6bfba-131">Especifica o nome do host para o qual esse cmdlet adiciona um ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="6bfba-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="6bfba-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bfba-132">-Name</span></span>
<span data-ttu-id="6bfba-133">Especifica o nome da porta de front-end que esse comando adiciona.</span><span class="sxs-lookup"><span data-stu-id="6bfba-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="6bfba-134">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="6bfba-134">-Protocol</span></span>
<span data-ttu-id="6bfba-135">Especifica o protocolo do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="6bfba-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="6bfba-136">Há suporte para HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6bfba-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="6bfba-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="6bfba-137">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="6bfba-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="6bfba-138">-SslCertificate</span></span>
<span data-ttu-id="6bfba-139">Especifica o certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6bfba-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="6bfba-140">Deve ser especificado se HTTPS for escolhido como protocolo de escuta.</span><span class="sxs-lookup"><span data-stu-id="6bfba-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="6bfba-141">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="6bfba-141">-SslCertificateId</span></span>
<span data-ttu-id="6bfba-142">Especifica a ID do certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6bfba-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="6bfba-143">Deve ser especificado se HTTPS for escolhido como protocolo de escuta.</span><span class="sxs-lookup"><span data-stu-id="6bfba-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="6bfba-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfba-144">CommonParameters</span></span>
<span data-ttu-id="6bfba-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bfba-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfba-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bfba-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfba-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6bfba-147">INPUTS</span></span>

### <span data-ttu-id="6bfba-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bfba-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6bfba-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6bfba-149">OUTPUTS</span></span>

### <span data-ttu-id="6bfba-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bfba-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6bfba-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6bfba-151">NOTES</span></span>

## <span data-ttu-id="6bfba-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bfba-152">RELATED LINKS</span></span>

[<span data-ttu-id="6bfba-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6bfba-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6bfba-154">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6bfba-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6bfba-155">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6bfba-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6bfba-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6bfba-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


