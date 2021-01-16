---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257508"
---
# <span data-ttu-id="67753-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="67753-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="67753-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67753-102">SYNOPSIS</span></span>
<span data-ttu-id="67753-103">Crie um objeto PSRulesEngineRule para a criação do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="67753-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="67753-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67753-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67753-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67753-105">DESCRIPTION</span></span>
<span data-ttu-id="67753-106">Crie um objeto PSRulesEngineRule para a criação do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="67753-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="67753-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" para criar um objeto PSRulesEngineAction para passar para o parâmetro "-Action".</span><span class="sxs-lookup"><span data-stu-id="67753-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="67753-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" para criar um objeto PSRulesEngineMatchCondition para passar para o parâmetro "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="67753-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="67753-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67753-109">EXAMPLES</span></span>

### <span data-ttu-id="67753-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67753-110">Example 1</span></span>
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

<span data-ttu-id="67753-111">Crie um novo objeto PSRulesEngineRule e demonstre como Ver os subcampos.</span><span class="sxs-lookup"><span data-stu-id="67753-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="67753-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="67753-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="67753-113">Esperar saída ao transmitir um valor de prioridade inválido.</span><span class="sxs-lookup"><span data-stu-id="67753-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="67753-114">OS</span><span class="sxs-lookup"><span data-stu-id="67753-114">PARAMETERS</span></span>

### <span data-ttu-id="67753-115">-Ação</span><span class="sxs-lookup"><span data-stu-id="67753-115">-Action</span></span>
<span data-ttu-id="67753-116">Ações a serem executadas na solicitação e na resposta se todas as condições de correspondência forem atendidas.</span><span class="sxs-lookup"><span data-stu-id="67753-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

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

### <span data-ttu-id="67753-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67753-117">-DefaultProfile</span></span>
<span data-ttu-id="67753-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67753-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67753-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="67753-119">-MatchCondition</span></span>
<span data-ttu-id="67753-120">Uma lista de condições de correspondência que devem ser cumpridas para que as ações desta regra sejam executadas.</span><span class="sxs-lookup"><span data-stu-id="67753-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="67753-121">Sem nenhuma condição de correspondência significa que as ações serão sempre executadas.</span><span class="sxs-lookup"><span data-stu-id="67753-121">Having no match conditions means the actions will always run.</span></span>

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

### <span data-ttu-id="67753-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="67753-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="67753-123">Se essa regra for uma correspondência, o mecanismo de regras continuará executando as regras restantes ou será interrompido.</span><span class="sxs-lookup"><span data-stu-id="67753-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="67753-124">Os valores possíveis são Continue e pare.</span><span class="sxs-lookup"><span data-stu-id="67753-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="67753-125">Se não estiver presente, o padrão será continuar.</span><span class="sxs-lookup"><span data-stu-id="67753-125">If not present, defaults to Continue.</span></span>

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

### <span data-ttu-id="67753-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="67753-126">-Name</span></span>
<span data-ttu-id="67753-127">Um nome para se referir a essa regra específica.</span><span class="sxs-lookup"><span data-stu-id="67753-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="67753-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="67753-128">-Priority</span></span>
<span data-ttu-id="67753-129">Uma prioridade atribuída a essa regra.</span><span class="sxs-lookup"><span data-stu-id="67753-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="67753-130">Não pode ser negativo.</span><span class="sxs-lookup"><span data-stu-id="67753-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="67753-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67753-131">CommonParameters</span></span>
<span data-ttu-id="67753-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67753-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67753-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67753-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67753-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67753-134">INPUTS</span></span>

### <span data-ttu-id="67753-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="67753-135">None</span></span>

## <span data-ttu-id="67753-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67753-136">OUTPUTS</span></span>

### <span data-ttu-id="67753-137">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="67753-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="67753-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67753-138">NOTES</span></span>

## <span data-ttu-id="67753-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67753-139">RELATED LINKS</span></span>
