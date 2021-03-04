---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 0c7e29b0c9b59842e885cf8763da63c2d65cfff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891791"
---
# <span data-ttu-id="5c951-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="5c951-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="5c951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c951-102">SYNOPSIS</span></span>
<span data-ttu-id="5c951-103">Criar uma nova regra de aplicativo de política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c951-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="5c951-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5c951-104">SYNTAX</span></span>

### <span data-ttu-id="5c951-105">SourceAddressAndTargetFqdn (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5c951-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c951-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="5c951-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c951-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="5c951-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c951-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="5c951-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c951-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="5c951-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c951-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="5c951-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c951-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="5c951-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c951-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="5c951-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c951-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5c951-113">DESCRIPTION</span></span>
<span data-ttu-id="5c951-114">O cmdlet **New-AzFirewallPolicyApplicationRule** cria uma Regra de Aplicativo para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c951-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="5c951-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c951-115">EXAMPLES</span></span>

### <span data-ttu-id="5c951-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c951-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="5c951-117">Este exemplo cria uma regra de aplicativo com o endereço de origem, o protocolo e os fqdns de destino.</span><span class="sxs-lookup"><span data-stu-id="5c951-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="5c951-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5c951-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="5c951-119">Este exemplo cria uma regra de aplicativo com o endereço de origem, o protocolo e as categorias da Web.</span><span class="sxs-lookup"><span data-stu-id="5c951-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="5c951-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5c951-120">PARAMETERS</span></span>

### <span data-ttu-id="5c951-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c951-121">-DefaultProfile</span></span>
<span data-ttu-id="5c951-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c951-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c951-123">-Description</span><span class="sxs-lookup"><span data-stu-id="5c951-123">-Description</span></span>
<span data-ttu-id="5c951-124">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="5c951-124">The description of the rule</span></span>

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

### <span data-ttu-id="5c951-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="5c951-125">-FqdnTag</span></span>
<span data-ttu-id="5c951-126">As marcas FQDN da regra</span><span class="sxs-lookup"><span data-stu-id="5c951-126">The FQDN Tags of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c951-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5c951-127">-Name</span></span>
<span data-ttu-id="5c951-128">O nome da Regra de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c951-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="5c951-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5c951-129">-Protocol</span></span>
<span data-ttu-id="5c951-130">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="5c951-130">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c951-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="5c951-131">-SourceAddress</span></span>
<span data-ttu-id="5c951-132">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="5c951-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c951-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="5c951-133">-SourceIpGroup</span></span>
<span data-ttu-id="5c951-134">Os grupos ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="5c951-134">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c951-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="5c951-135">-TargetFqdn</span></span>
<span data-ttu-id="5c951-136">Os FQDNs de destino da regra</span><span class="sxs-lookup"><span data-stu-id="5c951-136">The target FQDNs of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c951-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="5c951-137">-WebCategory</span></span>
<span data-ttu-id="5c951-138">As Categorias da Web da regra</span><span class="sxs-lookup"><span data-stu-id="5c951-138">The Web Categories of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c951-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="5c951-139">-TargetUrl</span></span>
<span data-ttu-id="5c951-140">A Url de destino da regra</span><span class="sxs-lookup"><span data-stu-id="5c951-140">The Target Url of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c951-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="5c951-141">-TerminateTLS</span></span>
<span data-ttu-id="5c951-142">Indica o término do TLS</span><span class="sxs-lookup"><span data-stu-id="5c951-142">Indicates terminating TLS</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c951-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c951-143">CommonParameters</span></span>
<span data-ttu-id="5c951-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c951-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c951-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c951-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c951-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c951-146">INPUTS</span></span>

### <span data-ttu-id="5c951-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5c951-147">None</span></span>

## <span data-ttu-id="5c951-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5c951-148">OUTPUTS</span></span>

### <span data-ttu-id="5c951-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="5c951-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="5c951-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="5c951-150">NOTES</span></span>

## <span data-ttu-id="5c951-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c951-151">RELATED LINKS</span></span>
