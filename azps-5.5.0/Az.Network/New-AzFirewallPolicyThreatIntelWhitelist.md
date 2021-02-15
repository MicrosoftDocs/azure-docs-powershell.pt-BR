---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114133"
---
# <span data-ttu-id="20fac-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="20fac-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="20fac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20fac-102">SYNOPSIS</span></span>
<span data-ttu-id="20fac-103">Criar uma nova lista de informações de ameaças para a Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="20fac-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="20fac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20fac-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20fac-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="20fac-105">DESCRIPTION</span></span>
<span data-ttu-id="20fac-106">O cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** cria um objeto de lista branca intel de ameaças, que pode ser usado ao criar ou definir uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="20fac-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="20fac-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20fac-107">EXAMPLES</span></span>

### <span data-ttu-id="20fac-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20fac-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="20fac-109">Este exemplo cria uma lista de ameaças que contém uma lista de whitelist FQDN de uma entrada e uma lista de branco de endereço Ip de duas entradas</span><span class="sxs-lookup"><span data-stu-id="20fac-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="20fac-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20fac-110">PARAMETERS</span></span>

### <span data-ttu-id="20fac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fac-111">-DefaultProfile</span></span>
<span data-ttu-id="20fac-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20fac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20fac-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="20fac-113">-FQDN</span></span>
<span data-ttu-id="20fac-114">Os FQDNs da Lista whitelist da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="20fac-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="20fac-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="20fac-115">-IpAddress</span></span>
<span data-ttu-id="20fac-116">Os endereços IP da Lista de Whitelist da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="20fac-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="20fac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fac-117">CommonParameters</span></span>
<span data-ttu-id="20fac-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20fac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fac-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20fac-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fac-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="20fac-120">INPUTS</span></span>

### <span data-ttu-id="20fac-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20fac-121">None</span></span>

## <span data-ttu-id="20fac-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="20fac-122">OUTPUTS</span></span>

### <span data-ttu-id="20fac-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="20fac-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="20fac-124">Notas</span><span class="sxs-lookup"><span data-stu-id="20fac-124">NOTES</span></span>

## <span data-ttu-id="20fac-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20fac-125">RELATED LINKS</span></span>
