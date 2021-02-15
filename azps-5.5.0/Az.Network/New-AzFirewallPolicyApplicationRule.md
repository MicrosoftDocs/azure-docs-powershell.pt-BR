---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 25a81344d9d8d5b8af8eed907bce7977408515ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112842"
---
# <span data-ttu-id="490c1-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="490c1-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="490c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="490c1-102">SYNOPSIS</span></span>
<span data-ttu-id="490c1-103">Criar uma nova Regra de Aplicativo de Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="490c1-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="490c1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="490c1-104">SYNTAX</span></span>

### <span data-ttu-id="490c1-105">SourceAddressAndTargetFqdn (Padrão)</span><span class="sxs-lookup"><span data-stu-id="490c1-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490c1-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="490c1-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490c1-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="490c1-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490c1-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="490c1-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490c1-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="490c1-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490c1-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="490c1-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490c1-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="490c1-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490c1-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="490c1-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="490c1-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="490c1-113">DESCRIPTION</span></span>
<span data-ttu-id="490c1-114">O cmdlet **New-AzFirewallPolicyApplicationRule** cria uma Regra de Aplicativo para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="490c1-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="490c1-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="490c1-115">EXAMPLES</span></span>

### <span data-ttu-id="490c1-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="490c1-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="490c1-117">Este exemplo cria uma regra de aplicativo com o endereço de origem, o protocolo e os fqdns de destino.</span><span class="sxs-lookup"><span data-stu-id="490c1-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="490c1-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="490c1-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="490c1-119">Este exemplo cria uma regra de aplicativo com o endereço de origem, protocolo e categorias da Web.</span><span class="sxs-lookup"><span data-stu-id="490c1-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="490c1-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="490c1-120">PARAMETERS</span></span>

### <span data-ttu-id="490c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490c1-121">-DefaultProfile</span></span>
<span data-ttu-id="490c1-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="490c1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="490c1-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="490c1-123">-Description</span></span>
<span data-ttu-id="490c1-124">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="490c1-124">The description of the rule</span></span>

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

### <span data-ttu-id="490c1-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="490c1-125">-FqdnTag</span></span>
<span data-ttu-id="490c1-126">As Marcas FQDN da regra</span><span class="sxs-lookup"><span data-stu-id="490c1-126">The FQDN Tags of the rule</span></span>

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

### <span data-ttu-id="490c1-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="490c1-127">-Name</span></span>
<span data-ttu-id="490c1-128">O nome da Regra de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="490c1-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="490c1-129">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="490c1-129">-Protocol</span></span>
<span data-ttu-id="490c1-130">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="490c1-130">The protocols of the rule</span></span>

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

### <span data-ttu-id="490c1-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="490c1-131">-SourceAddress</span></span>
<span data-ttu-id="490c1-132">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="490c1-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="490c1-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="490c1-133">-SourceIpGroup</span></span>
<span data-ttu-id="490c1-134">Os grupos ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="490c1-134">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="490c1-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="490c1-135">-TargetFqdn</span></span>
<span data-ttu-id="490c1-136">Os FQDNs de destino da regra</span><span class="sxs-lookup"><span data-stu-id="490c1-136">The target FQDNs of the rule</span></span>

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

### <span data-ttu-id="490c1-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="490c1-137">-WebCategory</span></span>
<span data-ttu-id="490c1-138">As Categorias Da Web da regra</span><span class="sxs-lookup"><span data-stu-id="490c1-138">The Web Categories of the rule</span></span>

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

### <span data-ttu-id="490c1-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="490c1-139">-TargetUrl</span></span>
<span data-ttu-id="490c1-140">A Url de Destino da regra</span><span class="sxs-lookup"><span data-stu-id="490c1-140">The Target Url of the rule</span></span>

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

### <span data-ttu-id="490c1-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="490c1-141">-TerminateTLS</span></span>
<span data-ttu-id="490c1-142">Indica o encerramento de TLS</span><span class="sxs-lookup"><span data-stu-id="490c1-142">Indicates terminating TLS</span></span>

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

### <span data-ttu-id="490c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490c1-143">CommonParameters</span></span>
<span data-ttu-id="490c1-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490c1-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="490c1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490c1-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="490c1-146">INPUTS</span></span>

### <span data-ttu-id="490c1-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="490c1-147">None</span></span>

## <span data-ttu-id="490c1-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="490c1-148">OUTPUTS</span></span>

### <span data-ttu-id="490c1-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="490c1-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="490c1-150">Notas</span><span class="sxs-lookup"><span data-stu-id="490c1-150">NOTES</span></span>

## <span data-ttu-id="490c1-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="490c1-151">RELATED LINKS</span></span>
