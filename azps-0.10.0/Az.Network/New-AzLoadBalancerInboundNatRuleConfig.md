---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 52aad9586840875cf63a27a8f27ff7296d080bd7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775388"
---
# <span data-ttu-id="807de-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="807de-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="807de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="807de-102">SYNOPSIS</span></span>
<span data-ttu-id="807de-103">Cria uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="807de-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="807de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="807de-104">SYNTAX</span></span>

### <span data-ttu-id="807de-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="807de-105">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807de-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="807de-106">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="807de-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="807de-107">DESCRIPTION</span></span>
<span data-ttu-id="807de-108">O cmdlet **New-AzLoadBalancerInboundNatRuleConfig** cria uma configuração de regra NAT (conversão de endereços de rede) de entrada para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="807de-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="807de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="807de-109">EXAMPLES</span></span>

### <span data-ttu-id="807de-110">Exemplo 1: criar uma configuração de regra NAT de entrada para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="807de-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="807de-111">O primeiro comando cria um endereço IP público chamado MyPublicIP no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="807de-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="807de-112">O segundo comando cria uma configuração de IP de front-end chamada FrontendIpConfig01 usando o endereço IP público no $publicip e, em seguida, armazena-o na variável $frontend.</span><span class="sxs-lookup"><span data-stu-id="807de-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="807de-113">O terceiro comando cria uma configuração de regra NAT de entrada chamada MyInboundNatRule usando o objeto front-end no $frontend.</span><span class="sxs-lookup"><span data-stu-id="807de-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="807de-114">O protocolo TCP é especificado e a porta de front-end é 3389, a mesma que a porta back-end nesse caso.</span><span class="sxs-lookup"><span data-stu-id="807de-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="807de-115">Os parâmetros *FrontendIpConfiguration* , *Procotol* , *FrontendPort* e *BackendPort* são necessários para criar uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="807de-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="807de-116">OS</span><span class="sxs-lookup"><span data-stu-id="807de-116">PARAMETERS</span></span>

### <span data-ttu-id="807de-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="807de-117">-BackendPort</span></span>
<span data-ttu-id="807de-118">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="807de-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="807de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807de-119">-DefaultProfile</span></span>
<span data-ttu-id="807de-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="807de-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="807de-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="807de-121">-EnableFloatingIP</span></span>
<span data-ttu-id="807de-122">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="807de-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807de-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="807de-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="807de-124">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="807de-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807de-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="807de-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="807de-126">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="807de-126">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807de-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="807de-127">-FrontendPort</span></span>
<span data-ttu-id="807de-128">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="807de-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="807de-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="807de-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="807de-130">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="807de-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="807de-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="807de-131">-Name</span></span>
<span data-ttu-id="807de-132">Especifica o nome da configuração de regra que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="807de-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="807de-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="807de-133">-Protocol</span></span>
<span data-ttu-id="807de-134">Especifica um protocolo.</span><span class="sxs-lookup"><span data-stu-id="807de-134">Specifies a protocol.</span></span>
<span data-ttu-id="807de-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="807de-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="807de-136">Protocol</span><span class="sxs-lookup"><span data-stu-id="807de-136">Tcp</span></span>
- <span data-ttu-id="807de-137">Grama</span><span class="sxs-lookup"><span data-stu-id="807de-137">Udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807de-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807de-138">CommonParameters</span></span>
<span data-ttu-id="807de-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807de-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807de-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="807de-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807de-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="807de-141">INPUTS</span></span>

## <span data-ttu-id="807de-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="807de-142">OUTPUTS</span></span>

### <span data-ttu-id="807de-143">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="807de-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="807de-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="807de-144">NOTES</span></span>

## <span data-ttu-id="807de-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="807de-145">RELATED LINKS</span></span>

[<span data-ttu-id="807de-146">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="807de-146">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="807de-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="807de-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="807de-148">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="807de-148">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="807de-149">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="807de-149">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="807de-150">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="807de-150">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="807de-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="807de-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


