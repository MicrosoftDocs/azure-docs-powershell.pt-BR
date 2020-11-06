---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 6c40a54dd230bc4c7e45f97b4fa6f969940e1673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596416"
---
# <span data-ttu-id="9c1f6-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="9c1f6-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="9c1f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9c1f6-103">Criar objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="9c1f6-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="9c1f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c1f6-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c1f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c1f6-105">DESCRIPTION</span></span>
<span data-ttu-id="9c1f6-106">Criar objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="9c1f6-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="9c1f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c1f6-107">EXAMPLES</span></span>

### <span data-ttu-id="9c1f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c1f6-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="9c1f6-109">Criar um objeto CustomRule</span><span class="sxs-lookup"><span data-stu-id="9c1f6-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="9c1f6-110">OS</span><span class="sxs-lookup"><span data-stu-id="9c1f6-110">PARAMETERS</span></span>

### <span data-ttu-id="9c1f6-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="9c1f6-111">-Action</span></span>
<span data-ttu-id="9c1f6-112">Tipo de ações.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-112">Type of Actions.</span></span>
<span data-ttu-id="9c1f6-113">Os valores possíveis incluem: ' Allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="9c1f6-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="9c1f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c1f6-114">-DefaultProfile</span></span>
<span data-ttu-id="9c1f6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c1f6-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="9c1f6-116">-MatchCondition</span></span>
<span data-ttu-id="9c1f6-117">Lista de condições de correspondência.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-117">List of match conditions.</span></span>

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

### <span data-ttu-id="9c1f6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c1f6-118">-Name</span></span>
<span data-ttu-id="9c1f6-119">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="9c1f6-119">Name of the rule</span></span>

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

### <span data-ttu-id="9c1f6-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="9c1f6-120">-Priority</span></span>
<span data-ttu-id="9c1f6-121">Descreve a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="9c1f6-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="9c1f6-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="9c1f6-123">Tempo limite da taxa.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-123">Rate limit duration.</span></span> <span data-ttu-id="9c1f6-124">Padrão-1 minuto</span><span class="sxs-lookup"><span data-stu-id="9c1f6-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="9c1f6-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="9c1f6-125">-RateLimitThreshold</span></span>
<span data-ttu-id="9c1f6-126">Limite de limite de taxa</span><span class="sxs-lookup"><span data-stu-id="9c1f6-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="9c1f6-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="9c1f6-127">-RuleType</span></span>
<span data-ttu-id="9c1f6-128">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-128">Type of the rule.</span></span>
<span data-ttu-id="9c1f6-129">Os valores possíveis incluem: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="9c1f6-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="9c1f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c1f6-130">CommonParameters</span></span>
<span data-ttu-id="9c1f6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c1f6-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c1f6-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c1f6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c1f6-133">INPUTS</span></span>

### <span data-ttu-id="9c1f6-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9c1f6-134">None</span></span>

## <span data-ttu-id="9c1f6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c1f6-135">OUTPUTS</span></span>

### <span data-ttu-id="9c1f6-136">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="9c1f6-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="9c1f6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c1f6-137">NOTES</span></span>

## <span data-ttu-id="9c1f6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c1f6-138">RELATED LINKS</span></span>

<span data-ttu-id="9c1f6-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="9c1f6-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
