---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283876"
---
# <span data-ttu-id="1a848-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="1a848-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="1a848-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a848-102">SYNOPSIS</span></span>
<span data-ttu-id="1a848-103">Criar uma nova regra de NAT da política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="1a848-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="1a848-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a848-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a848-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a848-105">DESCRIPTION</span></span>
<span data-ttu-id="1a848-106">O cmdlet **New-AzFirewallPolicyNatRule** cria uma regra NAT para uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a848-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="1a848-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a848-107">EXAMPLES</span></span>

### <span data-ttu-id="1a848-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1a848-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="1a848-109">Este exemplo cria uma regra NAT com o endereço de origem, o protocolo, o endereço de destino, a porta de destino, o endereço traduzido e a porta traduzida.</span><span class="sxs-lookup"><span data-stu-id="1a848-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="1a848-110">OS</span><span class="sxs-lookup"><span data-stu-id="1a848-110">PARAMETERS</span></span>

### <span data-ttu-id="1a848-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a848-111">-DefaultProfile</span></span>
<span data-ttu-id="1a848-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a848-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a848-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a848-113">-Name</span></span>
<span data-ttu-id="1a848-114">O nome da coleção de regras NAT</span><span class="sxs-lookup"><span data-stu-id="1a848-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="1a848-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="1a848-115">-Description</span></span>
<span data-ttu-id="1a848-116">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="1a848-116">The description of the rule</span></span>

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

### <span data-ttu-id="1a848-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="1a848-117">-DestinationAddress</span></span>
<span data-ttu-id="1a848-118">Os endereços de destino da regra.</span><span class="sxs-lookup"><span data-stu-id="1a848-118">The destination addresses of the rule.</span></span> <span data-ttu-id="1a848-119">Isso deve ser um IP público do firewall.</span><span class="sxs-lookup"><span data-stu-id="1a848-119">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="1a848-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="1a848-120">-DestinationPort</span></span>
<span data-ttu-id="1a848-121">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="1a848-121">The destination ports of the rule</span></span>

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

### <span data-ttu-id="1a848-122">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="1a848-122">-Protocols</span></span>
<span data-ttu-id="1a848-123">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="1a848-123">The protocols of the rule</span></span>

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

### <span data-ttu-id="1a848-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="1a848-124">-SourceAddress</span></span>
<span data-ttu-id="1a848-125">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="1a848-125">The source addresses of the rule</span></span>

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

### <span data-ttu-id="1a848-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="1a848-126">-SourceIpGroup</span></span>
<span data-ttu-id="1a848-127">O ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="1a848-127">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="1a848-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="1a848-128">-TranslatedAddress</span></span>
<span data-ttu-id="1a848-129">O endereço traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="1a848-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="1a848-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="1a848-130">-TranslatedPort</span></span>
<span data-ttu-id="1a848-131">A porta traduzida para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="1a848-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="1a848-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a848-132">-Confirm</span></span>
<span data-ttu-id="1a848-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a848-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a848-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a848-134">-WhatIf</span></span>
<span data-ttu-id="1a848-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a848-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a848-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a848-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a848-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a848-137">CommonParameters</span></span>
<span data-ttu-id="1a848-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a848-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a848-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a848-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a848-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a848-140">INPUTS</span></span>

### <span data-ttu-id="1a848-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1a848-141">None</span></span>

## <span data-ttu-id="1a848-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a848-142">OUTPUTS</span></span>

### <span data-ttu-id="1a848-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="1a848-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="1a848-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a848-144">NOTES</span></span>

## <span data-ttu-id="1a848-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a848-145">RELATED LINKS</span></span>
