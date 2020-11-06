---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 212af54a6b3484b81e0914bd82e8ff68553f30ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440617"
---
# <span data-ttu-id="22665-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="22665-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="22665-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22665-102">SYNOPSIS</span></span>
<span data-ttu-id="22665-103">Adiciona uma configuração de IP de front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22665-103">Adds a front-end IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22665-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22665-104">SYNTAX</span></span>

### <span data-ttu-id="22665-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="22665-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22665-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="22665-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22665-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22665-107">DESCRIPTION</span></span>
<span data-ttu-id="22665-108">O cmdlet **Add-AzureRmApplicationGatewayFrontendIPConfig** adiciona uma configuração de IP de front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22665-108">The **Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="22665-109">Um gateway de aplicativo dá suporte a dois tipos de configurações de IP front-end:</span><span class="sxs-lookup"><span data-stu-id="22665-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="22665-110">Endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="22665-110">Public IP addresses</span></span>
- <span data-ttu-id="22665-111">Endereços IP particulares usando balanceamento de carga interna (ILB)</span><span class="sxs-lookup"><span data-stu-id="22665-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="22665-112">Um gateway de aplicativo pode ter no máximo um IP público e um IP privado.</span><span class="sxs-lookup"><span data-stu-id="22665-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="22665-113">Adicione o endereço IP público e o endereço IP privado como IPs de front-end separados.</span><span class="sxs-lookup"><span data-stu-id="22665-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="22665-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22665-114">EXAMPLES</span></span>

### <span data-ttu-id="22665-115">Exemplo 1: adicionar um IP público como o endereço IP de front-end</span><span class="sxs-lookup"><span data-stu-id="22665-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="22665-116">O primeiro comando cria um objeto de endereço IP público e o armazena na variável $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="22665-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="22665-117">O segundo comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="22665-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="22665-118">O terceiro comando adiciona a configuração de IP de front-end chamada FrontEndIp01, para o gateway em $AppGw, usando o endereço armazenado no $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="22665-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="22665-119">Exemplo 2: adicionar um IP privado estático como o endereço IP de front-end</span><span class="sxs-lookup"><span data-stu-id="22665-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="22665-120">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="22665-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="22665-121">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="22665-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="22665-122">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="22665-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="22665-123">O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="22665-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="22665-124">Exemplo 3: adicionar um IP privado dinâmico como o endereço IP de front-end</span><span class="sxs-lookup"><span data-stu-id="22665-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="22665-125">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="22665-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="22665-126">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="22665-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="22665-127">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="22665-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="22665-128">O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando.</span><span class="sxs-lookup"><span data-stu-id="22665-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="22665-129">OS</span><span class="sxs-lookup"><span data-stu-id="22665-129">PARAMETERS</span></span>

### <span data-ttu-id="22665-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22665-130">-ApplicationGateway</span></span>
<span data-ttu-id="22665-131">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="22665-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="22665-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="22665-132">-Name</span></span>
<span data-ttu-id="22665-133">Especifica o nome da configuração de IP de front-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="22665-133">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="22665-134">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="22665-134">-PrivateIPAddress</span></span>
<span data-ttu-id="22665-135">Especifica o endereço IP privado a ser adicionado como um IP front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22665-135">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="22665-136">Se especificado, esse IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="22665-136">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="22665-137">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="22665-137">-PublicIPAddress</span></span>
<span data-ttu-id="22665-138">Especifica o endereço IP público que esse cmdlet adiciona como um endereço IP front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22665-138">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22665-139">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="22665-139">-PublicIPAddressId</span></span>
<span data-ttu-id="22665-140">Especifica a ID do endereço IP público que esse cmdlet adiciona como um endereço IP front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22665-140">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="22665-141">-Subnet</span><span class="sxs-lookup"><span data-stu-id="22665-141">-Subnet</span></span>
<span data-ttu-id="22665-142">Especifica a sub-rede que esse cmdlet adiciona como configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="22665-142">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="22665-143">Se você especificar esse parâmetro, ele implica que o gateway do aplicativo dá suporte a uma configuração baseada em IP privado.</span><span class="sxs-lookup"><span data-stu-id="22665-143">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="22665-144">Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="22665-144">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="22665-145">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22665-145">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22665-146">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="22665-146">-SubnetId</span></span>
<span data-ttu-id="22665-147">Especifica a identificação de sub-rede que esse cmdlet adiciona como a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="22665-147">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="22665-148">Passar sub-rede implica IP privado.</span><span class="sxs-lookup"><span data-stu-id="22665-148">Passing subnet implies private IP.</span></span>
<span data-ttu-id="22665-149">Se o parâmetro *PrivateIPAddresss* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="22665-149">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="22665-150">Caso contrário, um dos IP desta sub-rede será retirado dinamicamente como o IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22665-150">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="22665-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22665-151">-DefaultProfile</span></span>
<span data-ttu-id="22665-152">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22665-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22665-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22665-153">CommonParameters</span></span>
<span data-ttu-id="22665-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22665-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22665-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22665-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22665-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22665-156">INPUTS</span></span>

### <span data-ttu-id="22665-157">System. String</span><span class="sxs-lookup"><span data-stu-id="22665-157">System.String</span></span>

## <span data-ttu-id="22665-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22665-158">OUTPUTS</span></span>

### <span data-ttu-id="22665-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22665-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22665-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22665-160">NOTES</span></span>

## <span data-ttu-id="22665-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22665-161">RELATED LINKS</span></span>

[<span data-ttu-id="22665-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="22665-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="22665-163">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="22665-163">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="22665-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="22665-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="22665-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="22665-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)

