---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116789"
---
# <span data-ttu-id="2d38e-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2d38e-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="2d38e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d38e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d38e-103">Crie um objeto PSRulesEngineMatchCondition para criar uma regra de mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="2d38e-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="2d38e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d38e-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d38e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d38e-105">DESCRIPTION</span></span>
<span data-ttu-id="2d38e-106">Crie um objeto PSRulesEngineMatchCondition para criar uma regra de mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="2d38e-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="2d38e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d38e-107">EXAMPLES</span></span>

### <span data-ttu-id="2d38e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d38e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="2d38e-109">Greate a new PSRulesEngineMatchCondition object.</span><span class="sxs-lookup"><span data-stu-id="2d38e-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="2d38e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d38e-110">PARAMETERS</span></span>

### <span data-ttu-id="2d38e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d38e-111">-DefaultProfile</span></span>
<span data-ttu-id="2d38e-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d38e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d38e-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="2d38e-113">-MatchValue</span></span>
<span data-ttu-id="2d38e-114">Corresponder valores para corresponder.</span><span class="sxs-lookup"><span data-stu-id="2d38e-114">Match values to match against.</span></span>
<span data-ttu-id="2d38e-115">O operador será aplicado a cada valor aqui com semântica OU.</span><span class="sxs-lookup"><span data-stu-id="2d38e-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="2d38e-116">Se algum deles corresponder à variável com o operador determinado, essa condição de match será considerada uma combinação.</span><span class="sxs-lookup"><span data-stu-id="2d38e-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="2d38e-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="2d38e-117">-MatchVariable</span></span>
<span data-ttu-id="2d38e-118">Corresponder Variável.</span><span class="sxs-lookup"><span data-stu-id="2d38e-118">Match Variable.</span></span>
<span data-ttu-id="2d38e-119">Os valores possíveis são IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestFile, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="2d38e-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d38e-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="2d38e-120">-NegateCondition</span></span>
<span data-ttu-id="2d38e-121">Descreve se essa é uma condição negada ou não</span><span class="sxs-lookup"><span data-stu-id="2d38e-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="2d38e-122">-Operador</span><span class="sxs-lookup"><span data-stu-id="2d38e-122">-Operator</span></span>
<span data-ttu-id="2d38e-123">Descreve o operador a ser aplicado à condição de combinação.</span><span class="sxs-lookup"><span data-stu-id="2d38e-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="2d38e-124">Os valores possíveis são Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="2d38e-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d38e-125">-Seletor</span><span class="sxs-lookup"><span data-stu-id="2d38e-125">-Selector</span></span>
<span data-ttu-id="2d38e-126">Nome do seletor no RequestHeader ou RequestHeader para ser corresponder</span><span class="sxs-lookup"><span data-stu-id="2d38e-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="2d38e-127">-Transformar</span><span class="sxs-lookup"><span data-stu-id="2d38e-127">-Transform</span></span>
<span data-ttu-id="2d38e-128">Lista de quais transformaçãos são aplicadas antes da correspondência.</span><span class="sxs-lookup"><span data-stu-id="2d38e-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="2d38e-129">Possíveis valores de transformação individual são Minúsculas, Maiúsculas, Cortar, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="2d38e-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d38e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d38e-130">CommonParameters</span></span>
<span data-ttu-id="2d38e-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d38e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d38e-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d38e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d38e-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="2d38e-133">INPUTS</span></span>

### <span data-ttu-id="2d38e-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2d38e-134">None</span></span>

## <span data-ttu-id="2d38e-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="2d38e-135">OUTPUTS</span></span>

### <span data-ttu-id="2d38e-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="2d38e-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="2d38e-137">Notas</span><span class="sxs-lookup"><span data-stu-id="2d38e-137">NOTES</span></span>

## <span data-ttu-id="2d38e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d38e-138">RELATED LINKS</span></span>
