---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 68bcbcf0aa99ee4ee1a40c038e3eb5255deb690a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115210"
---
# <span data-ttu-id="30f06-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="30f06-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="30f06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30f06-102">SYNOPSIS</span></span>
<span data-ttu-id="30f06-103">Adiciona uma configuração IP front-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30f06-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="30f06-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30f06-104">SYNTAX</span></span>

### <span data-ttu-id="30f06-105">SetByResourceSubnet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="30f06-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30f06-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="30f06-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30f06-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="30f06-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30f06-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="30f06-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30f06-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="30f06-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30f06-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="30f06-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30f06-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="30f06-111">DESCRIPTION</span></span>
<span data-ttu-id="30f06-112">O cmdlet **Add-AzLoadBalancerFrontendIpConfig** adiciona uma configuração IP front-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="30f06-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="30f06-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30f06-113">EXAMPLES</span></span>

### <span data-ttu-id="30f06-114">Exemplo 1 Adicionar uma configuração IP front-end com um endereço IP dinâmico</span><span class="sxs-lookup"><span data-stu-id="30f06-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="30f06-115">O primeiro comando obtém a rede virtual do Azure chamada MyVnet e passa o resultado usando o pipeline para o cmdlet **Get-AzVirtualNetworkSubnetConfig** para obter a sub-rede chamada MySubnet.</span><span class="sxs-lookup"><span data-stu-id="30f06-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="30f06-116">Em seguida, o comando armazena o resultado na variável chamada $Subnet.</span><span class="sxs-lookup"><span data-stu-id="30f06-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="30f06-117">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzLoadBalancerFrontendIpConfig** que adiciona uma configuração IP front-end ao balanceador de carga com um endereço IP particular dinâmico da sub-rede armazenada na variável chamada $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="30f06-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="30f06-118">Exemplo 2 Adicionar uma configuração IP front-end com um endereço IP estático</span><span class="sxs-lookup"><span data-stu-id="30f06-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="30f06-119">O primeiro comando obtém a rede virtual do Azure chamada MyVnet e passa o resultado usando o pipeline para o cmdlet **Get-AzVirtualNetworkSubnetConfig** para obter a sub-rede chamada MySubnet.</span><span class="sxs-lookup"><span data-stu-id="30f06-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="30f06-120">Em seguida, o comando armazena o resultado na variável chamada $Subnet.</span><span class="sxs-lookup"><span data-stu-id="30f06-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="30f06-121">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzLoadBalancerFrontendIpConfig** que adiciona uma configuração IP front-end ao balanceador de carga com um endereço IP particular estático da sub-rede armazenada na variável chamada $Subnet.</span><span class="sxs-lookup"><span data-stu-id="30f06-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="30f06-122">Exemplo 3 Adicionar uma configuração IP front-end com um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="30f06-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="30f06-123">O primeiro comando obtém o endereço IP público do Azure chamado MyPub e armazena o resultado na variável chamada $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="30f06-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="30f06-124">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzLoadBalancerFrontendIpConfig** que adiciona uma configuração IP front-end ao balanceador de carga com endereço IP público armazenado na variável chamada $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="30f06-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="30f06-125">Exemplo 4 Adicionar uma configuração ip front-end com um prefixo IP público</span><span class="sxs-lookup"><span data-stu-id="30f06-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="30f06-126">O primeiro comando obtém o prefixo IP público do Azure chamado MyPubPrefix e armazena o resultado na variável chamada $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="30f06-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="30f06-127">O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzLoadBalancerFrontendIpConfig** que adiciona uma configuração IP front-end ao balanceador de carga com prefixo IP público armazenado na variável chamada $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="30f06-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="30f06-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30f06-128">PARAMETERS</span></span>

