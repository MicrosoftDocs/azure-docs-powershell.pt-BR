---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: a81f8b260b0631692bb24a571bcb86b8ecf038d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786290"
---
# <span data-ttu-id="241f3-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="241f3-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="241f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="241f3-102">SYNOPSIS</span></span>
<span data-ttu-id="241f3-103">Cria uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="241f3-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="241f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="241f3-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="241f3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="241f3-105">DESCRIPTION</span></span>
<span data-ttu-id="241f3-106">O cmdlet **New-AzureRmVirtualNetwork** cria uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="241f3-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="241f3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="241f3-107">EXAMPLES</span></span>

### <span data-ttu-id="241f3-108">1: criar uma rede virtual com duas sub-redes</span><span class="sxs-lookup"><span data-stu-id="241f3-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="241f3-109">Este exemplo cria uma rede virtual com duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="241f3-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="241f3-110">Primeiro, um novo grupo de recursos é criado na região centralus.</span><span class="sxs-lookup"><span data-stu-id="241f3-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="241f3-111">Em seguida, o exemplo cria representações de duas sub-redes na memória.</span><span class="sxs-lookup"><span data-stu-id="241f3-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="241f3-112">O cmdlet New-AzureRmVirtualNetworkSubnetConfig não criará nenhuma sub-rede no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="241f3-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="241f3-113">Há uma sub-rede chamada frontendSubnet e uma sub-rede chamada backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="241f3-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="241f3-114">Em seguida, o cmdlet New-AzureRmVirtualNetwork cria uma rede virtual usando o 10.0.0.0 10.0.0.0/16 como o prefixo de endereço e duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="241f3-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="241f3-115">2: criar uma rede virtual com configurações de DNS</span><span class="sxs-lookup"><span data-stu-id="241f3-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="241f3-116">Este exemplo cria uma rede virtual com duas sub-redes e dois servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="241f3-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="241f3-117">O efeito de especificar os servidores DNS na rede virtual é que as NICs/VMs implantadas nesta rede virtual herdem esses servidores DNS como padrões.</span><span class="sxs-lookup"><span data-stu-id="241f3-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="241f3-118">Esses padrões podem ser substituídos por NIC por meio de uma configuração no nível da NIC.</span><span class="sxs-lookup"><span data-stu-id="241f3-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="241f3-119">Se nenhum servidor DNS estiver especificado em uma VNET e nenhum servidor DNS nas NICs, os servidores DNS padrão do Azure serão usados para resolução de DNS.</span><span class="sxs-lookup"><span data-stu-id="241f3-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="241f3-120">3: criar uma rede virtual com uma sub-rede referenciando um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="241f3-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="241f3-121">Este exemplo cria uma rede virtual com sub-redes que fazem referência a um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="241f3-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="241f3-122">Primeiro, o exemplo cria um grupo de recursos como um contêiner para os recursos que serão criados.</span><span class="sxs-lookup"><span data-stu-id="241f3-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="241f3-123">Em seguida, um grupo de segurança de rede é criado para permitir o acesso ao RDP de entrada, mas, caso contrário, impõe as regras de grupo de segurança de rede padrão.</span><span class="sxs-lookup"><span data-stu-id="241f3-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="241f3-124">Em seguida, o cmdlet New-AzureRmVirtualNetworkSubnetConfig cria representações na memória de duas sub-redes que fazem referência ao grupo de segurança de rede que foi criado.</span><span class="sxs-lookup"><span data-stu-id="241f3-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="241f3-125">O comando New-AzureRmVirtualNetwork cria a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="241f3-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="241f3-126">OS</span><span class="sxs-lookup"><span data-stu-id="241f3-126">PARAMETERS</span></span>

### <span data-ttu-id="241f3-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="241f3-127">-AddressPrefix</span></span>
<span data-ttu-id="241f3-128">Especifica um intervalo de endereços IP para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="241f3-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="241f3-129">-AsJob</span></span>
<span data-ttu-id="241f3-130">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="241f3-130">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241f3-131">-DefaultProfile</span></span>
<span data-ttu-id="241f3-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="241f3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-133">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="241f3-133">-DnsServer</span></span>
<span data-ttu-id="241f3-134">Especifica o servidor DNS para uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="241f3-134">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="241f3-135">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="241f3-135">-EnableDDoSProtection</span></span>
<span data-ttu-id="241f3-136">Um parâmetro de opção que representa se a proteção contra DDoS está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="241f3-136">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-137">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="241f3-137">-EnableVmProtection</span></span>
<span data-ttu-id="241f3-138">Um parâmetro de opção que representa se a proteção da VM está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="241f3-138">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-139">-Force</span><span class="sxs-lookup"><span data-stu-id="241f3-139">-Force</span></span>
<span data-ttu-id="241f3-140">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="241f3-140">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-141">-Local</span><span class="sxs-lookup"><span data-stu-id="241f3-141">-Location</span></span>
<span data-ttu-id="241f3-142">Especifica a região da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="241f3-142">Specifies the region for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="241f3-143">-Name</span></span>
<span data-ttu-id="241f3-144">Especifica o nome da rede virtual que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="241f3-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241f3-145">-ResourceGroupName</span></span>
<span data-ttu-id="241f3-146">Especifica o nome de um grupo de recursos para conter a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="241f3-146">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-147">-Subnet</span><span class="sxs-lookup"><span data-stu-id="241f3-147">-Subnet</span></span>
<span data-ttu-id="241f3-148">Especifica uma lista de sub-redes a serem associadas à rede virtual.</span><span class="sxs-lookup"><span data-stu-id="241f3-148">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-149">-Marca</span><span class="sxs-lookup"><span data-stu-id="241f3-149">-Tag</span></span>
<span data-ttu-id="241f3-150">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="241f3-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="241f3-151">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="241f3-151">For example:</span></span>

<span data-ttu-id="241f3-152">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="241f3-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="241f3-153">-Confirm</span></span>
<span data-ttu-id="241f3-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="241f3-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241f3-155">-WhatIf</span></span>
<span data-ttu-id="241f3-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="241f3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="241f3-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="241f3-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241f3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241f3-158">CommonParameters</span></span>
<span data-ttu-id="241f3-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="241f3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241f3-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241f3-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241f3-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="241f3-161">INPUTS</span></span>

## <span data-ttu-id="241f3-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="241f3-162">OUTPUTS</span></span>

### <span data-ttu-id="241f3-163">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="241f3-163">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="241f3-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="241f3-164">NOTES</span></span>

## <span data-ttu-id="241f3-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="241f3-165">RELATED LINKS</span></span>

[<span data-ttu-id="241f3-166">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="241f3-166">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="241f3-167">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="241f3-167">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="241f3-168">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="241f3-168">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)
