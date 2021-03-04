---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 17ef06c6f91f650da95ddcbfb87b09a60c1948d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885984"
---
# <span data-ttu-id="b76ff-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b76ff-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="b76ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b76ff-103">Modifica uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b76ff-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="b76ff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b76ff-104">SYNTAX</span></span>

### <span data-ttu-id="b76ff-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b76ff-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b76ff-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b76ff-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b76ff-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b76ff-107">DESCRIPTION</span></span>
<span data-ttu-id="b76ff-108">O cmdlet **Set-AzApplicationGatewayFrontendIPConfig** atualiza uma configuração de IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b76ff-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="b76ff-109">Um gateway de aplicativo dá suporte a dois tipos de endereços IP front-end:</span><span class="sxs-lookup"><span data-stu-id="b76ff-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="b76ff-110">Endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="b76ff-110">Public IP addresses</span></span>
- <span data-ttu-id="b76ff-111">Endereços IP privados para os quais a configuração usa o ILB (Internal Load Balancing) Um gateway de aplicativo pode ter no máximo um endereço IP público e um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="b76ff-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="b76ff-112">Um endereço IP público e um endereço IP privado devem ser adicionados separadamente como endereços IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b76ff-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="b76ff-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b76ff-113">EXAMPLES</span></span>

### <span data-ttu-id="b76ff-114">Exemplo 1: definir um IP público como IP front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b76ff-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="b76ff-115">O primeiro comando cria um objeto de endereço IP público e o armazena na $PublicIp variável.</span><span class="sxs-lookup"><span data-stu-id="b76ff-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="b76ff-116">O segundo comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b76ff-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b76ff-117">O terceiro comando atualiza a configuração de IP front-end chamada FrontEndIp01, para o gateway no $AppGw, usando o endereço armazenado no $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="b76ff-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="b76ff-118">Exemplo 2: definir um IP privado estático como o IP front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b76ff-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="b76ff-119">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="b76ff-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="b76ff-120">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b76ff-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b76ff-121">O terceiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b76ff-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b76ff-122">O quarto comando adiciona uma configuração ip front-end chamada FrontendIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="b76ff-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="b76ff-123">Exemplo 3: definir um IP privado dinâmico como o IP front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b76ff-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="b76ff-124">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="b76ff-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="b76ff-125">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b76ff-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b76ff-126">O terceiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b76ff-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b76ff-127">O quarto comando adiciona uma configuração de IP front-end chamada FrontendIP02 usando $Subnet do segundo comando.</span><span class="sxs-lookup"><span data-stu-id="b76ff-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="b76ff-128">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b76ff-128">PARAMETERS</span></span>

### <span data-ttu-id="b76ff-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b76ff-129">-ApplicationGateway</span></span>
<span data-ttu-id="b76ff-130">Especifica um objeto gateway de aplicativo no qual modificar a configuração de IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b76ff-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="b76ff-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76ff-131">-DefaultProfile</span></span>
<span data-ttu-id="b76ff-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b76ff-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76ff-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b76ff-133">-Name</span></span>
<span data-ttu-id="b76ff-134">Especifica o nome da configuração ip front-end que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b76ff-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b76ff-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="b76ff-135">-PrivateIPAddress</span></span>
<span data-ttu-id="b76ff-136">Especifica o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="b76ff-136">Specifies the private IP address.</span></span>
<span data-ttu-id="b76ff-137">Se especificado, esse IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b76ff-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="b76ff-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b76ff-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="b76ff-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b76ff-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="b76ff-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b76ff-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="b76ff-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b76ff-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="b76ff-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b76ff-142">-PublicIPAddress</span></span>
<span data-ttu-id="b76ff-143">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="b76ff-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="b76ff-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="b76ff-144">-PublicIPAddressId</span></span>
<span data-ttu-id="b76ff-145">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="b76ff-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="b76ff-146">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="b76ff-146">-Subnet</span></span>
<span data-ttu-id="b76ff-147">Especifica a sub-rede que o gateway de aplicativo usa.</span><span class="sxs-lookup"><span data-stu-id="b76ff-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="b76ff-148">Especifique esse parâmetro se o gateway usar um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="b76ff-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="b76ff-149">Se o *endereço PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b76ff-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="b76ff-150">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será escolhido dinamicamente como o endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b76ff-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b76ff-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b76ff-151">-SubnetId</span></span>
<span data-ttu-id="b76ff-152">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b76ff-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="b76ff-153">Especifique esse parâmetro se o gateway usar um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="b76ff-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="b76ff-154">Se o *parâmetro PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b76ff-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="b76ff-155">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será escolhido dinamicamente como o endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b76ff-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b76ff-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76ff-156">CommonParameters</span></span>
<span data-ttu-id="b76ff-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76ff-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76ff-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b76ff-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76ff-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b76ff-159">INPUTS</span></span>

### <span data-ttu-id="b76ff-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b76ff-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b76ff-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b76ff-161">OUTPUTS</span></span>

### <span data-ttu-id="b76ff-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b76ff-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b76ff-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="b76ff-163">NOTES</span></span>

## <span data-ttu-id="b76ff-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b76ff-164">RELATED LINKS</span></span>

[<span data-ttu-id="b76ff-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b76ff-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b76ff-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b76ff-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b76ff-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b76ff-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b76ff-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b76ff-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b76ff-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b76ff-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


