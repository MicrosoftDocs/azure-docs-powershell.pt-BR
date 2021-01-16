---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428526"
---
# <span data-ttu-id="a84ff-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="a84ff-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="a84ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a84ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a84ff-103">Cria uma condição de correspondência para a regra personalizada</span><span class="sxs-lookup"><span data-stu-id="a84ff-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="a84ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a84ff-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a84ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a84ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a84ff-106">O **New-AzApplicationGatewayFirewallCondition** cria uma condição match para a regra personalizada do firewall.</span><span class="sxs-lookup"><span data-stu-id="a84ff-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="a84ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a84ff-107">EXAMPLES</span></span>

### <span data-ttu-id="a84ff-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a84ff-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="a84ff-109">O comando cria uma nova condição de correspondência usando a variável Match definida no $variable, o operador é contém e a condição de negação é falsa, transvariando incluindo lowercase e Trim, o valor match é ABC e CDE.</span><span class="sxs-lookup"><span data-stu-id="a84ff-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="a84ff-110">A nova condição de correspondência é salva em $condition.</span><span class="sxs-lookup"><span data-stu-id="a84ff-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="a84ff-111">OS</span><span class="sxs-lookup"><span data-stu-id="a84ff-111">PARAMETERS</span></span>

### <span data-ttu-id="a84ff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84ff-112">-DefaultProfile</span></span>
<span data-ttu-id="a84ff-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a84ff-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a84ff-114">-Matchvalue</span><span class="sxs-lookup"><span data-stu-id="a84ff-114">-MatchValue</span></span>
<span data-ttu-id="a84ff-115">Valor correspondente.</span><span class="sxs-lookup"><span data-stu-id="a84ff-115">Match value.</span></span>

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

### <span data-ttu-id="a84ff-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="a84ff-116">-MatchVariable</span></span>
<span data-ttu-id="a84ff-117">Lista de variáveis de correspondência.</span><span class="sxs-lookup"><span data-stu-id="a84ff-117">List of match variables.</span></span>

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

### <span data-ttu-id="a84ff-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="a84ff-118">-NegationCondition</span></span>
<span data-ttu-id="a84ff-119">Descreve se essa condição é negação ou não.</span><span class="sxs-lookup"><span data-stu-id="a84ff-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="a84ff-120">-Operador</span><span class="sxs-lookup"><span data-stu-id="a84ff-120">-Operator</span></span>
<span data-ttu-id="a84ff-121">Descreve o operador a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="a84ff-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="a84ff-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="a84ff-122">-Transform</span></span>
<span data-ttu-id="a84ff-123">Lista de transformações.</span><span class="sxs-lookup"><span data-stu-id="a84ff-123">List of transforms.</span></span>

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

### <span data-ttu-id="a84ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84ff-124">CommonParameters</span></span>
<span data-ttu-id="a84ff-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84ff-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a84ff-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84ff-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a84ff-127">INPUTS</span></span>

### <span data-ttu-id="a84ff-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a84ff-128">None</span></span>

## <span data-ttu-id="a84ff-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a84ff-129">OUTPUTS</span></span>

### <span data-ttu-id="a84ff-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="a84ff-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="a84ff-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a84ff-131">NOTES</span></span>

## <span data-ttu-id="a84ff-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a84ff-132">RELATED LINKS</span></span>
