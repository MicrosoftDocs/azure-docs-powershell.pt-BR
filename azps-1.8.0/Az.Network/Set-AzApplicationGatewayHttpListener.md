---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600054"
---
# <span data-ttu-id="94f43-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="94f43-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="94f43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94f43-102">SYNOPSIS</span></span>
<span data-ttu-id="94f43-103">Modifica um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94f43-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="94f43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94f43-104">SYNTAX</span></span>

### <span data-ttu-id="94f43-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="94f43-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94f43-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="94f43-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94f43-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94f43-107">DESCRIPTION</span></span>
<span data-ttu-id="94f43-108">O cmdlet **set-AzApplicationGatewayHttpListener** modifica um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="94f43-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="94f43-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94f43-109">EXAMPLES</span></span>

### <span data-ttu-id="94f43-110">Exemplo 1: definir um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="94f43-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="94f43-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="94f43-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="94f43-112">O segundo comando define o ouvinte HTTP do gateway para usar a configuração de front-end armazenada em $FIP 01 com o protocolo HTTP na porta 80.</span><span class="sxs-lookup"><span data-stu-id="94f43-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="94f43-113">OS</span><span class="sxs-lookup"><span data-stu-id="94f43-113">PARAMETERS</span></span>

### <span data-ttu-id="94f43-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94f43-114">-ApplicationGateway</span></span>
<span data-ttu-id="94f43-115">Especifica o gateway do aplicativo com o qual esse cmdlet associa o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="94f43-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="94f43-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="94f43-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="94f43-117">Erro de cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="94f43-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="94f43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f43-118">-DefaultProfile</span></span>
<span data-ttu-id="94f43-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94f43-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f43-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="94f43-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="94f43-121">Especifica o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94f43-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="94f43-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="94f43-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="94f43-123">Especifica a ID do endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94f43-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="94f43-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="94f43-124">-FrontendPort</span></span>
<span data-ttu-id="94f43-125">Especifica a porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94f43-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="94f43-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="94f43-126">-FrontendPortId</span></span>
<span data-ttu-id="94f43-127">Especifica a ID da porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94f43-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="94f43-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="94f43-128">-HostName</span></span>
<span data-ttu-id="94f43-129">Especifica o nome do host para o qual esse cmdlet envia o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="94f43-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="94f43-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="94f43-130">-Name</span></span>
<span data-ttu-id="94f43-131">Especifica o nome do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="94f43-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="94f43-132">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="94f43-132">-Protocol</span></span>
<span data-ttu-id="94f43-133">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="94f43-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="94f43-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="94f43-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94f43-135">Http</span><span class="sxs-lookup"><span data-stu-id="94f43-135">Http</span></span>
- <span data-ttu-id="94f43-136">Https</span><span class="sxs-lookup"><span data-stu-id="94f43-136">Https</span></span>

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

### <span data-ttu-id="94f43-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="94f43-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="94f43-138">Especifica se o cmdlet requer uma indicação de nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="94f43-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="94f43-139">Os valores aceitáveis para esse parâmetro são: true ou false.</span><span class="sxs-lookup"><span data-stu-id="94f43-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="94f43-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="94f43-140">-SslCertificate</span></span>
<span data-ttu-id="94f43-141">Especifica o certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="94f43-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="94f43-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="94f43-142">-SslCertificateId</span></span>
<span data-ttu-id="94f43-143">Especifica a ID do certificado SSL (Secure Socket Layer) da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="94f43-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="94f43-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f43-144">CommonParameters</span></span>
<span data-ttu-id="94f43-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f43-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f43-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f43-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f43-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94f43-147">INPUTS</span></span>

### <span data-ttu-id="94f43-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94f43-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="94f43-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94f43-149">OUTPUTS</span></span>

### <span data-ttu-id="94f43-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94f43-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="94f43-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94f43-151">NOTES</span></span>

## <span data-ttu-id="94f43-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94f43-152">RELATED LINKS</span></span>

[<span data-ttu-id="94f43-153">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="94f43-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="94f43-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="94f43-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="94f43-155">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="94f43-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="94f43-156">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="94f43-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


