---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 9692f44ce5d0a819d0176e0b295571ca260a2a71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776542"
---
# <span data-ttu-id="4c7fa-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c7fa-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4c7fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7fa-103">Define o estado da meta para uma configuração de IP de front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="4c7fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c7fa-104">SYNTAX</span></span>

### <span data-ttu-id="4c7fa-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="4c7fa-105">SetByResourceSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c7fa-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="4c7fa-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c7fa-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4c7fa-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c7fa-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4c7fa-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c7fa-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c7fa-109">DESCRIPTION</span></span>
<span data-ttu-id="4c7fa-110">O cmdlet **set-AzLoadBalancerFrontendIpConfig** define o estado da meta para uma configuração de IP de front-end em um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="4c7fa-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c7fa-111">EXAMPLES</span></span>

### <span data-ttu-id="4c7fa-112">Exemplo 1: modificar a configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="4c7fa-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="4c7fa-113">O primeiro comando obtém a sub-rede virtual chamada sub-rede e, em seguida, armazena-a na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="4c7fa-114">O segundo comando obtém o balanceador de carga associado chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="4c7fa-115">O terceiro comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzLoadBalancerFrontendIpConfig, que cria uma configuração de IP front-end chamada NewFrontend para $slb.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="4c7fa-116">O quarto comando passa o balanceador de carga em $slb para **set-AzLoadBalancerFrontendIpConfig** , que salva e atualiza a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="4c7fa-117">OS</span><span class="sxs-lookup"><span data-stu-id="4c7fa-117">PARAMETERS</span></span>

### <span data-ttu-id="4c7fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7fa-118">-DefaultProfile</span></span>
<span data-ttu-id="4c7fa-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c7fa-120">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="4c7fa-120">-LoadBalancer</span></span>
<span data-ttu-id="4c7fa-121">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-121">Specifies a load balancer.</span></span>
<span data-ttu-id="4c7fa-122">Esse cmdlet define o estado da meta para uma configuração de front-end para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c7fa-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c7fa-123">-Name</span></span>
<span data-ttu-id="4c7fa-124">Especifica o nome da configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="4c7fa-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4c7fa-125">-PrivateIpAddress</span></span>
<span data-ttu-id="4c7fa-126">Especifica o endereço IP privado do balanceador de carga associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="4c7fa-127">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="4c7fa-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="4c7fa-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4c7fa-128">-PublicIpAddress</span></span>
<span data-ttu-id="4c7fa-129">Especifica o objeto **PublicIpAddress** que está associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="4c7fa-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4c7fa-130">-PublicIpAddressId</span></span>
<span data-ttu-id="4c7fa-131">Especifica a ID do objeto **PublicIpAddress** associado à configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4c7fa-132">-Subnet</span><span class="sxs-lookup"><span data-stu-id="4c7fa-132">-Subnet</span></span>
<span data-ttu-id="4c7fa-133">Especifica o objeto de **sub-rede** que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4c7fa-134">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="4c7fa-134">-SubnetId</span></span>
<span data-ttu-id="4c7fa-135">Especifica a ID da sub-rede que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4c7fa-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="4c7fa-136">-Zone</span></span>
<span data-ttu-id="4c7fa-137">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="4c7fa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7fa-138">CommonParameters</span></span>
<span data-ttu-id="4c7fa-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c7fa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7fa-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c7fa-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7fa-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c7fa-141">INPUTS</span></span>

### <span data-ttu-id="4c7fa-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c7fa-142">PSLoadBalancer</span></span>
<span data-ttu-id="4c7fa-143">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4c7fa-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4c7fa-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c7fa-144">OUTPUTS</span></span>

### <span data-ttu-id="4c7fa-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c7fa-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4c7fa-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c7fa-146">NOTES</span></span>

## <span data-ttu-id="4c7fa-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c7fa-147">RELATED LINKS</span></span>

[<span data-ttu-id="4c7fa-148">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c7fa-148">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4c7fa-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c7fa-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4c7fa-150">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c7fa-150">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4c7fa-151">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4c7fa-151">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4c7fa-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c7fa-152">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4c7fa-153">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c7fa-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

