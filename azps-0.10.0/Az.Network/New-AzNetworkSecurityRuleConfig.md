---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 17e73f28595a0b99c8209634a6dee6838fa4599d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775377"
---
# <span data-ttu-id="e7805-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7805-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="e7805-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7805-102">SYNOPSIS</span></span>
<span data-ttu-id="e7805-103">Cria uma configuração de regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="e7805-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="e7805-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7805-104">SYNTAX</span></span>

### <span data-ttu-id="e7805-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7805-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7805-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7805-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7805-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7805-107">DESCRIPTION</span></span>
<span data-ttu-id="e7805-108">O cmdlet **New-AzNetworkSecurityRuleConfig** cria uma configuração de regra de segurança de rede do Azure para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="e7805-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="e7805-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7805-109">EXAMPLES</span></span>

### <span data-ttu-id="e7805-110">1: criar uma regra de segurança de rede para permitir o RDP</span><span class="sxs-lookup"><span data-stu-id="e7805-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="e7805-111">Este comando cria uma regra de segurança que permite o acesso da Internet à porta 3389</span><span class="sxs-lookup"><span data-stu-id="e7805-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="e7805-112">2: criar uma regra de segurança de rede que permita HTTP</span><span class="sxs-lookup"><span data-stu-id="e7805-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="e7805-113">Este comando cria uma regra de segurança que permite o acesso da Internet à porta 80</span><span class="sxs-lookup"><span data-stu-id="e7805-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="e7805-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7805-114">PARAMETERS</span></span>

### <span data-ttu-id="e7805-115">-Acesso</span><span class="sxs-lookup"><span data-stu-id="e7805-115">-Access</span></span>
<span data-ttu-id="e7805-116">Especifica se o tráfego de rede é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="e7805-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="e7805-117">Os valores aceitáveis para esse parâmetro são: allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="e7805-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7805-118">-DefaultProfile</span></span>
<span data-ttu-id="e7805-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7805-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7805-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e7805-120">-Description</span></span>
<span data-ttu-id="e7805-121">Especifica uma descrição da configuração de regra de segurança de rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="e7805-121">Specifies a description of the network security rule configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e7805-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="e7805-123">Especifica um prefixo de endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="e7805-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="e7805-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e7805-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7805-125">Um endereço de roteamento entre domínios sem classe (CIDR)</span><span class="sxs-lookup"><span data-stu-id="e7805-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="e7805-126">Um intervalo de endereços IP de destino</span><span class="sxs-lookup"><span data-stu-id="e7805-126">A destination IP address range</span></span> 
- <span data-ttu-id="e7805-127">Um caractere curinga (\*) para corresponder a qualquer endereço IP</span><span class="sxs-lookup"><span data-stu-id="e7805-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="e7805-128">Você pode usar marcas como o VirtualNetwork, o AzureLoadBalancer e a Internet.</span><span class="sxs-lookup"><span data-stu-id="e7805-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7805-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="e7805-130">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="e7805-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="e7805-131">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="e7805-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e7805-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="e7805-133">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="e7805-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="e7805-134">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="e7805-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="e7805-135">-DestinationPortRange</span></span>
<span data-ttu-id="e7805-136">Especifica uma porta de destino ou um intervalo.</span><span class="sxs-lookup"><span data-stu-id="e7805-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="e7805-137">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e7805-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7805-138">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="e7805-138">An integer</span></span>
- <span data-ttu-id="e7805-139">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="e7805-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="e7805-140">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="e7805-140">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-141">-Direction</span><span class="sxs-lookup"><span data-stu-id="e7805-141">-Direction</span></span>
<span data-ttu-id="e7805-142">Especifica se uma regra é avaliada no tráfego de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="e7805-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="e7805-143">Os valores aceitáveis para esse parâmetro são: de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="e7805-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7805-144">-Name</span></span>
<span data-ttu-id="e7805-145">Especifica o nome da configuração de regra de segurança de rede que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="e7805-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-146">-Priority</span><span class="sxs-lookup"><span data-stu-id="e7805-146">-Priority</span></span>
<span data-ttu-id="e7805-147">Especifica a prioridade de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="e7805-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="e7805-148">Os valores aceitáveis para esse parâmetro são: um inteiro entre 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="e7805-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="e7805-149">O número de prioridade deve ser exclusivo para cada regra na coleção.</span><span class="sxs-lookup"><span data-stu-id="e7805-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="e7805-150">Quanto menor o número de prioridade, maior a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="e7805-150">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-151">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="e7805-151">-Protocol</span></span>
<span data-ttu-id="e7805-152">Especifica o protocolo de rede ao qual uma nova configuração de regra se aplica.</span><span class="sxs-lookup"><span data-stu-id="e7805-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="e7805-153">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e7805-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7805-154">Protocol</span><span class="sxs-lookup"><span data-stu-id="e7805-154">Tcp</span></span>
- <span data-ttu-id="e7805-155">Grama</span><span class="sxs-lookup"><span data-stu-id="e7805-155">Udp</span></span>
- <span data-ttu-id="e7805-156">caractere curinga (\*) para corresponder a ambos.</span><span class="sxs-lookup"><span data-stu-id="e7805-156">wildcard character (\*) to match both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e7805-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="e7805-158">Especifica um prefixo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="e7805-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="e7805-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e7805-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7805-160">UM CIDR</span><span class="sxs-lookup"><span data-stu-id="e7805-160">A CIDR</span></span>
- <span data-ttu-id="e7805-161">Um intervalo de IP de origem</span><span class="sxs-lookup"><span data-stu-id="e7805-161">A source IP range</span></span>
- <span data-ttu-id="e7805-162">Um caractere curinga (\*) para corresponder a qualquer endereço IP.</span><span class="sxs-lookup"><span data-stu-id="e7805-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="e7805-163">Você também pode usar marcas como o VirtualNetwork, o AzureLoadBalancer e a Internet.</span><span class="sxs-lookup"><span data-stu-id="e7805-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7805-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="e7805-165">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="e7805-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="e7805-166">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="e7805-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e7805-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="e7805-168">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="e7805-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="e7805-169">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="e7805-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="e7805-170">-SourcePortRange</span></span>
<span data-ttu-id="e7805-171">Especifica a porta de origem ou o intervalo.</span><span class="sxs-lookup"><span data-stu-id="e7805-171">Specifies the source port or range.</span></span>
<span data-ttu-id="e7805-172">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e7805-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7805-173">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="e7805-173">An integer</span></span>
- <span data-ttu-id="e7805-174">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="e7805-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="e7805-175">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="e7805-175">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7805-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7805-176">CommonParameters</span></span>
<span data-ttu-id="e7805-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7805-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7805-178">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7805-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7805-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7805-179">INPUTS</span></span>

## <span data-ttu-id="e7805-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7805-180">OUTPUTS</span></span>

### <span data-ttu-id="e7805-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="e7805-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="e7805-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7805-182">NOTES</span></span>

## <span data-ttu-id="e7805-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7805-183">RELATED LINKS</span></span>

[<span data-ttu-id="e7805-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7805-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7805-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7805-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7805-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7805-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7805-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7805-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


