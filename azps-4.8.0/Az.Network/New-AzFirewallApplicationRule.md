---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114856"
---
# <span data-ttu-id="40d41-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="40d41-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="40d41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40d41-102">SYNOPSIS</span></span>
<span data-ttu-id="40d41-103">Cria uma regra de aplicativo de firewall.</span><span class="sxs-lookup"><span data-stu-id="40d41-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="40d41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40d41-104">SYNTAX</span></span>

### <span data-ttu-id="40d41-105">TargetFqdn (padrão)</span><span class="sxs-lookup"><span data-stu-id="40d41-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d41-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="40d41-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d41-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40d41-107">DESCRIPTION</span></span>
<span data-ttu-id="40d41-108">O cmdlet **New-AzFirewallApplicationRule** cria uma regra de aplicativo para o Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="40d41-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="40d41-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40d41-109">EXAMPLES</span></span>

### <span data-ttu-id="40d41-110">Exemplo 1: criar uma regra para permitir todo o tráfego HTTPS de 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="40d41-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="40d41-111">Este exemplo cria uma regra que permitirá que todo o tráfego HTTPS na porta 443 de 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="40d41-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="40d41-112">Exemplo 2: criar uma regra para permitir o WindowsUpdate para a sub-rede 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="40d41-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="40d41-113">Este exemplo cria uma regra que permitirá o tráfego de atualizações do Windows para domínio 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="40d41-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="40d41-114">OS</span><span class="sxs-lookup"><span data-stu-id="40d41-114">PARAMETERS</span></span>

### <span data-ttu-id="40d41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d41-115">-DefaultProfile</span></span>
<span data-ttu-id="40d41-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40d41-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d41-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="40d41-117">-Description</span></span>
<span data-ttu-id="40d41-118">Especifica uma descrição opcional desta regra.</span><span class="sxs-lookup"><span data-stu-id="40d41-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="40d41-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="40d41-119">-FqdnTag</span></span>
<span data-ttu-id="40d41-120">Especifica uma lista de marcas de FQDN para esta regra.</span><span class="sxs-lookup"><span data-stu-id="40d41-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="40d41-121">As marcas disponíveis podem ser recuperadas usando o cmdlet [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="40d41-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="40d41-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="40d41-122">-Name</span></span>
<span data-ttu-id="40d41-123">Especifica o nome desta regra de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40d41-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="40d41-124">O nome deve ser exclusivo dentro de uma coleção de regras.</span><span class="sxs-lookup"><span data-stu-id="40d41-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="40d41-125">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="40d41-125">-Protocol</span></span>
<span data-ttu-id="40d41-126">Especifica o tipo de tráfego a ser filtrado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="40d41-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="40d41-127">O formato é <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="40d41-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="40d41-128">Por exemplo, "http: 80" ou "https: 443".</span><span class="sxs-lookup"><span data-stu-id="40d41-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="40d41-129">O protocolo é obrigatório quando TargetFqdn é usado, mas não pode ser usado com FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="40d41-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="40d41-130">Os protocolos com suporte são HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="40d41-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="40d41-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="40d41-131">-SourceAddress</span></span>
<span data-ttu-id="40d41-132">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="40d41-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="40d41-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="40d41-133">-SourceIpGroup</span></span>
<span data-ttu-id="40d41-134">O ipgroup de origem da regra</span><span class="sxs-lookup"><span data-stu-id="40d41-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="40d41-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="40d41-135">-TargetFqdn</span></span>
<span data-ttu-id="40d41-136">Especifica uma lista de nomes de domínio filtrados por essa regra.</span><span class="sxs-lookup"><span data-stu-id="40d41-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="40d41-137">O caractere de asterisco ' *', é aceito apenas como o primeiro caractere de um FQDN na lista. Quando usado, o asterisco corresponde a qualquer número de caracteres. (por exemplo, '* MSN.com ' corresponderá MSN.com e todos os seus subdomínios)</span><span class="sxs-lookup"><span data-stu-id="40d41-137">The asterisk character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="40d41-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40d41-138">-Confirm</span></span>
<span data-ttu-id="40d41-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d41-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d41-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d41-140">-WhatIf</span></span>
<span data-ttu-id="40d41-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40d41-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d41-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40d41-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d41-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d41-143">CommonParameters</span></span>
<span data-ttu-id="40d41-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d41-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d41-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d41-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d41-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40d41-146">INPUTS</span></span>

### <span data-ttu-id="40d41-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="40d41-147">None</span></span>

## <span data-ttu-id="40d41-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40d41-148">OUTPUTS</span></span>

### <span data-ttu-id="40d41-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="40d41-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="40d41-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40d41-150">NOTES</span></span>

## <span data-ttu-id="40d41-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40d41-151">RELATED LINKS</span></span>

[<span data-ttu-id="40d41-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="40d41-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="40d41-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="40d41-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="40d41-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="40d41-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="40d41-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="40d41-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
