---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428964"
---
# <span data-ttu-id="d5c04-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d5c04-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="d5c04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5c04-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c04-103">Criar uma nova regra de rede de política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d5c04-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="d5c04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5c04-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5c04-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5c04-105">DESCRIPTION</span></span>
<span data-ttu-id="d5c04-106">O cmdlet **New-AzFirewallPolicyNetworkRule** cria uma regra de rede para uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c04-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="d5c04-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5c04-107">EXAMPLES</span></span>

### <span data-ttu-id="d5c04-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5c04-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="d5c04-109">Este exemplo cria uma regra de rede com o endereço de origem, o protocolo, o endereço de destino e a porta de destino</span><span class="sxs-lookup"><span data-stu-id="d5c04-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="d5c04-110">OS</span><span class="sxs-lookup"><span data-stu-id="d5c04-110">PARAMETERS</span></span>

### <span data-ttu-id="d5c04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c04-111">-DefaultProfile</span></span>
<span data-ttu-id="d5c04-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c04-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c04-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d5c04-113">-Description</span></span>
<span data-ttu-id="d5c04-114">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="d5c04-114">The description of the rule</span></span>

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

### <span data-ttu-id="d5c04-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d5c04-115">-DestinationAddress</span></span>
<span data-ttu-id="d5c04-116">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="d5c04-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="d5c04-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="d5c04-117">-DestinationFqdn</span></span>
<span data-ttu-id="d5c04-118">O FQDN de destino da regra</span><span class="sxs-lookup"><span data-stu-id="d5c04-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="d5c04-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="d5c04-119">-DestinationIpGroup</span></span>
<span data-ttu-id="d5c04-120">O ipgroups de destino da regra</span><span class="sxs-lookup"><span data-stu-id="d5c04-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="d5c04-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d5c04-121">-DestinationPort</span></span>
<span data-ttu-id="d5c04-122">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="d5c04-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="d5c04-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5c04-123">-Name</span></span>
<span data-ttu-id="d5c04-124">O nome da regra de rede</span><span class="sxs-lookup"><span data-stu-id="d5c04-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="d5c04-125">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="d5c04-125">-Protocol</span></span>
<span data-ttu-id="d5c04-126">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="d5c04-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="d5c04-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d5c04-127">-SourceAddress</span></span>
<span data-ttu-id="d5c04-128">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="d5c04-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="d5c04-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="d5c04-129">-SourceIpGroup</span></span>
<span data-ttu-id="d5c04-130">O ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="d5c04-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="d5c04-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d5c04-131">-Confirm</span></span>
<span data-ttu-id="d5c04-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5c04-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c04-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c04-133">-WhatIf</span></span>
<span data-ttu-id="d5c04-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5c04-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5c04-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5c04-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c04-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c04-136">CommonParameters</span></span>
<span data-ttu-id="d5c04-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c04-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c04-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5c04-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c04-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5c04-139">INPUTS</span></span>

### <span data-ttu-id="d5c04-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d5c04-140">None</span></span>

## <span data-ttu-id="d5c04-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5c04-141">OUTPUTS</span></span>

### <span data-ttu-id="d5c04-142">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d5c04-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="d5c04-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5c04-143">NOTES</span></span>

## <span data-ttu-id="d5c04-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5c04-144">RELATED LINKS</span></span>
