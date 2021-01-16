---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258787"
---
# <span data-ttu-id="1d7ee-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1d7ee-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="1d7ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="1d7ee-103">Criar uma regra de firewall em um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="1d7ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d7ee-104">SYNTAX</span></span>

### <span data-ttu-id="1d7ee-105">NormalParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d7ee-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d7ee-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="1d7ee-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d7ee-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d7ee-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d7ee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d7ee-108">DESCRIPTION</span></span>
<span data-ttu-id="1d7ee-109">Criar uma regra de firewall em um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="1d7ee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d7ee-110">EXAMPLES</span></span>

### <span data-ttu-id="1d7ee-111">Exemplo 1: criar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="1d7ee-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="1d7ee-112">Esse comando cria uma regra de firewall chamada ruleone em Redis cache chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="1d7ee-113">OS</span><span class="sxs-lookup"><span data-stu-id="1d7ee-113">PARAMETERS</span></span>

### <span data-ttu-id="1d7ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d7ee-114">-DefaultProfile</span></span>
<span data-ttu-id="1d7ee-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d7ee-116">-Ip_final</span><span class="sxs-lookup"><span data-stu-id="1d7ee-116">-EndIP</span></span>
<span data-ttu-id="1d7ee-117">Endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-117">Ending IP address.</span></span>

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

### <span data-ttu-id="1d7ee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d7ee-118">-InputObject</span></span>
<span data-ttu-id="1d7ee-119">objeto do tipo RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="1d7ee-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="1d7ee-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d7ee-120">-Name</span></span>
<span data-ttu-id="1d7ee-121">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="1d7ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d7ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="1d7ee-123">Nome do grupo de recursos no qual existe o cache.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="1d7ee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d7ee-124">-ResourceId</span></span>
<span data-ttu-id="1d7ee-125">ID do braço do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="1d7ee-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="1d7ee-126">-RuleName</span></span>
<span data-ttu-id="1d7ee-127">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="1d7ee-128">-Ip_inicial</span><span class="sxs-lookup"><span data-stu-id="1d7ee-128">-StartIP</span></span>
<span data-ttu-id="1d7ee-129">Endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-129">Starting IP address.</span></span>

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

### <span data-ttu-id="1d7ee-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1d7ee-130">-Confirm</span></span>
<span data-ttu-id="1d7ee-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d7ee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d7ee-132">-WhatIf</span></span>
<span data-ttu-id="1d7ee-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d7ee-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d7ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d7ee-135">CommonParameters</span></span>
<span data-ttu-id="1d7ee-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d7ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d7ee-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d7ee-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d7ee-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d7ee-138">INPUTS</span></span>

### <span data-ttu-id="1d7ee-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1d7ee-139">System.String</span></span>

### <span data-ttu-id="1d7ee-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="1d7ee-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="1d7ee-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d7ee-141">OUTPUTS</span></span>

### <span data-ttu-id="1d7ee-142">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1d7ee-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="1d7ee-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d7ee-143">NOTES</span></span>

## <span data-ttu-id="1d7ee-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d7ee-144">RELATED LINKS</span></span>

[<span data-ttu-id="1d7ee-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1d7ee-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="1d7ee-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1d7ee-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="1d7ee-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1d7ee-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="1d7ee-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1d7ee-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1d7ee-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1d7ee-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="1d7ee-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1d7ee-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)