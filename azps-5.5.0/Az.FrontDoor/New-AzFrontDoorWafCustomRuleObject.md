---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111880"
---
# <span data-ttu-id="3f464-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="3f464-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="3f464-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f464-102">SYNOPSIS</span></span>
<span data-ttu-id="3f464-103">Criar Objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="3f464-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="3f464-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f464-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f464-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f464-105">DESCRIPTION</span></span>
<span data-ttu-id="3f464-106">Criar Objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="3f464-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="3f464-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f464-107">EXAMPLES</span></span>

### <span data-ttu-id="3f464-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f464-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="3f464-109">Criar um Objeto CustomRule</span><span class="sxs-lookup"><span data-stu-id="3f464-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="3f464-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f464-110">PARAMETERS</span></span>

### <span data-ttu-id="3f464-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="3f464-111">-Action</span></span>
<span data-ttu-id="3f464-112">Tipo de Ações.</span><span class="sxs-lookup"><span data-stu-id="3f464-112">Type of Actions.</span></span>
<span data-ttu-id="3f464-113">Os valores possíveis incluem: 'Permitir', 'Bloquear', 'Log'</span><span class="sxs-lookup"><span data-stu-id="3f464-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="3f464-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f464-114">-DefaultProfile</span></span>
<span data-ttu-id="3f464-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f464-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f464-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="3f464-116">-EnabledState</span></span>
<span data-ttu-id="3f464-117">Estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="3f464-117">Enabled State.</span></span> <span data-ttu-id="3f464-118">Os valores possíveis incluem: "Habilitado", "Desabilitado".</span><span class="sxs-lookup"><span data-stu-id="3f464-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="3f464-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="3f464-119">-MatchCondition</span></span>
<span data-ttu-id="3f464-120">Lista de condições de combinação.</span><span class="sxs-lookup"><span data-stu-id="3f464-120">List of match conditions.</span></span>

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

### <span data-ttu-id="3f464-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f464-121">-Name</span></span>
<span data-ttu-id="3f464-122">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="3f464-122">Name of the rule</span></span>

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

### <span data-ttu-id="3f464-123">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="3f464-123">-Priority</span></span>
<span data-ttu-id="3f464-124">Descreve a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="3f464-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="3f464-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="3f464-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="3f464-126">Duração do limite da taxa.</span><span class="sxs-lookup"><span data-stu-id="3f464-126">Rate limit duration.</span></span> <span data-ttu-id="3f464-127">Padrão – 1 minuto</span><span class="sxs-lookup"><span data-stu-id="3f464-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="3f464-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="3f464-128">-RateLimitThreshold</span></span>
<span data-ttu-id="3f464-129">Limite de taxa</span><span class="sxs-lookup"><span data-stu-id="3f464-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="3f464-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="3f464-130">-RuleType</span></span>
<span data-ttu-id="3f464-131">Tipo da regra.</span><span class="sxs-lookup"><span data-stu-id="3f464-131">Type of the rule.</span></span>
<span data-ttu-id="3f464-132">Os valores possíveis incluem: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="3f464-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="3f464-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f464-133">CommonParameters</span></span>
<span data-ttu-id="3f464-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f464-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f464-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f464-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f464-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="3f464-136">INPUTS</span></span>

### <span data-ttu-id="3f464-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3f464-137">None</span></span>

## <span data-ttu-id="3f464-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="3f464-138">OUTPUTS</span></span>

### <span data-ttu-id="3f464-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="3f464-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="3f464-140">Notas</span><span class="sxs-lookup"><span data-stu-id="3f464-140">NOTES</span></span>

## <span data-ttu-id="3f464-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f464-141">RELATED LINKS</span></span>

<span data-ttu-id="3f464-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3f464-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
