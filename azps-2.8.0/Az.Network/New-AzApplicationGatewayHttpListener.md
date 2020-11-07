---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771662"
---
# <span data-ttu-id="7e962-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7e962-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7e962-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e962-102">SYNOPSIS</span></span>
<span data-ttu-id="7e962-103">Cria um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7e962-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="7e962-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e962-104">SYNTAX</span></span>

### <span data-ttu-id="7e962-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e962-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e962-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7e962-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e962-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e962-107">DESCRIPTION</span></span>
<span data-ttu-id="7e962-108">O cmdlet **New-AzApplicationGatewayHttpListener** cria um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e962-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="7e962-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e962-109">EXAMPLES</span></span>

### <span data-ttu-id="7e962-110">Exemplo 1: criar um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="7e962-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="7e962-111">Esse comando cria um ouvinte HTTP chamado Listener01 e armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="7e962-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="7e962-112">Exemplo 2: criar um ouvinte HTTP com SSL</span><span class="sxs-lookup"><span data-stu-id="7e962-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="7e962-113">Esse comando cria um ouvinte HTTP que usa o Offload SSL e fornece o certificado SSL na variável $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="7e962-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="7e962-114">O comando armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="7e962-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="7e962-115">OS</span><span class="sxs-lookup"><span data-stu-id="7e962-115">PARAMETERS</span></span>

### <span data-ttu-id="7e962-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e962-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="7e962-117">Erro de cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7e962-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="7e962-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e962-118">-DefaultProfile</span></span>
<span data-ttu-id="7e962-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e962-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e962-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e962-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="7e962-121">Especifica o objeto de configuração de IP de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="7e962-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="7e962-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7e962-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="7e962-123">Especifica a ID da configuração de IP de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="7e962-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="7e962-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7e962-124">-FrontendPort</span></span>
<span data-ttu-id="7e962-125">Especifica a porta de front-end do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="7e962-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="7e962-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="7e962-126">-FrontendPortId</span></span>
<span data-ttu-id="7e962-127">Especifica a ID do objeto de porta de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="7e962-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="7e962-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="7e962-128">-HostName</span></span>
<span data-ttu-id="7e962-129">Especifica o nome do host do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e962-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="7e962-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e962-130">-Name</span></span>
<span data-ttu-id="7e962-131">Especifica o nome da escuta HTTP que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="7e962-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7e962-132">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="7e962-132">-Protocol</span></span>
<span data-ttu-id="7e962-133">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="7e962-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="7e962-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="7e962-134">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="7e962-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e962-135">-SslCertificate</span></span>
<span data-ttu-id="7e962-136">Especifica o objeto de certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="7e962-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="7e962-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="7e962-137">-SslCertificateId</span></span>
<span data-ttu-id="7e962-138">Especifica a ID do certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="7e962-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="7e962-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e962-139">CommonParameters</span></span>
<span data-ttu-id="7e962-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e962-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e962-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e962-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e962-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e962-142">INPUTS</span></span>

### <span data-ttu-id="7e962-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7e962-143">None</span></span>

## <span data-ttu-id="7e962-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e962-144">OUTPUTS</span></span>

### <span data-ttu-id="7e962-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7e962-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7e962-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e962-146">NOTES</span></span>

## <span data-ttu-id="7e962-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e962-147">RELATED LINKS</span></span>

[<span data-ttu-id="7e962-148">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7e962-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7e962-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7e962-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7e962-150">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7e962-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7e962-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7e962-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


