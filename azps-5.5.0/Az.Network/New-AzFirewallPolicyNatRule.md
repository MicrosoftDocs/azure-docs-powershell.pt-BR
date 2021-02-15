---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114682"
---
# <span data-ttu-id="6e552-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="6e552-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="6e552-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e552-102">SYNOPSIS</span></span>
<span data-ttu-id="6e552-103">Criar uma nova regra NAT de Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6e552-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="6e552-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e552-104">SYNTAX</span></span>

### <span data-ttu-id="6e552-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="6e552-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e552-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="6e552-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e552-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="6e552-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e552-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="6e552-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e552-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e552-109">DESCRIPTION</span></span>
<span data-ttu-id="6e552-110">O cmdlet **New-AzFirewallPolicyNatRule** cria uma regra NAT para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e552-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="6e552-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e552-111">EXAMPLES</span></span>

### <span data-ttu-id="6e552-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e552-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="6e552-113">Este exemplo cria uma regra NAT com o endereço de origem, protocolo, endereço de destino, porta de destino, endereço traduzido e porta traduzida.</span><span class="sxs-lookup"><span data-stu-id="6e552-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="6e552-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6e552-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="6e552-115">Este exemplo cria uma regra NAT com o endereço de origem, protocolo, endereço de destino, porta de destino, fqdn traduzido e porta traduzida.</span><span class="sxs-lookup"><span data-stu-id="6e552-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="6e552-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e552-116">PARAMETERS</span></span>

### <span data-ttu-id="6e552-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e552-117">-DefaultProfile</span></span>
<span data-ttu-id="6e552-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e552-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e552-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6e552-119">-Description</span></span>
<span data-ttu-id="6e552-120">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="6e552-120">The description of the rule</span></span>

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

### <span data-ttu-id="6e552-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6e552-121">-DestinationAddress</span></span>
<span data-ttu-id="6e552-122">Os endereços de destino da regra.</span><span class="sxs-lookup"><span data-stu-id="6e552-122">The destination addresses of the rule.</span></span> <span data-ttu-id="6e552-123">Esse deve ser o IP público do Firewall.</span><span class="sxs-lookup"><span data-stu-id="6e552-123">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="6e552-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6e552-124">-DestinationPort</span></span>
<span data-ttu-id="6e552-125">As portas de destino da regra</span><span class="sxs-lookup"><span data-stu-id="6e552-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="6e552-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e552-126">-Name</span></span>
<span data-ttu-id="6e552-127">O nome da Coleção de Regras NAT</span><span class="sxs-lookup"><span data-stu-id="6e552-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="6e552-128">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="6e552-128">-Protocol</span></span>
<span data-ttu-id="6e552-129">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="6e552-129">The protocols of the rule</span></span>

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

### <span data-ttu-id="6e552-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="6e552-130">-SourceAddress</span></span>
<span data-ttu-id="6e552-131">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="6e552-131">The source addresses of the rule</span></span>

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

### <span data-ttu-id="6e552-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="6e552-132">-SourceIpGroup</span></span>
<span data-ttu-id="6e552-133">Os grupos ipgroups de origem da regra</span><span class="sxs-lookup"><span data-stu-id="6e552-133">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="6e552-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="6e552-134">-TranslatedAddress</span></span>
<span data-ttu-id="6e552-135">O endereço traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="6e552-135">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="6e552-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="6e552-136">-TranslatedFqdn</span></span>
<span data-ttu-id="6e552-137">O FQDN traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="6e552-137">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="6e552-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="6e552-138">-TranslatedPort</span></span>
<span data-ttu-id="6e552-139">A porta traduzida para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="6e552-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="6e552-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e552-140">CommonParameters</span></span>
<span data-ttu-id="6e552-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e552-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e552-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e552-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e552-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="6e552-143">INPUTS</span></span>

### <span data-ttu-id="6e552-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6e552-144">None</span></span>

## <span data-ttu-id="6e552-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="6e552-145">OUTPUTS</span></span>

### <span data-ttu-id="6e552-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="6e552-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="6e552-147">Notas</span><span class="sxs-lookup"><span data-stu-id="6e552-147">NOTES</span></span>

## <span data-ttu-id="6e552-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e552-148">RELATED LINKS</span></span>
