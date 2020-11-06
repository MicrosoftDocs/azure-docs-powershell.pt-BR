---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 28a7fa45c8c6dc291f5e0c2a54c9fcf5fb5242dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600564"
---
# <span data-ttu-id="c3b4e-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="c3b4e-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="c3b4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b4e-103">Obtém as marcas de FQDN do firewall do Azure disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="c3b4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3b4e-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3b4e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3b4e-105">DESCRIPTION</span></span>
<span data-ttu-id="c3b4e-106">O cmdlet **Get-AzFirewallFqdnTag** Obtém a lista de marcas de FQDN que podem ser usadas para as regras do aplicativo de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="c3b4e-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="c3b4e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3b4e-107">EXAMPLES</span></span>

### <span data-ttu-id="c3b4e-108">1: recuperar todas as marcas de FQDN disponíveis</span><span class="sxs-lookup"><span data-stu-id="c3b4e-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="c3b4e-109">Este exemplo recupera todas as marcas FQDN disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="c3b4e-110">2: usar primeira marca FQDN disponível em uma regra de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c3b4e-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="c3b4e-111">Este exemplo cria uma regra de aplicativo de firewall usando a primeira marca FQDN disponível</span><span class="sxs-lookup"><span data-stu-id="c3b4e-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="c3b4e-112">OS</span><span class="sxs-lookup"><span data-stu-id="c3b4e-112">PARAMETERS</span></span>

### <span data-ttu-id="c3b4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b4e-113">-DefaultProfile</span></span>
<span data-ttu-id="c3b4e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3b4e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b4e-115">CommonParameters</span></span>
<span data-ttu-id="c3b4e-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b4e-117">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3b4e-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b4e-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3b4e-118">INPUTS</span></span>

### <span data-ttu-id="c3b4e-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c3b4e-119">None</span></span>

## <span data-ttu-id="c3b4e-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3b4e-120">OUTPUTS</span></span>

### <span data-ttu-id="c3b4e-121">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="c3b4e-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="c3b4e-122">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. cmdlets. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c3b4e-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c3b4e-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3b4e-123">NOTES</span></span>

## <span data-ttu-id="c3b4e-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3b4e-124">RELATED LINKS</span></span>

[<span data-ttu-id="c3b4e-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c3b4e-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="c3b4e-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c3b4e-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
