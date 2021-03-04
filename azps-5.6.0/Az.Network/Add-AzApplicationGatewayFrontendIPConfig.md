---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 32e8671267efddd94252e592de45cb014b5dd0de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887383"
---
# <span data-ttu-id="99d27-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99d27-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="99d27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d27-102">SYNOPSIS</span></span>
<span data-ttu-id="99d27-103">Adiciona uma configuração de IP front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99d27-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="99d27-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="99d27-104">SYNTAX</span></span>

### <span data-ttu-id="99d27-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="99d27-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d27-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="99d27-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d27-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="99d27-107">DESCRIPTION</span></span>
<span data-ttu-id="99d27-108">O cmdlet **Add-AzApplicationGatewayFrontendIPConfig** adiciona uma configuração de IP front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99d27-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="99d27-109">Um gateway de aplicativo oferece suporte a dois tipos de configurações de IP front-end:</span><span class="sxs-lookup"><span data-stu-id="99d27-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="99d27-110">Endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="99d27-110">Public IP addresses</span></span>
- <span data-ttu-id="99d27-111">Endereços IP privados usando ILB (balanceamento de carga interno) Um gateway de aplicativo pode ter no máximo um IP público e um IP privado.</span><span class="sxs-lookup"><span data-stu-id="99d27-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="99d27-112">Adicione o endereço IP público e o endereço IP privado como IPs front-end separados.</span><span class="sxs-lookup"><span data-stu-id="99d27-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="99d27-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99d27-113">EXAMPLES</span></span>

### <span data-ttu-id="99d27-114">Exemplo 1: Adicionar um IP público como o endereço IP front-end</span><span class="sxs-lookup"><span data-stu-id="99d27-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="99d27-115">O primeiro comando cria um objeto de endereço IP público e o armazena na $PublicIp variável.</span><span class="sxs-lookup"><span data-stu-id="99d27-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="99d27-116">O segundo comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="99d27-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="99d27-117">O terceiro comando adiciona a configuração de IP front-end chamada FrontEndIp01, para o gateway no $AppGw, usando o endereço armazenado no $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="99d27-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="99d27-118">Exemplo 2: Adicionar um IP privado estático como o endereço IP front-end</span><span class="sxs-lookup"><span data-stu-id="99d27-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="99d27-119">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="99d27-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="99d27-120">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="99d27-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="99d27-121">O terceiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="99d27-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="99d27-122">O quarto comando adiciona uma configuração ip front-end chamada FrontendIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="99d27-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="99d27-123">Exemplo 3: Adicionar um IP privado dinâmico como o endereço IP front-end</span><span class="sxs-lookup"><span data-stu-id="99d27-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="99d27-124">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="99d27-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="99d27-125">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="99d27-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="99d27-126">O terceiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="99d27-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="99d27-127">O quarto comando adiciona uma configuração de IP front-end chamada FrontendIP02 usando $Subnet do segundo comando.</span><span class="sxs-lookup"><span data-stu-id="99d27-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="99d27-128">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="99d27-128">PARAMETERS</span></span>

### <span data-ttu-id="99d27-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99d27-129">-ApplicationGateway</span></span>
<span data-ttu-id="99d27-130">Especifica o gateway de aplicativo ao qual este cmdlet adiciona uma configuração de IP front-end.</span><span class="sxs-lookup"><span data-stu-id="99d27-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="99d27-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d27-131">-DefaultProfile</span></span>
<span data-ttu-id="99d27-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="99d27-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d27-133">-Name</span><span class="sxs-lookup"><span data-stu-id="99d27-133">-Name</span></span>
<span data-ttu-id="99d27-134">Especifica o nome da configuração de IP front-end a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="99d27-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="99d27-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="99d27-135">-PrivateIPAddress</span></span>
<span data-ttu-id="99d27-136">Especifica o endereço IP privado a ser acrescentado como um IP front-end para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99d27-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="99d27-137">Se especificado, esse IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="99d27-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="99d27-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="99d27-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="99d27-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="99d27-139">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d27-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="99d27-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="99d27-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="99d27-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="99d27-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="99d27-142">-PublicIPAddress</span></span>
<span data-ttu-id="99d27-143">Especifica o endereço IP público que este cmdlet adiciona como um endereço IP front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99d27-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d27-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="99d27-144">-PublicIPAddressId</span></span>
<span data-ttu-id="99d27-145">Especifica a ID do endereço IP público que este cmdlet adiciona como um endereço IP front-end para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99d27-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="99d27-146">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="99d27-146">-Subnet</span></span>
<span data-ttu-id="99d27-147">Especifica a sub-rede que este cmdlet adiciona como configuração ip front-end.</span><span class="sxs-lookup"><span data-stu-id="99d27-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="99d27-148">Se você especificar esse parâmetro, ele implica que o gateway de aplicativo oferece suporte a uma configuração baseada em IP privada.</span><span class="sxs-lookup"><span data-stu-id="99d27-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="99d27-149">Se o *parâmetro PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="99d27-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="99d27-150">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será escolhido dinamicamente como o endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99d27-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d27-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="99d27-151">-SubnetId</span></span>
<span data-ttu-id="99d27-152">Especifica a ID da sub-rede que esse cmdlet adiciona como a configuração ip front-end.</span><span class="sxs-lookup"><span data-stu-id="99d27-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="99d27-153">Passar sub-rede implica em IP particular.</span><span class="sxs-lookup"><span data-stu-id="99d27-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="99d27-154">Se o *parâmetro PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="99d27-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="99d27-155">Caso contrário, um dos IP dessa sub-rede é escolhido dinamicamente como o IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99d27-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="99d27-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d27-156">CommonParameters</span></span>
<span data-ttu-id="99d27-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d27-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d27-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99d27-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d27-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99d27-159">INPUTS</span></span>

### <span data-ttu-id="99d27-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99d27-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99d27-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="99d27-161">OUTPUTS</span></span>

### <span data-ttu-id="99d27-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99d27-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99d27-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="99d27-163">NOTES</span></span>

## <span data-ttu-id="99d27-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99d27-164">RELATED LINKS</span></span>

[<span data-ttu-id="99d27-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99d27-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99d27-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99d27-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99d27-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99d27-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99d27-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99d27-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


