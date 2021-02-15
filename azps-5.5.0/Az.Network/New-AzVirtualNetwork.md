---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114676"
---
# <span data-ttu-id="7426b-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7426b-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="7426b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7426b-102">SYNOPSIS</span></span>
<span data-ttu-id="7426b-103">Cria uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7426b-103">Creates a virtual network.</span></span>

## <span data-ttu-id="7426b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7426b-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7426b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7426b-105">DESCRIPTION</span></span>
<span data-ttu-id="7426b-106">O **cmdlet New-AzVirtualNetwork** cria uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7426b-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="7426b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7426b-107">EXAMPLES</span></span>

### <span data-ttu-id="7426b-108">Exemplo 1: Criar uma rede virtual com duas sub-redes</span><span class="sxs-lookup"><span data-stu-id="7426b-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="7426b-109">Este exemplo cria uma rede virtual com duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="7426b-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="7426b-110">Primeiro, um novo grupo de recursos é criado na região central.</span><span class="sxs-lookup"><span data-stu-id="7426b-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="7426b-111">Em seguida, o exemplo cria representações na memória de duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="7426b-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="7426b-112">O New-AzVirtualNetworkSubnetConfig cmdlet não criará nenhuma sub-rede no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="7426b-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="7426b-113">Há uma sub-rede chamada frontendSubnet e uma sub-rede chamada backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="7426b-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="7426b-114">O cmdlet New-AzVirtualNetwork cria uma rede virtual usando a CIDR 10.0.0.0/16 como prefixo de endereço e duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="7426b-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="7426b-115">Exemplo 2: Criar uma rede virtual com configurações de DNS</span><span class="sxs-lookup"><span data-stu-id="7426b-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="7426b-116">Este exemplo cria uma rede virtual com duas sub-redes e dois servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="7426b-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="7426b-117">O efeito de especificar os servidores DNS na rede virtual é que os NICs/VMs implantados nessa rede virtual herdam esses servidores DNS como padrão.</span><span class="sxs-lookup"><span data-stu-id="7426b-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="7426b-118">Esses padrões podem ser substituídos por NIC por meio de uma configuração de nível NIC.</span><span class="sxs-lookup"><span data-stu-id="7426b-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="7426b-119">Se nenhum servidor DNS for especificado em uma VNET e nenhum servidor DNS nos NICs, os servidores DNS padrão do Azure serão usados para a resolução de DNS.</span><span class="sxs-lookup"><span data-stu-id="7426b-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="7426b-120">Exemplo 3: Criar uma rede virtual com uma sub-rede fazendo referência a um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="7426b-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="7426b-121">Este exemplo cria uma rede virtual com sub-redes que referenciam um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="7426b-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="7426b-122">Primeiro, o exemplo cria um grupo de recursos como um contêiner para os recursos que serão criados.</span><span class="sxs-lookup"><span data-stu-id="7426b-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="7426b-123">Em seguida, é criado um grupo de segurança de rede que permite acesso RDP de entrada, mas, de outra forma, impõe as regras padrão de grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="7426b-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="7426b-124">O New-AzVirtualNetworkSubnetConfig cmdlet cria representações na memória de duas sub-redes que referenciam o grupo de segurança de rede que foi criado.</span><span class="sxs-lookup"><span data-stu-id="7426b-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="7426b-125">O New-AzVirtualNetwork em seguida cria a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7426b-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="7426b-126">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7426b-126">PARAMETERS</span></span>

### <span data-ttu-id="7426b-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7426b-127">-AddressPrefix</span></span>
<span data-ttu-id="7426b-128">Especifica um intervalo de endereços IP para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7426b-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7426b-129">-AsJob</span></span>
<span data-ttu-id="7426b-130">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7426b-130">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="7426b-131">-BgpCommunity</span></span>
<span data-ttu-id="7426b-132">A Comunidade BGP anunciada pelo ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7426b-132">The BGP Community advertised over ExpressRoute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="7426b-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="7426b-134">Referência ao recurso de plano de proteção DDoS associado à rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7426b-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7426b-135">-DefaultProfile</span></span>
<span data-ttu-id="7426b-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7426b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7426b-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="7426b-137">-DnsServer</span></span>
<span data-ttu-id="7426b-138">Especifica o servidor DNS de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7426b-138">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="7426b-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="7426b-139">-EnableDdosProtection</span></span>
<span data-ttu-id="7426b-140">Um parâmetro de opção que representa se a proteção DDoS está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="7426b-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-141">-Forçar</span><span class="sxs-lookup"><span data-stu-id="7426b-141">-Force</span></span>
<span data-ttu-id="7426b-142">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7426b-142">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="7426b-143">-IpAllocation</span></span>
<span data-ttu-id="7426b-144">Especifica IpAllocations para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7426b-144">Specifies IpAllocations for a virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-145">-Local</span><span class="sxs-lookup"><span data-stu-id="7426b-145">-Location</span></span>
<span data-ttu-id="7426b-146">Especifica a região da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7426b-146">Specifies the region for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="7426b-147">-Name</span></span>
<span data-ttu-id="7426b-148">Especifica o nome da rede virtual que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="7426b-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7426b-149">-ResourceGroupName</span></span>
<span data-ttu-id="7426b-150">Especifica o nome de um grupo de recursos para conter a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7426b-150">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-151">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="7426b-151">-Subnet</span></span>
<span data-ttu-id="7426b-152">Especifica uma lista de sub-redes para associar à rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7426b-152">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="7426b-153">-Tag</span></span>
<span data-ttu-id="7426b-154">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="7426b-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7426b-155">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="7426b-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-156">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7426b-156">-Confirm</span></span>
<span data-ttu-id="7426b-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7426b-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7426b-158">-WhatIf</span></span>
<span data-ttu-id="7426b-159">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7426b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7426b-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7426b-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7426b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7426b-161">CommonParameters</span></span>
<span data-ttu-id="7426b-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7426b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7426b-163">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7426b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7426b-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="7426b-164">INPUTS</span></span>

### <span data-ttu-id="7426b-165">System.String</span><span class="sxs-lookup"><span data-stu-id="7426b-165">System.String</span></span>

### <span data-ttu-id="7426b-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7426b-166">System.String[]</span></span>

### <span data-ttu-id="7426b-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span><span class="sxs-lookup"><span data-stu-id="7426b-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="7426b-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7426b-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7426b-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="7426b-169">OUTPUTS</span></span>

### <span data-ttu-id="7426b-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7426b-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7426b-171">Notas</span><span class="sxs-lookup"><span data-stu-id="7426b-171">NOTES</span></span>

## <span data-ttu-id="7426b-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7426b-172">RELATED LINKS</span></span>

[<span data-ttu-id="7426b-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7426b-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7426b-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7426b-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="7426b-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7426b-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="7426b-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="7426b-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
