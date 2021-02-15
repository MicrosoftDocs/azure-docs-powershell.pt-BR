---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111876"
---
# <span data-ttu-id="b34da-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="b34da-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="b34da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b34da-102">SYNOPSIS</span></span>
<span data-ttu-id="b34da-103">Crie um objeto de exclusão de regra gerenciado para conjuntos de regras gerenciados pelo WAF, grupos ou regras.</span><span class="sxs-lookup"><span data-stu-id="b34da-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="b34da-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b34da-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b34da-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b34da-105">DESCRIPTION</span></span>
<span data-ttu-id="b34da-106">Crie um objeto de exclusão de regra gerenciado para conjuntos de regras gerenciados pelo WAF, grupos ou regras.</span><span class="sxs-lookup"><span data-stu-id="b34da-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="b34da-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b34da-107">EXAMPLES</span></span>

### <span data-ttu-id="b34da-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b34da-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="b34da-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b34da-109">PARAMETERS</span></span>

### <span data-ttu-id="b34da-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34da-110">-DefaultProfile</span></span>
<span data-ttu-id="b34da-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b34da-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b34da-112">-Operador</span><span class="sxs-lookup"><span data-stu-id="b34da-112">-Operator</span></span>
<span data-ttu-id="b34da-113">Operador a ser usado ao corresponder ao seletor, Igual aAny significa nenhum seletor (todas as variáveis correspondentes do tipo especificado)</span><span class="sxs-lookup"><span data-stu-id="b34da-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="b34da-114">-Seletor</span><span class="sxs-lookup"><span data-stu-id="b34da-114">-Selector</span></span>
<span data-ttu-id="b34da-115">Padrão de seletor para corresponder usando o operador (se o operador não for Igual aAny)</span><span class="sxs-lookup"><span data-stu-id="b34da-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="b34da-116">-Variável</span><span class="sxs-lookup"><span data-stu-id="b34da-116">-Variable</span></span>
<span data-ttu-id="b34da-117">Corresponder variável.</span><span class="sxs-lookup"><span data-stu-id="b34da-117">Match variable.</span></span> <span data-ttu-id="b34da-118">Os valores possíveis são RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestOokiePostArgNames.</span><span class="sxs-lookup"><span data-stu-id="b34da-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="b34da-119">Por exemplo, QueryStringArgNames é uma exclusão dos parâmetros GET que coincidem com o seletor com o operador determinado.</span><span class="sxs-lookup"><span data-stu-id="b34da-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="b34da-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34da-120">CommonParameters</span></span>
<span data-ttu-id="b34da-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34da-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34da-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b34da-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34da-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="b34da-123">INPUTS</span></span>

### <span data-ttu-id="b34da-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b34da-124">None</span></span>

## <span data-ttu-id="b34da-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="b34da-125">OUTPUTS</span></span>

### <span data-ttu-id="b34da-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="b34da-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="b34da-127">Notas</span><span class="sxs-lookup"><span data-stu-id="b34da-127">NOTES</span></span>

## <span data-ttu-id="b34da-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b34da-128">RELATED LINKS</span></span>

<span data-ttu-id="b34da-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="b34da-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
