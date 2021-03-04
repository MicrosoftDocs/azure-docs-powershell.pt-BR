---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 4f8764a40d536897ee71e36c1be1d691040e2ab9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887747"
---
# <span data-ttu-id="081e2-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="081e2-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="081e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="081e2-102">SYNOPSIS</span></span>
<span data-ttu-id="081e2-103">Crie um objeto de exclusão de regra gerenciada para conjuntos de regras, grupos ou regras gerenciados do WAF.</span><span class="sxs-lookup"><span data-stu-id="081e2-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="081e2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="081e2-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="081e2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="081e2-105">DESCRIPTION</span></span>
<span data-ttu-id="081e2-106">Crie um objeto de exclusão de regra gerenciada para conjuntos de regras, grupos ou regras gerenciados do WAF.</span><span class="sxs-lookup"><span data-stu-id="081e2-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="081e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="081e2-107">EXAMPLES</span></span>

### <span data-ttu-id="081e2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="081e2-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="081e2-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="081e2-109">PARAMETERS</span></span>

### <span data-ttu-id="081e2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081e2-110">-DefaultProfile</span></span>
<span data-ttu-id="081e2-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="081e2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="081e2-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="081e2-112">-Operator</span></span>
<span data-ttu-id="081e2-113">Operador a ser usado ao corresponder ao seletor, EqualsAny significa nenhum seletor (todas as variáveis de correspondência do tipo especificado)</span><span class="sxs-lookup"><span data-stu-id="081e2-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="081e2-114">-Seletor</span><span class="sxs-lookup"><span data-stu-id="081e2-114">-Selector</span></span>
<span data-ttu-id="081e2-115">Padrão de seletor para corresponder usando o operador (se o operador não for EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="081e2-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="081e2-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="081e2-116">-Variable</span></span>
<span data-ttu-id="081e2-117">Variável match.</span><span class="sxs-lookup"><span data-stu-id="081e2-117">Match variable.</span></span> <span data-ttu-id="081e2-118">Os valores possíveis são RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="081e2-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="081e2-119">Por exemplo, QueryStringArgNames é uma exclusão dos parâmetros GET correspondentes ao seletor com o operador determinado.</span><span class="sxs-lookup"><span data-stu-id="081e2-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="081e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081e2-120">CommonParameters</span></span>
<span data-ttu-id="081e2-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081e2-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="081e2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081e2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="081e2-123">INPUTS</span></span>

### <span data-ttu-id="081e2-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="081e2-124">None</span></span>

## <span data-ttu-id="081e2-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="081e2-125">OUTPUTS</span></span>

### <span data-ttu-id="081e2-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="081e2-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="081e2-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="081e2-127">NOTES</span></span>

## <span data-ttu-id="081e2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="081e2-128">RELATED LINKS</span></span>

<span data-ttu-id="081e2-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="081e2-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
