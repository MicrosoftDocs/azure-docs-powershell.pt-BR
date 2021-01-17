---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434708"
---
# <span data-ttu-id="e0320-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e0320-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="e0320-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0320-102">SYNOPSIS</span></span>
<span data-ttu-id="e0320-103">Cria uma configuração de IP de front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e0320-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="e0320-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0320-104">SYNTAX</span></span>

### <span data-ttu-id="e0320-105">SetByResourceSubnet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0320-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0320-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="e0320-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0320-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0320-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0320-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0320-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0320-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e0320-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0320-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e0320-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0320-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0320-111">DESCRIPTION</span></span>
<span data-ttu-id="e0320-112">O cmdlet **New-AzLoadBalancerFrontendIpConfig** cria uma configuração de IP de front-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0320-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e0320-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0320-113">EXAMPLES</span></span>

### <span data-ttu-id="e0320-114">Exemplo 1: criar uma configuração de IP de front-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="e0320-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="e0320-115">O primeiro comando cria um endereço IP público dinâmico chamado MyPublicIP no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="e0320-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="e0320-116">O segundo comando cria uma configuração de IP de front-end chamada FrontendIpConfig01 usando o endereço IP público em $publicip.</span><span class="sxs-lookup"><span data-stu-id="e0320-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="e0320-117">Exemplo 2: criar uma configuração de IP de front-end para um balanceador de carga usando prefixo de IP</span><span class="sxs-lookup"><span data-stu-id="e0320-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="e0320-118">O primeiro comando cria um prefixo de IP público chamado MyPublicIP de tamanho 28 no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="e0320-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="e0320-119">O segundo comando cria uma configuração de IP de front-end chamada FrontendIpConfig01 usando o prefixo de IP público em $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="e0320-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="e0320-120">OS</span><span class="sxs-lookup"><span data-stu-id="e0320-120">PARAMETERS</span></span>

### <span data-ttu-id="e0320-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0320-121">-DefaultProfile</span></span>
<span data-ttu-id="e0320-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0320-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0320-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0320-123">-Name</span></span>
<span data-ttu-id="e0320-124">Especifica a configuração de IP de front-end que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="e0320-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e0320-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0320-125">-PrivateIpAddress</span></span>
<span data-ttu-id="e0320-126">Especifica o endereço IP privado do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e0320-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="e0320-127">Especifique esse parâmetro somente se você também especificar o parâmetro de *sub-rede* .</span><span class="sxs-lookup"><span data-stu-id="e0320-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="e0320-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e0320-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="e0320-129">A versão do endereço IP privado da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="e0320-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="e0320-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0320-130">-PublicIpAddress</span></span>
<span data-ttu-id="e0320-131">Especifica o objeto **PublicIpAddress** para associar a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="e0320-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="e0320-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="e0320-132">-PublicIpAddressId</span></span>
<span data-ttu-id="e0320-133">Especifica a ID do objeto **PublicIpAddress** a ser associado a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="e0320-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="e0320-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e0320-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="e0320-135">Especifica o objeto **PublicIpAddressPrefix** para associar a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="e0320-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="e0320-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="e0320-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="e0320-137">Especifica a ID do objeto **PublicIpAddressPrefix** a ser associado a uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="e0320-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="e0320-138">-Subnet</span><span class="sxs-lookup"><span data-stu-id="e0320-138">-Subnet</span></span>
<span data-ttu-id="e0320-139">Especifica o objeto de **sub-rede** no qual criar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="e0320-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="e0320-140">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="e0320-140">-SubnetId</span></span>
<span data-ttu-id="e0320-141">Especifica a ID da sub-rede na qual criar uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="e0320-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="e0320-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="e0320-142">-Zone</span></span>
<span data-ttu-id="e0320-143">Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.</span><span class="sxs-lookup"><span data-stu-id="e0320-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="e0320-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0320-144">-Confirm</span></span>
<span data-ttu-id="e0320-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0320-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0320-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0320-146">-WhatIf</span></span>
<span data-ttu-id="e0320-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0320-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0320-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0320-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0320-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0320-149">CommonParameters</span></span>
<span data-ttu-id="e0320-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0320-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0320-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0320-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0320-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0320-152">INPUTS</span></span>

### <span data-ttu-id="e0320-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e0320-153">System.String</span></span>

### <span data-ttu-id="e0320-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="e0320-154">System.String[]</span></span>

### <span data-ttu-id="e0320-155">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e0320-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="e0320-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0320-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="e0320-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0320-157">OUTPUTS</span></span>

### <span data-ttu-id="e0320-158">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0320-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="e0320-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0320-159">NOTES</span></span>

## <span data-ttu-id="e0320-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0320-160">RELATED LINKS</span></span>

[<span data-ttu-id="e0320-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e0320-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e0320-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e0320-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e0320-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0320-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="e0320-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e0320-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e0320-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e0320-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


