---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 096fb182ae330750eeb23e365bc929edb17b21f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892620"
---
# <span data-ttu-id="3c664-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="3c664-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="3c664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c664-102">SYNOPSIS</span></span>
<span data-ttu-id="3c664-103">Cria uma condição de match para regra personalizada</span><span class="sxs-lookup"><span data-stu-id="3c664-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="3c664-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3c664-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c664-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3c664-105">DESCRIPTION</span></span>
<span data-ttu-id="3c664-106">O **New-AzApplicationGatewayFirewallCondition** cria uma condição de match para a regra personalizada do firewall.</span><span class="sxs-lookup"><span data-stu-id="3c664-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="3c664-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c664-107">EXAMPLES</span></span>

### <span data-ttu-id="3c664-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c664-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="3c664-109">O comando cria uma nova condição de match usando a variável match definida no $variable, o operador é Contains e a condição de negação é false, Transfroms incluindo minúsculas e corte, o valor de match é abc e cde.</span><span class="sxs-lookup"><span data-stu-id="3c664-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="3c664-110">A nova condição de match é salva $condition.</span><span class="sxs-lookup"><span data-stu-id="3c664-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="3c664-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3c664-111">PARAMETERS</span></span>

### <span data-ttu-id="3c664-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c664-112">-DefaultProfile</span></span>
<span data-ttu-id="3c664-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c664-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c664-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="3c664-114">-MatchValue</span></span>
<span data-ttu-id="3c664-115">Valor de match.</span><span class="sxs-lookup"><span data-stu-id="3c664-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c664-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="3c664-116">-MatchVariable</span></span>
<span data-ttu-id="3c664-117">Lista de variáveis de combinação.</span><span class="sxs-lookup"><span data-stu-id="3c664-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c664-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="3c664-118">-NegationCondition</span></span>
<span data-ttu-id="3c664-119">Descreve se essa condição é negada ou não.</span><span class="sxs-lookup"><span data-stu-id="3c664-119">Describes if this is negate condition or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c664-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="3c664-120">-Operator</span></span>
<span data-ttu-id="3c664-121">Descreve o operador a ser matched.</span><span class="sxs-lookup"><span data-stu-id="3c664-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c664-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="3c664-122">-Transform</span></span>
<span data-ttu-id="3c664-123">Lista de transformação.</span><span class="sxs-lookup"><span data-stu-id="3c664-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c664-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c664-124">CommonParameters</span></span>
<span data-ttu-id="3c664-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c664-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c664-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c664-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c664-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c664-127">INPUTS</span></span>

### <span data-ttu-id="3c664-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3c664-128">None</span></span>

## <span data-ttu-id="3c664-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3c664-129">OUTPUTS</span></span>

### <span data-ttu-id="3c664-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="3c664-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="3c664-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="3c664-131">NOTES</span></span>

## <span data-ttu-id="3c664-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c664-132">RELATED LINKS</span></span>
