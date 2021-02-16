---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118347"
---
# <span data-ttu-id="fd17a-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fd17a-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="fd17a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd17a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd17a-103">Cria uma configuração IP front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd17a-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="fd17a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd17a-104">SYNTAX</span></span>

### <span data-ttu-id="fd17a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd17a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd17a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fd17a-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd17a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd17a-107">DESCRIPTION</span></span>
<span data-ttu-id="fd17a-108">O cmdlet **New-AzApplicationGatewayFrontendIPConfig** cria uma configuração IP front-end para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd17a-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="fd17a-109">Um gateway de aplicativo dá suporte a dois tipos de configuração IP front-end:</span><span class="sxs-lookup"><span data-stu-id="fd17a-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="fd17a-110">Endereços IP públicos - endereços IP particulares usando o balanceamento de carga interno (ILB).</span><span class="sxs-lookup"><span data-stu-id="fd17a-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="fd17a-111">Um gateway de aplicativo pode ter no máximo um endereço IP público e um endereço IP particular.</span><span class="sxs-lookup"><span data-stu-id="fd17a-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="fd17a-112">O endereço IP público e o endereço IP particular devem ser adicionados separadamente como endereços IP front-end.</span><span class="sxs-lookup"><span data-stu-id="fd17a-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="fd17a-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd17a-113">EXAMPLES</span></span>

### <span data-ttu-id="fd17a-114">Exemplo 1: Criar uma configuração IP front-end usando um objeto de recurso IP público</span><span class="sxs-lookup"><span data-stu-id="fd17a-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="fd17a-115">O primeiro comando cria um objeto de recurso IP público e o armazena na variável $PublicIP dados.</span><span class="sxs-lookup"><span data-stu-id="fd17a-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="fd17a-116">O segundo comando usa $PublicIP para criar uma nova configuração de IP front-end chamada FrontEndIP01 e a armazena na variável $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="fd17a-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="fd17a-117">Exemplo 2: Criar um IP privado estático como o endereço IP front-end</span><span class="sxs-lookup"><span data-stu-id="fd17a-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="fd17a-118">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="fd17a-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="fd17a-119">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet dados.</span><span class="sxs-lookup"><span data-stu-id="fd17a-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="fd17a-120">O terceiro comando cria uma configuração IP front-end chamada FrontEndIP02 usando o $Subnet do segundo comando e o endereço IP particular 10.0.1.1 e armazena-o na variável $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="fd17a-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="fd17a-121">Exemplo 3: Criar um IP privado dinâmico como o endereço IP front-end</span><span class="sxs-lookup"><span data-stu-id="fd17a-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="fd17a-122">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="fd17a-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="fd17a-123">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet dados.</span><span class="sxs-lookup"><span data-stu-id="fd17a-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="fd17a-124">O terceiro comando cria uma configuração IP front-end chamada FrontEndIP03 usando $Subnet do segundo comando e a armazena na variável $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="fd17a-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="fd17a-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd17a-125">PARAMETERS</span></span>

### <span data-ttu-id="fd17a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd17a-126">-DefaultProfile</span></span>
<span data-ttu-id="fd17a-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fd17a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd17a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd17a-128">-Name</span></span>
<span data-ttu-id="fd17a-129">Especifica o nome da configuração IP de front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="fd17a-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fd17a-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="fd17a-130">-PrivateIPAddress</span></span>
<span data-ttu-id="fd17a-131">Especifica o endereço IP particular que este cmdlet associa ao endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd17a-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="fd17a-132">Isso só poderá ser especificado se uma sub-rede for especificada.</span><span class="sxs-lookup"><span data-stu-id="fd17a-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="fd17a-133">Este IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fd17a-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="fd17a-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd17a-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="fd17a-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd17a-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="fd17a-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fd17a-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="fd17a-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fd17a-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="fd17a-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="fd17a-138">-PublicIPAddress</span></span>
<span data-ttu-id="fd17a-139">Especifica o objeto de endereço IP público que este cmdlet associa ao endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd17a-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fd17a-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="fd17a-140">-PublicIPAddressId</span></span>
<span data-ttu-id="fd17a-141">Especifica a ID de endereço IP pública que este cmdlet associa ao IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd17a-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="fd17a-142">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="fd17a-142">-Subnet</span></span>
<span data-ttu-id="fd17a-143">Especifica o objeto da sub-rede que esse cmdlet associa ao endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd17a-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="fd17a-144">Se você especificar esse parâmetro, isso implica que o gateway usa um endereço IP particular.</span><span class="sxs-lookup"><span data-stu-id="fd17a-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="fd17a-145">Se o *parâmetro PrivateIPAddress* for especificado, ele deve pertencer à sub-rede especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fd17a-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="fd17a-146">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será escolhido dinamicamente como o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd17a-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fd17a-147">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="fd17a-147">-SubnetId</span></span>
<span data-ttu-id="fd17a-148">Especifica a ID da sub-rede que esse cmdlet associa à configuração de IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd17a-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="fd17a-149">Se você especificar o parâmetro *sub-rede,* isso implica que o gateway usa um endereço IP particular.</span><span class="sxs-lookup"><span data-stu-id="fd17a-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="fd17a-150">Se o *parâmetro PrivateIPAddress* for especificado, ele deve pertencer à sub-rede especificada pela *Sub-rede.*</span><span class="sxs-lookup"><span data-stu-id="fd17a-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="fd17a-151">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será escolhido dinamicamente como o endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd17a-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fd17a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd17a-152">CommonParameters</span></span>
<span data-ttu-id="fd17a-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd17a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd17a-154">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd17a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd17a-155">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd17a-155">INPUTS</span></span>

### <span data-ttu-id="fd17a-156">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fd17a-156">None</span></span>

## <span data-ttu-id="fd17a-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd17a-157">OUTPUTS</span></span>

### <span data-ttu-id="fd17a-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd17a-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="fd17a-159">Notas</span><span class="sxs-lookup"><span data-stu-id="fd17a-159">NOTES</span></span>

## <span data-ttu-id="fd17a-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd17a-160">RELATED LINKS</span></span>

[<span data-ttu-id="fd17a-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fd17a-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fd17a-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fd17a-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fd17a-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fd17a-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fd17a-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fd17a-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


