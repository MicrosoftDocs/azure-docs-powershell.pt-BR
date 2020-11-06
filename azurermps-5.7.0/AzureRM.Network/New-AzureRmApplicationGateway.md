---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: a9751806760a8e2265737e72d726fb491191fa5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432458"
---
# <span data-ttu-id="fc66a-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc66a-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="fc66a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc66a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc66a-103">Cria um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc66a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc66a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-EnableHttp2] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc66a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc66a-105">DESCRIPTION</span></span>
<span data-ttu-id="fc66a-106">O cmdlet **New-AzureRmApplicationGateway** cria um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc66a-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="fc66a-107">Um gateway de aplicativo requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fc66a-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="fc66a-108">Um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fc66a-108">A resource group.</span></span>
- <span data-ttu-id="fc66a-109">Uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fc66a-109">A virtual network.</span></span>
- <span data-ttu-id="fc66a-110">Um pool de servidores back-end que contém os endereços IP dos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="fc66a-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="fc66a-111">Configurações de pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="fc66a-111">Back-end server pool settings.</span></span> <span data-ttu-id="fc66a-112">Cada pool tem configurações como portabilidade baseada em protocolo e porta, que são aplicadas a todos os servidores dentro do pool.</span><span class="sxs-lookup"><span data-stu-id="fc66a-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="fc66a-113">Endereços IP front-end, que são os endereços IP abertos no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="fc66a-114">Um endereço IP front-end pode ser um endereço IP público ou um endereço IP interno.</span><span class="sxs-lookup"><span data-stu-id="fc66a-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="fc66a-115">Portas de front-end, que são as portas públicas abertas no Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fc66a-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="fc66a-116">O tráfego que atinge essas portas é redirecionado para os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="fc66a-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="fc66a-117">Uma regra de roteamento de solicitação que associa o ouvinte e o pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="fc66a-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="fc66a-118">A regra define qual pool de servidores back-end o tráfego deve ser direcionado quando ele atinge um ouvinte específico.</span><span class="sxs-lookup"><span data-stu-id="fc66a-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="fc66a-119">Um ouvinte tem uma porta de front-end, endereço IP front-end, protocolo (HTTP ou HTTPS) e nome de certificado SSL (se estiver configurando o descarregamento de SSL).</span><span class="sxs-lookup"><span data-stu-id="fc66a-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="fc66a-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc66a-120">EXAMPLES</span></span>

### <span data-ttu-id="fc66a-121">Exemplo 1: criar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="fc66a-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="fc66a-122">O exemplo a seguir cria um aplicativo gateway criando primeiro um grupo de recursos e uma rede virtual, bem como os seguintes:</span><span class="sxs-lookup"><span data-stu-id="fc66a-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="fc66a-123">Um pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="fc66a-123">A back-end server pool</span></span>
- <span data-ttu-id="fc66a-124">Configurações de pool de servidor back-end</span><span class="sxs-lookup"><span data-stu-id="fc66a-124">Back-end server pool settings</span></span>
- <span data-ttu-id="fc66a-125">Portas de front-end</span><span class="sxs-lookup"><span data-stu-id="fc66a-125">Front-end ports</span></span>
- <span data-ttu-id="fc66a-126">Endereços IP front-end</span><span class="sxs-lookup"><span data-stu-id="fc66a-126">Front-end IP addresses</span></span>
- <span data-ttu-id="fc66a-127">Uma regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="fc66a-127">A request routing rule</span></span>

<span data-ttu-id="fc66a-128">Estes quatro comandos criam uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fc66a-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="fc66a-129">O primeiro comando cria uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fc66a-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="fc66a-130">O segundo comando cria uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fc66a-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="fc66a-131">O terceiro comando verifica a configuração de sub-rede e o quarto comando verifica se a rede virtual foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="fc66a-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="fc66a-132">Os comandos a seguir criam o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fc66a-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="fc66a-133">O primeiro comando cria uma configuração de IP chamada GatewayIp01 para a sub-rede criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fc66a-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="fc66a-134">O segundo comando cria um pool de servidores back-end chamado Pool01 com uma lista de endereços IP back-end e armazena o pool na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="fc66a-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="fc66a-135">O terceiro comando cria as configurações do pool de servidores back-end e armazena as configurações na variável $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="fc66a-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="fc66a-136">O comando avançar cria uma porta de front-end na porta 80, nomeia-a FrontEndPort01 e armazena a porta na variável $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="fc66a-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="fc66a-137">O quinto comando cria um endereço IP público usando New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="fc66a-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="fc66a-138">O sexto comando cria uma configuração de IP de front-end usando $PublicIp, nomeia-a FrontEndPortConfig01 e a armazena na variável $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="fc66a-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="fc66a-139">O sétimo comando cria um ouvinte usando o $FrontEndPort de $FrontEndIpConfig criadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fc66a-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="fc66a-140">O oitavo comando cria uma regra para o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="fc66a-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="fc66a-141">O nono comando define a SKU.</span><span class="sxs-lookup"><span data-stu-id="fc66a-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="fc66a-142">O comando décimo cria o gateway usando os objetos definidos pelos comandos anteriores.</span><span class="sxs-lookup"><span data-stu-id="fc66a-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="fc66a-143">OS</span><span class="sxs-lookup"><span data-stu-id="fc66a-143">PARAMETERS</span></span>

