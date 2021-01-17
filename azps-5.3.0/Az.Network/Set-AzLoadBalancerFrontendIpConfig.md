---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434630"
---
# <span data-ttu-id="a02c2-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a02c2-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="a02c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a02c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a02c2-103">Atualiza uma configuração de IP front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a02c2-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="a02c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a02c2-104">SYNTAX</span></span>

### <span data-ttu-id="a02c2-105">SetByResourceSubnet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a02c2-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a02c2-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="a02c2-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a02c2-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a02c2-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a02c2-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a02c2-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a02c2-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a02c2-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a02c2-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a02c2-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a02c2-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a02c2-111">DESCRIPTION</span></span>
<span data-ttu-id="a02c2-112">O cmdlet **set-AzLoadBalancerFrontendIpConfig** atualiza uma configuração de IP front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a02c2-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="a02c2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a02c2-113">EXAMPLES</span></span>

### <span data-ttu-id="a02c2-114">Exemplo 1: modificar a configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="a02c2-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="a02c2-115">O primeiro comando obtém a sub-rede virtual chamada sub-rede e, em seguida, armazena-a na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="a02c2-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="a02c2-116">O segundo comando obtém o balanceador de carga associado chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="a02c2-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="a02c2-117">O terceiro comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzLoadBalancerFrontendIpConfig, que cria uma configuração de IP front-end chamada NewFrontend para $slb.</span><span class="sxs-lookup"><span data-stu-id="a02c2-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="a02c2-118">O quarto comando passa o balanceador de carga em $slb para **set-AzLoadBalancerFrontendIpConfig**, que salva e atualiza a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="a02c2-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="a02c2-119">OS</span><span class="sxs-lookup"><span data-stu-id="a02c2-119">PARAMETERS</span></span>

### <span data-ttu-id="a02c2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02c2-120">-DefaultProfile</span></span>
<span data-ttu-id="a02c2-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a02c2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a02c2-122">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="a02c2-122">-LoadBalancer</span></span>
<span data-ttu-id="a02c2-123">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a02c2-123">Specifies a load balancer.</span></span>
<span data-ttu-id="a02c2-124">Esse cmdlet atualiza uma configuração de front-end para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a02c2-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a02c2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a02c2-125">-Name</span></span>
<span data-ttu-id="a02c2-126">Especifica o nome da configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="a02c2-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="a02c2-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a02c2-127">-PrivateIpAddress</span></span>
<span data-ttu-id="a02c2-128">Especifica o endereço IP privado do balanceador de carga associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="a02c2-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="a02c2-129">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="a02c2-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="a02c2-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a02c2-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="a02c2-131">A versão do endereço IP privado da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="a02c2-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="a02c2-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a02c2-132">-PublicIpAddress</span></span>
<span data-ttu-id="a02c2-133">Especifica o objeto **PublicIpAddress** que está associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="a02c2-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="a02c2-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a02c2-134">-PublicIpAddressId</span></span>
<span data-ttu-id="a02c2-135">Especifica a ID do objeto **PublicIpAddress** associado à configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="a02c2-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="a02c2-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a02c2-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="a02c2-137">Especifica o objeto **PublicIpAddressPrefix** para associar a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="a02c2-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02c2-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="a02c2-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="a02c2-139">Especifica a ID do objeto **PublicIpAddressPrefix** a ser associado a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="a02c2-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02c2-140">-Subnet</span><span class="sxs-lookup"><span data-stu-id="a02c2-140">-Subnet</span></span>
<span data-ttu-id="a02c2-141">Especifica o objeto de **sub-rede** que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="a02c2-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="a02c2-142">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="a02c2-142">-SubnetId</span></span>
<span data-ttu-id="a02c2-143">Especifica a ID da sub-rede que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="a02c2-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="a02c2-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="a02c2-144">-Zone</span></span>
<span data-ttu-id="a02c2-145">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="a02c2-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="a02c2-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a02c2-146">-Confirm</span></span>
<span data-ttu-id="a02c2-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a02c2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a02c2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a02c2-148">-WhatIf</span></span>
<span data-ttu-id="a02c2-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a02c2-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a02c2-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a02c2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a02c2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02c2-151">CommonParameters</span></span>
<span data-ttu-id="a02c2-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a02c2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02c2-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a02c2-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02c2-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a02c2-154">INPUTS</span></span>

### <span data-ttu-id="a02c2-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a02c2-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a02c2-156">System. String</span><span class="sxs-lookup"><span data-stu-id="a02c2-156">System.String</span></span>

### <span data-ttu-id="a02c2-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="a02c2-157">System.String[]</span></span>

### <span data-ttu-id="a02c2-158">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a02c2-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="a02c2-159">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a02c2-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="a02c2-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a02c2-160">OUTPUTS</span></span>

### <span data-ttu-id="a02c2-161">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a02c2-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a02c2-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a02c2-162">NOTES</span></span>

## <span data-ttu-id="a02c2-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a02c2-163">RELATED LINKS</span></span>

[<span data-ttu-id="a02c2-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a02c2-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a02c2-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a02c2-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a02c2-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a02c2-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a02c2-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a02c2-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="a02c2-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a02c2-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a02c2-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a02c2-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


