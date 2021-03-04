---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 170ab2536eb03bc04867ad7a3c6828fff5c94749
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887875"
---
# <span data-ttu-id="58ea2-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="58ea2-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="58ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="58ea2-103">Cria uma configuração ip front-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="58ea2-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="58ea2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="58ea2-104">SYNTAX</span></span>

### <span data-ttu-id="58ea2-105">SetByResourceSubnet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="58ea2-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ea2-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="58ea2-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ea2-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="58ea2-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ea2-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="58ea2-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ea2-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="58ea2-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ea2-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="58ea2-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ea2-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="58ea2-111">DESCRIPTION</span></span>
<span data-ttu-id="58ea2-112">O cmdlet **New-AzLoadBalancerFrontendIpConfig** cria uma configuração de IP front-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="58ea2-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="58ea2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58ea2-113">EXAMPLES</span></span>

### <span data-ttu-id="58ea2-114">Exemplo 1: Criar uma configuração de IP front-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="58ea2-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="58ea2-115">O primeiro comando cria um endereço IP público dinâmico chamado MyPublicIP no grupo de recursos chamado MyResourceGroup e o armazena na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="58ea2-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="58ea2-116">O segundo comando cria uma configuração de IP front-end chamada FrontendIpConfig01 usando o endereço IP público em $publicip.</span><span class="sxs-lookup"><span data-stu-id="58ea2-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="58ea2-117">Exemplo 2: Criar uma configuração de IP front-end para um balanceador de carga usando prefixo ip</span><span class="sxs-lookup"><span data-stu-id="58ea2-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="58ea2-118">O primeiro comando cria um prefixo ip público chamado MyPublicIP de comprimento 28 no grupo de recursos chamado MyResourceGroup e o armazena na variável $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="58ea2-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="58ea2-119">O segundo comando cria uma configuração de IP front-end chamada FrontendIpConfig01 usando o prefixo IP público em $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="58ea2-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="58ea2-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="58ea2-120">PARAMETERS</span></span>

### <span data-ttu-id="58ea2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ea2-121">-DefaultProfile</span></span>
<span data-ttu-id="58ea2-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="58ea2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58ea2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="58ea2-123">-Name</span></span>
<span data-ttu-id="58ea2-124">Especifica a configuração de IP front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="58ea2-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="58ea2-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="58ea2-125">-PrivateIpAddress</span></span>
<span data-ttu-id="58ea2-126">Especifica o endereço IP privado do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="58ea2-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="58ea2-127">Especifique esse parâmetro somente se você também especificar o parâmetro *Subnet.*</span><span class="sxs-lookup"><span data-stu-id="58ea2-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="58ea2-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="58ea2-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="58ea2-129">A versão de endereço IP privado da configuração IP.</span><span class="sxs-lookup"><span data-stu-id="58ea2-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="58ea2-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="58ea2-130">-PublicIpAddress</span></span>
<span data-ttu-id="58ea2-131">Especifica o **objeto PublicIpAddress** a ser associado a uma configuração de IP front-end.</span><span class="sxs-lookup"><span data-stu-id="58ea2-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="58ea2-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="58ea2-132">-PublicIpAddressId</span></span>
<span data-ttu-id="58ea2-133">Especifica a ID do **objeto PublicIpAddress** a ser associado a uma configuração de IP front-end.</span><span class="sxs-lookup"><span data-stu-id="58ea2-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="58ea2-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="58ea2-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="58ea2-135">Especifica o **objeto PublicIpAddressPrefix a** ser associado a uma configuração ip front-end.</span><span class="sxs-lookup"><span data-stu-id="58ea2-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="58ea2-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="58ea2-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="58ea2-137">Especifica a ID do **objeto PublicIpAddressPrefix a** ser associado a uma configuração de IP front-end.</span><span class="sxs-lookup"><span data-stu-id="58ea2-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="58ea2-138">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="58ea2-138">-Subnet</span></span>
<span data-ttu-id="58ea2-139">Especifica o **objeto Subnet** no qual criar uma configuração ip front-end.</span><span class="sxs-lookup"><span data-stu-id="58ea2-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="58ea2-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="58ea2-140">-SubnetId</span></span>
<span data-ttu-id="58ea2-141">Especifica a ID da sub-rede na qual criar uma configuração ip front-end.</span><span class="sxs-lookup"><span data-stu-id="58ea2-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="58ea2-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="58ea2-142">-Zone</span></span>
<span data-ttu-id="58ea2-143">Uma lista de zonas de disponibilidade que denotam o IP alocado para o recurso precisa vir.</span><span class="sxs-lookup"><span data-stu-id="58ea2-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="58ea2-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58ea2-144">-Confirm</span></span>
<span data-ttu-id="58ea2-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58ea2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ea2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ea2-146">-WhatIf</span></span>
<span data-ttu-id="58ea2-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58ea2-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58ea2-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58ea2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ea2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ea2-149">CommonParameters</span></span>
<span data-ttu-id="58ea2-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ea2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ea2-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58ea2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ea2-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58ea2-152">INPUTS</span></span>

### <span data-ttu-id="58ea2-153">System.String</span><span class="sxs-lookup"><span data-stu-id="58ea2-153">System.String</span></span>

### <span data-ttu-id="58ea2-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="58ea2-154">System.String[]</span></span>

### <span data-ttu-id="58ea2-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="58ea2-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="58ea2-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="58ea2-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="58ea2-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="58ea2-157">OUTPUTS</span></span>

### <span data-ttu-id="58ea2-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="58ea2-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="58ea2-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="58ea2-159">NOTES</span></span>

## <span data-ttu-id="58ea2-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58ea2-160">RELATED LINKS</span></span>

[<span data-ttu-id="58ea2-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="58ea2-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="58ea2-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="58ea2-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="58ea2-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="58ea2-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="58ea2-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="58ea2-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="58ea2-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="58ea2-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


