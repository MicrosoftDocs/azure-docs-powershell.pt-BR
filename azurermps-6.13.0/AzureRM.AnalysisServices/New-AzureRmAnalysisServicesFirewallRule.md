---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 2a47c97ea189d4064edae7a871e21465d866f1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429622"
---
# <span data-ttu-id="6bda3-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6bda3-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="6bda3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bda3-102">SYNOPSIS</span></span>
<span data-ttu-id="6bda3-103">Cria uma nova regra de firewall do Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6bda3-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bda3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bda3-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String>
 [-RangeEnd] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bda3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6bda3-105">DESCRIPTION</span></span>
<span data-ttu-id="6bda3-106">O New-AzureRmAnalysisServicesFirewallRule cria um novo objeto de regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="6bda3-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="6bda3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bda3-107">EXAMPLES</span></span>

### <span data-ttu-id="6bda3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6bda3-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="6bda3-109">Cria uma regra de firewall chamada rule1 com o intervalo de início 0.0.0.0 e o intervalo de término 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="6bda3-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="6bda3-110">OS</span><span class="sxs-lookup"><span data-stu-id="6bda3-110">PARAMETERS</span></span>

### <span data-ttu-id="6bda3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bda3-111">-DefaultProfile</span></span>
<span data-ttu-id="6bda3-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bda3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bda3-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="6bda3-113">-FirewallRuleName</span></span>
<span data-ttu-id="6bda3-114">Nome da regra de firewall</span><span class="sxs-lookup"><span data-stu-id="6bda3-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="6bda3-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="6bda3-115">-RangeEnd</span></span>
<span data-ttu-id="6bda3-116">O final do intervalo de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="6bda3-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="6bda3-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="6bda3-117">-RangeStart</span></span>
<span data-ttu-id="6bda3-118">O início da faixa de uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="6bda3-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="6bda3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bda3-119">CommonParameters</span></span>
<span data-ttu-id="6bda3-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bda3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bda3-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bda3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bda3-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6bda3-122">INPUTS</span></span>

### <span data-ttu-id="6bda3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6bda3-123">System.String</span></span>

## <span data-ttu-id="6bda3-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6bda3-124">OUTPUTS</span></span>

### <span data-ttu-id="6bda3-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6bda3-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="6bda3-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6bda3-126">NOTES</span></span>

## <span data-ttu-id="6bda3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bda3-127">RELATED LINKS</span></span>

[<span data-ttu-id="6bda3-128">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="6bda3-128">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
