---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258179"
---
# <span data-ttu-id="670d2-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="670d2-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="670d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="670d2-102">SYNOPSIS</span></span>
<span data-ttu-id="670d2-103">Cria uma nova regra de firewall do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="670d2-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="670d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="670d2-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="670d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="670d2-105">DESCRIPTION</span></span>
<span data-ttu-id="670d2-106">O New-AzAnalysisServicesFirewallRule cria um novo objeto de regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="670d2-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="670d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="670d2-107">EXAMPLES</span></span>

### <span data-ttu-id="670d2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="670d2-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="670d2-109">Cria uma regra de firewall chamada rule1 com o intervalo de início 0.0.0.0 e o intervalo de término 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="670d2-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="670d2-110">OS</span><span class="sxs-lookup"><span data-stu-id="670d2-110">PARAMETERS</span></span>

### <span data-ttu-id="670d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670d2-111">-DefaultProfile</span></span>
<span data-ttu-id="670d2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="670d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="670d2-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="670d2-113">-FirewallRuleName</span></span>
<span data-ttu-id="670d2-114">Nome da regra de firewall</span><span class="sxs-lookup"><span data-stu-id="670d2-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670d2-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="670d2-115">-RangeEnd</span></span>
<span data-ttu-id="670d2-116">O final do intervalo de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="670d2-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670d2-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="670d2-117">-RangeStart</span></span>
<span data-ttu-id="670d2-118">O início da faixa de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="670d2-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670d2-119">CommonParameters</span></span>
<span data-ttu-id="670d2-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670d2-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="670d2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670d2-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="670d2-122">INPUTS</span></span>

### <span data-ttu-id="670d2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="670d2-123">System.String</span></span>

## <span data-ttu-id="670d2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="670d2-124">OUTPUTS</span></span>

### <span data-ttu-id="670d2-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="670d2-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="670d2-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="670d2-126">NOTES</span></span>

## <span data-ttu-id="670d2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="670d2-127">RELATED LINKS</span></span>

[<span data-ttu-id="670d2-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="670d2-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)