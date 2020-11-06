---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: 7fccc6b16d44e9bd050d40a21a748dbd1d251a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441526"
---
# <span data-ttu-id="414e9-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="414e9-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="414e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="414e9-102">SYNOPSIS</span></span>
<span data-ttu-id="414e9-103">Cria uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="414e9-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="414e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="414e9-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="414e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="414e9-105">DESCRIPTION</span></span>
<span data-ttu-id="414e9-106">O cmdlet **New-AzureRmVirtualNetwork** cria uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="414e9-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="414e9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="414e9-107">EXAMPLES</span></span>

### <span data-ttu-id="414e9-108">1: criar uma rede virtual com duas sub-redes</span><span class="sxs-lookup"><span data-stu-id="414e9-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="414e9-109">Este exemplo cria uma rede virtual com duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="414e9-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="414e9-110">Primeiro, um novo grupo de recursos é criado na região centralus.</span><span class="sxs-lookup"><span data-stu-id="414e9-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="414e9-111">Em seguida, o exemplo cria representações de duas sub-redes na memória.</span><span class="sxs-lookup"><span data-stu-id="414e9-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="414e9-112">O cmdlet New-AzureRmVirtualNetworkSubnetConfig não criará nenhuma sub-rede no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="414e9-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="414e9-113">Há uma sub-rede chamada frontendSubnet e uma sub-rede chamada backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="414e9-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="414e9-114">Em seguida, o cmdlet New-AzureRmVirtualNetwork cria uma rede virtual usando o 10.0.0.0 10.0.0.0/16 como o prefixo de endereço e duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="414e9-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="414e9-115">2: criar uma rede virtual com configurações de DNS</span><span class="sxs-lookup"><span data-stu-id="414e9-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="414e9-116">Este exemplo cria uma rede virtual com duas sub-redes e dois servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="414e9-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="414e9-117">O efeito de especificar os servidores DNS na rede virtual é que as NICs/VMs implantadas nesta rede virtual herdem esses servidores DNS como padrões.</span><span class="sxs-lookup"><span data-stu-id="414e9-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="414e9-118">Esses padrões podem ser substituídos por NIC por meio de uma configuração no nível da NIC.</span><span class="sxs-lookup"><span data-stu-id="414e9-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="414e9-119">Se nenhum servidor DNS estiver especificado em uma VNET e nenhum servidor DNS nas NICs, os servidores DNS padrão do Azure serão usados para resolução de DNS.</span><span class="sxs-lookup"><span data-stu-id="414e9-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="414e9-120">3: criar uma rede virtual com uma sub-rede referenciando um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="414e9-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="414e9-121">Este exemplo cria uma rede virtual com sub-redes que fazem referência a um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="414e9-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="414e9-122">Primeiro, o exemplo cria um grupo de recursos como um contêiner para os recursos que serão criados.</span><span class="sxs-lookup"><span data-stu-id="414e9-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="414e9-123">Em seguida, um grupo de segurança de rede é criado para permitir o acesso ao RDP de entrada, mas, caso contrário, impõe as regras de grupo de segurança de rede padrão.</span><span class="sxs-lookup"><span data-stu-id="414e9-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="414e9-124">Em seguida, o cmdlet New-AzureRmVirtualNetworkSubnetConfig cria representações na memória de duas sub-redes que fazem referência ao grupo de segurança de rede que foi criado.</span><span class="sxs-lookup"><span data-stu-id="414e9-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="414e9-125">O comando New-AzureRmVirtualNetwork cria a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="414e9-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="414e9-126">OS</span><span class="sxs-lookup"><span data-stu-id="414e9-126">PARAMETERS</span></span>

### <span data-ttu-id="414e9-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="414e9-127">-AddressPrefix</span></span>
<span data-ttu-id="414e9-128">Especifica um intervalo de endereços IP para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="414e9-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="414e9-129">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="414e9-129">-DnsServer</span></span>
<span data-ttu-id="414e9-130">Especifica o servidor DNS para uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="414e9-130">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="414e9-131">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="414e9-131">-EnableVmProtection</span></span>
<span data-ttu-id="414e9-132">Um parâmetro de opção que representa se a proteção da VM está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="414e9-132">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414e9-133">-Force</span><span class="sxs-lookup"><span data-stu-id="414e9-133">-Force</span></span>
<span data-ttu-id="414e9-134">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="414e9-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="414e9-135">-Local</span><span class="sxs-lookup"><span data-stu-id="414e9-135">-Location</span></span>
<span data-ttu-id="414e9-136">Especifica a região da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="414e9-136">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="414e9-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="414e9-137">-Name</span></span>
<span data-ttu-id="414e9-138">Especifica o nome da rede virtual que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="414e9-138">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="414e9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="414e9-139">-ResourceGroupName</span></span>
<span data-ttu-id="414e9-140">Especifica o nome de um grupo de recursos para conter a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="414e9-140">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="414e9-141">-Subnet</span><span class="sxs-lookup"><span data-stu-id="414e9-141">-Subnet</span></span>
<span data-ttu-id="414e9-142">Especifica uma lista de sub-redes a serem associadas à rede virtual.</span><span class="sxs-lookup"><span data-stu-id="414e9-142">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="414e9-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="414e9-143">-Tag</span></span>
<span data-ttu-id="414e9-144">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="414e9-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="414e9-145">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="414e9-145">For example:</span></span>

<span data-ttu-id="414e9-146">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="414e9-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="414e9-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="414e9-147">-Confirm</span></span>
<span data-ttu-id="414e9-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="414e9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414e9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414e9-149">-WhatIf</span></span>
<span data-ttu-id="414e9-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="414e9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="414e9-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="414e9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="414e9-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414e9-152">-DefaultProfile</span></span>
<span data-ttu-id="414e9-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="414e9-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="414e9-154">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="414e9-154">-EnableDDoSProtection</span></span>
<span data-ttu-id="414e9-155">Um parâmetro de opção que representa se a proteção contra DDoS está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="414e9-155">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414e9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414e9-156">CommonParameters</span></span>
<span data-ttu-id="414e9-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="414e9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414e9-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="414e9-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414e9-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="414e9-159">INPUTS</span></span>

## <span data-ttu-id="414e9-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="414e9-160">OUTPUTS</span></span>

### <span data-ttu-id="414e9-161">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="414e9-161">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="414e9-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="414e9-162">NOTES</span></span>

## <span data-ttu-id="414e9-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="414e9-163">RELATED LINKS</span></span>

[<span data-ttu-id="414e9-164">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="414e9-164">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="414e9-165">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="414e9-165">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="414e9-166">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="414e9-166">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)