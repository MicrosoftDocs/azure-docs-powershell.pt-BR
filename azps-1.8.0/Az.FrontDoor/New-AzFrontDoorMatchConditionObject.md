---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770849"
---
# <span data-ttu-id="b2e17-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="b2e17-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="b2e17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2e17-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e17-103">Criar objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="b2e17-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="b2e17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2e17-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2e17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2e17-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e17-106">Criar objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="b2e17-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="b2e17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2e17-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e17-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2e17-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="b2e17-109">Criar um objeto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="b2e17-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="b2e17-110">OS</span><span class="sxs-lookup"><span data-stu-id="b2e17-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e17-111">-DefaultProfile</span></span>
<span data-ttu-id="b2e17-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e17-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e17-113">-Matchvalue</span><span class="sxs-lookup"><span data-stu-id="b2e17-113">-MatchValue</span></span>
<span data-ttu-id="b2e17-114">Valor correspondente.</span><span class="sxs-lookup"><span data-stu-id="b2e17-114">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="b2e17-115">-MatchVariable</span></span>
<span data-ttu-id="b2e17-116">Corresponder variável.</span><span class="sxs-lookup"><span data-stu-id="b2e17-116">Match Variable.</span></span>
<span data-ttu-id="b2e17-117">Os valores possíveis incluem: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' createargs ', ' RequestUri ', ' RequestHeader ', ' RequestBody '</span><span class="sxs-lookup"><span data-stu-id="b2e17-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="b2e17-118">-NegateCondition</span></span>
<span data-ttu-id="b2e17-119">Descreve se a condição é negação ou o valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="b2e17-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="b2e17-120">-Operatorproperty</span><span class="sxs-lookup"><span data-stu-id="b2e17-120">-OperatorProperty</span></span>
<span data-ttu-id="b2e17-121">Descreve o operador a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="b2e17-121">Describes operator to be matched.</span></span>
<span data-ttu-id="b2e17-122">Os valores possíveis incluem: ' any ', ' IPMatch ', ' geomatch ', ' EQUAL ', ' GreaterThanOrEqual ', ' começa ', ' EndsWith ', ' LessThanOrEqual ', ' ', ' ', ' EndsWith ' '</span><span class="sxs-lookup"><span data-stu-id="b2e17-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-123">-Seletor</span><span class="sxs-lookup"><span data-stu-id="b2e17-123">-Selector</span></span>
<span data-ttu-id="b2e17-124">Nome do seletor em RequestHeader ou RequestBody para ser correspondido</span><span class="sxs-lookup"><span data-stu-id="b2e17-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="b2e17-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e17-125">CommonParameters</span></span>
<span data-ttu-id="b2e17-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e17-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e17-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2e17-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e17-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2e17-128">INPUTS</span></span>

### <span data-ttu-id="b2e17-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b2e17-129">None</span></span>

## <span data-ttu-id="b2e17-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2e17-130">OUTPUTS</span></span>

### <span data-ttu-id="b2e17-131">Microsoft. Azure. Commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="b2e17-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="b2e17-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2e17-132">NOTES</span></span>

## <span data-ttu-id="b2e17-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2e17-133">RELATED LINKS</span></span>

[<span data-ttu-id="b2e17-134">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="b2e17-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
