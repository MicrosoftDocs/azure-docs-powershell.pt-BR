---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115451"
---
# <span data-ttu-id="28a5c-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="28a5c-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="28a5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="28a5c-103">Criar objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="28a5c-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="28a5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28a5c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a5c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="28a5c-106">Criar objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="28a5c-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="28a5c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28a5c-107">EXAMPLES</span></span>

### <span data-ttu-id="28a5c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28a5c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="28a5c-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28a5c-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="28a5c-110">Criar um objeto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="28a5c-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="28a5c-111">OS</span><span class="sxs-lookup"><span data-stu-id="28a5c-111">PARAMETERS</span></span>

### <span data-ttu-id="28a5c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a5c-112">-DefaultProfile</span></span>
<span data-ttu-id="28a5c-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28a5c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a5c-114">-Matchvalue</span><span class="sxs-lookup"><span data-stu-id="28a5c-114">-MatchValue</span></span>
<span data-ttu-id="28a5c-115">Valor correspondente.</span><span class="sxs-lookup"><span data-stu-id="28a5c-115">Match value.</span></span>

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

### <span data-ttu-id="28a5c-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="28a5c-116">-MatchVariable</span></span>
<span data-ttu-id="28a5c-117">Corresponder variável.</span><span class="sxs-lookup"><span data-stu-id="28a5c-117">Match Variable.</span></span>
<span data-ttu-id="28a5c-118">Os valores possíveis incluem: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' createargs ', ' RequestUri ', ' RequestHeader ', ' RequestBody ', ' SocketAddr '</span><span class="sxs-lookup"><span data-stu-id="28a5c-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="28a5c-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="28a5c-119">-NegateCondition</span></span>
<span data-ttu-id="28a5c-120">Descreve se a condição é negação ou o valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="28a5c-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="28a5c-121">-Operatorproperty</span><span class="sxs-lookup"><span data-stu-id="28a5c-121">-OperatorProperty</span></span>
<span data-ttu-id="28a5c-122">Descreve o operador a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="28a5c-122">Describes operator to be matched.</span></span>
<span data-ttu-id="28a5c-123">Os valores possíveis incluem: ' any ', ' IPMatch ', ' geomatch ', ' ' EQUAL ', ' GreaterThanOrEqual ', ' começa ', ' EndsWith ', ' RegEx ', ' ', ' ', ' EndsWith ', ' RegEx '</span><span class="sxs-lookup"><span data-stu-id="28a5c-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="28a5c-124">-Seletor</span><span class="sxs-lookup"><span data-stu-id="28a5c-124">-Selector</span></span>
<span data-ttu-id="28a5c-125">Nome do seletor em RequestHeader ou RequestBody para ser correspondido</span><span class="sxs-lookup"><span data-stu-id="28a5c-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="28a5c-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="28a5c-126">-Transform</span></span>
<span data-ttu-id="28a5c-127">Transformações a serem aplicadas.</span><span class="sxs-lookup"><span data-stu-id="28a5c-127">Transforms to apply.</span></span> <span data-ttu-id="28a5c-128">Os valores possíveis incluem: ' minúscula ', ' maiúscula ', ' arrumar ', ' UrlDecode ', ' UrlEncode ', ' RemoveNulls '.</span><span class="sxs-lookup"><span data-stu-id="28a5c-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="28a5c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a5c-129">CommonParameters</span></span>
<span data-ttu-id="28a5c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a5c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a5c-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28a5c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a5c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28a5c-132">INPUTS</span></span>

### <span data-ttu-id="28a5c-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="28a5c-133">None</span></span>

## <span data-ttu-id="28a5c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28a5c-134">OUTPUTS</span></span>

### <span data-ttu-id="28a5c-135">Microsoft. Azure. Commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="28a5c-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="28a5c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28a5c-136">NOTES</span></span>

## <span data-ttu-id="28a5c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28a5c-137">RELATED LINKS</span></span>

[<span data-ttu-id="28a5c-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="28a5c-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
