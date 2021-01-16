---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258529"
---
# <span data-ttu-id="e71a6-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="e71a6-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="e71a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e71a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e71a6-103">Cria uma regra NAT de firewall.</span><span class="sxs-lookup"><span data-stu-id="e71a6-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="e71a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e71a6-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e71a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e71a6-105">DESCRIPTION</span></span>
<span data-ttu-id="e71a6-106">O cmdlet **New-AzFirewallNatRule** cria uma regra NAT para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="e71a6-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="e71a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e71a6-107">EXAMPLES</span></span>

### <span data-ttu-id="e71a6-108">Exemplo 1: criar uma regra para DNAT todo o tráfego TCP de 10.0.0.0/24 com o destino 10.1.2.3:80 para o destino 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="e71a6-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="e71a6-109">Este exemplo cria uma regra que DNAT todo o tráfego originário em 10.0.0.0/24 com o destino 10.1.2.3:80 para 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="e71a6-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="e71a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="e71a6-110">PARAMETERS</span></span>

### <span data-ttu-id="e71a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71a6-111">-DefaultProfile</span></span>
<span data-ttu-id="e71a6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e71a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e71a6-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e71a6-113">-Description</span></span>
<span data-ttu-id="e71a6-114">Especifica uma descrição opcional desta regra.</span><span class="sxs-lookup"><span data-stu-id="e71a6-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="e71a6-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e71a6-115">-DestinationAddress</span></span>
<span data-ttu-id="e71a6-116">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="e71a6-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="e71a6-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e71a6-117">-DestinationPort</span></span>
<span data-ttu-id="e71a6-118">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="e71a6-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="e71a6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e71a6-119">-Name</span></span>
<span data-ttu-id="e71a6-120">Especifica o nome da regra NAT.</span><span class="sxs-lookup"><span data-stu-id="e71a6-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="e71a6-121">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="e71a6-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="e71a6-122">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="e71a6-122">-Protocol</span></span>
<span data-ttu-id="e71a6-123">Especifica o tipo de tráfego a ser filtrado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="e71a6-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="e71a6-124">Os protocolos compatíveis são TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="e71a6-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="e71a6-125">Um valor especial "any" é permitido, o que significa que ele corresponderá tanto ao TCP quanto ao UDP, mas não aos outros protocolos.</span><span class="sxs-lookup"><span data-stu-id="e71a6-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71a6-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e71a6-126">-SourceAddress</span></span>
<span data-ttu-id="e71a6-127">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="e71a6-127">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71a6-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="e71a6-128">-SourceIpGroup</span></span>
<span data-ttu-id="e71a6-129">O ipgroup de origem da regra</span><span class="sxs-lookup"><span data-stu-id="e71a6-129">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71a6-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="e71a6-130">-TranslatedAddress</span></span>
<span data-ttu-id="e71a6-131">Especifica o resultado desejado da tradução de endereço</span><span class="sxs-lookup"><span data-stu-id="e71a6-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="e71a6-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="e71a6-132">-TranslatedFqdn</span></span>
<span data-ttu-id="e71a6-133">O FQDN traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="e71a6-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="e71a6-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="e71a6-134">-TranslatedPort</span></span>
<span data-ttu-id="e71a6-135">Especifica o resultado desejado da tradução de porta</span><span class="sxs-lookup"><span data-stu-id="e71a6-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="e71a6-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e71a6-136">-Confirm</span></span>
<span data-ttu-id="e71a6-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e71a6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e71a6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e71a6-138">-WhatIf</span></span>
<span data-ttu-id="e71a6-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e71a6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e71a6-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e71a6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e71a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71a6-141">CommonParameters</span></span>
<span data-ttu-id="e71a6-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e71a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71a6-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e71a6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71a6-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e71a6-144">INPUTS</span></span>

### <span data-ttu-id="e71a6-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e71a6-145">None</span></span>

## <span data-ttu-id="e71a6-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e71a6-146">OUTPUTS</span></span>

### <span data-ttu-id="e71a6-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="e71a6-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="e71a6-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e71a6-148">NOTES</span></span>

## <span data-ttu-id="e71a6-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e71a6-149">RELATED LINKS</span></span>

[<span data-ttu-id="e71a6-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e71a6-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="e71a6-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e71a6-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="e71a6-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e71a6-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
