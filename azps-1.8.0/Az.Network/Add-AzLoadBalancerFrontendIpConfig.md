---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2dba7d00ea308225736de6714c90c74b0ce30837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600711"
---
# <span data-ttu-id="c3025-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c3025-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="c3025-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3025-102">SYNOPSIS</span></span>
<span data-ttu-id="c3025-103">Adiciona uma configuração de IP front-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c3025-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="c3025-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3025-104">SYNTAX</span></span>

### <span data-ttu-id="c3025-105">SetByResourceSubnet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3025-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3025-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="c3025-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3025-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3025-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3025-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3025-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3025-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3025-109">DESCRIPTION</span></span>
<span data-ttu-id="c3025-110">O cmdlet **Add-AzLoadBalancerFrontendIpConifg** adiciona uma configuração de IP de front-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3025-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c3025-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3025-111">EXAMPLES</span></span>

### <span data-ttu-id="c3025-112">Exemplo 1 adicionar uma configuração de IP de front-end com um endereço IP dinâmico</span><span class="sxs-lookup"><span data-stu-id="c3025-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="c3025-113">O primeiro comando obtém a rede virtual do Azure chamada MyVnet e passa o resultado usando o pipeline para o cmdlet **Get-AzVirtualNetworkSubnetConfig** para obter a sub-rede chamada mysubnet.</span><span class="sxs-lookup"><span data-stu-id="c3025-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="c3025-114">Em seguida, o comando armazena o resultado na variável chamada $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c3025-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="c3025-115">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com um endereço IP privado dinâmico da sub-rede armazenada na variável chamada $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="c3025-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="c3025-116">Exemplo 2 adicionar uma configuração de IP de front-end com um endereço IP estático</span><span class="sxs-lookup"><span data-stu-id="c3025-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="c3025-117">O primeiro comando obtém a rede virtual do Azure chamada MyVnet e passa o resultado usando o pipeline para o cmdlet **Get-AzVirtualNetworkSubnetConfig** para obter a sub-rede chamada mysubnet.</span><span class="sxs-lookup"><span data-stu-id="c3025-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="c3025-118">Em seguida, o comando armazena o resultado na variável chamada $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c3025-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="c3025-119">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com um endereço IP privado estático da sub-rede armazenada na variável chamada $subnet.</span><span class="sxs-lookup"><span data-stu-id="c3025-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="c3025-120">Exemplo 3 adicionar uma configuração de IP de front-end com um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="c3025-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="c3025-121">O primeiro comando obtém o endereço IP público do Azure chamado MyPub e armazena o resultado na variável chamada $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="c3025-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="c3025-122">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com endereço IP público armazenado na variável chamada $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="c3025-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="c3025-123">OS</span><span class="sxs-lookup"><span data-stu-id="c3025-123">PARAMETERS</span></span>

### <span data-ttu-id="c3025-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3025-124">-DefaultProfile</span></span>
<span data-ttu-id="c3025-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3025-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3025-126">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="c3025-126">-LoadBalancer</span></span>
<span data-ttu-id="c3025-127">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="c3025-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="c3025-128">Esse cmdlet adiciona uma configuração de IP de front-end para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c3025-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c3025-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3025-129">-Name</span></span>
<span data-ttu-id="c3025-130">Especifica o nome da configuração de IP de front-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="c3025-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="c3025-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3025-131">-PrivateIpAddress</span></span>
<span data-ttu-id="c3025-132">Especifica o endereço IP privado a ser associado a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="c3025-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="c3025-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3025-133">-PublicIpAddress</span></span>
<span data-ttu-id="c3025-134">Especifica o endereço IP público para associar a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="c3025-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="c3025-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c3025-135">-PublicIpAddressId</span></span>
<span data-ttu-id="c3025-136">Especifica a ID do endereço IP público no qual adicionar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="c3025-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="c3025-137">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c3025-137">-Subnet</span></span>
<span data-ttu-id="c3025-138">Especifica o objeto de sub-rede no qual adicionar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="c3025-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="c3025-139">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="c3025-139">-SubnetId</span></span>
<span data-ttu-id="c3025-140">Especifica a ID da sub-rede na qual adicionar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="c3025-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="c3025-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="c3025-141">-Zone</span></span>
<span data-ttu-id="c3025-142">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="c3025-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="c3025-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3025-143">-Confirm</span></span>
<span data-ttu-id="c3025-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3025-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3025-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3025-145">-WhatIf</span></span>
<span data-ttu-id="c3025-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3025-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3025-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3025-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3025-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3025-148">CommonParameters</span></span>
<span data-ttu-id="c3025-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3025-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3025-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3025-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3025-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3025-151">INPUTS</span></span>

### <span data-ttu-id="c3025-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3025-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c3025-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c3025-153">System.String</span></span>

### <span data-ttu-id="c3025-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="c3025-154">System.String[]</span></span>

### <span data-ttu-id="c3025-155">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c3025-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="c3025-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3025-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="c3025-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3025-157">OUTPUTS</span></span>

### <span data-ttu-id="c3025-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3025-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c3025-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3025-159">NOTES</span></span>

## <span data-ttu-id="c3025-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3025-160">RELATED LINKS</span></span>

[<span data-ttu-id="c3025-161">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c3025-161">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c3025-162">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c3025-162">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="c3025-163">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c3025-163">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c3025-164">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c3025-164">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c3025-165">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c3025-165">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c3025-166">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c3025-166">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


