---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259836"
---
# <span data-ttu-id="430ea-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="430ea-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="430ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="430ea-102">SYNOPSIS</span></span>
<span data-ttu-id="430ea-103">Criar uma nova lista branca de inteligência de ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="430ea-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="430ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="430ea-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="430ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="430ea-105">DESCRIPTION</span></span>
<span data-ttu-id="430ea-106">O cmdlet **New-AzFirewallThreatIntelWhitelist** cria um objeto de lista branca da Intel com ameaças, que pode ser usado ao criar ou configurar um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="430ea-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="430ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="430ea-107">EXAMPLES</span></span>

### <span data-ttu-id="430ea-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="430ea-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="430ea-109">Este exemplo cria uma lista branca da Intel com ameaças contendo uma lista branca do FQDN de duas entradas e uma lista de endereços IP de duas entradas</span><span class="sxs-lookup"><span data-stu-id="430ea-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="430ea-110">OS</span><span class="sxs-lookup"><span data-stu-id="430ea-110">PARAMETERS</span></span>

### <span data-ttu-id="430ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="430ea-111">-DefaultProfile</span></span>
<span data-ttu-id="430ea-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="430ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="430ea-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="430ea-113">-FQDN</span></span>
<span data-ttu-id="430ea-114">Os FQDNs da lista branca da Intel® Threat</span><span class="sxs-lookup"><span data-stu-id="430ea-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="430ea-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="430ea-115">-IpAddress</span></span>
<span data-ttu-id="430ea-116">Os endereços IP da lista branca da Intel® Threat</span><span class="sxs-lookup"><span data-stu-id="430ea-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="430ea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430ea-117">CommonParameters</span></span>
<span data-ttu-id="430ea-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="430ea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430ea-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="430ea-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430ea-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="430ea-120">INPUTS</span></span>

### <span data-ttu-id="430ea-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="430ea-121">None</span></span>

## <span data-ttu-id="430ea-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="430ea-122">OUTPUTS</span></span>

### <span data-ttu-id="430ea-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="430ea-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="430ea-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="430ea-124">NOTES</span></span>

## <span data-ttu-id="430ea-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="430ea-125">RELATED LINKS</span></span>

[<span data-ttu-id="430ea-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="430ea-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="430ea-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="430ea-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="430ea-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="430ea-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)