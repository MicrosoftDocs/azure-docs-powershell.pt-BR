---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: d071e6f20d91dacfd99ca9566c64c4734ae93e31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429244"
---
# <span data-ttu-id="53263-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="53263-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="53263-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53263-102">SYNOPSIS</span></span>
<span data-ttu-id="53263-103">Define o estado da meta para uma configuração de IP de front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53263-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53263-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53263-104">SYNTAX</span></span>

### <span data-ttu-id="53263-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="53263-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53263-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="53263-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53263-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53263-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53263-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53263-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53263-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53263-109">DESCRIPTION</span></span>
<span data-ttu-id="53263-110">O cmdlet **set-AzureRmLoadBalancerFrontendIpConfig** define o estado da meta para uma configuração de IP de front-end em um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="53263-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="53263-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53263-111">EXAMPLES</span></span>

### <span data-ttu-id="53263-112">Exemplo 1: modificar a configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="53263-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="53263-113">O primeiro comando obtém a sub-rede virtual chamada sub-rede e, em seguida, armazena-a na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="53263-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="53263-114">O segundo comando obtém o balanceador de carga associado chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="53263-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="53263-115">O terceiro comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzureRmLoadBalancerFrontendIpConfig, que cria uma configuração de IP front-end chamada NewFrontend para $slb.</span><span class="sxs-lookup"><span data-stu-id="53263-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="53263-116">O quarto comando passa o balanceador de carga em $slb para **set-AzureRmLoadBalancerFrontendIpConfig** , que salva e atualiza a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="53263-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="53263-117">OS</span><span class="sxs-lookup"><span data-stu-id="53263-117">PARAMETERS</span></span>

### <span data-ttu-id="53263-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53263-118">-DefaultProfile</span></span>
<span data-ttu-id="53263-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53263-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53263-120">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="53263-120">-LoadBalancer</span></span>
<span data-ttu-id="53263-121">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53263-121">Specifies a load balancer.</span></span>
<span data-ttu-id="53263-122">Esse cmdlet define o estado da meta para uma configuração de front-end para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="53263-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53263-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="53263-123">-Name</span></span>
<span data-ttu-id="53263-124">Especifica o nome da configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="53263-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="53263-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="53263-125">-PrivateIpAddress</span></span>
<span data-ttu-id="53263-126">Especifica o endereço IP privado do balanceador de carga associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="53263-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="53263-127">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="53263-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53263-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="53263-128">-PublicIpAddress</span></span>
<span data-ttu-id="53263-129">Especifica o objeto **PublicIpAddress** que está associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="53263-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53263-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="53263-130">-PublicIpAddressId</span></span>
<span data-ttu-id="53263-131">Especifica a ID do objeto **PublicIpAddress** associado à configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="53263-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53263-132">-Subnet</span><span class="sxs-lookup"><span data-stu-id="53263-132">-Subnet</span></span>
<span data-ttu-id="53263-133">Especifica o objeto de **sub-rede** que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="53263-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53263-134">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="53263-134">-SubnetId</span></span>
<span data-ttu-id="53263-135">Especifica a ID da sub-rede que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="53263-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53263-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="53263-136">-Zone</span></span>
<span data-ttu-id="53263-137">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="53263-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="53263-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53263-138">CommonParameters</span></span>
<span data-ttu-id="53263-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53263-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53263-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53263-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53263-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53263-141">INPUTS</span></span>

### <span data-ttu-id="53263-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53263-142">PSLoadBalancer</span></span>
<span data-ttu-id="53263-143">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="53263-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="53263-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53263-144">OUTPUTS</span></span>

### <span data-ttu-id="53263-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53263-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="53263-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53263-146">NOTES</span></span>

## <span data-ttu-id="53263-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53263-147">RELATED LINKS</span></span>

[<span data-ttu-id="53263-148">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="53263-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="53263-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53263-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="53263-150">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="53263-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="53263-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="53263-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="53263-152">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="53263-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="53263-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="53263-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


