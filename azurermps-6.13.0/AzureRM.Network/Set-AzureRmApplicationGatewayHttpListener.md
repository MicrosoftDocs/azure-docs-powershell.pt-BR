---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 231ee3dc8d66d3960f0416cb410b6747b25ae278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440315"
---
# <span data-ttu-id="a379e-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a379e-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a379e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a379e-102">SYNOPSIS</span></span>
<span data-ttu-id="a379e-103">Modifica um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a379e-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a379e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a379e-104">SYNTAX</span></span>

### <span data-ttu-id="a379e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a379e-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a379e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a379e-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a379e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a379e-107">DESCRIPTION</span></span>
<span data-ttu-id="a379e-108">O cmdlet **set-AzureRmApplicationGatewayHttpListener** modifica um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="a379e-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a379e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a379e-109">EXAMPLES</span></span>

### <span data-ttu-id="a379e-110">Exemplo 1: definir um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="a379e-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="a379e-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a379e-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a379e-112">O segundo comando define o ouvinte HTTP do gateway para usar a configuração de front-end armazenada em $FIP 01 com o protocolo HTTP na porta 80.</span><span class="sxs-lookup"><span data-stu-id="a379e-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="a379e-113">OS</span><span class="sxs-lookup"><span data-stu-id="a379e-113">PARAMETERS</span></span>

### <span data-ttu-id="a379e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a379e-114">-ApplicationGateway</span></span>
<span data-ttu-id="a379e-115">Especifica o gateway do aplicativo com o qual esse cmdlet associa o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="a379e-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="a379e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a379e-116">-DefaultProfile</span></span>
<span data-ttu-id="a379e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a379e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a379e-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a379e-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a379e-119">Especifica o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a379e-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a379e-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a379e-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a379e-121">Especifica a ID do endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a379e-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a379e-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a379e-122">-FrontendPort</span></span>
<span data-ttu-id="a379e-123">Especifica a porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a379e-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="a379e-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a379e-124">-FrontendPortId</span></span>
<span data-ttu-id="a379e-125">Especifica a ID da porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a379e-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="a379e-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="a379e-126">-HostName</span></span>
<span data-ttu-id="a379e-127">Especifica o nome do host para o qual esse cmdlet envia o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="a379e-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="a379e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a379e-128">-Name</span></span>
<span data-ttu-id="a379e-129">Especifica o nome do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="a379e-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="a379e-130">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="a379e-130">-Protocol</span></span>
<span data-ttu-id="a379e-131">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="a379e-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="a379e-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a379e-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a379e-133">Http</span><span class="sxs-lookup"><span data-stu-id="a379e-133">Http</span></span>
- <span data-ttu-id="a379e-134">Https</span><span class="sxs-lookup"><span data-stu-id="a379e-134">Https</span></span>

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

### <span data-ttu-id="a379e-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a379e-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="a379e-136">Especifica se o cmdlet requer uma indicação de nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a379e-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="a379e-137">Os valores aceitáveis para esse parâmetro são: true ou false.</span><span class="sxs-lookup"><span data-stu-id="a379e-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="a379e-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a379e-138">-SslCertificate</span></span>
<span data-ttu-id="a379e-139">Especifica o certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a379e-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="a379e-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a379e-140">-SslCertificateId</span></span>
<span data-ttu-id="a379e-141">Especifica a ID do certificado SSL (Secure Socket Layer) da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a379e-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="a379e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a379e-142">CommonParameters</span></span>
<span data-ttu-id="a379e-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a379e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a379e-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a379e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a379e-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a379e-145">INPUTS</span></span>

### <span data-ttu-id="a379e-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a379e-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="a379e-147">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a379e-147">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="a379e-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a379e-148">OUTPUTS</span></span>

### <span data-ttu-id="a379e-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a379e-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a379e-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a379e-150">NOTES</span></span>

## <span data-ttu-id="a379e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a379e-151">RELATED LINKS</span></span>

[<span data-ttu-id="a379e-152">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a379e-152">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a379e-153">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a379e-153">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a379e-154">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a379e-154">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a379e-155">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a379e-155">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