### <span data-ttu-id="30f06-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f06-129">-DefaultProfile</span></span>
<span data-ttu-id="30f06-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="30f06-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30f06-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30f06-131">-LoadBalancer</span></span>
<span data-ttu-id="30f06-132">Especifica um **objeto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="30f06-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="30f06-133">Esse cmdlet adiciona uma configuração IP front-end ao balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="30f06-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="30f06-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="30f06-134">-Name</span></span>
<span data-ttu-id="30f06-135">Especifica o nome da configuração IP front-end a ser adicionar.</span><span class="sxs-lookup"><span data-stu-id="30f06-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="30f06-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="30f06-136">-PrivateIpAddress</span></span>
<span data-ttu-id="30f06-137">Especifica o endereço IP particular para associar a uma configuração IP front-end.</span><span class="sxs-lookup"><span data-stu-id="30f06-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="30f06-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="30f06-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="30f06-139">A versão de endereço IP particular da configuração IP.</span><span class="sxs-lookup"><span data-stu-id="30f06-139">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="30f06-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="30f06-140">-PublicIpAddress</span></span>
<span data-ttu-id="30f06-141">Especifica o endereço IP público para associar a uma configuração IP front-end.</span><span class="sxs-lookup"><span data-stu-id="30f06-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="30f06-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="30f06-142">-PublicIpAddressId</span></span>
<span data-ttu-id="30f06-143">Especifica a ID do endereço IP público no qual se adiciona uma configuração IP front-end.</span><span class="sxs-lookup"><span data-stu-id="30f06-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="30f06-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="30f06-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="30f06-145">Especifica o objeto de prefixo de endereço ip público para associar a uma configuração IP front-end.</span><span class="sxs-lookup"><span data-stu-id="30f06-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="30f06-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="30f06-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="30f06-147">Especifica a ID do objeto de prefixo de endereço ip público para associar a uma configuração IP front-end.</span><span class="sxs-lookup"><span data-stu-id="30f06-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="30f06-148">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="30f06-148">-Subnet</span></span>
<span data-ttu-id="30f06-149">Especifica o objeto da sub-rede no qual adicionar uma configuração IP front-end.</span><span class="sxs-lookup"><span data-stu-id="30f06-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="30f06-150">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="30f06-150">-SubnetId</span></span>
<span data-ttu-id="30f06-151">Especifica a ID da sub-rede na qual se adiciona uma configuração IP front-end.</span><span class="sxs-lookup"><span data-stu-id="30f06-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="30f06-152">-Zona</span><span class="sxs-lookup"><span data-stu-id="30f06-152">-Zone</span></span>
<span data-ttu-id="30f06-153">Uma lista de zonas de disponibilidade que denotam o IP alocado para o recurso precisa vir.</span><span class="sxs-lookup"><span data-stu-id="30f06-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="30f06-154">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="30f06-154">-Confirm</span></span>
<span data-ttu-id="30f06-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f06-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f06-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f06-156">-WhatIf</span></span>
<span data-ttu-id="30f06-157">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="30f06-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30f06-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30f06-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f06-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f06-159">CommonParameters</span></span>
<span data-ttu-id="30f06-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f06-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f06-161">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30f06-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f06-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="30f06-162">INPUTS</span></span>

### <span data-ttu-id="30f06-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30f06-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="30f06-164">System.String</span><span class="sxs-lookup"><span data-stu-id="30f06-164">System.String</span></span>

### <span data-ttu-id="30f06-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="30f06-165">System.String[]</span></span>

### <span data-ttu-id="30f06-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="30f06-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="30f06-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="30f06-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="30f06-168">Saídas</span><span class="sxs-lookup"><span data-stu-id="30f06-168">OUTPUTS</span></span>

### <span data-ttu-id="30f06-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30f06-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="30f06-170">Notas</span><span class="sxs-lookup"><span data-stu-id="30f06-170">NOTES</span></span>

## <span data-ttu-id="30f06-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30f06-171">RELATED LINKS</span></span>

[<span data-ttu-id="30f06-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="30f06-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="30f06-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30f06-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="30f06-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="30f06-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="30f06-175">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="30f06-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="30f06-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="30f06-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="30f06-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="30f06-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


