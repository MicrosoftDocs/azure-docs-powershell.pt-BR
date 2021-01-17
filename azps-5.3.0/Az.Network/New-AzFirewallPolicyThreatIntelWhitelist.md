---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428956"
---
# <span data-ttu-id="2e20e-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2e20e-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="2e20e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e20e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e20e-103">Criar uma nova lista branca de inteligência de ameaças para a política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="2e20e-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="2e20e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e20e-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e20e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e20e-105">DESCRIPTION</span></span>
<span data-ttu-id="2e20e-106">O cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** cria um objeto de lista branca da Intel com ameaças, que pode ser usado ao criar ou configurar uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e20e-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="2e20e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e20e-107">EXAMPLES</span></span>

### <span data-ttu-id="2e20e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e20e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="2e20e-109">Este exemplo cria uma lista branca da Intel com ameaças contendo uma lista branca do FQDN de uma entrada e uma lista branca de endereços IP de duas entradas</span><span class="sxs-lookup"><span data-stu-id="2e20e-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="2e20e-110">OS</span><span class="sxs-lookup"><span data-stu-id="2e20e-110">PARAMETERS</span></span>

### <span data-ttu-id="2e20e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e20e-111">-DefaultProfile</span></span>
<span data-ttu-id="2e20e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e20e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e20e-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="2e20e-113">-FQDN</span></span>
<span data-ttu-id="2e20e-114">Os FQDNs da lista branca da Intel® Threat</span><span class="sxs-lookup"><span data-stu-id="2e20e-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="2e20e-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="2e20e-115">-IpAddress</span></span>
<span data-ttu-id="2e20e-116">Os endereços IP da lista branca da Intel® Threat</span><span class="sxs-lookup"><span data-stu-id="2e20e-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="2e20e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e20e-117">CommonParameters</span></span>
<span data-ttu-id="2e20e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e20e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e20e-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e20e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e20e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e20e-120">INPUTS</span></span>

### <span data-ttu-id="2e20e-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2e20e-121">None</span></span>

## <span data-ttu-id="2e20e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e20e-122">OUTPUTS</span></span>

### <span data-ttu-id="2e20e-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2e20e-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="2e20e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e20e-124">NOTES</span></span>

## <span data-ttu-id="2e20e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e20e-125">RELATED LINKS</span></span>
