---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: cc3ef8146d7a8ba9f5deb9ad65cf6fcc2dd6ac5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771634"
---
# <span data-ttu-id="f8d3f-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f8d3f-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="f8d3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d3f-103">Cria uma regra de aplicativo de firewall.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="f8d3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8d3f-104">SYNTAX</span></span>

### <span data-ttu-id="f8d3f-105">TargetFqdn (padrão)</span><span class="sxs-lookup"><span data-stu-id="f8d3f-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8d3f-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="f8d3f-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d3f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8d3f-107">DESCRIPTION</span></span>
<span data-ttu-id="f8d3f-108">O cmdlet **New-AzFirewallApplicationRule** cria uma regra de aplicativo para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="f8d3f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8d3f-109">EXAMPLES</span></span>

### <span data-ttu-id="f8d3f-110">1: criar uma regra para permitir todo o tráfego HTTPS de 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="f8d3f-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="f8d3f-111">Este exemplo cria uma regra que permitirá que todo o tráfego HTTPS na porta 443 de 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="f8d3f-112">2: criar uma regra para permitir o WindowsUpdate para a sub-rede 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="f8d3f-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="f8d3f-113">Este exemplo cria uma regra que permitirá o tráfego de atualizações do Windows para domínio 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="f8d3f-114">OS</span><span class="sxs-lookup"><span data-stu-id="f8d3f-114">PARAMETERS</span></span>

### <span data-ttu-id="f8d3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d3f-115">-DefaultProfile</span></span>
<span data-ttu-id="f8d3f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8d3f-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f8d3f-117">-Description</span></span>
<span data-ttu-id="f8d3f-118">Especifica uma descrição opcional desta regra.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="f8d3f-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="f8d3f-119">-FqdnTag</span></span>
<span data-ttu-id="f8d3f-120">Especifica uma lista de marcas de FQDN para esta regra.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="f8d3f-121">As marcas disponíveis podem ser recuperadas usando o cmdlet [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="f8d3f-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d3f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8d3f-122">-Name</span></span>
<span data-ttu-id="f8d3f-123">Especifica o nome desta regra de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="f8d3f-124">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="f8d3f-125">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f8d3f-125">-Protocol</span></span>
<span data-ttu-id="f8d3f-126">Especifica o tipo de tráfego a ser filtrado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="f8d3f-127">O formato é <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="f8d3f-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="f8d3f-128">Por exemplo, "http: 80" ou "https: 443".</span><span class="sxs-lookup"><span data-stu-id="f8d3f-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="f8d3f-129">O protocolo é obrigatório quando TargetFqdn é usado, mas não pode ser usado com FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="f8d3f-130">Os protocolos com suporte são HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d3f-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f8d3f-131">-SourceAddress</span></span>
<span data-ttu-id="f8d3f-132">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="f8d3f-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="f8d3f-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="f8d3f-133">-TargetFqdn</span></span>
<span data-ttu-id="f8d3f-134">Especifica uma lista de nomes de domínio filtrados por essa regra.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="f8d3f-135">O caractere de asterisco ' *', é aceito apenas como o primeiro caractere de um FQDN na lista. Quando usado, o asterisco corresponde a qualquer número de caracteres. (por exemplo, '* MSN.com ' corresponderá MSN.com e todos os seus subdomínios)</span><span class="sxs-lookup"><span data-stu-id="f8d3f-135">The asterisk character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d3f-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f8d3f-136">-Confirm</span></span>
<span data-ttu-id="f8d3f-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d3f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d3f-138">-WhatIf</span></span>
<span data-ttu-id="f8d3f-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d3f-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d3f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d3f-141">CommonParameters</span></span>
<span data-ttu-id="f8d3f-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8d3f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d3f-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d3f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d3f-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8d3f-144">INPUTS</span></span>

### <span data-ttu-id="f8d3f-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f8d3f-145">None</span></span>

## <span data-ttu-id="f8d3f-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8d3f-146">OUTPUTS</span></span>

### <span data-ttu-id="f8d3f-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f8d3f-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="f8d3f-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8d3f-148">NOTES</span></span>

## <span data-ttu-id="f8d3f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8d3f-149">RELATED LINKS</span></span>

[<span data-ttu-id="f8d3f-150">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f8d3f-150">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="f8d3f-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f8d3f-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f8d3f-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f8d3f-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="f8d3f-153">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="f8d3f-153">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
