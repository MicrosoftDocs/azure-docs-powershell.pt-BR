---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610558"
---
# <span data-ttu-id="96306-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="96306-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="96306-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96306-102">SYNOPSIS</span></span>
<span data-ttu-id="96306-103">Cria uma regra de aplicativo de firewall.</span><span class="sxs-lookup"><span data-stu-id="96306-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96306-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96306-104">SYNTAX</span></span>

### <span data-ttu-id="96306-105">TargetFqdn (padrão)</span><span class="sxs-lookup"><span data-stu-id="96306-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96306-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="96306-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96306-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96306-107">DESCRIPTION</span></span>
<span data-ttu-id="96306-108">O cmdlet **New-AzureRmFirewallApplicationRule** cria uma regra de aplicativo para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="96306-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="96306-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96306-109">EXAMPLES</span></span>

### <span data-ttu-id="96306-110">1: criar uma regra para permitir todo o tráfego HTTPS de 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="96306-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="96306-111">Este exemplo cria uma regra que permitirá que todo o tráfego HTTPS na porta 443 de 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="96306-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="96306-112">2: criar uma regra para permitir o WindowsUpdate para a sub-rede 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="96306-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="96306-113">Este exemplo cria uma regra que permitirá o tráfego de atualizações do Windows para domínio 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="96306-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="96306-114">OS</span><span class="sxs-lookup"><span data-stu-id="96306-114">PARAMETERS</span></span>

### <span data-ttu-id="96306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96306-115">-DefaultProfile</span></span>
<span data-ttu-id="96306-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96306-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96306-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="96306-117">-Description</span></span>
<span data-ttu-id="96306-118">Especifica uma descrição opcional desta regra.</span><span class="sxs-lookup"><span data-stu-id="96306-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="96306-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="96306-119">-FqdnTag</span></span>
<span data-ttu-id="96306-120">Especifica uma lista de marcas de FQDN para esta regra.</span><span class="sxs-lookup"><span data-stu-id="96306-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="96306-121">As marcas disponíveis podem ser recuperadas usando o cmdlet [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="96306-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96306-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="96306-122">-Name</span></span>
<span data-ttu-id="96306-123">Especifica o nome desta regra de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96306-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="96306-124">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="96306-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="96306-125">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="96306-125">-Protocol</span></span>
<span data-ttu-id="96306-126">Especifica o tipo de tráfego a ser filtrado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="96306-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="96306-127">O formato é <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="96306-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="96306-128">Por exemplo, "http: 80" ou "https: 443".</span><span class="sxs-lookup"><span data-stu-id="96306-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="96306-129">O protocolo é obrigatório quando TargetFqdn é usado, mas não pode ser usado com FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="96306-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="96306-130">Os protocolos com suporte são HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="96306-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96306-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="96306-131">-SourceAddress</span></span>
<span data-ttu-id="96306-132">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="96306-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96306-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="96306-133">-TargetFqdn</span></span>
<span data-ttu-id="96306-134">Especifica uma lista de nomes de domínio filtrados por essa regra.</span><span class="sxs-lookup"><span data-stu-id="96306-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="96306-135">O caractere asterisco, ' *', é aceito apenas como o primeiro caractere de um FQDN na lista. Quando usado, o asterisco corresponde a qualquer número de caracteres. (por exemplo, '* MSN.com ' corresponderá MSN.com e todos os seus subdomínios)</span><span class="sxs-lookup"><span data-stu-id="96306-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96306-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="96306-136">-Confirm</span></span>
<span data-ttu-id="96306-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96306-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96306-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96306-138">-WhatIf</span></span>
<span data-ttu-id="96306-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96306-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96306-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96306-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96306-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96306-141">CommonParameters</span></span>
<span data-ttu-id="96306-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96306-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96306-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96306-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96306-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96306-144">INPUTS</span></span>

### <span data-ttu-id="96306-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="96306-145">None</span></span>
<span data-ttu-id="96306-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="96306-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96306-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96306-147">OUTPUTS</span></span>

### <span data-ttu-id="96306-148">Microsoft. Azure. Commands. Network. Models. PSFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="96306-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="96306-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96306-149">NOTES</span></span>

## <span data-ttu-id="96306-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96306-150">RELATED LINKS</span></span>

[<span data-ttu-id="96306-151">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="96306-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="96306-152">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="96306-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="96306-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="96306-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="96306-154">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="96306-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)
