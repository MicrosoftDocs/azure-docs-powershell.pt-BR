---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114527"
---
# <span data-ttu-id="011c4-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="011c4-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="011c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="011c4-102">SYNOPSIS</span></span>
<span data-ttu-id="011c4-103">Criar objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="011c4-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="011c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="011c4-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="011c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="011c4-105">DESCRIPTION</span></span>
<span data-ttu-id="011c4-106">Criar objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="011c4-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="011c4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="011c4-107">EXAMPLES</span></span>

### <span data-ttu-id="011c4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="011c4-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="011c4-109">Criar um objeto CustomRule</span><span class="sxs-lookup"><span data-stu-id="011c4-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="011c4-110">OS</span><span class="sxs-lookup"><span data-stu-id="011c4-110">PARAMETERS</span></span>

### <span data-ttu-id="011c4-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="011c4-111">-Action</span></span>
<span data-ttu-id="011c4-112">Tipo de ações.</span><span class="sxs-lookup"><span data-stu-id="011c4-112">Type of Actions.</span></span>
<span data-ttu-id="011c4-113">Os valores possíveis incluem: ' Allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="011c4-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="011c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011c4-114">-DefaultProfile</span></span>
<span data-ttu-id="011c4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="011c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="011c4-116">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="011c4-116">-EnabledState</span></span>
<span data-ttu-id="011c4-117">Estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="011c4-117">Enabled State.</span></span> <span data-ttu-id="011c4-118">Os valores possíveis incluem: ' Enabled ', ' disabled '.</span><span class="sxs-lookup"><span data-stu-id="011c4-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="011c4-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="011c4-119">-MatchCondition</span></span>
<span data-ttu-id="011c4-120">Lista de condições de correspondência.</span><span class="sxs-lookup"><span data-stu-id="011c4-120">List of match conditions.</span></span>

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

### <span data-ttu-id="011c4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="011c4-121">-Name</span></span>
<span data-ttu-id="011c4-122">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="011c4-122">Name of the rule</span></span>

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

### <span data-ttu-id="011c4-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="011c4-123">-Priority</span></span>
<span data-ttu-id="011c4-124">Descreve a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="011c4-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="011c4-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="011c4-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="011c4-126">Tempo limite da taxa.</span><span class="sxs-lookup"><span data-stu-id="011c4-126">Rate limit duration.</span></span> <span data-ttu-id="011c4-127">Padrão-1 minuto</span><span class="sxs-lookup"><span data-stu-id="011c4-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="011c4-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="011c4-128">-RateLimitThreshold</span></span>
<span data-ttu-id="011c4-129">Limite de limite de taxa</span><span class="sxs-lookup"><span data-stu-id="011c4-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="011c4-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="011c4-130">-RuleType</span></span>
<span data-ttu-id="011c4-131">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="011c4-131">Type of the rule.</span></span>
<span data-ttu-id="011c4-132">Os valores possíveis incluem: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="011c4-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="011c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011c4-133">CommonParameters</span></span>
<span data-ttu-id="011c4-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="011c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011c4-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="011c4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011c4-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="011c4-136">INPUTS</span></span>

### <span data-ttu-id="011c4-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="011c4-137">None</span></span>

## <span data-ttu-id="011c4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="011c4-138">OUTPUTS</span></span>

### <span data-ttu-id="011c4-139">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="011c4-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="011c4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="011c4-140">NOTES</span></span>

## <span data-ttu-id="011c4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="011c4-141">RELATED LINKS</span></span>

<span data-ttu-id="011c4-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="011c4-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
