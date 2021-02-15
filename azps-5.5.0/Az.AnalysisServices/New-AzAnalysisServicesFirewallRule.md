---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112318"
---
# <span data-ttu-id="b247e-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b247e-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="b247e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b247e-102">SYNOPSIS</span></span>
<span data-ttu-id="b247e-103">Cria uma nova regra de firewall do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b247e-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="b247e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b247e-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b247e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b247e-105">DESCRIPTION</span></span>
<span data-ttu-id="b247e-106">A New-AzAnalysisServicesFirewallRule cria um novo objeto de regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="b247e-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="b247e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b247e-107">EXAMPLES</span></span>

### <span data-ttu-id="b247e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b247e-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="b247e-109">Cria uma regra de firewall chamada regra1 com o intervalo inicial 0.0.0.0 e o intervalo final 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="b247e-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="b247e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b247e-110">PARAMETERS</span></span>

### <span data-ttu-id="b247e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b247e-111">-DefaultProfile</span></span>
<span data-ttu-id="b247e-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b247e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b247e-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b247e-113">-FirewallRuleName</span></span>
<span data-ttu-id="b247e-114">Nome da regra de firewall</span><span class="sxs-lookup"><span data-stu-id="b247e-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="b247e-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="b247e-115">-RangeEnd</span></span>
<span data-ttu-id="b247e-116">O fim do intervalo de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="b247e-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="b247e-117">-Início do Intervalo</span><span class="sxs-lookup"><span data-stu-id="b247e-117">-RangeStart</span></span>
<span data-ttu-id="b247e-118">O início do intervalo de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="b247e-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="b247e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b247e-119">CommonParameters</span></span>
<span data-ttu-id="b247e-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b247e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b247e-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b247e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b247e-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="b247e-122">INPUTS</span></span>

### <span data-ttu-id="b247e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b247e-123">System.String</span></span>

## <span data-ttu-id="b247e-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="b247e-124">OUTPUTS</span></span>

### <span data-ttu-id="b247e-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b247e-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="b247e-126">Notas</span><span class="sxs-lookup"><span data-stu-id="b247e-126">NOTES</span></span>

## <span data-ttu-id="b247e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b247e-127">RELATED LINKS</span></span>

[<span data-ttu-id="b247e-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="b247e-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)