---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892061"
---
# <span data-ttu-id="1a63d-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a63d-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="1a63d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a63d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a63d-103">Atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1a63d-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="1a63d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1a63d-104">SYNTAX</span></span>

### <span data-ttu-id="1a63d-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1a63d-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a63d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a63d-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a63d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1a63d-107">DESCRIPTION</span></span>
<span data-ttu-id="1a63d-108">O cmdlet **Set-AzNetworkSecurityRuleConfig** atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1a63d-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="1a63d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a63d-109">EXAMPLES</span></span>

### <span data-ttu-id="1a63d-110">Exemplo 1: Alterar a configuração de acesso em uma regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="1a63d-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="1a63d-111">O primeiro comando obtém o grupo de segurança de rede chamado NSG-FrontEnd e o armazena na variável $nsg.</span><span class="sxs-lookup"><span data-stu-id="1a63d-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="1a63d-112">O segundo comando usa o operador de pipeline para passar o grupo de segurança no $nsg para Get-AzNetworkSecurityRuleConfig, que obtém a configuração de regra de segurança denominada rdp-rule.</span><span class="sxs-lookup"><span data-stu-id="1a63d-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="1a63d-113">O terceiro comando altera a configuração de acesso do rdp-rule para Negar.</span><span class="sxs-lookup"><span data-stu-id="1a63d-113">The third command changes the access configuration of rdp-rule to Deny.</span></span> <span data-ttu-id="1a63d-114">No entanto, isso substitui a regra e define apenas os parâmetros que são passados para a função Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="1a63d-114">However, this overwrites the rule and only sets the parameters that are passed to the Set-AzNetworkSecurityRuleConfig function.</span></span>   <span data-ttu-id="1a63d-115">OBSERVAÇÃO: Não há como alterar um único atributo</span><span class="sxs-lookup"><span data-stu-id="1a63d-115">NOTE: There is no way to change a single attribute</span></span>

### <span data-ttu-id="1a63d-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1a63d-116">Example 2</span></span>

<span data-ttu-id="1a63d-117">Atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1a63d-117">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="1a63d-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="1a63d-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="1a63d-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1a63d-119">PARAMETERS</span></span>

