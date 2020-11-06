---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432524"
---
# <span data-ttu-id="22feb-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="22feb-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="22feb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22feb-102">SYNOPSIS</span></span>
<span data-ttu-id="22feb-103">Cria uma nova regra de firewall do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="22feb-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22feb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22feb-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="22feb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22feb-105">DESCRIPTION</span></span>
<span data-ttu-id="22feb-106">O New-AzureRmAnalysisServicesFirewallRule cria um novo objeto de regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="22feb-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="22feb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22feb-107">EXAMPLES</span></span>

### <span data-ttu-id="22feb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22feb-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="22feb-109">Cria uma regra de firewall chamada rule1 com o intervalo de início 0.0.0.0 e o intervalo de término 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="22feb-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="22feb-110">OS</span><span class="sxs-lookup"><span data-stu-id="22feb-110">PARAMETERS</span></span>

### <span data-ttu-id="22feb-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="22feb-111">-FirewallRuleName</span></span>
<span data-ttu-id="22feb-112">Nome da regra de firewall</span><span class="sxs-lookup"><span data-stu-id="22feb-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22feb-113">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="22feb-113">-RangeStart</span></span>
<span data-ttu-id="22feb-114">O início da faixa de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="22feb-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22feb-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="22feb-115">-RangeEnd</span></span>
<span data-ttu-id="22feb-116">O final do intervalo de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="22feb-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="22feb-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22feb-117">INPUTS</span></span>

## <span data-ttu-id="22feb-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22feb-118">OUTPUTS</span></span>

### <span data-ttu-id="22feb-119">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="22feb-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="22feb-120">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22feb-120">RELATED LINKS</span></span>

[<span data-ttu-id="22feb-121">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="22feb-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
