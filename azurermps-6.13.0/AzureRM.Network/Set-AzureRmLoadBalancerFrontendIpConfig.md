---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 93313b6a2d9623ed518d6e79fabcda8fea5cc7b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602594"
---
# <span data-ttu-id="92cd3-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="92cd3-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="92cd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="92cd3-103">Define o estado da meta para uma configuração de IP de front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="92cd3-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92cd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92cd3-104">SYNTAX</span></span>

### <span data-ttu-id="92cd3-105">SetByResourceSubnet (padrão)</span><span class="sxs-lookup"><span data-stu-id="92cd3-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92cd3-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="92cd3-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92cd3-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="92cd3-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92cd3-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="92cd3-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92cd3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92cd3-109">DESCRIPTION</span></span>
<span data-ttu-id="92cd3-110">O cmdlet **set-AzureRmLoadBalancerFrontendIpConfig** define o estado da meta para uma configuração de IP de front-end em um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="92cd3-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="92cd3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92cd3-111">EXAMPLES</span></span>

### <span data-ttu-id="92cd3-112">Exemplo 1: modificar a configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="92cd3-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="92cd3-113">O primeiro comando obtém a sub-rede virtual chamada sub-rede e, em seguida, armazena-a na variável $Subnet.</span><span class="sxs-lookup"><span data-stu-id="92cd3-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="92cd3-114">O segundo comando obtém o balanceador de carga associado chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="92cd3-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="92cd3-115">O terceiro comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzureRmLoadBalancerFrontendIpConfig, que cria uma configuração de IP front-end chamada NewFrontend para $slb.</span><span class="sxs-lookup"><span data-stu-id="92cd3-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="92cd3-116">O quarto comando passa o balanceador de carga em $slb para **set-AzureRmLoadBalancerFrontendIpConfig** , que salva e atualiza a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="92cd3-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="92cd3-117">OS</span><span class="sxs-lookup"><span data-stu-id="92cd3-117">PARAMETERS</span></span>

### <span data-ttu-id="92cd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92cd3-118">-DefaultProfile</span></span>
<span data-ttu-id="92cd3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92cd3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92cd3-120">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="92cd3-120">-LoadBalancer</span></span>
<span data-ttu-id="92cd3-121">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="92cd3-121">Specifies a load balancer.</span></span>
<span data-ttu-id="92cd3-122">Esse cmdlet define o estado da meta para uma configuração de front-end para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="92cd3-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="92cd3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="92cd3-123">-Name</span></span>
<span data-ttu-id="92cd3-124">Especifica o nome da configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="92cd3-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="92cd3-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="92cd3-125">-PrivateIpAddress</span></span>
<span data-ttu-id="92cd3-126">Especifica o endereço IP privado do balanceador de carga associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="92cd3-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="92cd3-127">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="92cd3-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="92cd3-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="92cd3-128">-PublicIpAddress</span></span>
<span data-ttu-id="92cd3-129">Especifica o objeto **PublicIpAddress** que está associado à configuração de IP de front-end a ser definida.</span><span class="sxs-lookup"><span data-stu-id="92cd3-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="92cd3-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="92cd3-130">-PublicIpAddressId</span></span>
<span data-ttu-id="92cd3-131">Especifica a ID do objeto **PublicIpAddress** associado à configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="92cd3-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="92cd3-132">-Subnet</span><span class="sxs-lookup"><span data-stu-id="92cd3-132">-Subnet</span></span>
<span data-ttu-id="92cd3-133">Especifica o objeto de **sub-rede** que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="92cd3-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="92cd3-134">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="92cd3-134">-SubnetId</span></span>
<span data-ttu-id="92cd3-135">Especifica a ID da sub-rede que contém a configuração de IP de front-end que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="92cd3-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="92cd3-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="92cd3-136">-Zone</span></span>
<span data-ttu-id="92cd3-137">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="92cd3-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="92cd3-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="92cd3-138">-Confirm</span></span>
<span data-ttu-id="92cd3-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92cd3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92cd3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92cd3-140">-WhatIf</span></span>
<span data-ttu-id="92cd3-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92cd3-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92cd3-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92cd3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92cd3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92cd3-143">CommonParameters</span></span>
<span data-ttu-id="92cd3-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92cd3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92cd3-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92cd3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92cd3-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92cd3-146">INPUTS</span></span>

### <span data-ttu-id="92cd3-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92cd3-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="92cd3-148">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92cd3-148">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="92cd3-149">System. Collections. Generic. List \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="92cd3-149">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="92cd3-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92cd3-150">OUTPUTS</span></span>

### <span data-ttu-id="92cd3-151">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92cd3-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="92cd3-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92cd3-152">NOTES</span></span>

## <span data-ttu-id="92cd3-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92cd3-153">RELATED LINKS</span></span>

[<span data-ttu-id="92cd3-154">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="92cd3-154">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="92cd3-155">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92cd3-155">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="92cd3-156">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="92cd3-156">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="92cd3-157">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="92cd3-157">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="92cd3-158">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="92cd3-158">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="92cd3-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="92cd3-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


