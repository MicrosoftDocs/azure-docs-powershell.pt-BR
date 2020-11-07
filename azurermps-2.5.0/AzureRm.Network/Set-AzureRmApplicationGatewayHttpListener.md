---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 7b3d38b8f55c93c4527d92969ec64ce792bca44b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785165"
---
# <span data-ttu-id="1b5fa-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b5fa-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1b5fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5fa-103">Modifica um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b5fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b5fa-104">SYNTAX</span></span>

### <span data-ttu-id="1b5fa-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b5fa-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b5fa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1b5fa-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b5fa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b5fa-107">DESCRIPTION</span></span>
<span data-ttu-id="1b5fa-108">O cmdlet **set-AzureRmApplicationGatewayHttpListener** modifica um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="1b5fa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b5fa-109">EXAMPLES</span></span>

### <span data-ttu-id="1b5fa-110">Exemplo 1: definir um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="1b5fa-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="1b5fa-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1b5fa-112">O segundo comando define o ouvinte HTTP do gateway para usar a configuração de front-end armazenada em $FIP 01 com o protocolo HTTP na porta 80.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="1b5fa-113">OS</span><span class="sxs-lookup"><span data-stu-id="1b5fa-113">PARAMETERS</span></span>

### <span data-ttu-id="1b5fa-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b5fa-114">-ApplicationGateway</span></span>
<span data-ttu-id="1b5fa-115">Especifica o gateway do aplicativo com o qual esse cmdlet associa o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="1b5fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5fa-116">-DefaultProfile</span></span>
<span data-ttu-id="1b5fa-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b5fa-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b5fa-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="1b5fa-119">Especifica o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-119">Specifies the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5fa-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1b5fa-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="1b5fa-121">Especifica a ID do endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="1b5fa-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1b5fa-122">-FrontendPort</span></span>
<span data-ttu-id="1b5fa-123">Especifica a porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-123">Specifies the application gateway front-end port.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5fa-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="1b5fa-124">-FrontendPortId</span></span>
<span data-ttu-id="1b5fa-125">Especifica a ID da porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="1b5fa-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="1b5fa-126">-HostName</span></span>
<span data-ttu-id="1b5fa-127">Especifica o nome do host para o qual esse cmdlet envia o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5fa-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b5fa-128">-Name</span></span>
<span data-ttu-id="1b5fa-129">Especifica o nome do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="1b5fa-130">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="1b5fa-130">-Protocol</span></span>
<span data-ttu-id="1b5fa-131">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="1b5fa-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1b5fa-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b5fa-133">Http</span><span class="sxs-lookup"><span data-stu-id="1b5fa-133">Http</span></span>
- <span data-ttu-id="1b5fa-134">Https</span><span class="sxs-lookup"><span data-stu-id="1b5fa-134">Https</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5fa-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="1b5fa-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="1b5fa-136">Especifica se o cmdlet requer uma indicação de nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="1b5fa-137">Os valores aceitáveis para esse parâmetro são: true ou false.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-137">The acceptable values for this parameter are: true or false.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5fa-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b5fa-138">-SslCertificate</span></span>
<span data-ttu-id="1b5fa-139">Especifica o certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-139">Specifies the SSL certificate of the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5fa-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="1b5fa-140">-SslCertificateId</span></span>
<span data-ttu-id="1b5fa-141">Especifica a ID do certificado SSL (Secure Socket Layer) da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="1b5fa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5fa-142">CommonParameters</span></span>
<span data-ttu-id="1b5fa-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5fa-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b5fa-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5fa-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b5fa-145">INPUTS</span></span>

### <span data-ttu-id="1b5fa-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1b5fa-146">System.String</span></span>

## <span data-ttu-id="1b5fa-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b5fa-147">OUTPUTS</span></span>

### <span data-ttu-id="1b5fa-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b5fa-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b5fa-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b5fa-149">NOTES</span></span>

## <span data-ttu-id="1b5fa-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b5fa-150">RELATED LINKS</span></span>

[<span data-ttu-id="1b5fa-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b5fa-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1b5fa-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b5fa-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1b5fa-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b5fa-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1b5fa-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b5fa-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


