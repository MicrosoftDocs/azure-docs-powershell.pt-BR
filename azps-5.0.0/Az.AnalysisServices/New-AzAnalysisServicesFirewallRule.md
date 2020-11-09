---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282302"
---
# <span data-ttu-id="aacce-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="aacce-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="aacce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aacce-102">SYNOPSIS</span></span>
<span data-ttu-id="aacce-103">Cria uma nova regra de firewall do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="aacce-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="aacce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aacce-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aacce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aacce-105">DESCRIPTION</span></span>
<span data-ttu-id="aacce-106">O New-AzAnalysisServicesFirewallRule cria um novo objeto de regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="aacce-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="aacce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aacce-107">EXAMPLES</span></span>

### <span data-ttu-id="aacce-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aacce-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="aacce-109">Cria uma regra de firewall chamada rule1 com o intervalo de início 0.0.0.0 e o intervalo de término 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="aacce-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="aacce-110">OS</span><span class="sxs-lookup"><span data-stu-id="aacce-110">PARAMETERS</span></span>

### <span data-ttu-id="aacce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacce-111">-DefaultProfile</span></span>
<span data-ttu-id="aacce-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aacce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aacce-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="aacce-113">-FirewallRuleName</span></span>
<span data-ttu-id="aacce-114">Nome da regra de firewall</span><span class="sxs-lookup"><span data-stu-id="aacce-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="aacce-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="aacce-115">-RangeEnd</span></span>
<span data-ttu-id="aacce-116">O final do intervalo de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="aacce-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="aacce-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="aacce-117">-RangeStart</span></span>
<span data-ttu-id="aacce-118">O início da faixa de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="aacce-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="aacce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacce-119">CommonParameters</span></span>
<span data-ttu-id="aacce-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aacce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacce-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aacce-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacce-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aacce-122">INPUTS</span></span>

### <span data-ttu-id="aacce-123">System. String</span><span class="sxs-lookup"><span data-stu-id="aacce-123">System.String</span></span>

## <span data-ttu-id="aacce-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aacce-124">OUTPUTS</span></span>

### <span data-ttu-id="aacce-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="aacce-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="aacce-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aacce-126">NOTES</span></span>

## <span data-ttu-id="aacce-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aacce-127">RELATED LINKS</span></span>

[<span data-ttu-id="aacce-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="aacce-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)