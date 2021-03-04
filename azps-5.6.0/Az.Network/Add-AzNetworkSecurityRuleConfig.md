---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 11481d2063b6acb2938361726de45f72dba539c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886439"
---
# <span data-ttu-id="afa81-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="afa81-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="afa81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afa81-102">SYNOPSIS</span></span>
<span data-ttu-id="afa81-103">Adiciona uma configuração de regra de segurança de rede a um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="afa81-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="afa81-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="afa81-104">SYNTAX</span></span>

### <span data-ttu-id="afa81-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="afa81-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afa81-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="afa81-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afa81-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="afa81-107">DESCRIPTION</span></span>
<span data-ttu-id="afa81-108">O cmdlet **Add-AzNetworkSecurityRuleConfig** adiciona uma configuração de regra de segurança de rede a um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="afa81-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="afa81-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afa81-109">EXAMPLES</span></span>

### <span data-ttu-id="afa81-110">1: Adicionando um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="afa81-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="afa81-111">O primeiro comando recupera um grupo de segurança de rede do Azure chamado "nsg1" do grupo de recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="afa81-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="afa81-112">O segundo comando adiciona uma regra de segurança de rede chamada "rdp-rule" que permite o tráfego da Internet na porta 3389 ao objeto do grupo de segurança de rede recuperado.</span><span class="sxs-lookup"><span data-stu-id="afa81-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="afa81-113">Persiste o grupo de segurança de rede modificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="afa81-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="afa81-114">2: Adicionar uma nova regra de segurança com grupos de segurança de aplicativos</span><span class="sxs-lookup"><span data-stu-id="afa81-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="afa81-115">Primeiro, criamos dois novos grupos de segurança de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="afa81-115">First, we create two new application security groups.</span></span> <span data-ttu-id="afa81-116">Em seguida, recuperamos um grupo de segurança de rede do Azure chamado "nsg1" do grupo de recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="afa81-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="afa81-117">e adicione uma regra de segurança de rede chamada "rdp-rule" a ela.</span><span class="sxs-lookup"><span data-stu-id="afa81-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="afa81-118">A regra permite o tráfego de todas as configurações IP no grupo de segurança do aplicativo "srcAsg" para todas as configurações de IP em "destAsg" na porta 3389.</span><span class="sxs-lookup"><span data-stu-id="afa81-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="afa81-119">Depois de adicionar a regra, persistimos o grupo de segurança de rede modificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="afa81-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="afa81-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="afa81-120">PARAMETERS</span></span>

