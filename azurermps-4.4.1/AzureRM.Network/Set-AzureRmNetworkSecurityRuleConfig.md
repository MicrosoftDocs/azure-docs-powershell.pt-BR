---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: fa1416d7bd65236d3a4e1198d6f70efb1a860985
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429229"
---
# <span data-ttu-id="41724-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41724-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="41724-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41724-102">SYNOPSIS</span></span>
<span data-ttu-id="41724-103">Define o estado da meta para uma configuração de regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="41724-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41724-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41724-104">SYNTAX</span></span>

### <span data-ttu-id="41724-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="41724-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41724-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="41724-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41724-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41724-107">DESCRIPTION</span></span>
<span data-ttu-id="41724-108">O cmdlet **set-AzureRmNetworkSecurityRuleConfig** define o estado da meta para uma configuração de regra de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="41724-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="41724-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41724-109">EXAMPLES</span></span>

### <span data-ttu-id="41724-110">Exemplo 1: alterar a configuração do Access em uma regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="41724-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="41724-111">O primeiro comando obtém o grupo de segurança de rede chamado NSG-FrontEnd e, em seguida, armazena-o na variável $nsg.</span><span class="sxs-lookup"><span data-stu-id="41724-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="41724-112">O segundo comando usa o operador pipeline para passar o grupo de segurança em $nsg para Get-AzureRmNetworkSecurityRuleConfig, que obtém a configuração da regra de segurança chamada RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="41724-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="41724-113">O terceiro comando altera a configuração de acesso de RDP-Rule para Deny.</span><span class="sxs-lookup"><span data-stu-id="41724-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="41724-114">OS</span><span class="sxs-lookup"><span data-stu-id="41724-114">PARAMETERS</span></span>

### <span data-ttu-id="41724-115">-Acesso</span><span class="sxs-lookup"><span data-stu-id="41724-115">-Access</span></span>
<span data-ttu-id="41724-116">Especifica se o tráfego de rede é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="41724-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="41724-117">Os valores aceitáveis para esse parâmetro são: allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="41724-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="41724-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41724-118">-DefaultProfile</span></span>
<span data-ttu-id="41724-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41724-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41724-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="41724-120">-Description</span></span>
<span data-ttu-id="41724-121">Especifica uma descrição para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="41724-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="41724-122">O tamanho máximo é de 140 caracteres.</span><span class="sxs-lookup"><span data-stu-id="41724-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="41724-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="41724-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="41724-124">Especifica um prefixo de endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="41724-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="41724-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="41724-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41724-126">Um endereço de roteamento entre domínios sem classe (CIDR)</span><span class="sxs-lookup"><span data-stu-id="41724-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="41724-127">Um intervalo de endereços IP de destino</span><span class="sxs-lookup"><span data-stu-id="41724-127">A destination IP address range</span></span> 
- <span data-ttu-id="41724-128">Um caractere curinga (\*) para corresponder a qualquer endereço IP</span><span class="sxs-lookup"><span data-stu-id="41724-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="41724-129">Você pode usar marcas como o VirtualNetwork, o AzureLoadBalancer e a Internet.</span><span class="sxs-lookup"><span data-stu-id="41724-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="41724-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41724-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="41724-131">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="41724-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="41724-132">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="41724-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="41724-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="41724-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="41724-134">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="41724-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="41724-135">Ele não pode ser usado com o parâmetro ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="41724-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="41724-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="41724-136">-DestinationPortRange</span></span>
<span data-ttu-id="41724-137">Especifica uma porta de destino ou um intervalo.</span><span class="sxs-lookup"><span data-stu-id="41724-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="41724-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="41724-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41724-139">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="41724-139">An integer</span></span> 
- <span data-ttu-id="41724-140">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="41724-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="41724-141">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="41724-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="41724-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="41724-142">-Direction</span></span>
<span data-ttu-id="41724-143">Especifica se uma regra é avaliada para tráfego de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="41724-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="41724-144">Os valores aceitáveis para esse parâmetro são: de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="41724-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="41724-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="41724-145">-Name</span></span>
<span data-ttu-id="41724-146">Especifica o nome da configuração de regra de segurança de rede que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="41724-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="41724-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41724-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="41724-148">Especifica o objeto **NetworkSecurityGroup** que contém a configuração de regra de segurança de rede a ser definida.</span><span class="sxs-lookup"><span data-stu-id="41724-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="41724-149">-Priority</span><span class="sxs-lookup"><span data-stu-id="41724-149">-Priority</span></span>
<span data-ttu-id="41724-150">Especifica a prioridade de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="41724-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="41724-151">Os valores aceitáveis para esse parâmetro são: um inteiro entre 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="41724-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="41724-152">O número de prioridade deve ser exclusivo para cada regra na coleção.</span><span class="sxs-lookup"><span data-stu-id="41724-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="41724-153">Quanto menor o número de prioridade, maior a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="41724-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="41724-154">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="41724-154">-Protocol</span></span>
<span data-ttu-id="41724-155">Especifica o protocolo de rede ao qual uma configuração de regra se aplica.</span><span class="sxs-lookup"><span data-stu-id="41724-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="41724-156">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="41724-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="41724-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="41724-157">--Tcp</span></span>
- <span data-ttu-id="41724-158">Grama</span><span class="sxs-lookup"><span data-stu-id="41724-158">Udp</span></span>
- <span data-ttu-id="41724-159">Um caractere curinga (\*) para corresponder a ambos</span><span class="sxs-lookup"><span data-stu-id="41724-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="41724-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="41724-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="41724-161">Especifica um prefixo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="41724-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="41724-162">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="41724-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41724-163">UM CIDR</span><span class="sxs-lookup"><span data-stu-id="41724-163">A CIDR</span></span>
- <span data-ttu-id="41724-164">Um intervalo de IP de origem</span><span class="sxs-lookup"><span data-stu-id="41724-164">A source IP range</span></span>
- <span data-ttu-id="41724-165">Um caractere curinga (\*) para corresponder a qualquer endereço IP</span><span class="sxs-lookup"><span data-stu-id="41724-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="41724-166">Você também pode usar marcas como o VirtualNetwork, o AzureLoadBalancer e a Internet.</span><span class="sxs-lookup"><span data-stu-id="41724-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="41724-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41724-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="41724-168">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="41724-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="41724-169">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="41724-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="41724-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="41724-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="41724-171">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="41724-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="41724-172">Ele não pode ser usado com o parâmetro ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="41724-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="41724-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="41724-173">-SourcePortRange</span></span>
<span data-ttu-id="41724-174">Especifica a porta de origem ou o intervalo.</span><span class="sxs-lookup"><span data-stu-id="41724-174">Specifies the source port or range.</span></span>
<span data-ttu-id="41724-175">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="41724-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41724-176">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="41724-176">An integer</span></span>
- <span data-ttu-id="41724-177">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="41724-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="41724-178">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="41724-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="41724-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41724-179">CommonParameters</span></span>
<span data-ttu-id="41724-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41724-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41724-181">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41724-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41724-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41724-182">INPUTS</span></span>

### <span data-ttu-id="41724-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41724-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="41724-184">O parâmetro ' NetworkSecurityGroup ' aceita o valor do tipo ' PSNetworkSecurityGroup ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="41724-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="41724-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41724-185">OUTPUTS</span></span>

### <span data-ttu-id="41724-186">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41724-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="41724-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41724-187">NOTES</span></span>

## <span data-ttu-id="41724-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41724-188">RELATED LINKS</span></span>

[<span data-ttu-id="41724-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41724-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41724-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41724-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41724-191">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41724-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41724-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41724-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


