---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: ea07f3b9f2dd1e79f59b3369f3f8d3a8c1434deb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776567"
---
# <span data-ttu-id="2f5ec-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2f5ec-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="2f5ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5ec-103">Modifica um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="2f5ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f5ec-104">SYNTAX</span></span>

### <span data-ttu-id="2f5ec-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f5ec-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f5ec-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2f5ec-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f5ec-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f5ec-107">DESCRIPTION</span></span>
<span data-ttu-id="2f5ec-108">O cmdlet **set-AzApplicationGatewayHttpListener** modifica um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="2f5ec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f5ec-109">EXAMPLES</span></span>

### <span data-ttu-id="2f5ec-110">Exemplo 1: definir um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="2f5ec-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="2f5ec-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2f5ec-112">O segundo comando define o ouvinte HTTP do gateway para usar a configuração de front-end armazenada em $FIP 01 com o protocolo HTTP na porta 80.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="2f5ec-113">OS</span><span class="sxs-lookup"><span data-stu-id="2f5ec-113">PARAMETERS</span></span>

### <span data-ttu-id="2f5ec-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f5ec-114">-ApplicationGateway</span></span>
<span data-ttu-id="2f5ec-115">Especifica o gateway do aplicativo com o qual esse cmdlet associa o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="2f5ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5ec-116">-DefaultProfile</span></span>
<span data-ttu-id="2f5ec-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f5ec-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f5ec-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="2f5ec-119">Especifica o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="2f5ec-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2f5ec-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="2f5ec-121">Especifica a ID do endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="2f5ec-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="2f5ec-122">-FrontendPort</span></span>
<span data-ttu-id="2f5ec-123">Especifica a porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="2f5ec-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="2f5ec-124">-FrontendPortId</span></span>
<span data-ttu-id="2f5ec-125">Especifica a ID da porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="2f5ec-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="2f5ec-126">-HostName</span></span>
<span data-ttu-id="2f5ec-127">Especifica o nome do host para o qual esse cmdlet envia o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="2f5ec-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f5ec-128">-Name</span></span>
<span data-ttu-id="2f5ec-129">Especifica o nome do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="2f5ec-130">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="2f5ec-130">-Protocol</span></span>
<span data-ttu-id="2f5ec-131">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="2f5ec-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2f5ec-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f5ec-133">Http</span><span class="sxs-lookup"><span data-stu-id="2f5ec-133">Http</span></span>
- <span data-ttu-id="2f5ec-134">Https</span><span class="sxs-lookup"><span data-stu-id="2f5ec-134">Https</span></span>

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

### <span data-ttu-id="2f5ec-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="2f5ec-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="2f5ec-136">Especifica se o cmdlet requer uma indicação de nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="2f5ec-137">Os valores aceitáveis para esse parâmetro são: true ou false.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="2f5ec-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f5ec-138">-SslCertificate</span></span>
<span data-ttu-id="2f5ec-139">Especifica o certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="2f5ec-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="2f5ec-140">-SslCertificateId</span></span>
<span data-ttu-id="2f5ec-141">Especifica a ID do certificado SSL (Secure Socket Layer) da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="2f5ec-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5ec-142">CommonParameters</span></span>
<span data-ttu-id="2f5ec-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f5ec-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5ec-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f5ec-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5ec-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f5ec-145">INPUTS</span></span>

### <span data-ttu-id="2f5ec-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2f5ec-146">System.String</span></span>

## <span data-ttu-id="2f5ec-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f5ec-147">OUTPUTS</span></span>

### <span data-ttu-id="2f5ec-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f5ec-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2f5ec-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f5ec-149">NOTES</span></span>

## <span data-ttu-id="2f5ec-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f5ec-150">RELATED LINKS</span></span>

[<span data-ttu-id="2f5ec-151">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2f5ec-151">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="2f5ec-152">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2f5ec-152">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="2f5ec-153">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2f5ec-153">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="2f5ec-154">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2f5ec-154">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


