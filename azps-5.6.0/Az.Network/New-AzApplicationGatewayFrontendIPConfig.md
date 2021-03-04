---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 214f408a5120982a903ed0d0d934c44073c32df8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889774"
---
# <span data-ttu-id="04961-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="04961-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="04961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04961-102">SYNOPSIS</span></span>
<span data-ttu-id="04961-103">Cria uma configuração de IP front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04961-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="04961-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="04961-104">SYNTAX</span></span>

### <span data-ttu-id="04961-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="04961-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04961-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="04961-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04961-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="04961-107">DESCRIPTION</span></span>
<span data-ttu-id="04961-108">O cmdlet **New-AzApplicationGatewayFrontendIPConfig** cria uma configuração de IP front-end para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="04961-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="04961-109">Um gateway de aplicativo dá suporte a dois tipos de configuração de IP front-end:</span><span class="sxs-lookup"><span data-stu-id="04961-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="04961-110">Endereços IP públicos - endereços IP privados usando o ILB (balanceamento de carga interno).</span><span class="sxs-lookup"><span data-stu-id="04961-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="04961-111">Um gateway de aplicativo pode ter no máximo um endereço IP público e um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="04961-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="04961-112">O endereço IP público e o endereço IP privado devem ser adicionados separadamente como endereços IP front-end.</span><span class="sxs-lookup"><span data-stu-id="04961-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="04961-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04961-113">EXAMPLES</span></span>

### <span data-ttu-id="04961-114">Exemplo 1: Criar uma configuração de IP front-end usando um objeto de recurso IP público</span><span class="sxs-lookup"><span data-stu-id="04961-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="04961-115">O primeiro comando cria um objeto de recurso IP público e o armazena na $PublicIP variável.</span><span class="sxs-lookup"><span data-stu-id="04961-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="04961-116">O segundo comando usa $PublicIP para criar uma nova configuração de IP front-end chamada FrontEndIP01 e a armazena na variável $FrontEnd front-end.</span><span class="sxs-lookup"><span data-stu-id="04961-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="04961-117">Exemplo 2: Criar um IP privado estático como o endereço IP front-end</span><span class="sxs-lookup"><span data-stu-id="04961-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="04961-118">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="04961-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="04961-119">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="04961-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="04961-120">O terceiro comando cria uma configuração ip front-end chamada FrontEndIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1 e, em seguida, o armazena na variável $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="04961-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="04961-121">Exemplo 3: Criar um IP privado dinâmico como o endereço IP front-end</span><span class="sxs-lookup"><span data-stu-id="04961-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="04961-122">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="04961-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="04961-123">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="04961-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="04961-124">O terceiro comando cria uma configuração ip front-end chamada FrontEndIP03 usando $Subnet do segundo comando e a armazena na variável $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="04961-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="04961-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="04961-125">PARAMETERS</span></span>

### <span data-ttu-id="04961-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04961-126">-DefaultProfile</span></span>
<span data-ttu-id="04961-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="04961-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04961-128">-Name</span><span class="sxs-lookup"><span data-stu-id="04961-128">-Name</span></span>
<span data-ttu-id="04961-129">Especifica o nome da configuração ip front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="04961-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="04961-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="04961-130">-PrivateIPAddress</span></span>
<span data-ttu-id="04961-131">Especifica o endereço IP privado que esse cmdlet associa ao endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04961-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="04961-132">Isso só poderá ser especificado se uma sub-rede for especificada.</span><span class="sxs-lookup"><span data-stu-id="04961-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="04961-133">Esse IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="04961-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="04961-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="04961-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="04961-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="04961-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="04961-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="04961-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="04961-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="04961-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="04961-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="04961-138">-PublicIPAddress</span></span>
<span data-ttu-id="04961-139">Especifica o objeto de endereço IP público que esse cmdlet associa ao endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04961-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="04961-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="04961-140">-PublicIPAddressId</span></span>
<span data-ttu-id="04961-141">Especifica a ID de endereço IP pública que esse cmdlet associa ao IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04961-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="04961-142">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="04961-142">-Subnet</span></span>
<span data-ttu-id="04961-143">Especifica o objeto de sub-rede que esse cmdlet associa ao endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04961-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="04961-144">Se você especificar esse parâmetro, ele implica que o gateway usa um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="04961-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="04961-145">Se o *parâmetro PrivateIPAddress* for especificado, ele deve pertencer à sub-rede especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="04961-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="04961-146">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será escolhido dinamicamente como o endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04961-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="04961-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="04961-147">-SubnetId</span></span>
<span data-ttu-id="04961-148">Especifica a ID de sub-rede que esse cmdlet associa à configuração de IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04961-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="04961-149">Se você especificar o parâmetro *Subnet,* ele implica que o gateway usa um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="04961-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="04961-150">Se o *parâmetro PrivateIPAddress* for especificado, ele deve pertencer à sub-rede especificada por *Subnet*.</span><span class="sxs-lookup"><span data-stu-id="04961-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="04961-151">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será escolhido dinamicamente como o endereço IP front-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04961-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="04961-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04961-152">CommonParameters</span></span>
<span data-ttu-id="04961-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04961-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04961-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04961-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04961-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04961-155">INPUTS</span></span>

### <span data-ttu-id="04961-156">Nenhum</span><span class="sxs-lookup"><span data-stu-id="04961-156">None</span></span>

## <span data-ttu-id="04961-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="04961-157">OUTPUTS</span></span>

### <span data-ttu-id="04961-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="04961-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="04961-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="04961-159">NOTES</span></span>

## <span data-ttu-id="04961-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04961-160">RELATED LINKS</span></span>

[<span data-ttu-id="04961-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="04961-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="04961-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="04961-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="04961-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="04961-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="04961-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="04961-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


