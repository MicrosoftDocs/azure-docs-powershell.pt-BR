---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 6367910117ff00219c3194a06bb51754913df063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892804"
---
# <span data-ttu-id="568f1-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="568f1-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="568f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="568f1-102">SYNOPSIS</span></span>
<span data-ttu-id="568f1-103">Cria uma condição de regra de entrega.</span><span class="sxs-lookup"><span data-stu-id="568f1-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="568f1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="568f1-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="568f1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="568f1-105">DESCRIPTION</span></span>
<span data-ttu-id="568f1-106">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para a criação do ponto de extremidade cdn.</span><span class="sxs-lookup"><span data-stu-id="568f1-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="568f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="568f1-107">EXAMPLES</span></span>

### <span data-ttu-id="568f1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="568f1-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="568f1-109">Crie uma condição simples.</span><span class="sxs-lookup"><span data-stu-id="568f1-109">Create a simple condition.</span></span>

## <span data-ttu-id="568f1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="568f1-110">PARAMETERS</span></span>

### <span data-ttu-id="568f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568f1-111">-DefaultProfile</span></span>
<span data-ttu-id="568f1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="568f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="568f1-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="568f1-113">-MatchValue</span></span>
<span data-ttu-id="568f1-114">Lista de valores de combinação possíveis.</span><span class="sxs-lookup"><span data-stu-id="568f1-114">List of possible match values.</span></span>

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

### <span data-ttu-id="568f1-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="568f1-115">-MatchVariable</span></span>
<span data-ttu-id="568f1-116">Corresponder variável da condição.</span><span class="sxs-lookup"><span data-stu-id="568f1-116">Match variable of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568f1-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="568f1-117">-NegateCondition</span></span>
<span data-ttu-id="568f1-118">Descreve se o resultado dessa condição deve ser negado.</span><span class="sxs-lookup"><span data-stu-id="568f1-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568f1-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="568f1-119">-Operator</span></span>
<span data-ttu-id="568f1-120">Descreve o operador a ser matched</span><span class="sxs-lookup"><span data-stu-id="568f1-120">Describes operator to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568f1-121">-Seletor</span><span class="sxs-lookup"><span data-stu-id="568f1-121">-Selector</span></span>
<span data-ttu-id="568f1-122">Nome do Seletor a ser corresponder</span><span class="sxs-lookup"><span data-stu-id="568f1-122">Name of Selector to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568f1-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="568f1-123">-Transform</span></span>
<span data-ttu-id="568f1-124">Transforme para aplicar antes da correspondência.</span><span class="sxs-lookup"><span data-stu-id="568f1-124">Transform to apply before matching.</span></span>
<span data-ttu-id="568f1-125">Os valores possíveis são Minúsculas e Maiúsculas</span><span class="sxs-lookup"><span data-stu-id="568f1-125">Possible values are Lowercase and Uppercase</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568f1-126">CommonParameters</span></span>
<span data-ttu-id="568f1-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="568f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568f1-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="568f1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568f1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="568f1-129">INPUTS</span></span>

### <span data-ttu-id="568f1-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="568f1-130">None</span></span>

## <span data-ttu-id="568f1-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="568f1-131">OUTPUTS</span></span>

### <span data-ttu-id="568f1-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="568f1-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="568f1-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="568f1-133">NOTES</span></span>

## <span data-ttu-id="568f1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="568f1-134">RELATED LINKS</span></span>
