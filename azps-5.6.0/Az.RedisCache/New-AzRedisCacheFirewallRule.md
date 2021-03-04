---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: bd0d6995cae0d32a7fb0ce46d42f87a480c275f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885970"
---
# <span data-ttu-id="270eb-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="270eb-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="270eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="270eb-102">SYNOPSIS</span></span>
<span data-ttu-id="270eb-103">Crie uma regra de firewall em um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="270eb-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="270eb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="270eb-104">SYNTAX</span></span>

### <span data-ttu-id="270eb-105">NormalParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="270eb-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="270eb-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="270eb-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="270eb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="270eb-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="270eb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="270eb-108">DESCRIPTION</span></span>
<span data-ttu-id="270eb-109">Crie uma regra de firewall em um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="270eb-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="270eb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="270eb-110">EXAMPLES</span></span>

### <span data-ttu-id="270eb-111">Exemplo 1: Criar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="270eb-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="270eb-112">Este comando cria uma regra de firewall chamada ruleone no Cache Redis chamado mycache.</span><span class="sxs-lookup"><span data-stu-id="270eb-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="270eb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="270eb-113">PARAMETERS</span></span>

### <span data-ttu-id="270eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270eb-114">-DefaultProfile</span></span>
<span data-ttu-id="270eb-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="270eb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="270eb-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="270eb-116">-EndIP</span></span>
<span data-ttu-id="270eb-117">Endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="270eb-117">Ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270eb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="270eb-118">-InputObject</span></span>
<span data-ttu-id="270eb-119">do tipo RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="270eb-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="270eb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="270eb-120">-Name</span></span>
<span data-ttu-id="270eb-121">Nome do cache redis.</span><span class="sxs-lookup"><span data-stu-id="270eb-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="270eb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270eb-122">-ResourceGroupName</span></span>
<span data-ttu-id="270eb-123">Nome do grupo de recursos no qual o cache existe.</span><span class="sxs-lookup"><span data-stu-id="270eb-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="270eb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="270eb-124">-ResourceId</span></span>
<span data-ttu-id="270eb-125">ARM ID do Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="270eb-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270eb-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="270eb-126">-RuleName</span></span>
<span data-ttu-id="270eb-127">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="270eb-127">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270eb-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="270eb-128">-StartIP</span></span>
<span data-ttu-id="270eb-129">Endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="270eb-129">Starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270eb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="270eb-130">-Confirm</span></span>
<span data-ttu-id="270eb-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270eb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270eb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270eb-132">-WhatIf</span></span>
<span data-ttu-id="270eb-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="270eb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="270eb-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="270eb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270eb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270eb-135">CommonParameters</span></span>
<span data-ttu-id="270eb-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270eb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270eb-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270eb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270eb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="270eb-138">INPUTS</span></span>

### <span data-ttu-id="270eb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="270eb-139">System.String</span></span>

### <span data-ttu-id="270eb-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="270eb-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="270eb-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="270eb-141">OUTPUTS</span></span>

### <span data-ttu-id="270eb-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="270eb-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="270eb-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="270eb-143">NOTES</span></span>

## <span data-ttu-id="270eb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="270eb-144">RELATED LINKS</span></span>

[<span data-ttu-id="270eb-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="270eb-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="270eb-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="270eb-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="270eb-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="270eb-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="270eb-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="270eb-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="270eb-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="270eb-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="270eb-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="270eb-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)