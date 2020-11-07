---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 62a479dd0c9c622100f5880c1aaf46836e179c53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940671"
---
# <span data-ttu-id="abb73-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="abb73-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="abb73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abb73-102">SYNOPSIS</span></span>
<span data-ttu-id="abb73-103">Atualiza uma configuração de IP front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="abb73-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="abb73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abb73-104">SYNTAX</span></span>

### <span data-ttu-id="abb73-105">SetByResourceSubnet (padrão)</span><span class="sxs-lookup"><span data-stu-id="abb73-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb73-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="abb73-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb73-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="abb73-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abb73-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="abb73-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abb73-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abb73-109">DESCRIPTION</span></span>
<span data-ttu-id="abb73-110">O cmdlet **set-AzLoadBalancerFrontendIpConfig** atualiza uma configuração de IP front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="abb73-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="abb73-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abb73-111">EXAMPLES</span></span>

### <span data-ttu-id="abb73-112">Exemplo 1: modificar a configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="abb73-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="abb73-113">O primeiro comando obtém a sub-rede virtual chamada sub-rede e, em seguida, armazena-a na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="abb73-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="abb73-114">O segundo comando obtém o balanceador de carga associado chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="abb73-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="abb73-115">O terceiro comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzLoadBalancerFrontendIpConfig, que cria uma configuração de IP front-end chamada NewFrontend para $slb.</span><span class="sxs-lookup"><span data-stu-id="abb73-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="abb73-116">O quarto comando passa o balanceador de carga em $slb para **set-AzLoadBalancerFrontendIpConfig** , que salva e atualiza a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="abb73-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="abb73-117">OS</span><span class="sxs-lookup"><span data-stu-id="abb73-117">PARAMETERS</span></span>

### <span data-ttu-id="abb73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb73-118">-DefaultProfile</span></span>
<span data-ttu-id="abb73-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abb73-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-120">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="abb73-120">-LoadBalancer</span></span>
<span data-ttu-id="abb73-121">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="abb73-121">Specifies a load balancer.</span></span>
<span data-ttu-id="abb73-122">Esse cmdlet atualiza uma configuração de front-end para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="abb73-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="abb73-123">-Name</span></span>
<span data-ttu-id="abb73-124">Especifica o nome da configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="abb73-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="abb73-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="abb73-125">-PrivateIpAddress</span></span>
<span data-ttu-id="abb73-126">Especifica o endereço IP privado do balanceador de carga associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="abb73-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="abb73-127">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="abb73-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="abb73-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="abb73-129">A versão do endereço IP privado da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="abb73-129">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="abb73-130">-PublicIpAddress</span></span>
<span data-ttu-id="abb73-131">Especifica o objeto **PublicIpAddress** que está associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="abb73-131">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="abb73-132">-PublicIpAddressId</span></span>
<span data-ttu-id="abb73-133">Especifica a ID do objeto **PublicIpAddress** associado à configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="abb73-133">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-134">-Subnet</span><span class="sxs-lookup"><span data-stu-id="abb73-134">-Subnet</span></span>
<span data-ttu-id="abb73-135">Especifica o objeto de **sub-rede** que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="abb73-135">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-136">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="abb73-136">-SubnetId</span></span>
<span data-ttu-id="abb73-137">Especifica a ID da sub-rede que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="abb73-137">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-138">-Zone</span><span class="sxs-lookup"><span data-stu-id="abb73-138">-Zone</span></span>
<span data-ttu-id="abb73-139">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="abb73-139">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="abb73-140">-Confirm</span></span>
<span data-ttu-id="abb73-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abb73-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb73-142">-WhatIf</span></span>
<span data-ttu-id="abb73-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abb73-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abb73-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abb73-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb73-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb73-145">CommonParameters</span></span>
<span data-ttu-id="abb73-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb73-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb73-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abb73-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb73-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abb73-148">INPUTS</span></span>

### <span data-ttu-id="abb73-149">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="abb73-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="abb73-150">System. String</span><span class="sxs-lookup"><span data-stu-id="abb73-150">System.String</span></span>

### <span data-ttu-id="abb73-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="abb73-151">System.String[]</span></span>

### <span data-ttu-id="abb73-152">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="abb73-152">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="abb73-153">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="abb73-153">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="abb73-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abb73-154">OUTPUTS</span></span>

### <span data-ttu-id="abb73-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="abb73-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="abb73-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abb73-156">NOTES</span></span>

## <span data-ttu-id="abb73-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abb73-157">RELATED LINKS</span></span>

[<span data-ttu-id="abb73-158">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="abb73-158">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="abb73-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="abb73-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="abb73-160">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="abb73-160">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="abb73-161">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="abb73-161">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="abb73-162">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="abb73-162">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="abb73-163">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="abb73-163">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


