---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 9c68e89d09d386d6071cb639fa77ba740a6da53f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887969"
---
# <span data-ttu-id="861c1-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="861c1-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="861c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="861c1-102">SYNOPSIS</span></span>
<span data-ttu-id="861c1-103">Remova uma regra de firewall de um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="861c1-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="861c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="861c1-104">SYNTAX</span></span>

### <span data-ttu-id="861c1-105">NormalParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="861c1-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="861c1-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="861c1-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="861c1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="861c1-107">DESCRIPTION</span></span>
<span data-ttu-id="861c1-108">Remova uma regra de firewall de um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="861c1-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="861c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="861c1-109">EXAMPLES</span></span>

### <span data-ttu-id="861c1-110">Exemplo 1: Remover uma única regra de firewall</span><span class="sxs-lookup"><span data-stu-id="861c1-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="861c1-111">Este comando remove uma regra de firewall chamada ruleone do Cache Redis chamado mycache.</span><span class="sxs-lookup"><span data-stu-id="861c1-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="861c1-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="861c1-112">PARAMETERS</span></span>

### <span data-ttu-id="861c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861c1-113">-DefaultProfile</span></span>
<span data-ttu-id="861c1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="861c1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="861c1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="861c1-115">-InputObject</span></span>
<span data-ttu-id="861c1-116">do tipo PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="861c1-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="861c1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="861c1-117">-Name</span></span>
<span data-ttu-id="861c1-118">Nome do cache redis.</span><span class="sxs-lookup"><span data-stu-id="861c1-118">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861c1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="861c1-119">-PassThru</span></span>
<span data-ttu-id="861c1-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="861c1-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861c1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="861c1-121">-ResourceGroupName</span></span>
<span data-ttu-id="861c1-122">Nome do grupo de recursos no qual o cache existe.</span><span class="sxs-lookup"><span data-stu-id="861c1-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861c1-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="861c1-123">-RuleName</span></span>
<span data-ttu-id="861c1-124">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="861c1-124">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861c1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="861c1-125">-Confirm</span></span>
<span data-ttu-id="861c1-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="861c1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861c1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="861c1-127">-WhatIf</span></span>
<span data-ttu-id="861c1-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="861c1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="861c1-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="861c1-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861c1-130">CommonParameters</span></span>
<span data-ttu-id="861c1-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="861c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861c1-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="861c1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861c1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="861c1-133">INPUTS</span></span>

### <span data-ttu-id="861c1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="861c1-134">System.String</span></span>

### <span data-ttu-id="861c1-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="861c1-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="861c1-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="861c1-136">OUTPUTS</span></span>

### <span data-ttu-id="861c1-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="861c1-137">System.Boolean</span></span>

## <span data-ttu-id="861c1-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="861c1-138">NOTES</span></span>

## <span data-ttu-id="861c1-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="861c1-139">RELATED LINKS</span></span>

[<span data-ttu-id="861c1-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="861c1-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="861c1-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="861c1-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="861c1-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="861c1-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="861c1-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="861c1-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="861c1-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="861c1-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="861c1-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="861c1-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)