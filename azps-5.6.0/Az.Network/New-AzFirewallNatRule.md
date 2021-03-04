---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: 2bbac9bebd79f1ca51a7defd4c57589764b2c34e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889636"
---
# <span data-ttu-id="20dc4-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="20dc4-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="20dc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="20dc4-103">Cria uma regra NAT do Firewall.</span><span class="sxs-lookup"><span data-stu-id="20dc4-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="20dc4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20dc4-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20dc4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="20dc4-106">O cmdlet **New-AzFirewallNatRule** cria uma regra NAT para Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="20dc4-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="20dc4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="20dc4-108">Exemplo 1: Criar uma regra para DNAT todo o tráfego TCP a partir de 10.0.0.0/24 com destino 10.1.2.3:80 para o destino 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="20dc4-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="20dc4-109">Este exemplo cria uma regra que fará o DNAT todo o tráfego originado em 10.0.0.0/24 com destino 10.1.2.3:80 a 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="20dc4-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="20dc4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="20dc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20dc4-111">-DefaultProfile</span></span>
<span data-ttu-id="20dc4-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="20dc4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20dc4-113">-Description</span><span class="sxs-lookup"><span data-stu-id="20dc4-113">-Description</span></span>
<span data-ttu-id="20dc4-114">Especifica uma descrição opcional dessa regra.</span><span class="sxs-lookup"><span data-stu-id="20dc4-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="20dc4-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="20dc4-115">-DestinationAddress</span></span>
<span data-ttu-id="20dc4-116">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="20dc4-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="20dc4-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="20dc4-117">-DestinationPort</span></span>
<span data-ttu-id="20dc4-118">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="20dc4-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="20dc4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="20dc4-119">-Name</span></span>
<span data-ttu-id="20dc4-120">Especifica o nome dessa regra NAT.</span><span class="sxs-lookup"><span data-stu-id="20dc4-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="20dc4-121">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="20dc4-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="20dc4-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="20dc4-122">-Protocol</span></span>
<span data-ttu-id="20dc4-123">Especifica o tipo de tráfego a ser filtrado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="20dc4-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="20dc4-124">Os protocolos com suporte são TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="20dc4-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="20dc4-125">Um valor especial "Any" é permitido, o que significa que ele corresponderá ao TCP e ao UDP, mas não a outros protocolos.</span><span class="sxs-lookup"><span data-stu-id="20dc4-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="20dc4-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="20dc4-126">-SourceAddress</span></span>
<span data-ttu-id="20dc4-127">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="20dc4-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="20dc4-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="20dc4-128">-SourceIpGroup</span></span>
<span data-ttu-id="20dc4-129">O grupo ipgroup de origem da regra</span><span class="sxs-lookup"><span data-stu-id="20dc4-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="20dc4-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="20dc4-130">-TranslatedAddress</span></span>
<span data-ttu-id="20dc4-131">Especifica o resultado desejado da conversão de endereços</span><span class="sxs-lookup"><span data-stu-id="20dc4-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="20dc4-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="20dc4-132">-TranslatedFqdn</span></span>
<span data-ttu-id="20dc4-133">O FQDN convertido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="20dc4-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="20dc4-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="20dc4-134">-TranslatedPort</span></span>
<span data-ttu-id="20dc4-135">Especifica o resultado desejado da conversão de porta</span><span class="sxs-lookup"><span data-stu-id="20dc4-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="20dc4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20dc4-136">-Confirm</span></span>
<span data-ttu-id="20dc4-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20dc4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20dc4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20dc4-138">-WhatIf</span></span>
<span data-ttu-id="20dc4-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20dc4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20dc4-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20dc4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20dc4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20dc4-141">CommonParameters</span></span>
<span data-ttu-id="20dc4-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20dc4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20dc4-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20dc4-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20dc4-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20dc4-144">INPUTS</span></span>

### <span data-ttu-id="20dc4-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20dc4-145">None</span></span>

## <span data-ttu-id="20dc4-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20dc4-146">OUTPUTS</span></span>

### <span data-ttu-id="20dc4-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="20dc4-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="20dc4-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="20dc4-148">NOTES</span></span>

## <span data-ttu-id="20dc4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20dc4-149">RELATED LINKS</span></span>

[<span data-ttu-id="20dc4-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="20dc4-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="20dc4-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="20dc4-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="20dc4-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="20dc4-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
