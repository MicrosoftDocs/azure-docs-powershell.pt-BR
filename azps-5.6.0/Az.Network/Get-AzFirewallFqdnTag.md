---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: ff5dee9a4e072cea7f1ee5bd46898857233ed0d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886004"
---
# <span data-ttu-id="96c74-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="96c74-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="96c74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96c74-102">SYNOPSIS</span></span>
<span data-ttu-id="96c74-103">Obtém as marcas Fqdn disponíveis do Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="96c74-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="96c74-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="96c74-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c74-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="96c74-105">DESCRIPTION</span></span>
<span data-ttu-id="96c74-106">O cmdlet **Get-AzFirewallFqdnTag** obtém a lista de Marcas FQDN que podem ser usadas para Regras de Aplicativo de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="96c74-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="96c74-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96c74-107">EXAMPLES</span></span>

### <span data-ttu-id="96c74-108">1: Recuperar todas as marcas FQDN disponíveis</span><span class="sxs-lookup"><span data-stu-id="96c74-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="96c74-109">Este exemplo recupera todas as marcas FQDN disponíveis.</span><span class="sxs-lookup"><span data-stu-id="96c74-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="96c74-110">2: Usar a primeira marca FQDN disponível em uma regra de aplicativo</span><span class="sxs-lookup"><span data-stu-id="96c74-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="96c74-111">Este exemplo cria uma Regra de Aplicativo de Firewall usando a primeira marca FQDN disponível</span><span class="sxs-lookup"><span data-stu-id="96c74-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="96c74-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="96c74-112">PARAMETERS</span></span>

### <span data-ttu-id="96c74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c74-113">-DefaultProfile</span></span>
<span data-ttu-id="96c74-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="96c74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c74-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c74-115">CommonParameters</span></span>
<span data-ttu-id="96c74-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c74-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c74-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96c74-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c74-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96c74-118">INPUTS</span></span>

### <span data-ttu-id="96c74-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="96c74-119">None</span></span>

## <span data-ttu-id="96c74-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="96c74-120">OUTPUTS</span></span>

### <span data-ttu-id="96c74-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="96c74-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="96c74-122">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="96c74-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="96c74-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="96c74-123">NOTES</span></span>

## <span data-ttu-id="96c74-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96c74-124">RELATED LINKS</span></span>

[<span data-ttu-id="96c74-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="96c74-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="96c74-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96c74-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
