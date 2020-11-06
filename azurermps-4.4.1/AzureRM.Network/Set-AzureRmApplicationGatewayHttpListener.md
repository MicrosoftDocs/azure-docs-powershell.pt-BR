---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 6805eaa6f1d710c607a7911b628d3642d48ece29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603097"
---
# <span data-ttu-id="318f9-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="318f9-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="318f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="318f9-102">SYNOPSIS</span></span>
<span data-ttu-id="318f9-103">Modifica um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="318f9-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="318f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="318f9-104">SYNTAX</span></span>

### <span data-ttu-id="318f9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="318f9-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="318f9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="318f9-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="318f9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="318f9-107">DESCRIPTION</span></span>
<span data-ttu-id="318f9-108">O cmdlet **set-AzureRmApplicationGatewayHttpListener** modifica um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="318f9-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="318f9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="318f9-109">EXAMPLES</span></span>

### <span data-ttu-id="318f9-110">Exemplo 1: definir um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="318f9-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="318f9-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="318f9-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="318f9-112">O segundo comando define o ouvinte HTTP do gateway para usar a configuração de front-end armazenada em $FIP 01 com o protocolo HTTP na porta 80.</span><span class="sxs-lookup"><span data-stu-id="318f9-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="318f9-113">OS</span><span class="sxs-lookup"><span data-stu-id="318f9-113">PARAMETERS</span></span>

### <span data-ttu-id="318f9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="318f9-114">-ApplicationGateway</span></span>
<span data-ttu-id="318f9-115">Especifica o gateway do aplicativo com o qual esse cmdlet associa o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="318f9-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="318f9-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="318f9-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="318f9-117">Especifica o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="318f9-117">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="318f9-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="318f9-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="318f9-119">Especifica a ID do endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="318f9-119">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="318f9-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="318f9-120">-FrontendPort</span></span>
<span data-ttu-id="318f9-121">Especifica a porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="318f9-121">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="318f9-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="318f9-122">-FrontendPortId</span></span>
<span data-ttu-id="318f9-123">Especifica a ID da porta de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="318f9-123">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="318f9-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="318f9-124">-HostName</span></span>
<span data-ttu-id="318f9-125">Especifica o nome do host para o qual esse cmdlet envia o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="318f9-125">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="318f9-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="318f9-126">-Name</span></span>
<span data-ttu-id="318f9-127">Especifica o nome do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="318f9-127">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="318f9-128">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="318f9-128">-Protocol</span></span>
<span data-ttu-id="318f9-129">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="318f9-129">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="318f9-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="318f9-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="318f9-131">Http</span><span class="sxs-lookup"><span data-stu-id="318f9-131">Http</span></span>
- <span data-ttu-id="318f9-132">Https</span><span class="sxs-lookup"><span data-stu-id="318f9-132">Https</span></span>

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

### <span data-ttu-id="318f9-133">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="318f9-133">-RequireServerNameIndication</span></span>
<span data-ttu-id="318f9-134">Especifica se o cmdlet requer uma indicação de nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="318f9-134">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="318f9-135">Os valores aceitáveis para esse parâmetro são: true ou false.</span><span class="sxs-lookup"><span data-stu-id="318f9-135">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="318f9-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="318f9-136">-SslCertificate</span></span>
<span data-ttu-id="318f9-137">Especifica o certificado SSL da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="318f9-137">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="318f9-138">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="318f9-138">-SslCertificateId</span></span>
<span data-ttu-id="318f9-139">Especifica a ID do certificado SSL (Secure Socket Layer) da escuta HTTP.</span><span class="sxs-lookup"><span data-stu-id="318f9-139">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="318f9-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318f9-140">-DefaultProfile</span></span>
<span data-ttu-id="318f9-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="318f9-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="318f9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318f9-142">CommonParameters</span></span>
<span data-ttu-id="318f9-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318f9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318f9-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318f9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318f9-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="318f9-145">INPUTS</span></span>

### <span data-ttu-id="318f9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="318f9-146">System.String</span></span>

## <span data-ttu-id="318f9-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="318f9-147">OUTPUTS</span></span>

### <span data-ttu-id="318f9-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="318f9-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="318f9-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="318f9-149">NOTES</span></span>

## <span data-ttu-id="318f9-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="318f9-150">RELATED LINKS</span></span>

[<span data-ttu-id="318f9-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="318f9-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="318f9-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="318f9-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="318f9-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="318f9-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="318f9-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="318f9-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


