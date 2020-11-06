---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 38a74e6f11516b3a873709dfec118ffd2a1ad6ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440436"
---
# <span data-ttu-id="885bb-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="885bb-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="885bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="885bb-102">SYNOPSIS</span></span>
<span data-ttu-id="885bb-103">Modifica uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="885bb-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="885bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="885bb-104">SYNTAX</span></span>

### <span data-ttu-id="885bb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="885bb-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="885bb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="885bb-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="885bb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="885bb-107">DESCRIPTION</span></span>
<span data-ttu-id="885bb-108">O cmdlet **set-AzureRmApplicationGatewayFrontendIPConfig** atualiza uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="885bb-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="885bb-109">Um gateway de aplicativo dá suporte a dois tipos de endereços IP front-end:</span><span class="sxs-lookup"><span data-stu-id="885bb-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="885bb-110">Endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="885bb-110">Public IP addresses</span></span>
- <span data-ttu-id="885bb-111">Endereços IP privados para os quais a configuração usa balanceamento de carga interno (ILB)</span><span class="sxs-lookup"><span data-stu-id="885bb-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="885bb-112">Um gateway de aplicativo pode ter no máximo um endereço IP público e um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="885bb-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="885bb-113">Um endereço IP público e um endereço IP privado devem ser adicionados separadamente como endereços IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="885bb-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="885bb-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="885bb-114">EXAMPLES</span></span>

### <span data-ttu-id="885bb-115">Exemplo 1: definir um IP público como IP front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="885bb-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="885bb-116">O primeiro comando cria um objeto de endereço IP público e o armazena na variável $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="885bb-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="885bb-117">O segundo comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="885bb-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="885bb-118">O terceiro comando atualiza a configuração de IP de front-end chamada FrontEndIp01, para o gateway em $AppGw, usando o endereço armazenado no $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="885bb-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="885bb-119">Exemplo 2: definir um IP privado estático como o IP de front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="885bb-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="885bb-120">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="885bb-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="885bb-121">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="885bb-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="885bb-122">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="885bb-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="885bb-123">O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="885bb-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="885bb-124">Exemplo 3: definir um IP privado dinâmico como o IP de front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="885bb-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="885bb-125">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="885bb-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="885bb-126">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="885bb-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="885bb-127">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="885bb-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="885bb-128">O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando.</span><span class="sxs-lookup"><span data-stu-id="885bb-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="885bb-129">OS</span><span class="sxs-lookup"><span data-stu-id="885bb-129">PARAMETERS</span></span>

### <span data-ttu-id="885bb-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="885bb-130">-ApplicationGateway</span></span>
<span data-ttu-id="885bb-131">Especifica um objeto do gateway do aplicativo no qual modificar a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="885bb-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="885bb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885bb-132">-DefaultProfile</span></span>
<span data-ttu-id="885bb-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="885bb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="885bb-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="885bb-134">-Name</span></span>
<span data-ttu-id="885bb-135">Especifica o nome da configuração de IP de front-end que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="885bb-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="885bb-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="885bb-136">-PrivateIPAddress</span></span>
<span data-ttu-id="885bb-137">Especifica o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="885bb-137">Specifies the private IP address.</span></span>
<span data-ttu-id="885bb-138">Se especificado, esse IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="885bb-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="885bb-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="885bb-139">-PublicIPAddress</span></span>
<span data-ttu-id="885bb-140">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="885bb-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="885bb-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="885bb-141">-PublicIPAddressId</span></span>
<span data-ttu-id="885bb-142">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="885bb-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="885bb-143">-Subnet</span><span class="sxs-lookup"><span data-stu-id="885bb-143">-Subnet</span></span>
<span data-ttu-id="885bb-144">Especifica a sub-rede que o gateway do aplicativo usa.</span><span class="sxs-lookup"><span data-stu-id="885bb-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="885bb-145">Especifique esse parâmetro se o gateway usar um endereço IP particular.</span><span class="sxs-lookup"><span data-stu-id="885bb-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="885bb-146">Se o endereço *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="885bb-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="885bb-147">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="885bb-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="885bb-148">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="885bb-148">-SubnetId</span></span>
<span data-ttu-id="885bb-149">Especifica a identificação de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="885bb-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="885bb-150">Especifique esse parâmetro se o gateway usar um endereço IP particular.</span><span class="sxs-lookup"><span data-stu-id="885bb-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="885bb-151">Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="885bb-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="885bb-152">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="885bb-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="885bb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885bb-153">CommonParameters</span></span>
<span data-ttu-id="885bb-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="885bb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885bb-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="885bb-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885bb-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="885bb-156">INPUTS</span></span>

### <span data-ttu-id="885bb-157">System. String</span><span class="sxs-lookup"><span data-stu-id="885bb-157">System.String</span></span>

## <span data-ttu-id="885bb-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="885bb-158">OUTPUTS</span></span>

### <span data-ttu-id="885bb-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="885bb-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="885bb-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="885bb-160">NOTES</span></span>

## <span data-ttu-id="885bb-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="885bb-161">RELATED LINKS</span></span>

[<span data-ttu-id="885bb-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="885bb-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="885bb-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="885bb-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="885bb-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="885bb-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="885bb-165">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="885bb-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="885bb-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="885bb-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


