---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112844"
---
# <span data-ttu-id="4621e-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4621e-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="4621e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4621e-102">SYNOPSIS</span></span>
<span data-ttu-id="4621e-103">Cria uma Regra de Rede de Firewall.</span><span class="sxs-lookup"><span data-stu-id="4621e-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="4621e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4621e-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4621e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4621e-105">DESCRIPTION</span></span>
<span data-ttu-id="4621e-106">O cmdlet **New-AzFirewallNetworkRule** cria uma regra de rede para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="4621e-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="4621e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4621e-107">EXAMPLES</span></span>

### <span data-ttu-id="4621e-108">Exemplo 1: Criar uma regra para todo o tráfego TCP</span><span class="sxs-lookup"><span data-stu-id="4621e-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="4621e-109">Este exemplo cria uma regra para todo o tráfego TCP.</span><span class="sxs-lookup"><span data-stu-id="4621e-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="4621e-110">O usuário impõe se o tráfego será permitido ou negado para uma regra com base no conjunto de regras a que ele está associado.</span><span class="sxs-lookup"><span data-stu-id="4621e-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4621e-111">Exemplo 2: Criar uma regra para todo o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="4621e-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="4621e-112">Este exemplo cria uma regra para todo o tráfego TCP de 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4621e-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4621e-113">O usuário impõe se o tráfego será permitido ou negado para uma regra com base no conjunto de regras a que ele está associado.</span><span class="sxs-lookup"><span data-stu-id="4621e-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4621e-114">Exemplo 3: Criar uma regra para todo o tráfego TCP e ICMP de qualquer fonte para 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="4621e-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="4621e-115">Este exemplo cria uma regra para todo o tráfego TCP de qualquer fonte para 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="4621e-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="4621e-116">O usuário impõe se o tráfego será permitido ou negado para uma regra com base no conjunto de regras a que ele está associado.</span><span class="sxs-lookup"><span data-stu-id="4621e-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="4621e-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4621e-117">PARAMETERS</span></span>

### <span data-ttu-id="4621e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4621e-118">-DefaultProfile</span></span>
<span data-ttu-id="4621e-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4621e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4621e-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4621e-120">-Description</span></span>
<span data-ttu-id="4621e-121">Especifica uma descrição opcional dessa regra.</span><span class="sxs-lookup"><span data-stu-id="4621e-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="4621e-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4621e-122">-DestinationAddress</span></span>
<span data-ttu-id="4621e-123">Os endereços de destino da regra</span><span class="sxs-lookup"><span data-stu-id="4621e-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="4621e-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="4621e-124">-DestinationFqdn</span></span>
<span data-ttu-id="4621e-125">O FQDN de destino da regra</span><span class="sxs-lookup"><span data-stu-id="4621e-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="4621e-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="4621e-126">-DestinationIpGroup</span></span>
<span data-ttu-id="4621e-127">O grupo ipgroup de destino da regra</span><span class="sxs-lookup"><span data-stu-id="4621e-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="4621e-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4621e-128">-DestinationPort</span></span>
<span data-ttu-id="4621e-129">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="4621e-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="4621e-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="4621e-130">-Name</span></span>
<span data-ttu-id="4621e-131">Especifica o nome desta regra de rede.</span><span class="sxs-lookup"><span data-stu-id="4621e-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="4621e-132">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="4621e-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="4621e-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="4621e-133">-Protocol</span></span>
<span data-ttu-id="4621e-134">Especifica o tipo de tráfego a ser filtrado por esta regra.</span><span class="sxs-lookup"><span data-stu-id="4621e-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="4621e-135">Os valores possíveis são TCP, UDP, ICMP e Any.</span><span class="sxs-lookup"><span data-stu-id="4621e-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="4621e-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="4621e-136">-SourceAddress</span></span>
<span data-ttu-id="4621e-137">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="4621e-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="4621e-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="4621e-138">-SourceIpGroup</span></span>
<span data-ttu-id="4621e-139">O grupo ipgroup de origem da regra</span><span class="sxs-lookup"><span data-stu-id="4621e-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="4621e-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4621e-140">-Confirm</span></span>
<span data-ttu-id="4621e-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4621e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4621e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4621e-142">-WhatIf</span></span>
<span data-ttu-id="4621e-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4621e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4621e-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4621e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4621e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4621e-145">CommonParameters</span></span>
<span data-ttu-id="4621e-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4621e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4621e-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4621e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4621e-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="4621e-148">INPUTS</span></span>

### <span data-ttu-id="4621e-149">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4621e-149">None</span></span>

## <span data-ttu-id="4621e-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="4621e-150">OUTPUTS</span></span>

### <span data-ttu-id="4621e-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4621e-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="4621e-152">Notas</span><span class="sxs-lookup"><span data-stu-id="4621e-152">NOTES</span></span>

## <span data-ttu-id="4621e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4621e-153">RELATED LINKS</span></span>

[<span data-ttu-id="4621e-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4621e-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="4621e-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4621e-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4621e-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4621e-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
