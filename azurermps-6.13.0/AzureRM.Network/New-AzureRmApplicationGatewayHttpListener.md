---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 29df7c4ac7cb941e8826c3e1fb929d92cc626512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432307"
---
# <span data-ttu-id="ddeb9-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddeb9-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ddeb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddeb9-102">SYNOPSIS</span></span>
<span data-ttu-id="ddeb9-103">Cria um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddeb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddeb9-104">SYNTAX</span></span>

### <span data-ttu-id="ddeb9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddeb9-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddeb9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ddeb9-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddeb9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ddeb9-107">DESCRIPTION</span></span>
<span data-ttu-id="ddeb9-108">O cmdlet **New-AzureRmApplicationGatewayHttpListener** cria um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="ddeb9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddeb9-109">EXAMPLES</span></span>

### <span data-ttu-id="ddeb9-110">Exemplo 1: criar um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="ddeb9-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="ddeb9-111">Esse comando cria um ouvinte HTTP chamado Listener01 e armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ddeb9-112">Exemplo 2: criar um ouvinte HTTP com SSL</span><span class="sxs-lookup"><span data-stu-id="ddeb9-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="ddeb9-113">Esse comando cria um ouvinte HTTP que usa o Offload SSL e fornece o certificado SSL na variável $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="ddeb9-114">O comando armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="ddeb9-115">OS</span><span class="sxs-lookup"><span data-stu-id="ddeb9-115">PARAMETERS</span></span>

### <span data-ttu-id="ddeb9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddeb9-116">-DefaultProfile</span></span>
<span data-ttu-id="ddeb9-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddeb9-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddeb9-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="ddeb9-119">Especifica o objeto de configuração de IP de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddeb9-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ddeb9-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="ddeb9-121">Especifica a ID da configuração de IP de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddeb9-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ddeb9-122">-FrontendPort</span></span>
<span data-ttu-id="ddeb9-123">Especifica a porta de front-end do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddeb9-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="ddeb9-124">-FrontendPortId</span></span>
<span data-ttu-id="ddeb9-125">Especifica a ID do objeto de porta de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddeb9-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="ddeb9-126">-HostName</span></span>
<span data-ttu-id="ddeb9-127">Especifica o nome do host do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="ddeb9-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddeb9-128">-Name</span></span>
<span data-ttu-id="ddeb9-129">Especifica o nome da escuta HTTP que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ddeb9-130">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="ddeb9-130">-Protocol</span></span>
<span data-ttu-id="ddeb9-131">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="ddeb9-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="ddeb9-132">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddeb9-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="ddeb9-133">-SslCertificate</span></span>
<span data-ttu-id="ddeb9-134">Especifica o objeto de certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="ddeb9-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="ddeb9-135">-SslCertificateId</span></span>
<span data-ttu-id="ddeb9-136">Especifica a ID do certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddeb9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddeb9-137">CommonParameters</span></span>
<span data-ttu-id="ddeb9-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddeb9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddeb9-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddeb9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddeb9-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ddeb9-140">INPUTS</span></span>

### <span data-ttu-id="ddeb9-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ddeb9-141">None</span></span>

## <span data-ttu-id="ddeb9-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ddeb9-142">OUTPUTS</span></span>

### <span data-ttu-id="ddeb9-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddeb9-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ddeb9-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ddeb9-144">NOTES</span></span>

## <span data-ttu-id="ddeb9-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddeb9-145">RELATED LINKS</span></span>

[<span data-ttu-id="ddeb9-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddeb9-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ddeb9-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddeb9-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ddeb9-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddeb9-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ddeb9-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddeb9-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


