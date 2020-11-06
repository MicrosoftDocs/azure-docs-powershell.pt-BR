---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431354"
---
# <span data-ttu-id="3e95e-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="3e95e-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="3e95e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e95e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e95e-103">Cria uma regra NAT de firewall.</span><span class="sxs-lookup"><span data-stu-id="3e95e-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e95e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e95e-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e95e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e95e-105">DESCRIPTION</span></span>
<span data-ttu-id="3e95e-106">O cmdlet **New-AzureRmFirewallNatRule** cria uma regra NAT para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e95e-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="3e95e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e95e-107">EXAMPLES</span></span>

### <span data-ttu-id="3e95e-108">1: Crie uma regra para DNAT todo o tráfego TCP de 10.0.0.0/24 com o destino 10.1.2.3:80 para o destino 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="3e95e-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="3e95e-109">Este exemplo cria uma regra que DNAT todo o tráfego originário em 10.0.0.0/24 com o destino 10.1.2.3:80 para 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="3e95e-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="3e95e-110">OS</span><span class="sxs-lookup"><span data-stu-id="3e95e-110">PARAMETERS</span></span>

### <span data-ttu-id="3e95e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e95e-111">-DefaultProfile</span></span>
<span data-ttu-id="3e95e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e95e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e95e-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3e95e-113">-Description</span></span>
<span data-ttu-id="3e95e-114">Especifica uma descrição opcional desta regra.</span><span class="sxs-lookup"><span data-stu-id="3e95e-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="3e95e-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3e95e-115">-DestinationAddress</span></span>
<span data-ttu-id="3e95e-116">Os endereços de destino da regra.</span><span class="sxs-lookup"><span data-stu-id="3e95e-116">The destination addresses of the rule.</span></span>

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

### <span data-ttu-id="3e95e-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3e95e-117">-DestinationPort</span></span>
<span data-ttu-id="3e95e-118">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="3e95e-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="3e95e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e95e-119">-Name</span></span>
<span data-ttu-id="3e95e-120">Especifica o nome da regra NAT.</span><span class="sxs-lookup"><span data-stu-id="3e95e-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="3e95e-121">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="3e95e-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="3e95e-122">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="3e95e-122">-Protocol</span></span>
<span data-ttu-id="3e95e-123">Especifica o tipo de tráfego a ser filtrado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="3e95e-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="3e95e-124">Os protocolos compatíveis são TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="3e95e-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="3e95e-125">Um valor especial "any" é permitido, o que significa que ele corresponderá tanto ao TCP quanto ao UDP, mas não aos outros protocolos.</span><span class="sxs-lookup"><span data-stu-id="3e95e-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e95e-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="3e95e-126">-SourceAddress</span></span>
<span data-ttu-id="3e95e-127">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="3e95e-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="3e95e-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="3e95e-128">-TranslatedAddress</span></span>
<span data-ttu-id="3e95e-129">Especifica o resultado desejado da tradução de endereço</span><span class="sxs-lookup"><span data-stu-id="3e95e-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="3e95e-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="3e95e-130">-TranslatedPort</span></span>
<span data-ttu-id="3e95e-131">Especifica o resultado desejado da tradução de porta</span><span class="sxs-lookup"><span data-stu-id="3e95e-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="3e95e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e95e-132">-Confirm</span></span>
<span data-ttu-id="3e95e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e95e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e95e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e95e-134">-WhatIf</span></span>
<span data-ttu-id="3e95e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e95e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e95e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e95e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e95e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e95e-137">CommonParameters</span></span>
<span data-ttu-id="3e95e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e95e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e95e-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e95e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e95e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e95e-140">INPUTS</span></span>

### <span data-ttu-id="3e95e-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3e95e-141">None</span></span>
<span data-ttu-id="3e95e-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3e95e-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e95e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e95e-143">OUTPUTS</span></span>

### <span data-ttu-id="3e95e-144">Microsoft. Azure. Commands. Network. Models. PSFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="3e95e-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="3e95e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e95e-145">NOTES</span></span>

## <span data-ttu-id="3e95e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e95e-146">RELATED LINKS</span></span>

[<span data-ttu-id="3e95e-147">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3e95e-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="3e95e-148">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3e95e-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="3e95e-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3e95e-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
