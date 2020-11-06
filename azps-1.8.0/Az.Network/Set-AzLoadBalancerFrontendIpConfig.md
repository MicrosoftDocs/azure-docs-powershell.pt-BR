---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: f1c6790ba733004a565087b261e0ca9b42f9688b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600009"
---
# <span data-ttu-id="1f77c-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f77c-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="1f77c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f77c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f77c-103">Atualiza uma configuração de IP front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1f77c-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="1f77c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f77c-104">SYNTAX</span></span>

### <span data-ttu-id="1f77c-105">SetByResourceSubnet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f77c-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f77c-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="1f77c-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f77c-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f77c-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f77c-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f77c-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f77c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f77c-109">DESCRIPTION</span></span>
<span data-ttu-id="1f77c-110">O cmdlet **set-AzLoadBalancerFrontendIpConfig** atualiza uma configuração de IP front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1f77c-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="1f77c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f77c-111">EXAMPLES</span></span>

### <span data-ttu-id="1f77c-112">Exemplo 1: modificar a configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="1f77c-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="1f77c-113">O primeiro comando obtém a sub-rede virtual chamada sub-rede e, em seguida, armazena-a na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="1f77c-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="1f77c-114">O segundo comando obtém o balanceador de carga associado chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="1f77c-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="1f77c-115">O terceiro comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzLoadBalancerFrontendIpConfig, que cria uma configuração de IP front-end chamada NewFrontend para $slb.</span><span class="sxs-lookup"><span data-stu-id="1f77c-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="1f77c-116">O quarto comando passa o balanceador de carga em $slb para **set-AzLoadBalancerFrontendIpConfig** , que salva e atualiza a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="1f77c-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="1f77c-117">OS</span><span class="sxs-lookup"><span data-stu-id="1f77c-117">PARAMETERS</span></span>

### <span data-ttu-id="1f77c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f77c-118">-DefaultProfile</span></span>
<span data-ttu-id="1f77c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f77c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f77c-120">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="1f77c-120">-LoadBalancer</span></span>
<span data-ttu-id="1f77c-121">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1f77c-121">Specifies a load balancer.</span></span>
<span data-ttu-id="1f77c-122">Esse cmdlet atualiza uma configuração de front-end para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1f77c-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f77c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f77c-123">-Name</span></span>
<span data-ttu-id="1f77c-124">Especifica o nome da configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="1f77c-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="1f77c-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f77c-125">-PrivateIpAddress</span></span>
<span data-ttu-id="1f77c-126">Especifica o endereço IP privado do balanceador de carga associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="1f77c-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="1f77c-127">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="1f77c-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="1f77c-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f77c-128">-PublicIpAddress</span></span>
<span data-ttu-id="1f77c-129">Especifica o objeto **PublicIpAddress** que está associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="1f77c-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="1f77c-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="1f77c-130">-PublicIpAddressId</span></span>
<span data-ttu-id="1f77c-131">Especifica a ID do objeto **PublicIpAddress** associado à configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="1f77c-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="1f77c-132">-Subnet</span><span class="sxs-lookup"><span data-stu-id="1f77c-132">-Subnet</span></span>
<span data-ttu-id="1f77c-133">Especifica o objeto de **sub-rede** que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="1f77c-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="1f77c-134">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="1f77c-134">-SubnetId</span></span>
<span data-ttu-id="1f77c-135">Especifica a ID da sub-rede que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="1f77c-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="1f77c-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="1f77c-136">-Zone</span></span>
<span data-ttu-id="1f77c-137">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="1f77c-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="1f77c-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f77c-138">-Confirm</span></span>
<span data-ttu-id="1f77c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f77c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f77c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f77c-140">-WhatIf</span></span>
<span data-ttu-id="1f77c-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f77c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f77c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f77c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f77c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f77c-143">CommonParameters</span></span>
<span data-ttu-id="1f77c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f77c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f77c-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f77c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f77c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f77c-146">INPUTS</span></span>

### <span data-ttu-id="1f77c-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f77c-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="1f77c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1f77c-148">System.String</span></span>

### <span data-ttu-id="1f77c-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="1f77c-149">System.String[]</span></span>

### <span data-ttu-id="1f77c-150">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="1f77c-150">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="1f77c-151">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1f77c-151">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="1f77c-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f77c-152">OUTPUTS</span></span>

### <span data-ttu-id="1f77c-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f77c-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1f77c-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f77c-154">NOTES</span></span>

## <span data-ttu-id="1f77c-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f77c-155">RELATED LINKS</span></span>

[<span data-ttu-id="1f77c-156">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f77c-156">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f77c-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f77c-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1f77c-158">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f77c-158">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f77c-159">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f77c-159">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="1f77c-160">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f77c-160">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1f77c-161">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1f77c-161">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


