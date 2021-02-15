---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113821"
---
# <span data-ttu-id="73367-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="73367-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="73367-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73367-102">SYNOPSIS</span></span>
<span data-ttu-id="73367-103">Criar Objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="73367-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="73367-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73367-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73367-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="73367-105">DESCRIPTION</span></span>
<span data-ttu-id="73367-106">Criar Objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="73367-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="73367-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73367-107">EXAMPLES</span></span>

### <span data-ttu-id="73367-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73367-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="73367-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="73367-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="73367-110">Criar um objeto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="73367-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="73367-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73367-111">PARAMETERS</span></span>

### <span data-ttu-id="73367-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73367-112">-DefaultProfile</span></span>
<span data-ttu-id="73367-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73367-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73367-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="73367-114">-MatchValue</span></span>
<span data-ttu-id="73367-115">Valor de match.</span><span class="sxs-lookup"><span data-stu-id="73367-115">Match value.</span></span>

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

### <span data-ttu-id="73367-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="73367-116">-MatchVariable</span></span>
<span data-ttu-id="73367-117">Corresponder Variável.</span><span class="sxs-lookup"><span data-stu-id="73367-117">Match Variable.</span></span>
<span data-ttu-id="73367-118">Os valores possíveis incluem: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestHeader', 'RequestHead', 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="73367-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="73367-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="73367-119">-NegateCondition</span></span>
<span data-ttu-id="73367-120">Descreve se essa condição é negada ou não o valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="73367-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="73367-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="73367-121">-OperatorProperty</span></span>
<span data-ttu-id="73367-122">Descreve o operador a ser corresponder.</span><span class="sxs-lookup"><span data-stu-id="73367-122">Describes operator to be matched.</span></span>
<span data-ttu-id="73367-123">Os valores possíveis incluem: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="73367-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="73367-124">-Seletor</span><span class="sxs-lookup"><span data-stu-id="73367-124">-Selector</span></span>
<span data-ttu-id="73367-125">Nome do seletor no RequestHeader ou RequestHeader para ser corresponder</span><span class="sxs-lookup"><span data-stu-id="73367-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="73367-126">-Transformar</span><span class="sxs-lookup"><span data-stu-id="73367-126">-Transform</span></span>
<span data-ttu-id="73367-127">Transforma para aplicar.</span><span class="sxs-lookup"><span data-stu-id="73367-127">Transforms to apply.</span></span> <span data-ttu-id="73367-128">Os valores possíveis incluem: 'Minúsculas', 'Maiúsculas', 'Cortar', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span><span class="sxs-lookup"><span data-stu-id="73367-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="73367-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73367-129">CommonParameters</span></span>
<span data-ttu-id="73367-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73367-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73367-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73367-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73367-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="73367-132">INPUTS</span></span>

### <span data-ttu-id="73367-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="73367-133">None</span></span>

## <span data-ttu-id="73367-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="73367-134">OUTPUTS</span></span>

### <span data-ttu-id="73367-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="73367-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="73367-136">Notas</span><span class="sxs-lookup"><span data-stu-id="73367-136">NOTES</span></span>

## <span data-ttu-id="73367-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73367-137">RELATED LINKS</span></span>

[<span data-ttu-id="73367-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="73367-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
