---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114131"
---
# <span data-ttu-id="634df-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="634df-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="634df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="634df-102">SYNOPSIS</span></span>
<span data-ttu-id="634df-103">Cria uma configuração de regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="634df-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="634df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="634df-104">SYNTAX</span></span>

### <span data-ttu-id="634df-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="634df-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="634df-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="634df-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="634df-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="634df-107">DESCRIPTION</span></span>
<span data-ttu-id="634df-108">O cmdlet **New-AzNetworkSecurityRuleConfig** cria uma configuração de regra de segurança de rede do Azure para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="634df-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="634df-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="634df-109">EXAMPLES</span></span>

### <span data-ttu-id="634df-110">Exemplo 1: Criar uma regra de segurança de rede para permitir RDP</span><span class="sxs-lookup"><span data-stu-id="634df-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="634df-111">Este comando cria uma regra de segurança que permite o acesso da Internet à porta 3389</span><span class="sxs-lookup"><span data-stu-id="634df-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="634df-112">Exemplo 2: Criar uma regra de segurança de rede que permita HTTP</span><span class="sxs-lookup"><span data-stu-id="634df-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="634df-113">Este comando cria uma regra de segurança que permite o acesso da Internet à porta 80</span><span class="sxs-lookup"><span data-stu-id="634df-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="634df-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="634df-114">PARAMETERS</span></span>

### <span data-ttu-id="634df-115">-Access</span><span class="sxs-lookup"><span data-stu-id="634df-115">-Access</span></span>
<span data-ttu-id="634df-116">Especifica se o tráfego de rede é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="634df-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="634df-117">Os valores aceitáveis para este parâmetro são: Permitir e Negar.</span><span class="sxs-lookup"><span data-stu-id="634df-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="634df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634df-118">-DefaultProfile</span></span>
<span data-ttu-id="634df-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="634df-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="634df-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="634df-120">-Description</span></span>
<span data-ttu-id="634df-121">Especifica uma descrição da configuração da regra de segurança de rede a ser criado.</span><span class="sxs-lookup"><span data-stu-id="634df-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="634df-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="634df-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="634df-123">Especifica um prefixo de endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="634df-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="634df-124">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="634df-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="634df-125">Um endereço CIDR (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="634df-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="634df-126">Um intervalo de endereços IP de destino</span><span class="sxs-lookup"><span data-stu-id="634df-126">A destination IP address range</span></span> 
- <span data-ttu-id="634df-127">Um caractere curinga (\*) para corresponder a qualquer endereço IP Você pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="634df-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="634df-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="634df-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="634df-129">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="634df-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="634df-130">Ele não pode ser usado com o parâmetro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="634df-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="634df-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="634df-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="634df-132">O grupo de segurança do aplicativo definido como destino para a regra.</span><span class="sxs-lookup"><span data-stu-id="634df-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="634df-133">Ele não pode ser usado com o parâmetro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="634df-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="634df-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="634df-134">-DestinationPortRange</span></span>
<span data-ttu-id="634df-135">Especifica uma porta ou intervalo de destino.</span><span class="sxs-lookup"><span data-stu-id="634df-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="634df-136">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="634df-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="634df-137">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="634df-137">An integer</span></span>
- <span data-ttu-id="634df-138">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="634df-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="634df-139">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="634df-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="634df-140">-Direção</span><span class="sxs-lookup"><span data-stu-id="634df-140">-Direction</span></span>
<span data-ttu-id="634df-141">Especifica se uma regra é avaliada sobre o tráfego de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="634df-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="634df-142">Os valores aceitáveis para este parâmetro são: Entrada e Saída.</span><span class="sxs-lookup"><span data-stu-id="634df-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="634df-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="634df-143">-Name</span></span>
<span data-ttu-id="634df-144">Especifica o nome da configuração da regra de segurança de rede que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="634df-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="634df-145">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="634df-145">-Priority</span></span>
<span data-ttu-id="634df-146">Especifica a prioridade de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="634df-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="634df-147">Os valores aceitáveis para este parâmetro são: um inteiro entre 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="634df-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="634df-148">O número de prioridade deve ser exclusivo para cada regra na coleção.</span><span class="sxs-lookup"><span data-stu-id="634df-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="634df-149">Quanto menor o número de prioridade, maior será a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="634df-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="634df-150">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="634df-150">-Protocol</span></span>
<span data-ttu-id="634df-151">Especifica o protocolo de rede ao que uma nova configuração de regra se aplica.</span><span class="sxs-lookup"><span data-stu-id="634df-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="634df-152">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="634df-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="634df-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="634df-153">Tcp</span></span>
- <span data-ttu-id="634df-154">Udp</span><span class="sxs-lookup"><span data-stu-id="634df-154">Udp</span></span>
- <span data-ttu-id="634df-155">caractere curinga (\*) para corresponder a ambos.</span><span class="sxs-lookup"><span data-stu-id="634df-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="634df-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="634df-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="634df-157">Especifica um prefixo de endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="634df-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="634df-158">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="634df-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="634df-159">A CIDR</span><span class="sxs-lookup"><span data-stu-id="634df-159">A CIDR</span></span>
- <span data-ttu-id="634df-160">Um intervalo IP de origem</span><span class="sxs-lookup"><span data-stu-id="634df-160">A source IP range</span></span>
- <span data-ttu-id="634df-161">Um caractere curinga (\*) para corresponder a qualquer endereço IP.</span><span class="sxs-lookup"><span data-stu-id="634df-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="634df-162">Você também pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="634df-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="634df-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="634df-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="634df-164">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="634df-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="634df-165">Ele não pode ser usado com o parâmetro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="634df-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="634df-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="634df-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="634df-167">O grupo de segurança do aplicativo definido como fonte para a regra.</span><span class="sxs-lookup"><span data-stu-id="634df-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="634df-168">Ele não pode ser usado com o parâmetro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="634df-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="634df-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="634df-169">-SourcePortRange</span></span>
<span data-ttu-id="634df-170">Especifica a porta ou intervalo de origem.</span><span class="sxs-lookup"><span data-stu-id="634df-170">Specifies the source port or range.</span></span>
<span data-ttu-id="634df-171">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="634df-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="634df-172">Um inteiro</span><span class="sxs-lookup"><span data-stu-id="634df-172">An integer</span></span>
- <span data-ttu-id="634df-173">Um intervalo de inteiros entre 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="634df-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="634df-174">Um caractere curinga (\*) para corresponder a qualquer porta</span><span class="sxs-lookup"><span data-stu-id="634df-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="634df-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634df-175">CommonParameters</span></span>
<span data-ttu-id="634df-176">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="634df-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634df-177">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="634df-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="634df-178">Entradas</span><span class="sxs-lookup"><span data-stu-id="634df-178">INPUTS</span></span>

### <span data-ttu-id="634df-179">Nenhum</span><span class="sxs-lookup"><span data-stu-id="634df-179">None</span></span>

## <span data-ttu-id="634df-180">Saídas</span><span class="sxs-lookup"><span data-stu-id="634df-180">OUTPUTS</span></span>

### <span data-ttu-id="634df-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="634df-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="634df-182">Notas</span><span class="sxs-lookup"><span data-stu-id="634df-182">NOTES</span></span>

## <span data-ttu-id="634df-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="634df-183">RELATED LINKS</span></span>

[<span data-ttu-id="634df-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="634df-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="634df-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="634df-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="634df-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="634df-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="634df-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="634df-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


