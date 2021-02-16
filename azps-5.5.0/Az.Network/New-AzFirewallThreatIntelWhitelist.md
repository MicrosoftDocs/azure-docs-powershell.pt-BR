---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118310"
---
# <span data-ttu-id="d5bf0-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d5bf0-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="d5bf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bf0-103">Criar uma nova lista de whitelist de inteligência contra ameaças para Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d5bf0-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="d5bf0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5bf0-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5bf0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="d5bf0-106">O cmdlet **New-AzFirewallThreatIntelWhitelist** cria um objeto de lista branca intel de ameaças, que pode ser usado ao criar ou definir um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="d5bf0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5bf0-107">EXAMPLES</span></span>

### <span data-ttu-id="d5bf0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5bf0-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="d5bf0-109">Este exemplo cria uma lista de ameaças que contém uma lista de whitelist FQDN de duas entradas e uma lista de branco de endereço Ip de duas entradas</span><span class="sxs-lookup"><span data-stu-id="d5bf0-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="d5bf0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5bf0-110">PARAMETERS</span></span>

### <span data-ttu-id="d5bf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5bf0-111">-DefaultProfile</span></span>
<span data-ttu-id="d5bf0-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5bf0-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="d5bf0-113">-FQDN</span></span>
<span data-ttu-id="d5bf0-114">Os FQDNs da Lista whitelist da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="d5bf0-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="d5bf0-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="d5bf0-115">-IpAddress</span></span>
<span data-ttu-id="d5bf0-116">Os endereços IP da Lista de Whitelist da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="d5bf0-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="d5bf0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bf0-117">CommonParameters</span></span>
<span data-ttu-id="d5bf0-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bf0-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5bf0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bf0-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="d5bf0-120">INPUTS</span></span>

### <span data-ttu-id="d5bf0-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d5bf0-121">None</span></span>

## <span data-ttu-id="d5bf0-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="d5bf0-122">OUTPUTS</span></span>

### <span data-ttu-id="d5bf0-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d5bf0-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="d5bf0-124">Notas</span><span class="sxs-lookup"><span data-stu-id="d5bf0-124">NOTES</span></span>

## <span data-ttu-id="d5bf0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5bf0-125">RELATED LINKS</span></span>

[<span data-ttu-id="d5bf0-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d5bf0-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d5bf0-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d5bf0-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d5bf0-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d5bf0-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)