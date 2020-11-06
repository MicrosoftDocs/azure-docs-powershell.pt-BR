---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428467"
---
# <span data-ttu-id="4cd26-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4cd26-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="4cd26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cd26-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd26-103">Cria uma regra de rede de firewall.</span><span class="sxs-lookup"><span data-stu-id="4cd26-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cd26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cd26-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cd26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cd26-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd26-106">O cmdlet **New-AzureRmFirewallNetworkRule** cria uma regra de rede para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd26-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="4cd26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cd26-107">EXAMPLES</span></span>

### <span data-ttu-id="4cd26-108">1: criar uma regra para todo o tráfego de TCP</span><span class="sxs-lookup"><span data-stu-id="4cd26-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="4cd26-109">Este exemplo cria uma regra para todo o tráfego TCP.</span><span class="sxs-lookup"><span data-stu-id="4cd26-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="4cd26-110">O usuário impõe a autorização ou negação do tráfego para uma regra baseada na coleção de regras à qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4cd26-111">2: criar uma regra para todo o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="4cd26-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="4cd26-112">Este exemplo cria uma regra para todo o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4cd26-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4cd26-113">O usuário impõe a autorização ou negação do tráfego para uma regra baseada na coleção de regras à qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4cd26-114">3: criar uma regra para todo o tráfego de TCP e ICMP de qualquer fonte para 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="4cd26-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="4cd26-115">Este exemplo cria uma regra para todo o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4cd26-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4cd26-116">O usuário impõe a autorização ou negação do tráfego para uma regra baseada na coleção de regras à qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="4cd26-117">OS</span><span class="sxs-lookup"><span data-stu-id="4cd26-117">PARAMETERS</span></span>

### <span data-ttu-id="4cd26-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd26-118">-DefaultProfile</span></span>
<span data-ttu-id="4cd26-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd26-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cd26-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4cd26-120">-Description</span></span>
<span data-ttu-id="4cd26-121">Especifica uma descrição opcional desta regra.</span><span class="sxs-lookup"><span data-stu-id="4cd26-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4cd26-122">-DestinationAddress</span></span>
<span data-ttu-id="4cd26-123">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="4cd26-123">The destination addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4cd26-124">-DestinationPort</span></span>
<span data-ttu-id="4cd26-125">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="4cd26-125">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cd26-126">-Name</span></span>
<span data-ttu-id="4cd26-127">Especifica o nome desta regra de rede.</span><span class="sxs-lookup"><span data-stu-id="4cd26-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="4cd26-128">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="4cd26-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="4cd26-129">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="4cd26-129">-Protocol</span></span>
<span data-ttu-id="4cd26-130">Especifica o tipo de tráfego a ser filtrado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="4cd26-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="4cd26-131">Os valores possíveis são TCP, UDP, ICMP e any.</span><span class="sxs-lookup"><span data-stu-id="4cd26-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="4cd26-132">-SourceAddress</span></span>
<span data-ttu-id="4cd26-133">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="4cd26-133">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4cd26-134">-Confirm</span></span>
<span data-ttu-id="4cd26-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cd26-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd26-136">-WhatIf</span></span>
<span data-ttu-id="4cd26-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cd26-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd26-139">CommonParameters</span></span>
<span data-ttu-id="4cd26-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd26-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd26-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd26-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd26-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cd26-142">INPUTS</span></span>

### <span data-ttu-id="4cd26-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4cd26-143">None</span></span>
<span data-ttu-id="4cd26-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4cd26-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4cd26-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cd26-145">OUTPUTS</span></span>

### <span data-ttu-id="4cd26-146">Microsoft. Azure. Commands. Network. Models. PSFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4cd26-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="4cd26-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cd26-147">NOTES</span></span>

## <span data-ttu-id="4cd26-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cd26-148">RELATED LINKS</span></span>

[<span data-ttu-id="4cd26-149">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4cd26-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="4cd26-150">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4cd26-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="4cd26-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4cd26-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
