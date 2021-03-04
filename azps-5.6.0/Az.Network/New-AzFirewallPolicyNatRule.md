---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 2ba006beef1c698c12086ef65efca0213920092c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889921"
---
# <span data-ttu-id="c961f-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="c961f-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="c961f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c961f-102">SYNOPSIS</span></span>
<span data-ttu-id="c961f-103">Criar uma nova regra NAT da Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="c961f-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="c961f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c961f-104">SYNTAX</span></span>

### <span data-ttu-id="c961f-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c961f-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c961f-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c961f-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c961f-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c961f-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c961f-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c961f-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c961f-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c961f-109">DESCRIPTION</span></span>
<span data-ttu-id="c961f-110">O cmdlet **New-AzFirewallPolicyNatRule** cria uma regra NAT para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="c961f-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="c961f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c961f-111">EXAMPLES</span></span>

### <span data-ttu-id="c961f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c961f-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="c961f-113">Este exemplo cria uma regra NAT com o endereço de origem, protocolo, endereço de destino, porta de destino, endereço traduzido e porta traduzida.</span><span class="sxs-lookup"><span data-stu-id="c961f-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="c961f-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c961f-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="c961f-115">Este exemplo cria uma regra NAT com o endereço de origem, protocolo, endereço de destino, porta de destino, fqdn convertido e porta traduzida.</span><span class="sxs-lookup"><span data-stu-id="c961f-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="c961f-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c961f-116">PARAMETERS</span></span>

### <span data-ttu-id="c961f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c961f-117">-DefaultProfile</span></span>
<span data-ttu-id="c961f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c961f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c961f-119">-Description</span><span class="sxs-lookup"><span data-stu-id="c961f-119">-Description</span></span>
<span data-ttu-id="c961f-120">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="c961f-120">The description of the rule</span></span>

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

### <span data-ttu-id="c961f-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="c961f-121">-DestinationAddress</span></span>
<span data-ttu-id="c961f-122">Os endereços de destino da regra.</span><span class="sxs-lookup"><span data-stu-id="c961f-122">The destination addresses of the rule.</span></span> <span data-ttu-id="c961f-123">Esse deve ser o IP público do Firewall.</span><span class="sxs-lookup"><span data-stu-id="c961f-123">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="c961f-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c961f-124">-DestinationPort</span></span>
<span data-ttu-id="c961f-125">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="c961f-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="c961f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c961f-126">-Name</span></span>
<span data-ttu-id="c961f-127">O nome da coleção de regras NAT</span><span class="sxs-lookup"><span data-stu-id="c961f-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="c961f-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c961f-128">-Protocol</span></span>
<span data-ttu-id="c961f-129">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="c961f-129">The protocols of the rule</span></span>

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

### <span data-ttu-id="c961f-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="c961f-130">-SourceAddress</span></span>
<span data-ttu-id="c961f-131">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="c961f-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c961f-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="c961f-132">-SourceIpGroup</span></span>
<span data-ttu-id="c961f-133">Os grupos ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="c961f-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c961f-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c961f-134">-TranslatedAddress</span></span>
<span data-ttu-id="c961f-135">O endereço convertido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="c961f-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c961f-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="c961f-136">-TranslatedFqdn</span></span>
<span data-ttu-id="c961f-137">O FQDN convertido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="c961f-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c961f-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="c961f-138">-TranslatedPort</span></span>
<span data-ttu-id="c961f-139">A porta traduzida para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="c961f-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="c961f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c961f-140">CommonParameters</span></span>
<span data-ttu-id="c961f-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c961f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c961f-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c961f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c961f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c961f-143">INPUTS</span></span>

### <span data-ttu-id="c961f-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c961f-144">None</span></span>

## <span data-ttu-id="c961f-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c961f-145">OUTPUTS</span></span>

### <span data-ttu-id="c961f-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c961f-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="c961f-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="c961f-147">NOTES</span></span>

## <span data-ttu-id="c961f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c961f-148">RELATED LINKS</span></span>
