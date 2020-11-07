---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6f724cb7208afb1a5f9474048b5e2dc46c17f5af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772368"
---
# <span data-ttu-id="a286b-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a286b-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a286b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a286b-102">SYNOPSIS</span></span>
<span data-ttu-id="a286b-103">Cria uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a286b-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a286b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a286b-104">SYNTAX</span></span>

### <span data-ttu-id="a286b-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="a286b-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a286b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a286b-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a286b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a286b-107">DESCRIPTION</span></span>
<span data-ttu-id="a286b-108">O cmdlet **New-AzLoadBalancerInboundNatRuleConfig** cria uma configuração de regra NAT (conversão de endereços de rede) de entrada para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="a286b-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a286b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a286b-109">EXAMPLES</span></span>

### <span data-ttu-id="a286b-110">Exemplo 1: criar uma configuração de regra NAT de entrada para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="a286b-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="a286b-111">O primeiro comando cria um endereço IP público chamado MyPublicIP no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="a286b-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="a286b-112">O segundo comando cria uma configuração de IP de front-end chamada FrontendIpConfig01 usando o endereço IP público no $publicip e, em seguida, armazena-o na variável $frontend.</span><span class="sxs-lookup"><span data-stu-id="a286b-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="a286b-113">O terceiro comando cria uma configuração de regra NAT de entrada chamada MyInboundNatRule usando o objeto front-end no $frontend.</span><span class="sxs-lookup"><span data-stu-id="a286b-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="a286b-114">O protocolo TCP é especificado e a porta de front-end é 3389, a mesma que a porta back-end nesse caso.</span><span class="sxs-lookup"><span data-stu-id="a286b-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="a286b-115">Os parâmetros *FrontendIpConfiguration* , *Protocol* , *FrontendPort* e *BackendPort* são necessários para criar uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="a286b-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="a286b-116">OS</span><span class="sxs-lookup"><span data-stu-id="a286b-116">PARAMETERS</span></span>

### <span data-ttu-id="a286b-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a286b-117">-BackendPort</span></span>
<span data-ttu-id="a286b-118">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="a286b-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a286b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a286b-119">-DefaultProfile</span></span>
<span data-ttu-id="a286b-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a286b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a286b-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a286b-121">-EnableFloatingIP</span></span>
<span data-ttu-id="a286b-122">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="a286b-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a286b-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a286b-123">-EnableTcpReset</span></span>
<span data-ttu-id="a286b-124">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="a286b-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a286b-125">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="a286b-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a286b-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a286b-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a286b-127">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a286b-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a286b-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a286b-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a286b-129">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="a286b-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a286b-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a286b-130">-FrontendPort</span></span>
<span data-ttu-id="a286b-131">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a286b-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a286b-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a286b-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a286b-133">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a286b-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a286b-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="a286b-134">-Name</span></span>
<span data-ttu-id="a286b-135">Especifica o nome da configuração de regra que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="a286b-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a286b-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="a286b-136">-Protocol</span></span>
<span data-ttu-id="a286b-137">Especifica um protocolo.</span><span class="sxs-lookup"><span data-stu-id="a286b-137">Specifies a protocol.</span></span>
<span data-ttu-id="a286b-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a286b-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a286b-139">Protocol</span><span class="sxs-lookup"><span data-stu-id="a286b-139">Tcp</span></span>
- <span data-ttu-id="a286b-140">Grama</span><span class="sxs-lookup"><span data-stu-id="a286b-140">Udp</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a286b-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a286b-141">-Confirm</span></span>
<span data-ttu-id="a286b-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a286b-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a286b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a286b-143">-WhatIf</span></span>
<span data-ttu-id="a286b-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a286b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a286b-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a286b-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a286b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a286b-146">CommonParameters</span></span>
<span data-ttu-id="a286b-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a286b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a286b-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a286b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a286b-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a286b-149">INPUTS</span></span>

### <span data-ttu-id="a286b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a286b-150">System.String</span></span>

### <span data-ttu-id="a286b-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a286b-151">System.Int32</span></span>

### <span data-ttu-id="a286b-152">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a286b-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a286b-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a286b-153">OUTPUTS</span></span>

### <span data-ttu-id="a286b-154">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a286b-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="a286b-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a286b-155">NOTES</span></span>

## <span data-ttu-id="a286b-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a286b-156">RELATED LINKS</span></span>

[<span data-ttu-id="a286b-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a286b-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a286b-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a286b-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a286b-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a286b-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a286b-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a286b-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="a286b-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a286b-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a286b-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a286b-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

