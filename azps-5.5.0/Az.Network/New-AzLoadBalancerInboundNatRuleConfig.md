---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d2508b233bc67cb49d0a1c525f7e43ccf07242b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111626"
---
# <span data-ttu-id="26bbd-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26bbd-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="26bbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="26bbd-103">Cria uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="26bbd-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="26bbd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26bbd-104">SYNTAX</span></span>

### <span data-ttu-id="26bbd-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="26bbd-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26bbd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26bbd-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26bbd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="26bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="26bbd-108">O cmdlet **New-AzLoadBalancerInboundNatRuleConfig** cria uma configuração de regra nat (conversão de endereço de rede de entrada) para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="26bbd-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="26bbd-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26bbd-109">EXAMPLES</span></span>

### <span data-ttu-id="26bbd-110">Exemplo 1: Criar uma configuração de regra NAT de entrada para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="26bbd-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="26bbd-111">O primeiro comando cria um endereço IP público chamado MyPublicIP no grupo de recursos chamado MyResourceGroup e o armazena na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="26bbd-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="26bbd-112">O segundo comando cria uma configuração IP front-end chamada FrontendIpConfig01 usando o endereço IP público no $publicip e, em seguida, armazena-a na variável $frontend.</span><span class="sxs-lookup"><span data-stu-id="26bbd-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="26bbd-113">O terceiro comando cria uma configuração de regra NAT de entrada chamada MyInboundNatRule usando o objeto front-end no $frontend.</span><span class="sxs-lookup"><span data-stu-id="26bbd-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="26bbd-114">O protocolo TCP é especificado e a porta front-end é 3389, o mesmo que a porta de back-end nesse caso.</span><span class="sxs-lookup"><span data-stu-id="26bbd-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="26bbd-115">Os *parâmetros FrontendIpConfiguration,* *Protocol,* *FrontendPort* e *BackendPort* são todos necessários para criar uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="26bbd-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="26bbd-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26bbd-116">PARAMETERS</span></span>

### <span data-ttu-id="26bbd-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="26bbd-117">-BackendPort</span></span>
<span data-ttu-id="26bbd-118">Especifica a porta de back-end do tráfego que é corresponder a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="26bbd-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="26bbd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26bbd-119">-DefaultProfile</span></span>
<span data-ttu-id="26bbd-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="26bbd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26bbd-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="26bbd-121">-EnableFloatingIP</span></span>
<span data-ttu-id="26bbd-122">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="26bbd-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="26bbd-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="26bbd-123">-EnableTcpReset</span></span>
<span data-ttu-id="26bbd-124">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="26bbd-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="26bbd-125">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="26bbd-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="26bbd-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="26bbd-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="26bbd-127">Especifica uma lista de endereços IP front-end para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="26bbd-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="26bbd-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="26bbd-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="26bbd-129">Especifica a ID de uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="26bbd-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="26bbd-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="26bbd-130">-FrontendPort</span></span>
<span data-ttu-id="26bbd-131">Especifica a porta front-end que é corresponder a uma configuração de regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="26bbd-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="26bbd-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="26bbd-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="26bbd-133">Especifica o tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="26bbd-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="26bbd-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="26bbd-134">-Name</span></span>
<span data-ttu-id="26bbd-135">Especifica o nome da configuração de regra que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="26bbd-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="26bbd-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="26bbd-136">-Protocol</span></span>
<span data-ttu-id="26bbd-137">Especifica um protocolo.</span><span class="sxs-lookup"><span data-stu-id="26bbd-137">Specifies a protocol.</span></span>
<span data-ttu-id="26bbd-138">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="26bbd-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26bbd-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="26bbd-139">Tcp</span></span>
- <span data-ttu-id="26bbd-140">Udp</span><span class="sxs-lookup"><span data-stu-id="26bbd-140">Udp</span></span>

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

### <span data-ttu-id="26bbd-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="26bbd-141">-Confirm</span></span>
<span data-ttu-id="26bbd-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26bbd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26bbd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26bbd-143">-WhatIf</span></span>
<span data-ttu-id="26bbd-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="26bbd-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26bbd-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26bbd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26bbd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26bbd-146">CommonParameters</span></span>
<span data-ttu-id="26bbd-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26bbd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26bbd-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26bbd-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26bbd-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="26bbd-149">INPUTS</span></span>

### <span data-ttu-id="26bbd-150">System.String</span><span class="sxs-lookup"><span data-stu-id="26bbd-150">System.String</span></span>

### <span data-ttu-id="26bbd-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="26bbd-151">System.Int32</span></span>

### <span data-ttu-id="26bbd-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="26bbd-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="26bbd-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="26bbd-153">OUTPUTS</span></span>

### <span data-ttu-id="26bbd-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="26bbd-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="26bbd-155">Notas</span><span class="sxs-lookup"><span data-stu-id="26bbd-155">NOTES</span></span>

## <span data-ttu-id="26bbd-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26bbd-156">RELATED LINKS</span></span>

[<span data-ttu-id="26bbd-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26bbd-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="26bbd-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26bbd-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="26bbd-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="26bbd-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="26bbd-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="26bbd-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="26bbd-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26bbd-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="26bbd-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26bbd-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


