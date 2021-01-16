---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263932"
---
# <span data-ttu-id="6fd3b-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="6fd3b-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="6fd3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd3b-103">Criar objeto de exclusão de regra gerenciada para conjuntos de regras, grupos ou regras gerenciados WAF.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="6fd3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fd3b-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fd3b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fd3b-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd3b-106">Criar objeto de exclusão de regra gerenciada para conjuntos de regras, grupos ou regras gerenciados WAF.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="6fd3b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fd3b-107">EXAMPLES</span></span>

### <span data-ttu-id="6fd3b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6fd3b-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="6fd3b-109">OS</span><span class="sxs-lookup"><span data-stu-id="6fd3b-109">PARAMETERS</span></span>

### <span data-ttu-id="6fd3b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd3b-110">-DefaultProfile</span></span>
<span data-ttu-id="6fd3b-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd3b-112">-Operador</span><span class="sxs-lookup"><span data-stu-id="6fd3b-112">-Operator</span></span>
<span data-ttu-id="6fd3b-113">Operador a ser usado quando corresponder ao seletor, EqualsAny significa sem seletor (todas as variáveis de correspondência do tipo especificado)</span><span class="sxs-lookup"><span data-stu-id="6fd3b-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="6fd3b-114">-Seletor</span><span class="sxs-lookup"><span data-stu-id="6fd3b-114">-Selector</span></span>
<span data-ttu-id="6fd3b-115">Padrão do seletor para corresponder usando o operador (se o operador não for EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="6fd3b-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="6fd3b-116">-Variável</span><span class="sxs-lookup"><span data-stu-id="6fd3b-116">-Variable</span></span>
<span data-ttu-id="6fd3b-117">Corresponder variável.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-117">Match variable.</span></span> <span data-ttu-id="6fd3b-118">Os valores possíveis são RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="6fd3b-119">Por exemplo, QueryStringArgNames é uma exclusão de parâmetros GET que correspondem ao seletor com o operador fornecido.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="6fd3b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd3b-120">CommonParameters</span></span>
<span data-ttu-id="6fd3b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd3b-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fd3b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd3b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fd3b-123">INPUTS</span></span>

### <span data-ttu-id="6fd3b-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6fd3b-124">None</span></span>

## <span data-ttu-id="6fd3b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fd3b-125">OUTPUTS</span></span>

### <span data-ttu-id="6fd3b-126">Microsoft. Azure. Commands. FrontDoor. Models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="6fd3b-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="6fd3b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fd3b-127">NOTES</span></span>

## <span data-ttu-id="6fd3b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fd3b-128">RELATED LINKS</span></span>

<span data-ttu-id="6fd3b-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="6fd3b-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
