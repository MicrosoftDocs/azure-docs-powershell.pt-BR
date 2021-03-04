---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: eed81fbd222220225a67378c67aa1d32d440577a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886435"
---
# <span data-ttu-id="95f6b-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="95f6b-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="95f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="95f6b-103">Criar uma nova lista branca de inteligência contra ameaças para a Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="95f6b-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="95f6b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="95f6b-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f6b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="95f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="95f6b-106">O cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** cria um objeto de lista branca intel de ameaças, que pode ser usado ao criar ou definir uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="95f6b-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="95f6b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95f6b-107">EXAMPLES</span></span>

### <span data-ttu-id="95f6b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95f6b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="95f6b-109">Este exemplo cria uma lista branca de intel de ameaça que contém uma lista branca FQDN de uma entrada e uma lista branca de endereço Ip de duas entradas</span><span class="sxs-lookup"><span data-stu-id="95f6b-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="95f6b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="95f6b-110">PARAMETERS</span></span>

### <span data-ttu-id="95f6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f6b-111">-DefaultProfile</span></span>
<span data-ttu-id="95f6b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95f6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f6b-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="95f6b-113">-FQDN</span></span>
<span data-ttu-id="95f6b-114">Os FQDNs da lista branca do Intel Threat</span><span class="sxs-lookup"><span data-stu-id="95f6b-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f6b-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="95f6b-115">-IpAddress</span></span>
<span data-ttu-id="95f6b-116">Os endereços IP da lista branca do Intel Threat</span><span class="sxs-lookup"><span data-stu-id="95f6b-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f6b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f6b-117">CommonParameters</span></span>
<span data-ttu-id="95f6b-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f6b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f6b-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95f6b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f6b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95f6b-120">INPUTS</span></span>

### <span data-ttu-id="95f6b-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="95f6b-121">None</span></span>

## <span data-ttu-id="95f6b-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="95f6b-122">OUTPUTS</span></span>

### <span data-ttu-id="95f6b-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="95f6b-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="95f6b-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="95f6b-124">NOTES</span></span>

## <span data-ttu-id="95f6b-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95f6b-125">RELATED LINKS</span></span>
