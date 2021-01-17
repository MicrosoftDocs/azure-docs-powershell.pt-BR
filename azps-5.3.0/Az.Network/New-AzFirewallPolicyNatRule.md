---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428966"
---
# <span data-ttu-id="bf951-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="bf951-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="bf951-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf951-102">SYNOPSIS</span></span>
<span data-ttu-id="bf951-103">Criar uma nova regra de NAT da política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bf951-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="bf951-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf951-104">SYNTAX</span></span>

### <span data-ttu-id="bf951-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="bf951-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf951-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="bf951-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf951-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="bf951-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf951-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="bf951-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf951-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf951-109">DESCRIPTION</span></span>
<span data-ttu-id="bf951-110">O cmdlet **New-AzFirewallPolicyNatRule** cria uma regra NAT para uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf951-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="bf951-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf951-111">EXAMPLES</span></span>

### <span data-ttu-id="bf951-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf951-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="bf951-113">Este exemplo cria uma regra NAT com o endereço de origem, o protocolo, o endereço de destino, a porta de destino, o endereço traduzido e a porta traduzida.</span><span class="sxs-lookup"><span data-stu-id="bf951-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="bf951-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bf951-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="bf951-115">Este exemplo cria uma regra NAT com o endereço de origem, o protocolo, o endereço de destino, a porta de destino, o FQDN traduzido e a porta traduzida.</span><span class="sxs-lookup"><span data-stu-id="bf951-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="bf951-116">OS</span><span class="sxs-lookup"><span data-stu-id="bf951-116">PARAMETERS</span></span>

### <span data-ttu-id="bf951-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf951-117">-DefaultProfile</span></span>
<span data-ttu-id="bf951-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf951-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf951-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="bf951-119">-Description</span></span>
<span data-ttu-id="bf951-120">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="bf951-120">The description of the rule</span></span>

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

### <span data-ttu-id="bf951-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="bf951-121">-DestinationAddress</span></span>
<span data-ttu-id="bf951-122">Os endereços de destino da regra.</span><span class="sxs-lookup"><span data-stu-id="bf951-122">The destination addresses of the rule.</span></span> <span data-ttu-id="bf951-123">Isso deve ser um IP público do firewall.</span><span class="sxs-lookup"><span data-stu-id="bf951-123">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="bf951-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="bf951-124">-DestinationPort</span></span>
<span data-ttu-id="bf951-125">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="bf951-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="bf951-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf951-126">-Name</span></span>
<span data-ttu-id="bf951-127">O nome da coleção de regras NAT</span><span class="sxs-lookup"><span data-stu-id="bf951-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="bf951-128">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="bf951-128">-Protocol</span></span>
<span data-ttu-id="bf951-129">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="bf951-129">The protocols of the rule</span></span>

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

### <span data-ttu-id="bf951-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="bf951-130">-SourceAddress</span></span>
<span data-ttu-id="bf951-131">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="bf951-131">The source addresses of the rule</span></span>

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

### <span data-ttu-id="bf951-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="bf951-132">-SourceIpGroup</span></span>
<span data-ttu-id="bf951-133">O ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="bf951-133">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="bf951-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="bf951-134">-TranslatedAddress</span></span>
<span data-ttu-id="bf951-135">O endereço traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="bf951-135">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="bf951-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="bf951-136">-TranslatedFqdn</span></span>
<span data-ttu-id="bf951-137">O FQDN traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="bf951-137">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="bf951-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="bf951-138">-TranslatedPort</span></span>
<span data-ttu-id="bf951-139">A porta traduzida para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="bf951-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="bf951-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf951-140">CommonParameters</span></span>
<span data-ttu-id="bf951-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf951-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf951-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf951-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf951-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf951-143">INPUTS</span></span>

### <span data-ttu-id="bf951-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bf951-144">None</span></span>

## <span data-ttu-id="bf951-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf951-145">OUTPUTS</span></span>

### <span data-ttu-id="bf951-146">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="bf951-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="bf951-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf951-147">NOTES</span></span>

## <span data-ttu-id="bf951-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf951-148">RELATED LINKS</span></span>
