---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 18946b74ea72ac3d5db2dd683657eda60b8eeec5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886905"
---
# <span data-ttu-id="f71fa-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f71fa-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="f71fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f71fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f71fa-103">Criar uma nova lista branca de inteligência contra ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f71fa-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="f71fa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f71fa-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f71fa-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f71fa-105">DESCRIPTION</span></span>
<span data-ttu-id="f71fa-106">O cmdlet **New-AzFirewallThreatIntelWhitelist** cria um objeto whitelist intel de ameaças, que pode ser usado ao criar ou definir um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="f71fa-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="f71fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f71fa-107">EXAMPLES</span></span>

### <span data-ttu-id="f71fa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f71fa-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="f71fa-109">Este exemplo cria uma lista branca de intel de ameaças que contém uma lista branca FQDN de duas entradas e uma lista branca de endereço Ip de duas entradas</span><span class="sxs-lookup"><span data-stu-id="f71fa-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="f71fa-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f71fa-110">PARAMETERS</span></span>

### <span data-ttu-id="f71fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f71fa-111">-DefaultProfile</span></span>
<span data-ttu-id="f71fa-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f71fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f71fa-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="f71fa-113">-FQDN</span></span>
<span data-ttu-id="f71fa-114">Os FQDNs da lista branca do Intel Threat</span><span class="sxs-lookup"><span data-stu-id="f71fa-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="f71fa-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f71fa-115">-IpAddress</span></span>
<span data-ttu-id="f71fa-116">Os endereços IP da lista branca do Intel Threat</span><span class="sxs-lookup"><span data-stu-id="f71fa-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="f71fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71fa-117">CommonParameters</span></span>
<span data-ttu-id="f71fa-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f71fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71fa-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f71fa-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71fa-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f71fa-120">INPUTS</span></span>

### <span data-ttu-id="f71fa-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f71fa-121">None</span></span>

## <span data-ttu-id="f71fa-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f71fa-122">OUTPUTS</span></span>

### <span data-ttu-id="f71fa-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f71fa-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="f71fa-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="f71fa-124">NOTES</span></span>

## <span data-ttu-id="f71fa-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f71fa-125">RELATED LINKS</span></span>

[<span data-ttu-id="f71fa-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f71fa-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="f71fa-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f71fa-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f71fa-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f71fa-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)