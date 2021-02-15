---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111666"
---
# <span data-ttu-id="37c28-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="37c28-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="37c28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37c28-102">SYNOPSIS</span></span>
<span data-ttu-id="37c28-103">Cria uma condição de combinação para a regra personalizada</span><span class="sxs-lookup"><span data-stu-id="37c28-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="37c28-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37c28-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37c28-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="37c28-105">DESCRIPTION</span></span>
<span data-ttu-id="37c28-106">O **New-AzApplicationGatewayFirewallCondition** cria uma condição de combinação para a regra personalizada do firewall.</span><span class="sxs-lookup"><span data-stu-id="37c28-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="37c28-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37c28-107">EXAMPLES</span></span>

### <span data-ttu-id="37c28-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37c28-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="37c28-109">O comando cria uma nova condição de match usando a variável de match definida no $variable, o operador contém e a condição de negação é falsa, Transfroms incluindo minúsculas e corte, o valor de match é abc e cde.</span><span class="sxs-lookup"><span data-stu-id="37c28-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="37c28-110">A nova condição de combinação é salva no $condition.</span><span class="sxs-lookup"><span data-stu-id="37c28-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="37c28-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37c28-111">PARAMETERS</span></span>

### <span data-ttu-id="37c28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c28-112">-DefaultProfile</span></span>
<span data-ttu-id="37c28-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37c28-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c28-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="37c28-114">-MatchValue</span></span>
<span data-ttu-id="37c28-115">Valor de match.</span><span class="sxs-lookup"><span data-stu-id="37c28-115">Match value.</span></span>

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

### <span data-ttu-id="37c28-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="37c28-116">-MatchVariable</span></span>
<span data-ttu-id="37c28-117">Lista de variáveis de combinação.</span><span class="sxs-lookup"><span data-stu-id="37c28-117">List of match variables.</span></span>

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

### <span data-ttu-id="37c28-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="37c28-118">-NegationCondition</span></span>
<span data-ttu-id="37c28-119">Descreve se essa é uma condição negada ou não.</span><span class="sxs-lookup"><span data-stu-id="37c28-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="37c28-120">-Operador</span><span class="sxs-lookup"><span data-stu-id="37c28-120">-Operator</span></span>
<span data-ttu-id="37c28-121">Descreve o operador a ser corresponder.</span><span class="sxs-lookup"><span data-stu-id="37c28-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="37c28-122">-Transformar</span><span class="sxs-lookup"><span data-stu-id="37c28-122">-Transform</span></span>
<span data-ttu-id="37c28-123">Lista de transformação.</span><span class="sxs-lookup"><span data-stu-id="37c28-123">List of transforms.</span></span>

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

### <span data-ttu-id="37c28-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c28-124">CommonParameters</span></span>
<span data-ttu-id="37c28-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c28-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c28-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c28-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c28-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="37c28-127">INPUTS</span></span>

### <span data-ttu-id="37c28-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="37c28-128">None</span></span>

## <span data-ttu-id="37c28-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="37c28-129">OUTPUTS</span></span>

### <span data-ttu-id="37c28-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="37c28-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="37c28-131">Notas</span><span class="sxs-lookup"><span data-stu-id="37c28-131">NOTES</span></span>

## <span data-ttu-id="37c28-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37c28-132">RELATED LINKS</span></span>
