---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 86e15e54a0091839bdce6a66f891c12e6c0376f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892619"
---
# <span data-ttu-id="500bc-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="500bc-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="500bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500bc-102">SYNOPSIS</span></span>
<span data-ttu-id="500bc-103">Criar uma nova regra de rede de política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="500bc-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="500bc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="500bc-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500bc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="500bc-105">DESCRIPTION</span></span>
<span data-ttu-id="500bc-106">O cmdlet **New-AzFirewallPolicyNetworkRule** cria uma regra de rede para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="500bc-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="500bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="500bc-107">EXAMPLES</span></span>

### <span data-ttu-id="500bc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="500bc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="500bc-109">Este exemplo cria uma regra de rede com o endereço de origem, protocolo , endereço de destino e porta de destino</span><span class="sxs-lookup"><span data-stu-id="500bc-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="500bc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="500bc-110">PARAMETERS</span></span>

### <span data-ttu-id="500bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500bc-111">-DefaultProfile</span></span>
<span data-ttu-id="500bc-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="500bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-113">-Description</span><span class="sxs-lookup"><span data-stu-id="500bc-113">-Description</span></span>
<span data-ttu-id="500bc-114">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="500bc-114">The description of the rule</span></span>

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

### <span data-ttu-id="500bc-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="500bc-115">-DestinationAddress</span></span>
<span data-ttu-id="500bc-116">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="500bc-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="500bc-117">-DestinationFqdn</span></span>
<span data-ttu-id="500bc-118">O FQDN de destino da regra</span><span class="sxs-lookup"><span data-stu-id="500bc-118">The destination FQDN of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="500bc-119">-DestinationIpGroup</span></span>
<span data-ttu-id="500bc-120">Os grupos ipgroups de destino da regra</span><span class="sxs-lookup"><span data-stu-id="500bc-120">The destination ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="500bc-121">-DestinationPort</span></span>
<span data-ttu-id="500bc-122">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="500bc-122">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="500bc-123">-Name</span></span>
<span data-ttu-id="500bc-124">O nome da Regra de Rede</span><span class="sxs-lookup"><span data-stu-id="500bc-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="500bc-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="500bc-125">-Protocol</span></span>
<span data-ttu-id="500bc-126">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="500bc-126">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="500bc-127">-SourceAddress</span></span>
<span data-ttu-id="500bc-128">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="500bc-128">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="500bc-129">-SourceIpGroup</span></span>
<span data-ttu-id="500bc-130">Os grupos ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="500bc-130">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="500bc-131">-Confirm</span></span>
<span data-ttu-id="500bc-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="500bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500bc-133">-WhatIf</span></span>
<span data-ttu-id="500bc-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="500bc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500bc-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="500bc-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500bc-136">CommonParameters</span></span>
<span data-ttu-id="500bc-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500bc-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="500bc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500bc-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="500bc-139">INPUTS</span></span>

### <span data-ttu-id="500bc-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="500bc-140">None</span></span>

## <span data-ttu-id="500bc-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="500bc-141">OUTPUTS</span></span>

### <span data-ttu-id="500bc-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="500bc-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="500bc-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="500bc-143">NOTES</span></span>

## <span data-ttu-id="500bc-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="500bc-144">RELATED LINKS</span></span>