### <span data-ttu-id="1a63d-120">-Access</span><span class="sxs-lookup"><span data-stu-id="1a63d-120">-Access</span></span>
<span data-ttu-id="1a63d-121">Especifica se o tráfego de rede é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="1a63d-121">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="1a63d-122">Os valores aceitáveis para este parâmetro são: Permitir e Negar.</span><span class="sxs-lookup"><span data-stu-id="1a63d-122">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="1a63d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a63d-123">-DefaultProfile</span></span>
<span data-ttu-id="1a63d-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1a63d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a63d-125">-Description</span><span class="sxs-lookup"><span data-stu-id="1a63d-125">-Description</span></span>
<span data-ttu-id="1a63d-126">Especifica uma descrição para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="1a63d-126">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="1a63d-127">O tamanho máximo é de 140 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1a63d-127">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="1a63d-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1a63d-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="1a63d-129">Especifica um prefixo de endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="1a63d-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="1a63d-130">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a63d-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a63d-131">Um Roteamento entre Domínios sem Classificação (CIDR)</span><span class="sxs-lookup"><span data-stu-id="1a63d-131">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="1a63d-132">Um intervalo de endereços IP de destino</span><span class="sxs-lookup"><span data-stu-id="1a63d-132">A destination IP address range</span></span> 
- <span data-ttu-id="1a63d-133">Um caractere curinga (\*) para corresponder a qualquer endereço IP Você pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="1a63d-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="1a63d-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1a63d-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="1a63d-135">O grupo de segurança do aplicativo definido como destino da regra.</span><span class="sxs-lookup"><span data-stu-id="1a63d-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="1a63d-136">Ele não pode ser usado com o parâmetro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="1a63d-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1a63d-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1a63d-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="1a63d-138">O grupo de segurança do aplicativo definido como destino da regra.</span><span class="sxs-lookup"><span data-stu-id="1a63d-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="1a63d-139">Ele não pode ser usado com o parâmetro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="1a63d-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1a63d-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="1a63d-140">-DestinationPortRange</span></span>
<span data-ttu-id="1a63d-141">Especifica uma porta de destino ou intervalo.</span><span class="sxs-lookup"><span data-stu-id="1a63d-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="1a63d-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a63d-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a63d-143">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="1a63d-143">An integer</span></span> 
- <span data-ttu-id="1a63d-144">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="1a63d-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="1a63d-145">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="1a63d-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="1a63d-146">-Direction</span><span class="sxs-lookup"><span data-stu-id="1a63d-146">-Direction</span></span>
<span data-ttu-id="1a63d-147">Especifica se uma regra é avaliada para tráfego de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="1a63d-147">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="1a63d-148">Os valores aceitáveis para este parâmetro são: Entrada e Saída.</span><span class="sxs-lookup"><span data-stu-id="1a63d-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="1a63d-149">-Name</span><span class="sxs-lookup"><span data-stu-id="1a63d-149">-Name</span></span>
<span data-ttu-id="1a63d-150">Especifica o nome da configuração de regra de segurança de rede que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="1a63d-150">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="1a63d-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1a63d-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1a63d-152">Especifica o **objeto NetworkSecurityGroup** que contém a configuração de regra de segurança de rede a ser definida.</span><span class="sxs-lookup"><span data-stu-id="1a63d-152">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="1a63d-153">-Priority</span><span class="sxs-lookup"><span data-stu-id="1a63d-153">-Priority</span></span>
<span data-ttu-id="1a63d-154">Especifica a prioridade de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="1a63d-154">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="1a63d-155">Os valores aceitáveis para este parâmetro são: Um inteiro entre 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="1a63d-155">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="1a63d-156">O número de prioridade deve ser exclusivo para cada regra na coleção.</span><span class="sxs-lookup"><span data-stu-id="1a63d-156">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="1a63d-157">Quanto menor for o número de prioridade, maior será a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="1a63d-157">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="1a63d-158">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1a63d-158">-Protocol</span></span>
<span data-ttu-id="1a63d-159">Especifica o protocolo de rede ao que uma configuração de regra se aplica.</span><span class="sxs-lookup"><span data-stu-id="1a63d-159">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="1a63d-160">Os valores aceitáveis para este parâmetro são: --Tcp</span><span class="sxs-lookup"><span data-stu-id="1a63d-160">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="1a63d-161">Udp</span><span class="sxs-lookup"><span data-stu-id="1a63d-161">Udp</span></span>
- <span data-ttu-id="1a63d-162">Um caractere curinga (\*) para corresponder a ambos</span><span class="sxs-lookup"><span data-stu-id="1a63d-162">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="1a63d-163">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1a63d-163">-SourceAddressPrefix</span></span>
<span data-ttu-id="1a63d-164">Especifica um prefixo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="1a63d-164">Specifies a source address prefix.</span></span>
<span data-ttu-id="1a63d-165">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a63d-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a63d-166">A CIDR</span><span class="sxs-lookup"><span data-stu-id="1a63d-166">A CIDR</span></span>
- <span data-ttu-id="1a63d-167">Um intervalo IP de origem</span><span class="sxs-lookup"><span data-stu-id="1a63d-167">A source IP range</span></span>
- <span data-ttu-id="1a63d-168">Um caractere curinga (\*) para corresponder a qualquer endereço IP Você também pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="1a63d-168">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="1a63d-169">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1a63d-169">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="1a63d-170">O grupo de segurança do aplicativo definido como fonte da regra.</span><span class="sxs-lookup"><span data-stu-id="1a63d-170">The application security group set as source for the rule.</span></span> <span data-ttu-id="1a63d-171">Ele não pode ser usado com o parâmetro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="1a63d-171">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1a63d-172">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1a63d-172">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="1a63d-173">O grupo de segurança do aplicativo definido como fonte da regra.</span><span class="sxs-lookup"><span data-stu-id="1a63d-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="1a63d-174">Ele não pode ser usado com o parâmetro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="1a63d-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1a63d-175">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="1a63d-175">-SourcePortRange</span></span>
<span data-ttu-id="1a63d-176">Especifica a porta de origem ou intervalo.</span><span class="sxs-lookup"><span data-stu-id="1a63d-176">Specifies the source port or range.</span></span>
<span data-ttu-id="1a63d-177">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a63d-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a63d-178">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="1a63d-178">An integer</span></span>
- <span data-ttu-id="1a63d-179">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="1a63d-179">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="1a63d-180">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="1a63d-180">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="1a63d-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a63d-181">CommonParameters</span></span>
<span data-ttu-id="1a63d-182">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a63d-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a63d-183">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a63d-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a63d-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a63d-184">INPUTS</span></span>

### <span data-ttu-id="1a63d-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1a63d-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1a63d-186">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1a63d-186">OUTPUTS</span></span>

### <span data-ttu-id="1a63d-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1a63d-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1a63d-188">NOTES</span><span class="sxs-lookup"><span data-stu-id="1a63d-188">NOTES</span></span>

## <span data-ttu-id="1a63d-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a63d-189">RELATED LINKS</span></span>

[<span data-ttu-id="1a63d-190">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a63d-190">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1a63d-191">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a63d-191">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1a63d-192">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a63d-192">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1a63d-193">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a63d-193">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


