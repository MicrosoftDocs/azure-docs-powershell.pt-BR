---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602929"
---
# <span data-ttu-id="cf1ad-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="cf1ad-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="cf1ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1ad-103">Criar objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="cf1ad-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf1ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf1ad-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf1ad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf1ad-105">DESCRIPTION</span></span>
<span data-ttu-id="cf1ad-106">Criar objeto MatchCondition para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="cf1ad-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="cf1ad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf1ad-107">EXAMPLES</span></span>

### <span data-ttu-id="cf1ad-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf1ad-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="cf1ad-109">Criar um objeto MatchCondition</span><span class="sxs-lookup"><span data-stu-id="cf1ad-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="cf1ad-110">OS</span><span class="sxs-lookup"><span data-stu-id="cf1ad-110">PARAMETERS</span></span>

### <span data-ttu-id="cf1ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1ad-111">-DefaultProfile</span></span>
<span data-ttu-id="cf1ad-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf1ad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1ad-113">-Matchvalue</span><span class="sxs-lookup"><span data-stu-id="cf1ad-113">-MatchValue</span></span>
<span data-ttu-id="cf1ad-114">Valor correspondente.</span><span class="sxs-lookup"><span data-stu-id="cf1ad-114">Match value.</span></span>

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

### <span data-ttu-id="cf1ad-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="cf1ad-115">-MatchVariable</span></span>
<span data-ttu-id="cf1ad-116">Corresponder variável.</span><span class="sxs-lookup"><span data-stu-id="cf1ad-116">Match Variable.</span></span>
<span data-ttu-id="cf1ad-117">Os valores possíveis incluem: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' createargs ', ' RequestUri ', ' RequestHeader ', ' RequestBody '</span><span class="sxs-lookup"><span data-stu-id="cf1ad-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="cf1ad-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="cf1ad-118">-NegateCondition</span></span>
<span data-ttu-id="cf1ad-119">Descreve se a condição é negação ou o valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="cf1ad-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="cf1ad-120">-Operatorproperty</span><span class="sxs-lookup"><span data-stu-id="cf1ad-120">-OperatorProperty</span></span>
<span data-ttu-id="cf1ad-121">Descreve o operador a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="cf1ad-121">Describes operator to be matched.</span></span>
<span data-ttu-id="cf1ad-122">Os valores possíveis incluem: ' any ', ' IPMatch ', ' geomatch ', ' EQUAL ', ' GreaterThanOrEqual ', ' começa ', ' EndsWith ', ' LessThanOrEqual ', ' ', ' ', ' EndsWith ' '</span><span class="sxs-lookup"><span data-stu-id="cf1ad-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="cf1ad-123">-Seletor</span><span class="sxs-lookup"><span data-stu-id="cf1ad-123">-Selector</span></span>
<span data-ttu-id="cf1ad-124">Nome do seletor em RequestHeader ou RequestBody para ser correspondido</span><span class="sxs-lookup"><span data-stu-id="cf1ad-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="cf1ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1ad-125">CommonParameters</span></span>
<span data-ttu-id="cf1ad-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1ad-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf1ad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1ad-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf1ad-128">INPUTS</span></span>

### <span data-ttu-id="cf1ad-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cf1ad-129">None</span></span>

## <span data-ttu-id="cf1ad-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf1ad-130">OUTPUTS</span></span>

### <span data-ttu-id="cf1ad-131">Microsoft. Azure. Commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="cf1ad-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="cf1ad-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf1ad-132">NOTES</span></span>

## <span data-ttu-id="cf1ad-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf1ad-133">RELATED LINKS</span></span>

[<span data-ttu-id="cf1ad-134">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="cf1ad-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
