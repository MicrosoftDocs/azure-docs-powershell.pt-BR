---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257285"
---
# <span data-ttu-id="55755-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="55755-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="55755-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55755-102">SYNOPSIS</span></span>
<span data-ttu-id="55755-103">Criar uma nova regra de rede de política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="55755-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="55755-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55755-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55755-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55755-105">DESCRIPTION</span></span>
<span data-ttu-id="55755-106">O cmdlet **New-AzFirewallPolicyNetworkRule** cria uma regra de rede para uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="55755-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="55755-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55755-107">EXAMPLES</span></span>

### <span data-ttu-id="55755-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55755-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="55755-109">Este exemplo cria uma regra de rede com o endereço de origem, o protocolo, o endereço de destino e a porta de destino</span><span class="sxs-lookup"><span data-stu-id="55755-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="55755-110">OS</span><span class="sxs-lookup"><span data-stu-id="55755-110">PARAMETERS</span></span>

### <span data-ttu-id="55755-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55755-111">-DefaultProfile</span></span>
<span data-ttu-id="55755-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55755-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55755-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="55755-113">-Description</span></span>
<span data-ttu-id="55755-114">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="55755-114">The description of the rule</span></span>

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

### <span data-ttu-id="55755-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="55755-115">-DestinationAddress</span></span>
<span data-ttu-id="55755-116">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="55755-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="55755-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="55755-117">-DestinationFqdn</span></span>
<span data-ttu-id="55755-118">O FQDN de destino da regra</span><span class="sxs-lookup"><span data-stu-id="55755-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="55755-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="55755-119">-DestinationIpGroup</span></span>
<span data-ttu-id="55755-120">O ipgroups de destino da regra</span><span class="sxs-lookup"><span data-stu-id="55755-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="55755-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="55755-121">-DestinationPort</span></span>
<span data-ttu-id="55755-122">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="55755-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="55755-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="55755-123">-Name</span></span>
<span data-ttu-id="55755-124">O nome da regra de rede</span><span class="sxs-lookup"><span data-stu-id="55755-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="55755-125">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="55755-125">-Protocol</span></span>
<span data-ttu-id="55755-126">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="55755-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="55755-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="55755-127">-SourceAddress</span></span>
<span data-ttu-id="55755-128">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="55755-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="55755-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="55755-129">-SourceIpGroup</span></span>
<span data-ttu-id="55755-130">O ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="55755-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="55755-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55755-131">-Confirm</span></span>
<span data-ttu-id="55755-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55755-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55755-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55755-133">-WhatIf</span></span>
<span data-ttu-id="55755-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55755-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55755-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55755-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55755-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55755-136">CommonParameters</span></span>
<span data-ttu-id="55755-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55755-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55755-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55755-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55755-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55755-139">INPUTS</span></span>

### <span data-ttu-id="55755-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="55755-140">None</span></span>

## <span data-ttu-id="55755-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55755-141">OUTPUTS</span></span>

### <span data-ttu-id="55755-142">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="55755-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="55755-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55755-143">NOTES</span></span>

## <span data-ttu-id="55755-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55755-144">RELATED LINKS</span></span>
