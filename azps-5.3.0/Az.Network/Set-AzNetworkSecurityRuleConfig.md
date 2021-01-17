---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433391"
---
# <span data-ttu-id="4846f-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4846f-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="4846f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4846f-102">SYNOPSIS</span></span>
<span data-ttu-id="4846f-103">Atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="4846f-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="4846f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4846f-104">SYNTAX</span></span>

### <span data-ttu-id="4846f-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="4846f-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4846f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4846f-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4846f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4846f-107">DESCRIPTION</span></span>
<span data-ttu-id="4846f-108">O cmdlet **set-AzNetworkSecurityRuleConfig** atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="4846f-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="4846f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4846f-109">EXAMPLES</span></span>

### <span data-ttu-id="4846f-110">Exemplo 1: alterar a configuração do Access em uma regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4846f-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="4846f-111">O primeiro comando obtém o grupo de segurança de rede chamado NSG-FrontEnd e, em seguida, armazena-o na variável $nsg.</span><span class="sxs-lookup"><span data-stu-id="4846f-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="4846f-112">O segundo comando usa o operador pipeline para passar o grupo de segurança em $nsg para Get-AzNetworkSecurityRuleConfig, que obtém a configuração da regra de segurança chamada RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="4846f-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="4846f-113">O terceiro comando altera a configuração de acesso de RDP-Rule para Deny.</span><span class="sxs-lookup"><span data-stu-id="4846f-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="4846f-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4846f-114">Example 2</span></span>

<span data-ttu-id="4846f-115">Atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="4846f-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="4846f-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="4846f-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="4846f-117">OS</span><span class="sxs-lookup"><span data-stu-id="4846f-117">PARAMETERS</span></span>

### <span data-ttu-id="4846f-118">-Acesso</span><span class="sxs-lookup"><span data-stu-id="4846f-118">-Access</span></span>
<span data-ttu-id="4846f-119">Especifica se o tráfego de rede é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="4846f-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="4846f-120">Os valores aceitáveis para esse parâmetro são: allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="4846f-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="4846f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4846f-121">-DefaultProfile</span></span>
<span data-ttu-id="4846f-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4846f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4846f-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4846f-123">-Description</span></span>
<span data-ttu-id="4846f-124">Especifica uma descrição para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="4846f-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="4846f-125">O tamanho máximo é de 140 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4846f-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="4846f-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4846f-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="4846f-127">Especifica um prefixo de endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="4846f-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="4846f-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4846f-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4846f-129">Um endereço de roteamento entre domínios sem classe (CIDR)</span><span class="sxs-lookup"><span data-stu-id="4846f-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="4846f-130">Um intervalo de endereços IP de destino</span><span class="sxs-lookup"><span data-stu-id="4846f-130">A destination IP address range</span></span> 
- <span data-ttu-id="4846f-131">Um caractere curinga (\*) para corresponder a qualquer endereço IP você pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="4846f-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="4846f-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4846f-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="4846f-133">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="4846f-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="4846f-134">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="4846f-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4846f-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4846f-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="4846f-136">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="4846f-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="4846f-137">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="4846f-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4846f-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="4846f-138">-DestinationPortRange</span></span>
<span data-ttu-id="4846f-139">Especifica uma porta de destino ou um intervalo.</span><span class="sxs-lookup"><span data-stu-id="4846f-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="4846f-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4846f-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4846f-141">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="4846f-141">An integer</span></span> 
- <span data-ttu-id="4846f-142">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="4846f-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="4846f-143">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="4846f-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="4846f-144">-Direction</span><span class="sxs-lookup"><span data-stu-id="4846f-144">-Direction</span></span>
<span data-ttu-id="4846f-145">Especifica se uma regra é avaliada para tráfego de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="4846f-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="4846f-146">Os valores aceitáveis para esse parâmetro são: de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="4846f-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="4846f-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="4846f-147">-Name</span></span>
<span data-ttu-id="4846f-148">Especifica o nome da configuração de regra de segurança de rede que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="4846f-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4846f-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4846f-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4846f-150">Especifica o objeto **NetworkSecurityGroup** que contém a configuração de regra de segurança de rede a ser definida.</span><span class="sxs-lookup"><span data-stu-id="4846f-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="4846f-151">-Priority</span><span class="sxs-lookup"><span data-stu-id="4846f-151">-Priority</span></span>
<span data-ttu-id="4846f-152">Especifica a prioridade de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="4846f-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="4846f-153">Os valores aceitáveis para esse parâmetro são: um inteiro entre 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="4846f-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="4846f-154">O número de prioridade deve ser exclusivo para cada regra na coleção.</span><span class="sxs-lookup"><span data-stu-id="4846f-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="4846f-155">Quanto menor o número de prioridade, maior a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="4846f-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="4846f-156">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="4846f-156">-Protocol</span></span>
<span data-ttu-id="4846f-157">Especifica o protocolo de rede ao qual uma configuração de regra se aplica.</span><span class="sxs-lookup"><span data-stu-id="4846f-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="4846f-158">Os valores aceitáveis para esse parâmetro são:--TCP</span><span class="sxs-lookup"><span data-stu-id="4846f-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="4846f-159">Grama</span><span class="sxs-lookup"><span data-stu-id="4846f-159">Udp</span></span>
- <span data-ttu-id="4846f-160">Um caractere curinga (\*) para corresponder a ambos</span><span class="sxs-lookup"><span data-stu-id="4846f-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="4846f-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4846f-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="4846f-162">Especifica um prefixo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="4846f-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="4846f-163">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4846f-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4846f-164">UM CIDR</span><span class="sxs-lookup"><span data-stu-id="4846f-164">A CIDR</span></span>
- <span data-ttu-id="4846f-165">Um intervalo de IP de origem</span><span class="sxs-lookup"><span data-stu-id="4846f-165">A source IP range</span></span>
- <span data-ttu-id="4846f-166">Um caractere curinga (\*) para corresponder a qualquer endereço IP você também pode usar marcas como o VirtualNetwork, o AzureLoadBalancer e a Internet.</span><span class="sxs-lookup"><span data-stu-id="4846f-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="4846f-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4846f-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="4846f-168">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="4846f-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="4846f-169">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="4846f-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4846f-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4846f-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="4846f-171">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="4846f-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="4846f-172">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="4846f-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4846f-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="4846f-173">-SourcePortRange</span></span>
<span data-ttu-id="4846f-174">Especifica a porta de origem ou o intervalo.</span><span class="sxs-lookup"><span data-stu-id="4846f-174">Specifies the source port or range.</span></span>
<span data-ttu-id="4846f-175">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4846f-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4846f-176">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="4846f-176">An integer</span></span>
- <span data-ttu-id="4846f-177">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="4846f-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="4846f-178">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="4846f-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="4846f-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4846f-179">CommonParameters</span></span>
<span data-ttu-id="4846f-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4846f-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4846f-181">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4846f-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4846f-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4846f-182">INPUTS</span></span>

### <span data-ttu-id="4846f-183">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4846f-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4846f-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4846f-184">OUTPUTS</span></span>

### <span data-ttu-id="4846f-185">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4846f-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4846f-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4846f-186">NOTES</span></span>

## <span data-ttu-id="4846f-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4846f-187">RELATED LINKS</span></span>

[<span data-ttu-id="4846f-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4846f-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4846f-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4846f-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4846f-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4846f-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4846f-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4846f-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


