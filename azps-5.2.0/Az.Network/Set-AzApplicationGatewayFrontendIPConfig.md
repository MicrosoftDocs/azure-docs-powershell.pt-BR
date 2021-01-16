---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257494"
---
# <span data-ttu-id="b9636-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b9636-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="b9636-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9636-102">SYNOPSIS</span></span>
<span data-ttu-id="b9636-103">Modifica uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b9636-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="b9636-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9636-104">SYNTAX</span></span>

### <span data-ttu-id="b9636-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9636-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9636-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b9636-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9636-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9636-107">DESCRIPTION</span></span>
<span data-ttu-id="b9636-108">O cmdlet **set-AzApplicationGatewayFrontendIPConfig** atualiza uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="b9636-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="b9636-109">Um gateway de aplicativo dá suporte a dois tipos de endereços IP front-end:</span><span class="sxs-lookup"><span data-stu-id="b9636-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="b9636-110">Endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="b9636-110">Public IP addresses</span></span>
- <span data-ttu-id="b9636-111">Endereços IP privados para os quais a configuração usa balanceamento de carga interno (ILB) um gateway de aplicativo pode ter no máximo um endereço IP público e um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="b9636-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="b9636-112">Um endereço IP público e um endereço IP privado devem ser adicionados separadamente como endereços IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="b9636-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="b9636-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9636-113">EXAMPLES</span></span>

### <span data-ttu-id="b9636-114">Exemplo 1: definir um IP público como IP front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b9636-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="b9636-115">O primeiro comando cria um objeto de endereço IP público e o armazena na variável $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="b9636-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="b9636-116">O segundo comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9636-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9636-117">O terceiro comando atualiza a configuração de IP de front-end chamada FrontEndIp01, para o gateway em $AppGw, usando o endereço armazenado no $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="b9636-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="b9636-118">Exemplo 2: definir um IP privado estático como o IP de front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b9636-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="b9636-119">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="b9636-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="b9636-120">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b9636-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b9636-121">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9636-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9636-122">O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="b9636-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="b9636-123">Exemplo 3: definir um IP privado dinâmico como o IP de front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b9636-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="b9636-124">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="b9636-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="b9636-125">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b9636-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b9636-126">O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9636-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9636-127">O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando.</span><span class="sxs-lookup"><span data-stu-id="b9636-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="b9636-128">OS</span><span class="sxs-lookup"><span data-stu-id="b9636-128">PARAMETERS</span></span>

### <span data-ttu-id="b9636-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9636-129">-ApplicationGateway</span></span>
<span data-ttu-id="b9636-130">Especifica um objeto do gateway do aplicativo no qual modificar a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="b9636-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="b9636-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9636-131">-DefaultProfile</span></span>
<span data-ttu-id="b9636-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9636-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9636-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9636-133">-Name</span></span>
<span data-ttu-id="b9636-134">Especifica o nome da configuração de IP de front-end que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b9636-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b9636-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9636-135">-PrivateIPAddress</span></span>
<span data-ttu-id="b9636-136">Especifica o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="b9636-136">Specifies the private IP address.</span></span>
<span data-ttu-id="b9636-137">Se especificado, esse IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b9636-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="b9636-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9636-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="b9636-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9636-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="b9636-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b9636-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="b9636-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b9636-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="b9636-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9636-142">-PublicIPAddress</span></span>
<span data-ttu-id="b9636-143">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="b9636-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="b9636-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="b9636-144">-PublicIPAddressId</span></span>
<span data-ttu-id="b9636-145">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="b9636-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="b9636-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b9636-146">-Subnet</span></span>
<span data-ttu-id="b9636-147">Especifica a sub-rede que o gateway do aplicativo usa.</span><span class="sxs-lookup"><span data-stu-id="b9636-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="b9636-148">Especifique esse parâmetro se o gateway usar um endereço IP particular.</span><span class="sxs-lookup"><span data-stu-id="b9636-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="b9636-149">Se o endereço *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b9636-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="b9636-150">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9636-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b9636-151">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="b9636-151">-SubnetId</span></span>
<span data-ttu-id="b9636-152">Especifica a identificação de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b9636-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="b9636-153">Especifique esse parâmetro se o gateway usar um endereço IP particular.</span><span class="sxs-lookup"><span data-stu-id="b9636-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="b9636-154">Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b9636-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="b9636-155">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9636-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b9636-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9636-156">CommonParameters</span></span>
<span data-ttu-id="b9636-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9636-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9636-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9636-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9636-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9636-159">INPUTS</span></span>

### <span data-ttu-id="b9636-160">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9636-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9636-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9636-161">OUTPUTS</span></span>

### <span data-ttu-id="b9636-162">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9636-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9636-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9636-163">NOTES</span></span>

## <span data-ttu-id="b9636-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9636-164">RELATED LINKS</span></span>

[<span data-ttu-id="b9636-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b9636-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b9636-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b9636-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b9636-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b9636-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b9636-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b9636-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b9636-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b9636-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


