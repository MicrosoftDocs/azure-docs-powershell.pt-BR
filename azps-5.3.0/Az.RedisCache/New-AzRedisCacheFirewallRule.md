---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428033"
---
# <span data-ttu-id="20a96-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20a96-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="20a96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20a96-102">SYNOPSIS</span></span>
<span data-ttu-id="20a96-103">Criar uma regra de firewall em um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="20a96-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="20a96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20a96-104">SYNTAX</span></span>

### <span data-ttu-id="20a96-105">NormalParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="20a96-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20a96-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="20a96-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20a96-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20a96-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20a96-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20a96-108">DESCRIPTION</span></span>
<span data-ttu-id="20a96-109">Criar uma regra de firewall em um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="20a96-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="20a96-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20a96-110">EXAMPLES</span></span>

### <span data-ttu-id="20a96-111">Exemplo 1: criar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="20a96-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="20a96-112">Esse comando cria uma regra de firewall chamada ruleone em Redis cache chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="20a96-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="20a96-113">OS</span><span class="sxs-lookup"><span data-stu-id="20a96-113">PARAMETERS</span></span>

### <span data-ttu-id="20a96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a96-114">-DefaultProfile</span></span>
<span data-ttu-id="20a96-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20a96-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20a96-116">-Ip_final</span><span class="sxs-lookup"><span data-stu-id="20a96-116">-EndIP</span></span>
<span data-ttu-id="20a96-117">Endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="20a96-117">Ending IP address.</span></span>

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

### <span data-ttu-id="20a96-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20a96-118">-InputObject</span></span>
<span data-ttu-id="20a96-119">objeto do tipo RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="20a96-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="20a96-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="20a96-120">-Name</span></span>
<span data-ttu-id="20a96-121">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="20a96-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="20a96-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a96-122">-ResourceGroupName</span></span>
<span data-ttu-id="20a96-123">Nome do grupo de recursos no qual existe o cache.</span><span class="sxs-lookup"><span data-stu-id="20a96-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="20a96-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20a96-124">-ResourceId</span></span>
<span data-ttu-id="20a96-125">ID do braço do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="20a96-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="20a96-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="20a96-126">-RuleName</span></span>
<span data-ttu-id="20a96-127">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="20a96-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="20a96-128">-Ip_inicial</span><span class="sxs-lookup"><span data-stu-id="20a96-128">-StartIP</span></span>
<span data-ttu-id="20a96-129">Endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="20a96-129">Starting IP address.</span></span>

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

### <span data-ttu-id="20a96-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20a96-130">-Confirm</span></span>
<span data-ttu-id="20a96-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a96-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20a96-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a96-132">-WhatIf</span></span>
<span data-ttu-id="20a96-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20a96-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a96-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20a96-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20a96-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a96-135">CommonParameters</span></span>
<span data-ttu-id="20a96-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a96-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a96-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a96-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a96-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20a96-138">INPUTS</span></span>

### <span data-ttu-id="20a96-139">System. String</span><span class="sxs-lookup"><span data-stu-id="20a96-139">System.String</span></span>

### <span data-ttu-id="20a96-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="20a96-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="20a96-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20a96-141">OUTPUTS</span></span>

### <span data-ttu-id="20a96-142">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20a96-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="20a96-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20a96-143">NOTES</span></span>

## <span data-ttu-id="20a96-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20a96-144">RELATED LINKS</span></span>

[<span data-ttu-id="20a96-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20a96-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="20a96-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20a96-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="20a96-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20a96-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="20a96-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20a96-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="20a96-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20a96-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="20a96-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20a96-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)