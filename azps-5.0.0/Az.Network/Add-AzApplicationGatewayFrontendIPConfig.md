---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117278"
---
# <span data-ttu-id="faab4-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="faab4-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="faab4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="faab4-102">SYNOPSIS</span></span>
<span data-ttu-id="faab4-103">Adiciona uma configuração de IP de front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="faab4-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="faab4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="faab4-104">SYNTAX</span></span>

### <span data-ttu-id="faab4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="faab4-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faab4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="faab4-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faab4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="faab4-107">DESCRIPTION</span></span>
<span data-ttu-id="faab4-108">O cmdlet **Add-AzApplicationGatewayFrontendIPConfig** adiciona uma configuração de IP de front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="faab4-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="faab4-109">Um gateway de aplicativo dá suporte a dois tipos de configurações de IP front-end:</span><span class="sxs-lookup"><span data-stu-id="faab4-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="faab4-110">Endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="faab4-110">Public IP addresses</span></span>
- <span data-ttu-id="faab4-111">Endereços IP privados usando o ILB (balanceamento de carga interna) um gateway de aplicativo pode ter no máximo um IP público e um IP privado.</span><span class="sxs-lookup"><span data-stu-id="faab4-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="faab4-112">Adicione o endereço IP público e o endereço IP privado como IPs de front-end separados.</span><span class="sxs-lookup"><span data-stu-id="faab4-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="faab4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="faab4-113">EXAMPLES</span></span>

### <span data-ttu-id="faab4-114">Exemplo 1: adicionar um IP público como o endereço IP de front-end</span><span class="sxs-lookup"><span data-stu-id="faab4-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="faab4-115">O primeiro comando cria um objeto de endereço IP público e o armazena na variável $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="faab4-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="faab4-116">O segundo comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="faab4-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="faab4-117">O terceiro comando adiciona a configuração de IP de front-end chamada FrontEndIp01, para o gateway em $AppGw, usando o endereço armazenado no $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="faab4-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="faab4-118">Exemplo 2: adicionar um IP privado estático como o endereço IP de front-end</span><span class="sxs-lookup"><span data-stu-id="faab4-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="faab4-119">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="faab4-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="faab4-120">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="faab4-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="faab4-121">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="faab4-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="faab4-122">O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="faab4-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="faab4-123">Exemplo 3: adicionar um IP privado dinâmico como o endereço IP de front-end</span><span class="sxs-lookup"><span data-stu-id="faab4-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="faab4-124">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="faab4-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="faab4-125">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="faab4-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="faab4-126">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="faab4-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="faab4-127">O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando.</span><span class="sxs-lookup"><span data-stu-id="faab4-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="faab4-128">OS</span><span class="sxs-lookup"><span data-stu-id="faab4-128">PARAMETERS</span></span>

### <span data-ttu-id="faab4-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="faab4-129">-ApplicationGateway</span></span>
<span data-ttu-id="faab4-130">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="faab4-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="faab4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faab4-131">-DefaultProfile</span></span>
<span data-ttu-id="faab4-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="faab4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faab4-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="faab4-133">-Name</span></span>
<span data-ttu-id="faab4-134">Especifica o nome da configuração de IP de front-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="faab4-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="faab4-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="faab4-135">-PrivateIPAddress</span></span>
<span data-ttu-id="faab4-136">Especifica o endereço IP privado a ser adicionado como um IP front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="faab4-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="faab4-137">Se especificado, esse IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="faab4-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="faab4-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="faab4-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="faab4-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="faab4-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="faab4-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="faab4-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="faab4-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="faab4-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="faab4-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="faab4-142">-PublicIPAddress</span></span>
<span data-ttu-id="faab4-143">Especifica o endereço IP público que esse cmdlet adiciona como um endereço IP front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="faab4-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="faab4-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="faab4-144">-PublicIPAddressId</span></span>
<span data-ttu-id="faab4-145">Especifica a ID do endereço IP público que esse cmdlet adiciona como um endereço IP front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="faab4-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="faab4-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="faab4-146">-Subnet</span></span>
<span data-ttu-id="faab4-147">Especifica a sub-rede que esse cmdlet adiciona como configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="faab4-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="faab4-148">Se você especificar esse parâmetro, ele implica que o gateway do aplicativo dá suporte a uma configuração baseada em IP privado.</span><span class="sxs-lookup"><span data-stu-id="faab4-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="faab4-149">Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="faab4-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="faab4-150">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="faab4-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="faab4-151">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="faab4-151">-SubnetId</span></span>
<span data-ttu-id="faab4-152">Especifica a identificação de sub-rede que esse cmdlet adiciona como a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="faab4-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="faab4-153">Passar sub-rede implica IP privado.</span><span class="sxs-lookup"><span data-stu-id="faab4-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="faab4-154">Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="faab4-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="faab4-155">Caso contrário, um dos IP desta sub-rede será retirado dinamicamente como o IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="faab4-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="faab4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faab4-156">CommonParameters</span></span>
<span data-ttu-id="faab4-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faab4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faab4-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faab4-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faab4-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="faab4-159">INPUTS</span></span>

### <span data-ttu-id="faab4-160">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="faab4-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="faab4-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="faab4-161">OUTPUTS</span></span>

### <span data-ttu-id="faab4-162">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="faab4-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="faab4-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="faab4-163">NOTES</span></span>

## <span data-ttu-id="faab4-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="faab4-164">RELATED LINKS</span></span>

[<span data-ttu-id="faab4-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="faab4-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="faab4-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="faab4-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="faab4-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="faab4-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="faab4-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="faab4-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


