---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118321"
---
# <span data-ttu-id="1abec-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="1abec-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="1abec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1abec-102">SYNOPSIS</span></span>
<span data-ttu-id="1abec-103">Cria uma Regra NAT de Firewall.</span><span class="sxs-lookup"><span data-stu-id="1abec-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="1abec-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1abec-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1abec-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1abec-105">DESCRIPTION</span></span>
<span data-ttu-id="1abec-106">O cmdlet **New-AzFirewallNatRule** cria uma regra NAT para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="1abec-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="1abec-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1abec-107">EXAMPLES</span></span>

### <span data-ttu-id="1abec-108">Exemplo 1: Criar uma regra para GERART todo o tráfego TCP a partir de 10.0.0.0/24 com destino 10.1.2.3:80 até o destino 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="1abec-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="1abec-109">Este exemplo cria uma regra que irá gerar todo o tráfego originado em 10.0.0.0/24 com destino 10.1.2.3:80 a 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="1abec-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="1abec-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1abec-110">PARAMETERS</span></span>

### <span data-ttu-id="1abec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abec-111">-DefaultProfile</span></span>
<span data-ttu-id="1abec-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1abec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1abec-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="1abec-113">-Description</span></span>
<span data-ttu-id="1abec-114">Especifica uma descrição opcional dessa regra.</span><span class="sxs-lookup"><span data-stu-id="1abec-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="1abec-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="1abec-115">-DestinationAddress</span></span>
<span data-ttu-id="1abec-116">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="1abec-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="1abec-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="1abec-117">-DestinationPort</span></span>
<span data-ttu-id="1abec-118">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="1abec-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="1abec-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1abec-119">-Name</span></span>
<span data-ttu-id="1abec-120">Especifica o nome desta regra NAT.</span><span class="sxs-lookup"><span data-stu-id="1abec-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="1abec-121">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="1abec-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="1abec-122">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="1abec-122">-Protocol</span></span>
<span data-ttu-id="1abec-123">Especifica o tipo de tráfego a ser filtrado por esta regra.</span><span class="sxs-lookup"><span data-stu-id="1abec-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="1abec-124">Os protocolos com suporte são TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="1abec-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="1abec-125">Um valor especial "Qualquer" é permitido, o que significa que ele corresponderá ao TCP e ao UDP, mas não a outros protocolos.</span><span class="sxs-lookup"><span data-stu-id="1abec-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="1abec-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="1abec-126">-SourceAddress</span></span>
<span data-ttu-id="1abec-127">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="1abec-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="1abec-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="1abec-128">-SourceIpGroup</span></span>
<span data-ttu-id="1abec-129">O grupo ipgroup de origem da regra</span><span class="sxs-lookup"><span data-stu-id="1abec-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="1abec-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="1abec-130">-TranslatedAddress</span></span>
<span data-ttu-id="1abec-131">Especifica o resultado desejado da tradução de endereço</span><span class="sxs-lookup"><span data-stu-id="1abec-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="1abec-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="1abec-132">-TranslatedFqdn</span></span>
<span data-ttu-id="1abec-133">O FQDN traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="1abec-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="1abec-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="1abec-134">-TranslatedPort</span></span>
<span data-ttu-id="1abec-135">Especifica o resultado desejado da tradução da porta</span><span class="sxs-lookup"><span data-stu-id="1abec-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="1abec-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1abec-136">-Confirm</span></span>
<span data-ttu-id="1abec-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1abec-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1abec-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1abec-138">-WhatIf</span></span>
<span data-ttu-id="1abec-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1abec-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1abec-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1abec-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1abec-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abec-141">CommonParameters</span></span>
<span data-ttu-id="1abec-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1abec-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abec-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1abec-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abec-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="1abec-144">INPUTS</span></span>

### <span data-ttu-id="1abec-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1abec-145">None</span></span>

## <span data-ttu-id="1abec-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="1abec-146">OUTPUTS</span></span>

### <span data-ttu-id="1abec-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="1abec-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="1abec-148">Notas</span><span class="sxs-lookup"><span data-stu-id="1abec-148">NOTES</span></span>

## <span data-ttu-id="1abec-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1abec-149">RELATED LINKS</span></span>

[<span data-ttu-id="1abec-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1abec-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="1abec-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1abec-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="1abec-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1abec-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