### <span data-ttu-id="fc66a-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc66a-144">-AsJob</span></span>
<span data-ttu-id="fc66a-145">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fc66a-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="fc66a-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="fc66a-147">Especifica certificados de autenticação para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-147">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="fc66a-148">-BackendAddressPools</span></span>
<span data-ttu-id="fc66a-149">Especifica a lista de pools de endereços back-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-149">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="fc66a-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="fc66a-151">Especifica a lista de configurações HTTP de back-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc66a-152">-DefaultProfile</span></span>
<span data-ttu-id="fc66a-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc66a-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc66a-154">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="fc66a-154">-EnableHttp2</span></span>
<span data-ttu-id="fc66a-155">Se o HTTP2 está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fc66a-155">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-156">-Force</span><span class="sxs-lookup"><span data-stu-id="fc66a-156">-Force</span></span>
<span data-ttu-id="fc66a-157">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc66a-157">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-158">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="fc66a-158">-FrontendIPConfigurations</span></span>
<span data-ttu-id="fc66a-159">Especifica uma lista de configurações de IP de front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-159">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-160">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="fc66a-160">-FrontendPorts</span></span>
<span data-ttu-id="fc66a-161">Especifica uma lista de portas front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-161">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-162">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="fc66a-162">-GatewayIPConfigurations</span></span>
<span data-ttu-id="fc66a-163">Especifica uma lista de configurações de IP para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-163">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-164">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="fc66a-164">-HttpListeners</span></span>
<span data-ttu-id="fc66a-165">Especifica uma lista de ouvintes HTTP para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fc66a-165">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-166">-Local</span><span class="sxs-lookup"><span data-stu-id="fc66a-166">-Location</span></span>
<span data-ttu-id="fc66a-167">Especifica a região na qual criar o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-167">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc66a-168">-Name</span></span>
<span data-ttu-id="fc66a-169">Especifica o nome do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-169">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-170">-Testes</span><span class="sxs-lookup"><span data-stu-id="fc66a-170">-Probes</span></span>
<span data-ttu-id="fc66a-171">Especifica os testes do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-171">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-172">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="fc66a-172">-RedirectConfigurations</span></span>
<span data-ttu-id="fc66a-173">A lista de configurações de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="fc66a-173">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-174">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="fc66a-174">-RequestRoutingRules</span></span>
<span data-ttu-id="fc66a-175">Especifica uma lista de regras de roteamento de solicitações para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-175">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc66a-176">-ResourceGroupName</span></span>
<span data-ttu-id="fc66a-177">Especifica o nome do grupo de recursos no qual o Application Gateway será criado.</span><span class="sxs-lookup"><span data-stu-id="fc66a-177">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-178">-SKU</span><span class="sxs-lookup"><span data-stu-id="fc66a-178">-Sku</span></span>
<span data-ttu-id="fc66a-179">Especifica a SKU (unidade de manutenção de estoque) do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-179">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-180">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="fc66a-180">-SslCertificates</span></span>
<span data-ttu-id="fc66a-181">Especifica a lista de certificados SSL (Secure Sockets Layer) para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fc66a-181">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-182">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="fc66a-182">-SslPolicy</span></span>
<span data-ttu-id="fc66a-183">Especifica uma política SSL para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fc66a-183">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-184">-Marca</span><span class="sxs-lookup"><span data-stu-id="fc66a-184">-Tag</span></span>
<span data-ttu-id="fc66a-185">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fc66a-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fc66a-186">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fc66a-186">For example:</span></span>

<span data-ttu-id="fc66a-187">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fc66a-187">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-188">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="fc66a-188">-UrlPathMaps</span></span>
<span data-ttu-id="fc66a-189">Especifica mapas de caminho de URL para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc66a-189">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-190">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc66a-190">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="fc66a-191">Especifica uma configuração de firewall de aplicativo Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="fc66a-191">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="fc66a-192">Você pode usar o cmdlet Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration para obter um WAF.</span><span class="sxs-lookup"><span data-stu-id="fc66a-192">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-193">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc66a-193">-Confirm</span></span>
<span data-ttu-id="fc66a-194">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc66a-194">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc66a-195">-WhatIf</span></span>
<span data-ttu-id="fc66a-196">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc66a-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc66a-197">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc66a-197">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc66a-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc66a-198">CommonParameters</span></span>
<span data-ttu-id="fc66a-199">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc66a-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc66a-200">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc66a-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc66a-201">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc66a-201">INPUTS</span></span>

### <span data-ttu-id="fc66a-202">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fc66a-202">None</span></span>
<span data-ttu-id="fc66a-203">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fc66a-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc66a-204">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc66a-204">OUTPUTS</span></span>

### <span data-ttu-id="fc66a-205">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc66a-205">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc66a-206">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc66a-206">NOTES</span></span>

## <span data-ttu-id="fc66a-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc66a-207">RELATED LINKS</span></span>

[<span data-ttu-id="fc66a-208">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fc66a-208">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="fc66a-209">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fc66a-209">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="fc66a-210">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fc66a-210">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fc66a-211">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fc66a-211">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fc66a-212">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fc66a-212">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="fc66a-213">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc66a-213">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="fc66a-214">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fc66a-214">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="fc66a-215">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="fc66a-215">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="fc66a-216">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc66a-216">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fc66a-217">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fc66a-217">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
