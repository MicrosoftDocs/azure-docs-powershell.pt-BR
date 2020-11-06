---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 06cac261d368dfafa19b96b42945ed9cda613122
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600336"
---
# <span data-ttu-id="a336e-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a336e-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="a336e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a336e-102">SYNOPSIS</span></span>
<span data-ttu-id="a336e-103">Cria uma regra de rede de firewall.</span><span class="sxs-lookup"><span data-stu-id="a336e-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="a336e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a336e-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a336e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a336e-105">DESCRIPTION</span></span>
<span data-ttu-id="a336e-106">O cmdlet **New-AzFirewallNetworkRule** cria uma regra de rede para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="a336e-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="a336e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a336e-107">EXAMPLES</span></span>

### <span data-ttu-id="a336e-108">1: criar uma regra para todo o tráfego de TCP</span><span class="sxs-lookup"><span data-stu-id="a336e-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="a336e-109">Este exemplo cria uma regra para todo o tráfego TCP.</span><span class="sxs-lookup"><span data-stu-id="a336e-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="a336e-110">O usuário impõe a autorização ou negação do tráfego para uma regra baseada na coleção de regras à qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="a336e-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="a336e-111">2: criar uma regra para todo o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="a336e-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="a336e-112">Este exemplo cria uma regra para todo o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="a336e-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="a336e-113">O usuário impõe a autorização ou negação do tráfego para uma regra baseada na coleção de regras à qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="a336e-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="a336e-114">3: criar uma regra para todo o tráfego de TCP e ICMP de qualquer fonte para 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="a336e-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="a336e-115">Este exemplo cria uma regra para todo o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="a336e-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="a336e-116">O usuário impõe a autorização ou negação do tráfego para uma regra baseada na coleção de regras à qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="a336e-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="a336e-117">OS</span><span class="sxs-lookup"><span data-stu-id="a336e-117">PARAMETERS</span></span>

### <span data-ttu-id="a336e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a336e-118">-DefaultProfile</span></span>
<span data-ttu-id="a336e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a336e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a336e-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a336e-120">-Description</span></span>
<span data-ttu-id="a336e-121">Especifica uma descrição opcional desta regra.</span><span class="sxs-lookup"><span data-stu-id="a336e-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="a336e-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a336e-122">-DestinationAddress</span></span>
<span data-ttu-id="a336e-123">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="a336e-123">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a336e-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a336e-124">-DestinationPort</span></span>
<span data-ttu-id="a336e-125">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="a336e-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a336e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a336e-126">-Name</span></span>
<span data-ttu-id="a336e-127">Especifica o nome desta regra de rede.</span><span class="sxs-lookup"><span data-stu-id="a336e-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="a336e-128">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="a336e-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="a336e-129">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="a336e-129">-Protocol</span></span>
<span data-ttu-id="a336e-130">Especifica o tipo de tráfego a ser filtrado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="a336e-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="a336e-131">Os valores possíveis são TCP, UDP, ICMP e any.</span><span class="sxs-lookup"><span data-stu-id="a336e-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a336e-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="a336e-132">-SourceAddress</span></span>
<span data-ttu-id="a336e-133">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="a336e-133">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a336e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a336e-134">-Confirm</span></span>
<span data-ttu-id="a336e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a336e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a336e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a336e-136">-WhatIf</span></span>
<span data-ttu-id="a336e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a336e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a336e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a336e-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a336e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a336e-139">CommonParameters</span></span>
<span data-ttu-id="a336e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a336e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a336e-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a336e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a336e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a336e-142">INPUTS</span></span>

### <span data-ttu-id="a336e-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a336e-143">None</span></span>

## <span data-ttu-id="a336e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a336e-144">OUTPUTS</span></span>

### <span data-ttu-id="a336e-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a336e-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="a336e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a336e-146">NOTES</span></span>

## <span data-ttu-id="a336e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a336e-147">RELATED LINKS</span></span>

[<span data-ttu-id="a336e-148">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a336e-148">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="a336e-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a336e-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a336e-150">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a336e-150">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
