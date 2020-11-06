---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
ms.openlocfilehash: a5a1494bd217147a4e6f4c94a85140313429898f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426348"
---
# <span data-ttu-id="c6457-101">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="c6457-101">New-AzureRmFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="c6457-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6457-102">SYNOPSIS</span></span>
<span data-ttu-id="c6457-103">Criar objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="c6457-103">Create CustomRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6457-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6457-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6457-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6457-105">DESCRIPTION</span></span>
<span data-ttu-id="c6457-106">Criar objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="c6457-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c6457-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6457-107">EXAMPLES</span></span>

### <span data-ttu-id="c6457-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6457-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

RuleType                   : MatchRule
Action                     : Block
MatchConditions            : {Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition}
Priority                   : 2
RateLimitDurationInMinutes : 1
RateLimitThreshold         :
Name                       : Rule1
Etag                       :
Transforms                 :
```

<span data-ttu-id="c6457-109">Criar um objeto CustomRule</span><span class="sxs-lookup"><span data-stu-id="c6457-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="c6457-110">OS</span><span class="sxs-lookup"><span data-stu-id="c6457-110">PARAMETERS</span></span>

### <span data-ttu-id="c6457-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="c6457-111">-Action</span></span>
<span data-ttu-id="c6457-112">Tipo de ações.</span><span class="sxs-lookup"><span data-stu-id="c6457-112">Type of Actions.</span></span>
<span data-ttu-id="c6457-113">Os valores possíveis incluem: ' Allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="c6457-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6457-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6457-114">-DefaultProfile</span></span>
<span data-ttu-id="c6457-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6457-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6457-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="c6457-116">-MatchCondition</span></span>
<span data-ttu-id="c6457-117">Lista de condições de correspondência.</span><span class="sxs-lookup"><span data-stu-id="c6457-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6457-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6457-118">-Name</span></span>
<span data-ttu-id="c6457-119">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="c6457-119">Name of the rule</span></span>

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

### <span data-ttu-id="c6457-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="c6457-120">-Priority</span></span>
<span data-ttu-id="c6457-121">Descreve a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="c6457-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="c6457-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="c6457-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="c6457-123">Tempo limite da taxa.</span><span class="sxs-lookup"><span data-stu-id="c6457-123">Rate limit duration.</span></span> <span data-ttu-id="c6457-124">Padrão-1 minuto</span><span class="sxs-lookup"><span data-stu-id="c6457-124">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6457-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="c6457-125">-RateLimitThreshold</span></span>
<span data-ttu-id="c6457-126">Limite de taxa thresold</span><span class="sxs-lookup"><span data-stu-id="c6457-126">Rate limit thresold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6457-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c6457-127">-RuleType</span></span>
<span data-ttu-id="c6457-128">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="c6457-128">Type of the rule.</span></span>
<span data-ttu-id="c6457-129">Os valores possíveis incluem: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="c6457-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6457-130">-Transform</span><span class="sxs-lookup"><span data-stu-id="c6457-130">-Transform</span></span>
<span data-ttu-id="c6457-131">Lista de transformações</span><span class="sxs-lookup"><span data-stu-id="c6457-131">List of transforms</span></span>

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

### <span data-ttu-id="c6457-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6457-132">CommonParameters</span></span>
<span data-ttu-id="c6457-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6457-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6457-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6457-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6457-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6457-135">INPUTS</span></span>

### <span data-ttu-id="c6457-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c6457-136">None</span></span>

## <span data-ttu-id="c6457-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6457-137">OUTPUTS</span></span>

### <span data-ttu-id="c6457-138">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="c6457-138">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="c6457-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6457-139">NOTES</span></span>

## <span data-ttu-id="c6457-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6457-140">RELATED LINKS</span></span>

<span data-ttu-id="c6457-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c6457-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span></span>
