---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 6f2e9ea87b478c4992bdad6c2c20029bec90ac13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603163"
---
# <span data-ttu-id="c6985-101">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6985-101">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="c6985-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6985-102">SYNOPSIS</span></span>
<span data-ttu-id="c6985-103">Cria uma configuração de IP de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6985-103">Creates a front-end IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6985-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6985-104">SYNTAX</span></span>

### <span data-ttu-id="c6985-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6985-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6985-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c6985-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6985-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6985-107">DESCRIPTION</span></span>
<span data-ttu-id="c6985-108">O cmdlet **New-AzureRmApplicationGatewayFrontendIPConfig** cria um CONFIGURATON de IP front-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6985-108">The **New-AzureRmApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuraton for an Azure application gateway.</span></span>
<span data-ttu-id="c6985-109">Um gateway de aplicativo dá suporte a dois tipos de configuração de IP front-end:</span><span class="sxs-lookup"><span data-stu-id="c6985-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="c6985-110">Endereços IP públicos--endereços IP privados usando o balanceamento de carga interno (ILB).</span><span class="sxs-lookup"><span data-stu-id="c6985-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="c6985-111">Um gateway de aplicativo pode ter no máximo um endereço IP público e um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="c6985-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="c6985-112">O endereço IP público e o endereço IP privado devem ser adicionados separadamente como endereços IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="c6985-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="c6985-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6985-113">EXAMPLES</span></span>

### <span data-ttu-id="c6985-114">Exemplo 1: criar uma configuração de IP de front-end usando um objeto de recurso de IP público</span><span class="sxs-lookup"><span data-stu-id="c6985-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="c6985-115">O primeiro comando cria um objeto de recurso de IP público e o armazena na variável $PublicIP.</span><span class="sxs-lookup"><span data-stu-id="c6985-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="c6985-116">O segundo comando usa $PublicIP para criar uma nova configuração de IP de front-end chamada FrontEndIP01 e a armazena na variável $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="c6985-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="c6985-117">Exemplo 2: criar um IP privado estático como o endereço IP de front-end</span><span class="sxs-lookup"><span data-stu-id="c6985-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="c6985-118">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="c6985-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="c6985-119">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c6985-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c6985-120">O terceiro comando cria uma configuração de IP de front-end chamada FrontEndIP02 usando $Subnet do segundo comando e do 10.0.1.1 de endereço IP privado e, em seguida, armazena-o na variável $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="c6985-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="c6985-121">Exemplo 3: criar um IP privado dinâmico como o endereço IP de front-end</span><span class="sxs-lookup"><span data-stu-id="c6985-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="c6985-122">O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="c6985-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="c6985-123">O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c6985-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c6985-124">O terceiro comando cria uma configuração de IP de front-end chamada FrontEndIP03 usando $Subnet do segundo comando e armazena-o na variável $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="c6985-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="c6985-125">OS</span><span class="sxs-lookup"><span data-stu-id="c6985-125">PARAMETERS</span></span>

### <span data-ttu-id="c6985-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6985-126">-DefaultProfile</span></span>
<span data-ttu-id="c6985-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6985-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6985-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6985-128">-Name</span></span>
<span data-ttu-id="c6985-129">Especifica o nome da configuração de IP de front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c6985-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c6985-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="c6985-130">-PrivateIPAddress</span></span>
<span data-ttu-id="c6985-131">Especifica o endereço IP privado que esse cmdlet associa ao endereço IP front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6985-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="c6985-132">Isso pode ser especificado apenas se uma sub-rede for especificada.</span><span class="sxs-lookup"><span data-stu-id="c6985-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="c6985-133">Este IP é alocado estaticamente da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="c6985-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="c6985-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="c6985-134">-PublicIPAddress</span></span>
<span data-ttu-id="c6985-135">Especifica o objeto de endereço IP público que esse cmdlet associa ao endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6985-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c6985-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="c6985-136">-PublicIPAddressId</span></span>
<span data-ttu-id="c6985-137">Especifica a identificação do endereço IP público que esse cmdlet associa ao IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6985-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="c6985-138">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c6985-138">-Subnet</span></span>
<span data-ttu-id="c6985-139">Especifica o objeto de sub-rede que este cmdlet associa ao endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6985-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="c6985-140">Se você especificar esse parâmetro, ele indicará que o gateway usa um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="c6985-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="c6985-141">Se o parâmetro *PrivateIPAddresss* for especificado, ele deve pertencer à sub-rede especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c6985-141">If the *PrivateIPAddresss* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="c6985-142">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6985-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c6985-143">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="c6985-143">-SubnetId</span></span>
<span data-ttu-id="c6985-144">Especifica a ID de sub-rede que esse cmdlet associa à configuração de IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6985-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="c6985-145">Se você especificar o parâmetro *subnet* , isso significa que o gateway usa um endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="c6985-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="c6985-146">Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer à sub-rede especificada pela *sub-rede*.</span><span class="sxs-lookup"><span data-stu-id="c6985-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="c6985-147">Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6985-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c6985-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6985-148">CommonParameters</span></span>
<span data-ttu-id="c6985-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6985-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6985-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6985-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6985-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6985-151">INPUTS</span></span>

### <span data-ttu-id="c6985-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c6985-152">None</span></span>

## <span data-ttu-id="c6985-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6985-153">OUTPUTS</span></span>

### <span data-ttu-id="c6985-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6985-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="c6985-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6985-155">NOTES</span></span>

## <span data-ttu-id="c6985-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6985-156">RELATED LINKS</span></span>

[<span data-ttu-id="c6985-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6985-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c6985-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6985-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c6985-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6985-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c6985-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6985-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


