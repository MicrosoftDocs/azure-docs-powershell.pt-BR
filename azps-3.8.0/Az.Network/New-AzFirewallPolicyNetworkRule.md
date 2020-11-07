---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: b4cbc404139cd56e75f03c5cb19cb9b761576e39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941817"
---
# <span data-ttu-id="78959-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="78959-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="78959-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78959-102">SYNOPSIS</span></span>
<span data-ttu-id="78959-103">Criar uma nova regra de rede de política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="78959-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="78959-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78959-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78959-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78959-105">DESCRIPTION</span></span>
<span data-ttu-id="78959-106">O cmdlet **New-AzFirewallPolicyNetworkRule** cria uma regra de rede para uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="78959-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="78959-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78959-107">EXAMPLES</span></span>

### <span data-ttu-id="78959-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78959-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="78959-109">Este exemplo cria uma regra de rede com o endereço de origem, o protocolo, o endereço de destino e a porta de destino</span><span class="sxs-lookup"><span data-stu-id="78959-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="78959-110">OS</span><span class="sxs-lookup"><span data-stu-id="78959-110">PARAMETERS</span></span>

### <span data-ttu-id="78959-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78959-111">-DefaultProfile</span></span>
<span data-ttu-id="78959-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78959-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78959-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="78959-113">-Description</span></span>
<span data-ttu-id="78959-114">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="78959-114">The description of the rule</span></span>

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

### <span data-ttu-id="78959-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="78959-115">-DestinationAddress</span></span>
<span data-ttu-id="78959-116">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="78959-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="78959-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="78959-117">-DestinationPort</span></span>
<span data-ttu-id="78959-118">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="78959-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="78959-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="78959-119">-Name</span></span>
<span data-ttu-id="78959-120">O nome da regra de rede</span><span class="sxs-lookup"><span data-stu-id="78959-120">The name of the Network Rule</span></span>

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

### <span data-ttu-id="78959-121">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="78959-121">-Protocols</span></span>
<span data-ttu-id="78959-122">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="78959-122">The protocols of the rule</span></span>

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

### <span data-ttu-id="78959-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="78959-123">-SourceAddress</span></span>
<span data-ttu-id="78959-124">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="78959-124">The source addresses of the rule</span></span>

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

### <span data-ttu-id="78959-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78959-125">-Confirm</span></span>
<span data-ttu-id="78959-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78959-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78959-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78959-127">-WhatIf</span></span>
<span data-ttu-id="78959-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78959-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78959-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78959-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78959-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78959-130">CommonParameters</span></span>
<span data-ttu-id="78959-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78959-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78959-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78959-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78959-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78959-133">INPUTS</span></span>

### <span data-ttu-id="78959-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="78959-134">None</span></span>

## <span data-ttu-id="78959-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78959-135">OUTPUTS</span></span>

### <span data-ttu-id="78959-136">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="78959-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="78959-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78959-137">NOTES</span></span>

## <span data-ttu-id="78959-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78959-138">RELATED LINKS</span></span>
