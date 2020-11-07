---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: f54527b167fa15ea4c4e878b81d86a00079e28a0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786509"
---
# <span data-ttu-id="9c1e6-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c1e6-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="9c1e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="9c1e6-103">Adiciona uma configuração de IP front-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c1e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c1e6-104">SYNTAX</span></span>

### <span data-ttu-id="9c1e6-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="9c1e6-105">SetByResourceSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c1e6-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="9c1e6-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c1e6-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9c1e6-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c1e6-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9c1e6-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c1e6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c1e6-109">DESCRIPTION</span></span>
<span data-ttu-id="9c1e6-110">O cmdlet **Add-AzureRmLoadBalancerFrontendIpConifg** adiciona uma configuração de IP de front-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="9c1e6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c1e6-111">EXAMPLES</span></span>

### <span data-ttu-id="9c1e6-112">Exemplo 1 adicionar uma configuração de IP de front-end com um endereço IP dinâmico</span><span class="sxs-lookup"><span data-stu-id="9c1e6-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="9c1e6-113">O primeiro comando obtém a rede virtual do Azure chamada MyVnet e passa o resultado usando o pipeline para o cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** para obter a sub-rede chamada mysubnet.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="9c1e6-114">Em seguida, o comando armazena o resultado na variável chamada $Subnet.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="9c1e6-115">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com um endereço IP privado dinâmico da sub-rede armazenada na variável chamada $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="9c1e6-116">Exemplo 2 adicionar uma configuração de IP de front-end com um endereço IP estático</span><span class="sxs-lookup"><span data-stu-id="9c1e6-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="9c1e6-117">O primeiro comando obtém a rede virtual do Azure chamada MyVnet e passa o resultado usando o pipeline para o cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** para obter a sub-rede chamada mysubnet.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="9c1e6-118">Em seguida, o comando armazena o resultado na variável chamada $Subnet.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="9c1e6-119">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com um endereço IP privado estático da sub-rede armazenada na variável chamada $subnet.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="9c1e6-120">Exemplo 3 adicionar uma configuração de IP de front-end com um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="9c1e6-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="9c1e6-121">O primeiro comando obtém o endereço IP público do Azure chamado MyPub e armazena o resultado na variável chamada $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="9c1e6-122">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com endereço IP público armazenado na variável chamada $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="9c1e6-123">OS</span><span class="sxs-lookup"><span data-stu-id="9c1e6-123">PARAMETERS</span></span>

### <span data-ttu-id="9c1e6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c1e6-124">-DefaultProfile</span></span>
<span data-ttu-id="9c1e6-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c1e6-126">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="9c1e6-126">-LoadBalancer</span></span>
<span data-ttu-id="9c1e6-127">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="9c1e6-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="9c1e6-128">Esse cmdlet adiciona uma configuração de IP de front-end para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c1e6-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c1e6-129">-Name</span></span>
<span data-ttu-id="9c1e6-130">Especifica o nome da configuração de IP de front-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="9c1e6-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9c1e6-131">-PrivateIpAddress</span></span>
<span data-ttu-id="9c1e6-132">Especifica o endereço IP privado a ser associado a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1e6-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9c1e6-133">-PublicIpAddress</span></span>
<span data-ttu-id="9c1e6-134">Especifica o endereço IP público para associar a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1e6-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9c1e6-135">-PublicIpAddressId</span></span>
<span data-ttu-id="9c1e6-136">Especifica a ID do endereço IP público no qual adicionar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1e6-137">-Subnet</span><span class="sxs-lookup"><span data-stu-id="9c1e6-137">-Subnet</span></span>
<span data-ttu-id="9c1e6-138">Especifica o objeto de sub-rede no qual adicionar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1e6-139">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="9c1e6-139">-SubnetId</span></span>
<span data-ttu-id="9c1e6-140">Especifica a ID da sub-rede na qual adicionar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1e6-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="9c1e6-141">-Zone</span></span>
<span data-ttu-id="9c1e6-142">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c1e6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c1e6-143">CommonParameters</span></span>
<span data-ttu-id="9c1e6-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c1e6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c1e6-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c1e6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c1e6-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c1e6-146">INPUTS</span></span>

### <span data-ttu-id="9c1e6-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c1e6-147">PSLoadBalancer</span></span>
<span data-ttu-id="9c1e6-148">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9c1e6-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9c1e6-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c1e6-149">OUTPUTS</span></span>

### <span data-ttu-id="9c1e6-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c1e6-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9c1e6-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c1e6-151">NOTES</span></span>

## <span data-ttu-id="9c1e6-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c1e6-152">RELATED LINKS</span></span>

[<span data-ttu-id="9c1e6-153">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c1e6-153">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9c1e6-154">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c1e6-154">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9c1e6-155">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c1e6-155">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9c1e6-156">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c1e6-156">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9c1e6-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c1e6-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9c1e6-158">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c1e6-158">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


