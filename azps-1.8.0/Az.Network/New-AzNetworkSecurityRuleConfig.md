---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: e3afa3ee5809af2760225be674990827c117bdfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600303"
---
# <span data-ttu-id="34f4e-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34f4e-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="34f4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="34f4e-103">Cria uma configuração de regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="34f4e-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="34f4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34f4e-104">SYNTAX</span></span>

### <span data-ttu-id="34f4e-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="34f4e-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34f4e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="34f4e-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34f4e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34f4e-107">DESCRIPTION</span></span>
<span data-ttu-id="34f4e-108">O cmdlet **New-AzNetworkSecurityRuleConfig** cria uma configuração de regra de segurança de rede do Azure para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="34f4e-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="34f4e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34f4e-109">EXAMPLES</span></span>

### <span data-ttu-id="34f4e-110">1: criar uma regra de segurança de rede para permitir o RDP</span><span class="sxs-lookup"><span data-stu-id="34f4e-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="34f4e-111">Este comando cria uma regra de segurança que permite o acesso da Internet à porta 3389</span><span class="sxs-lookup"><span data-stu-id="34f4e-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="34f4e-112">2: criar uma regra de segurança de rede que permita HTTP</span><span class="sxs-lookup"><span data-stu-id="34f4e-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="34f4e-113">Este comando cria uma regra de segurança que permite o acesso da Internet à porta 80</span><span class="sxs-lookup"><span data-stu-id="34f4e-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="34f4e-114">OS</span><span class="sxs-lookup"><span data-stu-id="34f4e-114">PARAMETERS</span></span>

### <span data-ttu-id="34f4e-115">-Acesso</span><span class="sxs-lookup"><span data-stu-id="34f4e-115">-Access</span></span>
<span data-ttu-id="34f4e-116">Especifica se o tráfego de rede é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="34f4e-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="34f4e-117">Os valores aceitáveis para esse parâmetro são: allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="34f4e-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="34f4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f4e-118">-DefaultProfile</span></span>
<span data-ttu-id="34f4e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34f4e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34f4e-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="34f4e-120">-Description</span></span>
<span data-ttu-id="34f4e-121">Especifica uma descrição da configuração de regra de segurança de rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="34f4e-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="34f4e-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="34f4e-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="34f4e-123">Especifica um prefixo de endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="34f4e-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="34f4e-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="34f4e-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34f4e-125">Um endereço de roteamento entre domínios sem classe (CIDR)</span><span class="sxs-lookup"><span data-stu-id="34f4e-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="34f4e-126">Um intervalo de endereços IP de destino</span><span class="sxs-lookup"><span data-stu-id="34f4e-126">A destination IP address range</span></span> 
- <span data-ttu-id="34f4e-127">Um caractere curinga (\*) para corresponder a qualquer endereço IP você pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="34f4e-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="34f4e-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="34f4e-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="34f4e-129">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="34f4e-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="34f4e-130">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="34f4e-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="34f4e-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="34f4e-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="34f4e-132">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="34f4e-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="34f4e-133">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="34f4e-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="34f4e-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="34f4e-134">-DestinationPortRange</span></span>
<span data-ttu-id="34f4e-135">Especifica uma porta de destino ou um intervalo.</span><span class="sxs-lookup"><span data-stu-id="34f4e-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="34f4e-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="34f4e-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34f4e-137">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="34f4e-137">An integer</span></span>
- <span data-ttu-id="34f4e-138">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="34f4e-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="34f4e-139">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="34f4e-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="34f4e-140">-Direction</span><span class="sxs-lookup"><span data-stu-id="34f4e-140">-Direction</span></span>
<span data-ttu-id="34f4e-141">Especifica se uma regra é avaliada no tráfego de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="34f4e-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="34f4e-142">Os valores aceitáveis para esse parâmetro são: de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="34f4e-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="34f4e-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="34f4e-143">-Name</span></span>
<span data-ttu-id="34f4e-144">Especifica o nome da configuração de regra de segurança de rede que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="34f4e-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="34f4e-145">-Priority</span><span class="sxs-lookup"><span data-stu-id="34f4e-145">-Priority</span></span>
<span data-ttu-id="34f4e-146">Especifica a prioridade de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="34f4e-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="34f4e-147">Os valores aceitáveis para esse parâmetro são: um inteiro entre 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="34f4e-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="34f4e-148">O número de prioridade deve ser exclusivo para cada regra na coleção.</span><span class="sxs-lookup"><span data-stu-id="34f4e-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="34f4e-149">Quanto menor o número de prioridade, maior a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="34f4e-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="34f4e-150">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="34f4e-150">-Protocol</span></span>
<span data-ttu-id="34f4e-151">Especifica o protocolo de rede ao qual uma nova configuração de regra se aplica.</span><span class="sxs-lookup"><span data-stu-id="34f4e-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="34f4e-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="34f4e-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34f4e-153">Protocol</span><span class="sxs-lookup"><span data-stu-id="34f4e-153">Tcp</span></span>
- <span data-ttu-id="34f4e-154">Grama</span><span class="sxs-lookup"><span data-stu-id="34f4e-154">Udp</span></span>
- <span data-ttu-id="34f4e-155">caractere curinga (\*) para corresponder a ambos.</span><span class="sxs-lookup"><span data-stu-id="34f4e-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="34f4e-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="34f4e-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="34f4e-157">Especifica um prefixo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="34f4e-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="34f4e-158">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="34f4e-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34f4e-159">UM CIDR</span><span class="sxs-lookup"><span data-stu-id="34f4e-159">A CIDR</span></span>
- <span data-ttu-id="34f4e-160">Um intervalo de IP de origem</span><span class="sxs-lookup"><span data-stu-id="34f4e-160">A source IP range</span></span>
- <span data-ttu-id="34f4e-161">Um caractere curinga (\*) para corresponder a qualquer endereço IP.</span><span class="sxs-lookup"><span data-stu-id="34f4e-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="34f4e-162">Você também pode usar marcas como o VirtualNetwork, o AzureLoadBalancer e a Internet.</span><span class="sxs-lookup"><span data-stu-id="34f4e-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="34f4e-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="34f4e-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="34f4e-164">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="34f4e-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="34f4e-165">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="34f4e-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="34f4e-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="34f4e-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="34f4e-167">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="34f4e-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="34f4e-168">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="34f4e-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="34f4e-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="34f4e-169">-SourcePortRange</span></span>
<span data-ttu-id="34f4e-170">Especifica a porta de origem ou o intervalo.</span><span class="sxs-lookup"><span data-stu-id="34f4e-170">Specifies the source port or range.</span></span>
<span data-ttu-id="34f4e-171">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="34f4e-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34f4e-172">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="34f4e-172">An integer</span></span>
- <span data-ttu-id="34f4e-173">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="34f4e-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="34f4e-174">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="34f4e-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="34f4e-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f4e-175">CommonParameters</span></span>
<span data-ttu-id="34f4e-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f4e-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f4e-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f4e-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f4e-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34f4e-178">INPUTS</span></span>

### <span data-ttu-id="34f4e-179">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="34f4e-179">None</span></span>

## <span data-ttu-id="34f4e-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34f4e-180">OUTPUTS</span></span>

### <span data-ttu-id="34f4e-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="34f4e-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="34f4e-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34f4e-182">NOTES</span></span>

## <span data-ttu-id="34f4e-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34f4e-183">RELATED LINKS</span></span>

[<span data-ttu-id="34f4e-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34f4e-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="34f4e-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34f4e-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="34f4e-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34f4e-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="34f4e-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34f4e-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


