---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111881"
---
# <span data-ttu-id="40c36-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="40c36-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="40c36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40c36-102">SYNOPSIS</span></span>
<span data-ttu-id="40c36-103">Crie um objeto PSRulesEngineRule para criação do Mecanismo de Regras.</span><span class="sxs-lookup"><span data-stu-id="40c36-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="40c36-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40c36-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40c36-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="40c36-105">DESCRIPTION</span></span>
<span data-ttu-id="40c36-106">Crie um objeto PSRulesEngineRule para criação do Mecanismo de Regras.</span><span class="sxs-lookup"><span data-stu-id="40c36-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="40c36-107">Use o cmdlet "New-AzFrontDoorRulesEngineActionObject" para criar um objeto PSRulesEngineAction para passar para o parâmetro "-Ação".</span><span class="sxs-lookup"><span data-stu-id="40c36-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="40c36-108">Use o cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" para criar o objeto PSRulesEngineMatchCondition para passar para o parâmetro "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="40c36-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="40c36-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40c36-109">EXAMPLES</span></span>

### <span data-ttu-id="40c36-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40c36-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="40c36-111">Crie um novo objeto PSRulesEngineRule e demonstre como ver os subcampos.</span><span class="sxs-lookup"><span data-stu-id="40c36-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="40c36-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="40c36-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="40c36-113">Espere a saída ao passar em um valor de prioridade inválido.</span><span class="sxs-lookup"><span data-stu-id="40c36-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="40c36-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40c36-114">PARAMETERS</span></span>

### <span data-ttu-id="40c36-115">-Ação</span><span class="sxs-lookup"><span data-stu-id="40c36-115">-Action</span></span>
<span data-ttu-id="40c36-116">Ações a executar na solicitação e resposta se todas as condições de match são atendidas.</span><span class="sxs-lookup"><span data-stu-id="40c36-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c36-117">-DefaultProfile</span></span>
<span data-ttu-id="40c36-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40c36-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40c36-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="40c36-119">-MatchCondition</span></span>
<span data-ttu-id="40c36-120">Uma lista de condições de combinação que deve atender para que as ações desta regra seja executado.</span><span class="sxs-lookup"><span data-stu-id="40c36-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="40c36-121">Não ter condições de combinação significa que as ações sempre serão executados.</span><span class="sxs-lookup"><span data-stu-id="40c36-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c36-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="40c36-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="40c36-123">Se essa regra for uma combinação, o mecanismo de regras deverá continuar executando as regras restantes ou parar.</span><span class="sxs-lookup"><span data-stu-id="40c36-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="40c36-124">Os valores possíveis são Continuar e Parar.</span><span class="sxs-lookup"><span data-stu-id="40c36-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="40c36-125">Se não estiver presente, o padrão é Continuar.</span><span class="sxs-lookup"><span data-stu-id="40c36-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c36-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="40c36-126">-Name</span></span>
<span data-ttu-id="40c36-127">Um nome para se referir a essa regra específica.</span><span class="sxs-lookup"><span data-stu-id="40c36-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="40c36-128">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="40c36-128">-Priority</span></span>
<span data-ttu-id="40c36-129">Uma prioridade atribuída a essa regra.</span><span class="sxs-lookup"><span data-stu-id="40c36-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="40c36-130">Não pode ser negativo.</span><span class="sxs-lookup"><span data-stu-id="40c36-130">Cannot be negative.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c36-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c36-131">CommonParameters</span></span>
<span data-ttu-id="40c36-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c36-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c36-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40c36-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c36-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="40c36-134">INPUTS</span></span>

### <span data-ttu-id="40c36-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="40c36-135">None</span></span>

## <span data-ttu-id="40c36-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="40c36-136">OUTPUTS</span></span>

### <span data-ttu-id="40c36-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="40c36-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="40c36-138">Notas</span><span class="sxs-lookup"><span data-stu-id="40c36-138">NOTES</span></span>

## <span data-ttu-id="40c36-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40c36-139">RELATED LINKS</span></span>