### <span data-ttu-id="afa81-121">-Access</span><span class="sxs-lookup"><span data-stu-id="afa81-121">-Access</span></span>
<span data-ttu-id="afa81-122">Especifica se o tráfego de rede é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="afa81-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="afa81-123">Os valores aceitáveis para este parâmetro são: Permitir e Negar.</span><span class="sxs-lookup"><span data-stu-id="afa81-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa81-124">-DefaultProfile</span></span>
<span data-ttu-id="afa81-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="afa81-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afa81-126">-Description</span><span class="sxs-lookup"><span data-stu-id="afa81-126">-Description</span></span>
<span data-ttu-id="afa81-127">Especifica uma descrição de uma configuração de regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="afa81-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="afa81-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="afa81-129">Especifica um prefixo de endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="afa81-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="afa81-130">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="afa81-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afa81-131">Um Roteamento entre Domínios sem Classificação (CIDR)</span><span class="sxs-lookup"><span data-stu-id="afa81-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="afa81-132">Um intervalo de endereços IP de destino</span><span class="sxs-lookup"><span data-stu-id="afa81-132">A destination IP address range</span></span>
- <span data-ttu-id="afa81-133">Um caractere curinga (\*) para corresponder a qualquer endereço IP Você pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="afa81-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="afa81-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="afa81-135">O grupo de segurança do aplicativo definido como destino da regra.</span><span class="sxs-lookup"><span data-stu-id="afa81-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="afa81-136">Ele não pode ser usado com o parâmetro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="afa81-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="afa81-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="afa81-138">O grupo de segurança do aplicativo definido como destino da regra.</span><span class="sxs-lookup"><span data-stu-id="afa81-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="afa81-139">Ele não pode ser usado com o parâmetro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="afa81-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="afa81-140">-DestinationPortRange</span></span>
<span data-ttu-id="afa81-141">Especifica uma porta de destino ou intervalo.</span><span class="sxs-lookup"><span data-stu-id="afa81-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="afa81-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="afa81-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afa81-143">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="afa81-143">An integer</span></span>
- <span data-ttu-id="afa81-144">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="afa81-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="afa81-145">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="afa81-145">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-146">-Direction</span><span class="sxs-lookup"><span data-stu-id="afa81-146">-Direction</span></span>
<span data-ttu-id="afa81-147">Especifica se uma regra é avaliada no tráfego de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="afa81-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="afa81-148">Os valores aceitáveis para este parâmetro são: Entrada e Saída.</span><span class="sxs-lookup"><span data-stu-id="afa81-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-149">-Name</span><span class="sxs-lookup"><span data-stu-id="afa81-149">-Name</span></span>
<span data-ttu-id="afa81-150">Especifica o nome de uma configuração de regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="afa81-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="afa81-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="afa81-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="afa81-152">Especifica um **objeto NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="afa81-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="afa81-153">Este cmdlet adiciona uma configuração de regra de segurança de rede ao objeto especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="afa81-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="afa81-154">-Priority</span></span>
<span data-ttu-id="afa81-155">Especifica a prioridade de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="afa81-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="afa81-156">Os valores aceitáveis para este parâmetro são: um inteiro entre 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="afa81-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="afa81-157">O número de prioridade deve ser exclusivo para cada regra na coleção.</span><span class="sxs-lookup"><span data-stu-id="afa81-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="afa81-158">Quanto menor for o número de prioridade, maior será a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="afa81-158">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-159">-Protocol</span><span class="sxs-lookup"><span data-stu-id="afa81-159">-Protocol</span></span>
<span data-ttu-id="afa81-160">Especifica o protocolo de rede ao que uma configuração de regra se aplica.</span><span class="sxs-lookup"><span data-stu-id="afa81-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="afa81-161">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="afa81-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afa81-162">Tcp</span><span class="sxs-lookup"><span data-stu-id="afa81-162">Tcp</span></span>
- <span data-ttu-id="afa81-163">Udp</span><span class="sxs-lookup"><span data-stu-id="afa81-163">Udp</span></span>
- <span data-ttu-id="afa81-164">Caractere curinga (\*) para corresponder a ambos</span><span class="sxs-lookup"><span data-stu-id="afa81-164">Wildcard character (\*) to match both</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="afa81-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="afa81-166">Especifica um prefixo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="afa81-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="afa81-167">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="afa81-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afa81-168">A CIDR</span><span class="sxs-lookup"><span data-stu-id="afa81-168">A CIDR</span></span>
- <span data-ttu-id="afa81-169">Um intervalo IP de origem</span><span class="sxs-lookup"><span data-stu-id="afa81-169">A source IP range</span></span>
- <span data-ttu-id="afa81-170">Um caractere curinga (\*) para corresponder a qualquer endereço IP.</span><span class="sxs-lookup"><span data-stu-id="afa81-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="afa81-171">Você também pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="afa81-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="afa81-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="afa81-173">O grupo de segurança do aplicativo definido como fonte da regra.</span><span class="sxs-lookup"><span data-stu-id="afa81-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="afa81-174">Ele não pode ser usado com o parâmetro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="afa81-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="afa81-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="afa81-176">O grupo de segurança do aplicativo definido como fonte da regra.</span><span class="sxs-lookup"><span data-stu-id="afa81-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="afa81-177">Ele não pode ser usado com o parâmetro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="afa81-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="afa81-178">-SourcePortRange</span></span>
<span data-ttu-id="afa81-179">Especifica uma porta de origem ou intervalo.</span><span class="sxs-lookup"><span data-stu-id="afa81-179">Specifies a source port or range.</span></span>
<span data-ttu-id="afa81-180">Esse valor é expresso como um inteiro, como um intervalo entre 0 e 65535 ou como um caractere curinga (\*) para corresponder a qualquer porta de origem.</span><span class="sxs-lookup"><span data-stu-id="afa81-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa81-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa81-181">CommonParameters</span></span>
<span data-ttu-id="afa81-182">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa81-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa81-183">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa81-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa81-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afa81-184">INPUTS</span></span>

### <span data-ttu-id="afa81-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="afa81-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="afa81-186">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="afa81-186">OUTPUTS</span></span>

### <span data-ttu-id="afa81-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="afa81-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="afa81-188">NOTES</span><span class="sxs-lookup"><span data-stu-id="afa81-188">NOTES</span></span>

## <span data-ttu-id="afa81-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afa81-189">RELATED LINKS</span></span>

[<span data-ttu-id="afa81-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="afa81-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="afa81-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="afa81-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="afa81-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="afa81-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="afa81-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="afa81-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


