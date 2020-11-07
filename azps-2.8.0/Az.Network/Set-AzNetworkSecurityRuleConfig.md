---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 4293f044a270a43f12c7b4d74a410a324d0284dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771431"
---
# <span data-ttu-id="6e135-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e135-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="6e135-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e135-102">SYNOPSIS</span></span>
<span data-ttu-id="6e135-103">Atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="6e135-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="6e135-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e135-104">SYNTAX</span></span>

### <span data-ttu-id="6e135-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e135-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e135-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e135-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e135-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e135-107">DESCRIPTION</span></span>
<span data-ttu-id="6e135-108">O cmdlet **set-AzNetworkSecurityRuleConfig** atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="6e135-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="6e135-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e135-109">EXAMPLES</span></span>

### <span data-ttu-id="6e135-110">Exemplo 1: alterar a configuração do Access em uma regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="6e135-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="6e135-111">O primeiro comando obtém o grupo de segurança de rede chamado NSG-FrontEnd e, em seguida, armazena-o na variável $nsg.</span><span class="sxs-lookup"><span data-stu-id="6e135-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="6e135-112">O segundo comando usa o operador pipeline para passar o grupo de segurança em $nsg para Get-AzNetworkSecurityRuleConfig, que obtém a configuração da regra de segurança chamada RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="6e135-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="6e135-113">O terceiro comando altera a configuração de acesso de RDP-Rule para Deny.</span><span class="sxs-lookup"><span data-stu-id="6e135-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="6e135-114">OS</span><span class="sxs-lookup"><span data-stu-id="6e135-114">PARAMETERS</span></span>

### <span data-ttu-id="6e135-115">-Acesso</span><span class="sxs-lookup"><span data-stu-id="6e135-115">-Access</span></span>
<span data-ttu-id="6e135-116">Especifica se o tráfego de rede é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="6e135-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="6e135-117">Os valores aceitáveis para esse parâmetro são: allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="6e135-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="6e135-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e135-118">-DefaultProfile</span></span>
<span data-ttu-id="6e135-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e135-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e135-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6e135-120">-Description</span></span>
<span data-ttu-id="6e135-121">Especifica uma descrição para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="6e135-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="6e135-122">O tamanho máximo é de 140 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6e135-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="6e135-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6e135-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="6e135-124">Especifica um prefixo de endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="6e135-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="6e135-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6e135-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e135-126">Um endereço de roteamento entre domínios sem classe (CIDR)</span><span class="sxs-lookup"><span data-stu-id="6e135-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="6e135-127">Um intervalo de endereços IP de destino</span><span class="sxs-lookup"><span data-stu-id="6e135-127">A destination IP address range</span></span> 
- <span data-ttu-id="6e135-128">Um caractere curinga (\*) para corresponder a qualquer endereço IP você pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="6e135-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="6e135-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e135-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="6e135-130">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="6e135-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="6e135-131">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="6e135-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="6e135-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6e135-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="6e135-133">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="6e135-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="6e135-134">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="6e135-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="6e135-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="6e135-135">-DestinationPortRange</span></span>
<span data-ttu-id="6e135-136">Especifica uma porta de destino ou um intervalo.</span><span class="sxs-lookup"><span data-stu-id="6e135-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="6e135-137">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6e135-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e135-138">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="6e135-138">An integer</span></span> 
- <span data-ttu-id="6e135-139">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="6e135-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="6e135-140">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="6e135-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="6e135-141">-Direction</span><span class="sxs-lookup"><span data-stu-id="6e135-141">-Direction</span></span>
<span data-ttu-id="6e135-142">Especifica se uma regra é avaliada para tráfego de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="6e135-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="6e135-143">Os valores aceitáveis para esse parâmetro são: de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="6e135-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="6e135-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e135-144">-Name</span></span>
<span data-ttu-id="6e135-145">Especifica o nome da configuração de regra de segurança de rede que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="6e135-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="6e135-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e135-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="6e135-147">Especifica o objeto **NetworkSecurityGroup** que contém a configuração de regra de segurança de rede a ser definida.</span><span class="sxs-lookup"><span data-stu-id="6e135-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="6e135-148">-Priority</span><span class="sxs-lookup"><span data-stu-id="6e135-148">-Priority</span></span>
<span data-ttu-id="6e135-149">Especifica a prioridade de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="6e135-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="6e135-150">Os valores aceitáveis para esse parâmetro são: um inteiro entre 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="6e135-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="6e135-151">O número de prioridade deve ser exclusivo para cada regra na coleção.</span><span class="sxs-lookup"><span data-stu-id="6e135-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="6e135-152">Quanto menor o número de prioridade, maior a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="6e135-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="6e135-153">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="6e135-153">-Protocol</span></span>
<span data-ttu-id="6e135-154">Especifica o protocolo de rede ao qual uma configuração de regra se aplica.</span><span class="sxs-lookup"><span data-stu-id="6e135-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="6e135-155">Os valores aceitáveis para esse parâmetro são:--TCP</span><span class="sxs-lookup"><span data-stu-id="6e135-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="6e135-156">Grama</span><span class="sxs-lookup"><span data-stu-id="6e135-156">Udp</span></span>
- <span data-ttu-id="6e135-157">Um caractere curinga (\*) para corresponder a ambos</span><span class="sxs-lookup"><span data-stu-id="6e135-157">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="6e135-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6e135-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="6e135-159">Especifica um prefixo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="6e135-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="6e135-160">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6e135-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e135-161">UM CIDR</span><span class="sxs-lookup"><span data-stu-id="6e135-161">A CIDR</span></span>
- <span data-ttu-id="6e135-162">Um intervalo de IP de origem</span><span class="sxs-lookup"><span data-stu-id="6e135-162">A source IP range</span></span>
- <span data-ttu-id="6e135-163">Um caractere curinga (\*) para corresponder a qualquer endereço IP você também pode usar marcas como o VirtualNetwork, o AzureLoadBalancer e a Internet.</span><span class="sxs-lookup"><span data-stu-id="6e135-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="6e135-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e135-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="6e135-165">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="6e135-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="6e135-166">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="6e135-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="6e135-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6e135-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="6e135-168">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="6e135-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="6e135-169">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="6e135-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="6e135-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="6e135-170">-SourcePortRange</span></span>
<span data-ttu-id="6e135-171">Especifica a porta de origem ou o intervalo.</span><span class="sxs-lookup"><span data-stu-id="6e135-171">Specifies the source port or range.</span></span>
<span data-ttu-id="6e135-172">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6e135-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e135-173">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="6e135-173">An integer</span></span>
- <span data-ttu-id="6e135-174">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="6e135-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="6e135-175">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="6e135-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="6e135-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e135-176">CommonParameters</span></span>
<span data-ttu-id="6e135-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e135-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e135-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e135-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e135-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e135-179">INPUTS</span></span>

### <span data-ttu-id="6e135-180">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e135-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="6e135-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e135-181">OUTPUTS</span></span>

### <span data-ttu-id="6e135-182">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e135-182">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="6e135-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e135-183">NOTES</span></span>

## <span data-ttu-id="6e135-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e135-184">RELATED LINKS</span></span>

[<span data-ttu-id="6e135-185">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e135-185">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6e135-186">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e135-186">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6e135-187">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e135-187">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6e135-188">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e135-188">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


