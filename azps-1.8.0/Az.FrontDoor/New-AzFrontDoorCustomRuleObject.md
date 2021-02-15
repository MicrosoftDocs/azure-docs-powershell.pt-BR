---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 8602bd4636e3e6034552f48a6f6514a453b816a0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400664"
---
# <span data-ttu-id="e02a0-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="e02a0-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="e02a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e02a0-102">SYNOPSIS</span></span>
<span data-ttu-id="e02a0-103">Criar Objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="e02a0-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e02a0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e02a0-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e02a0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e02a0-105">DESCRIPTION</span></span>
<span data-ttu-id="e02a0-106">Criar Objeto CustomRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="e02a0-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e02a0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e02a0-107">EXAMPLES</span></span>

### <span data-ttu-id="e02a0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e02a0-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="e02a0-109">Criar um Objeto CustomRule</span><span class="sxs-lookup"><span data-stu-id="e02a0-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="e02a0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e02a0-110">PARAMETERS</span></span>

### <span data-ttu-id="e02a0-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="e02a0-111">-Action</span></span>
<span data-ttu-id="e02a0-112">Tipo de Ações.</span><span class="sxs-lookup"><span data-stu-id="e02a0-112">Type of Actions.</span></span>
<span data-ttu-id="e02a0-113">Os valores possíveis incluem: 'Permitir', 'Bloquear', 'Log'</span><span class="sxs-lookup"><span data-stu-id="e02a0-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02a0-114">-DefaultProfile</span></span>
<span data-ttu-id="e02a0-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e02a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02a0-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="e02a0-116">-MatchCondition</span></span>
<span data-ttu-id="e02a0-117">Lista de condições de combinação.</span><span class="sxs-lookup"><span data-stu-id="e02a0-117">List of match conditions.</span></span>

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

### <span data-ttu-id="e02a0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e02a0-118">-Name</span></span>
<span data-ttu-id="e02a0-119">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="e02a0-119">Name of the rule</span></span>

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

### <span data-ttu-id="e02a0-120">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="e02a0-120">-Priority</span></span>
<span data-ttu-id="e02a0-121">Descreve a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="e02a0-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="e02a0-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="e02a0-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="e02a0-123">Duração do limite da taxa.</span><span class="sxs-lookup"><span data-stu-id="e02a0-123">Rate limit duration.</span></span> <span data-ttu-id="e02a0-124">Padrão – 1 minuto</span><span class="sxs-lookup"><span data-stu-id="e02a0-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="e02a0-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="e02a0-125">-RateLimitThreshold</span></span>
<span data-ttu-id="e02a0-126">Limite de taxas</span><span class="sxs-lookup"><span data-stu-id="e02a0-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="e02a0-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e02a0-127">-RuleType</span></span>
<span data-ttu-id="e02a0-128">Tipo da regra.</span><span class="sxs-lookup"><span data-stu-id="e02a0-128">Type of the rule.</span></span>
<span data-ttu-id="e02a0-129">Os valores possíveis incluem: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="e02a0-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="e02a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02a0-130">CommonParameters</span></span>
<span data-ttu-id="e02a0-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02a0-132">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e02a0-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02a0-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="e02a0-133">INPUTS</span></span>

### <span data-ttu-id="e02a0-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e02a0-134">None</span></span>

## <span data-ttu-id="e02a0-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="e02a0-135">OUTPUTS</span></span>

### <span data-ttu-id="e02a0-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="e02a0-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="e02a0-137">Notas</span><span class="sxs-lookup"><span data-stu-id="e02a0-137">NOTES</span></span>

## <span data-ttu-id="e02a0-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e02a0-138">RELATED LINKS</span></span>

<span data-ttu-id="e02a0-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="e02a0-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
