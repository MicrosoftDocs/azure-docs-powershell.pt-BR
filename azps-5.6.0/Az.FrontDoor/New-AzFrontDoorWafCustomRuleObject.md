---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: cf74b21d2b07ddf8f92203c43e7005f81cbb2a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887752"
---
# <span data-ttu-id="59254-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="59254-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="59254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59254-102">SYNOPSIS</span></span>
<span data-ttu-id="59254-103">Criar objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="59254-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="59254-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="59254-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59254-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="59254-105">DESCRIPTION</span></span>
<span data-ttu-id="59254-106">Criar objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="59254-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="59254-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59254-107">EXAMPLES</span></span>

### <span data-ttu-id="59254-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59254-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="59254-109">Criar um objeto CustomRule</span><span class="sxs-lookup"><span data-stu-id="59254-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="59254-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="59254-110">PARAMETERS</span></span>

### <span data-ttu-id="59254-111">-Action</span><span class="sxs-lookup"><span data-stu-id="59254-111">-Action</span></span>
<span data-ttu-id="59254-112">Tipo de ações.</span><span class="sxs-lookup"><span data-stu-id="59254-112">Type of Actions.</span></span>
<span data-ttu-id="59254-113">Os valores possíveis incluem: 'Allow', 'Block', 'Log'</span><span class="sxs-lookup"><span data-stu-id="59254-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="59254-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59254-114">-DefaultProfile</span></span>
<span data-ttu-id="59254-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59254-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59254-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="59254-116">-EnabledState</span></span>
<span data-ttu-id="59254-117">Estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="59254-117">Enabled State.</span></span> <span data-ttu-id="59254-118">Os valores possíveis incluem: 'Habilitado', 'Desabilitado'.</span><span class="sxs-lookup"><span data-stu-id="59254-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="59254-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="59254-119">-MatchCondition</span></span>
<span data-ttu-id="59254-120">Lista de condições de combinação.</span><span class="sxs-lookup"><span data-stu-id="59254-120">List of match conditions.</span></span>

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

### <span data-ttu-id="59254-121">-Name</span><span class="sxs-lookup"><span data-stu-id="59254-121">-Name</span></span>
<span data-ttu-id="59254-122">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="59254-122">Name of the rule</span></span>

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

### <span data-ttu-id="59254-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="59254-123">-Priority</span></span>
<span data-ttu-id="59254-124">Descreve a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="59254-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="59254-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="59254-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="59254-126">Duração do limite de taxa.</span><span class="sxs-lookup"><span data-stu-id="59254-126">Rate limit duration.</span></span> <span data-ttu-id="59254-127">Padrão - 1 minuto</span><span class="sxs-lookup"><span data-stu-id="59254-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="59254-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="59254-128">-RateLimitThreshold</span></span>
<span data-ttu-id="59254-129">Limite de taxa</span><span class="sxs-lookup"><span data-stu-id="59254-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="59254-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="59254-130">-RuleType</span></span>
<span data-ttu-id="59254-131">Tipo da regra.</span><span class="sxs-lookup"><span data-stu-id="59254-131">Type of the rule.</span></span>
<span data-ttu-id="59254-132">Os valores possíveis incluem: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="59254-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="59254-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59254-133">CommonParameters</span></span>
<span data-ttu-id="59254-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59254-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59254-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59254-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59254-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59254-136">INPUTS</span></span>

### <span data-ttu-id="59254-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="59254-137">None</span></span>

## <span data-ttu-id="59254-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="59254-138">OUTPUTS</span></span>

### <span data-ttu-id="59254-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="59254-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="59254-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="59254-140">NOTES</span></span>

## <span data-ttu-id="59254-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59254-141">RELATED LINKS</span></span>

<span data-ttu-id="59254-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="59254-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
