---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: dc52668a7d0f17d9cdbf9221a174228be1fa0f5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773419"
---
# <span data-ttu-id="9861e-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9861e-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="9861e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9861e-102">SYNOPSIS</span></span>
<span data-ttu-id="9861e-103">Criar uma regra de firewall em um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="9861e-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="9861e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9861e-104">SYNTAX</span></span>

### <span data-ttu-id="9861e-105">NormalParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9861e-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9861e-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="9861e-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9861e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9861e-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9861e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9861e-108">DESCRIPTION</span></span>
<span data-ttu-id="9861e-109">Criar uma regra de firewall em um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="9861e-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="9861e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9861e-110">EXAMPLES</span></span>

### <span data-ttu-id="9861e-111">Exemplo 1: criar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="9861e-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="9861e-112">Esse comando cria uma regra de firewall chamada ruleone em Redis cache chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="9861e-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="9861e-113">OS</span><span class="sxs-lookup"><span data-stu-id="9861e-113">PARAMETERS</span></span>

### <span data-ttu-id="9861e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9861e-114">-DefaultProfile</span></span>
<span data-ttu-id="9861e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9861e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9861e-116">-Ip_final</span><span class="sxs-lookup"><span data-stu-id="9861e-116">-EndIP</span></span>
<span data-ttu-id="9861e-117">Endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="9861e-117">Ending IP address.</span></span>

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

### <span data-ttu-id="9861e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9861e-118">-InputObject</span></span>
<span data-ttu-id="9861e-119">objeto do tipo RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="9861e-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="9861e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9861e-120">-Name</span></span>
<span data-ttu-id="9861e-121">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="9861e-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="9861e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9861e-122">-ResourceGroupName</span></span>
<span data-ttu-id="9861e-123">Nome do grupo de recursos no qual existe o cache.</span><span class="sxs-lookup"><span data-stu-id="9861e-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="9861e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9861e-124">-ResourceId</span></span>
<span data-ttu-id="9861e-125">ID do braço do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="9861e-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="9861e-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="9861e-126">-RuleName</span></span>
<span data-ttu-id="9861e-127">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="9861e-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="9861e-128">-Ip_inicial</span><span class="sxs-lookup"><span data-stu-id="9861e-128">-StartIP</span></span>
<span data-ttu-id="9861e-129">Endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="9861e-129">Starting IP address.</span></span>

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

### <span data-ttu-id="9861e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9861e-130">-Confirm</span></span>
<span data-ttu-id="9861e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9861e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9861e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9861e-132">-WhatIf</span></span>
<span data-ttu-id="9861e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9861e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9861e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9861e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9861e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9861e-135">CommonParameters</span></span>
<span data-ttu-id="9861e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9861e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9861e-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9861e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9861e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9861e-138">INPUTS</span></span>

### <span data-ttu-id="9861e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9861e-139">System.String</span></span>

### <span data-ttu-id="9861e-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="9861e-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="9861e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9861e-141">OUTPUTS</span></span>

### <span data-ttu-id="9861e-142">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9861e-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="9861e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9861e-143">NOTES</span></span>

## <span data-ttu-id="9861e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9861e-144">RELATED LINKS</span></span>

[<span data-ttu-id="9861e-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9861e-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="9861e-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9861e-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="9861e-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9861e-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="9861e-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9861e-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="9861e-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9861e-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="9861e-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9861e-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)