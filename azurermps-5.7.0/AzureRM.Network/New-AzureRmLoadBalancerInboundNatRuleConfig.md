---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 0b974d1d79be82f3c16f1052abe0eecc7fa9ba30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603258"
---
# <span data-ttu-id="3369e-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3369e-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="3369e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3369e-102">SYNOPSIS</span></span>
<span data-ttu-id="3369e-103">Cria uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3369e-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3369e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3369e-104">SYNTAX</span></span>

### <span data-ttu-id="3369e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3369e-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3369e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3369e-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3369e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3369e-107">DESCRIPTION</span></span>
<span data-ttu-id="3369e-108">O cmdlet **New-AzureRmLoadBalancerInboundNatRuleConfig** cria uma configuração de regra NAT (conversão de endereços de rede) de entrada para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="3369e-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="3369e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3369e-109">EXAMPLES</span></span>

### <span data-ttu-id="3369e-110">Exemplo 1: criar uma configuração de regra NAT de entrada para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="3369e-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="3369e-111">O primeiro comando cria um endereço IP público chamado MyPublicIP no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="3369e-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="3369e-112">O segundo comando cria uma configuração de IP de front-end chamada FrontendIpConfig01 usando o endereço IP público no $publicip e, em seguida, armazena-o na variável $frontend.</span><span class="sxs-lookup"><span data-stu-id="3369e-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="3369e-113">O terceiro comando cria uma configuração de regra NAT de entrada chamada MyInboundNatRule usando o objeto front-end no $frontend.</span><span class="sxs-lookup"><span data-stu-id="3369e-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="3369e-114">O protocolo TCP é especificado e a porta de front-end é 3389, a mesma que a porta back-end nesse caso.</span><span class="sxs-lookup"><span data-stu-id="3369e-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="3369e-115">Os parâmetros *FrontendIpConfiguration* , *Procotol* , *FrontendPort* e *BackendPort* são necessários para criar uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="3369e-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="3369e-116">OS</span><span class="sxs-lookup"><span data-stu-id="3369e-116">PARAMETERS</span></span>

### <span data-ttu-id="3369e-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="3369e-117">-BackendPort</span></span>
<span data-ttu-id="3369e-118">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="3369e-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="3369e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3369e-119">-DefaultProfile</span></span>
<span data-ttu-id="3369e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3369e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3369e-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="3369e-121">-EnableFloatingIP</span></span>
<span data-ttu-id="3369e-122">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="3369e-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="3369e-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3369e-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="3369e-124">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3369e-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3369e-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3369e-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="3369e-126">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="3369e-126">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="3369e-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3369e-127">-FrontendPort</span></span>
<span data-ttu-id="3369e-128">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3369e-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3369e-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3369e-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3369e-130">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3369e-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="3369e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="3369e-131">-Name</span></span>
<span data-ttu-id="3369e-132">Especifica o nome da configuração de regra que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="3369e-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3369e-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="3369e-133">-Protocol</span></span>
<span data-ttu-id="3369e-134">Especifica um protocolo.</span><span class="sxs-lookup"><span data-stu-id="3369e-134">Specifies a protocol.</span></span>
<span data-ttu-id="3369e-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3369e-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3369e-136">Protocol</span><span class="sxs-lookup"><span data-stu-id="3369e-136">Tcp</span></span>
- <span data-ttu-id="3369e-137">Grama</span><span class="sxs-lookup"><span data-stu-id="3369e-137">Udp</span></span>

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

### <span data-ttu-id="3369e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3369e-138">CommonParameters</span></span>
<span data-ttu-id="3369e-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3369e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3369e-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3369e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3369e-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3369e-141">INPUTS</span></span>

### <span data-ttu-id="3369e-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3369e-142">None</span></span>
<span data-ttu-id="3369e-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3369e-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3369e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3369e-144">OUTPUTS</span></span>

### <span data-ttu-id="3369e-145">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="3369e-145">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="3369e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3369e-146">NOTES</span></span>

## <span data-ttu-id="3369e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3369e-147">RELATED LINKS</span></span>

[<span data-ttu-id="3369e-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3369e-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3369e-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3369e-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3369e-150">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3369e-150">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3369e-151">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3369e-151">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3369e-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3369e-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="3369e-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3369e-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


