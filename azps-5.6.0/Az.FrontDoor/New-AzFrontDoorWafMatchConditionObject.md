---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: e67841073d6c7342e0bb88c52809a9c45d92f82f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887741"
---
# <span data-ttu-id="5df80-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5df80-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="5df80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5df80-102">SYNOPSIS</span></span>
<span data-ttu-id="5df80-103">Criar Objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="5df80-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="5df80-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5df80-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5df80-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5df80-105">DESCRIPTION</span></span>
<span data-ttu-id="5df80-106">Criar Objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="5df80-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="5df80-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5df80-107">EXAMPLES</span></span>

### <span data-ttu-id="5df80-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5df80-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="5df80-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5df80-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="5df80-110">Criar um objeto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="5df80-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="5df80-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5df80-111">PARAMETERS</span></span>

### <span data-ttu-id="5df80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df80-112">-DefaultProfile</span></span>
<span data-ttu-id="5df80-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5df80-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df80-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="5df80-114">-MatchValue</span></span>
<span data-ttu-id="5df80-115">Valor de match.</span><span class="sxs-lookup"><span data-stu-id="5df80-115">Match value.</span></span>

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

### <span data-ttu-id="5df80-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="5df80-116">-MatchVariable</span></span>
<span data-ttu-id="5df80-117">Match Variable.</span><span class="sxs-lookup"><span data-stu-id="5df80-117">Match Variable.</span></span>
<span data-ttu-id="5df80-118">Os valores possíveis incluem: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="5df80-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="5df80-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="5df80-119">-NegateCondition</span></span>
<span data-ttu-id="5df80-120">Descreve se essa condição é negada ou não O valor padrão é false</span><span class="sxs-lookup"><span data-stu-id="5df80-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="5df80-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="5df80-121">-OperatorProperty</span></span>
<span data-ttu-id="5df80-122">Descreve o operador a ser matched.</span><span class="sxs-lookup"><span data-stu-id="5df80-122">Describes operator to be matched.</span></span>
<span data-ttu-id="5df80-123">Os valores possíveis incluem: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="5df80-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="5df80-124">-Seletor</span><span class="sxs-lookup"><span data-stu-id="5df80-124">-Selector</span></span>
<span data-ttu-id="5df80-125">Nome do seletor em RequestHeader ou RequestBody a ser matched</span><span class="sxs-lookup"><span data-stu-id="5df80-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="5df80-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="5df80-126">-Transform</span></span>
<span data-ttu-id="5df80-127">Transforma-se para aplicar.</span><span class="sxs-lookup"><span data-stu-id="5df80-127">Transforms to apply.</span></span> <span data-ttu-id="5df80-128">Os valores possíveis incluem: 'Minúscula', 'Maiúscula', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span><span class="sxs-lookup"><span data-stu-id="5df80-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="5df80-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df80-129">CommonParameters</span></span>
<span data-ttu-id="5df80-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df80-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df80-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5df80-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df80-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5df80-132">INPUTS</span></span>

### <span data-ttu-id="5df80-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5df80-133">None</span></span>

## <span data-ttu-id="5df80-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5df80-134">OUTPUTS</span></span>

### <span data-ttu-id="5df80-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="5df80-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="5df80-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="5df80-136">NOTES</span></span>

## <span data-ttu-id="5df80-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5df80-137">RELATED LINKS</span></span>

[<span data-ttu-id="5df80-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="5df80-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
