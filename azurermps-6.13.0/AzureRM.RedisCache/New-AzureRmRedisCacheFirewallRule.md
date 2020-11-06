---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: e5e909107d740f67e3407347625270226c87839d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432752"
---
# <span data-ttu-id="b868b-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b868b-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="b868b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b868b-102">SYNOPSIS</span></span>
<span data-ttu-id="b868b-103">Criar uma regra de firewall em um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="b868b-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b868b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b868b-104">SYNTAX</span></span>

### <span data-ttu-id="b868b-105">NormalParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b868b-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b868b-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="b868b-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b868b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b868b-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b868b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b868b-108">DESCRIPTION</span></span>
<span data-ttu-id="b868b-109">Criar uma regra de firewall em um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="b868b-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="b868b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b868b-110">EXAMPLES</span></span>

### <span data-ttu-id="b868b-111">Exemplo 1: criar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="b868b-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="b868b-112">Esse comando cria uma regra de firewall chamada ruleone em Redis cache chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="b868b-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="b868b-113">OS</span><span class="sxs-lookup"><span data-stu-id="b868b-113">PARAMETERS</span></span>

### <span data-ttu-id="b868b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b868b-114">-DefaultProfile</span></span>
<span data-ttu-id="b868b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b868b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b868b-116">-Ip_final</span><span class="sxs-lookup"><span data-stu-id="b868b-116">-EndIP</span></span>
<span data-ttu-id="b868b-117">Endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="b868b-117">Ending IP address.</span></span>

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

### <span data-ttu-id="b868b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b868b-118">-InputObject</span></span>
<span data-ttu-id="b868b-119">objeto do tipo RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="b868b-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="b868b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b868b-120">-Name</span></span>
<span data-ttu-id="b868b-121">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b868b-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="b868b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b868b-122">-ResourceGroupName</span></span>
<span data-ttu-id="b868b-123">Nome do grupo de recursos no qual existe o cache.</span><span class="sxs-lookup"><span data-stu-id="b868b-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="b868b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b868b-124">-ResourceId</span></span>
<span data-ttu-id="b868b-125">ID do braço do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b868b-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="b868b-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b868b-126">-RuleName</span></span>
<span data-ttu-id="b868b-127">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="b868b-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="b868b-128">-Ip_inicial</span><span class="sxs-lookup"><span data-stu-id="b868b-128">-StartIP</span></span>
<span data-ttu-id="b868b-129">Endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="b868b-129">Starting IP address.</span></span>

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

### <span data-ttu-id="b868b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b868b-130">-Confirm</span></span>
<span data-ttu-id="b868b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b868b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b868b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b868b-132">-WhatIf</span></span>
<span data-ttu-id="b868b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b868b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b868b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b868b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b868b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b868b-135">CommonParameters</span></span>
<span data-ttu-id="b868b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b868b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b868b-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b868b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b868b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b868b-138">INPUTS</span></span>

### <span data-ttu-id="b868b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b868b-139">System.String</span></span>

### <span data-ttu-id="b868b-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="b868b-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="b868b-141">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b868b-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b868b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b868b-142">OUTPUTS</span></span>

### <span data-ttu-id="b868b-143">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b868b-143">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="b868b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b868b-144">NOTES</span></span>

## <span data-ttu-id="b868b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b868b-145">RELATED LINKS</span></span>

[<span data-ttu-id="b868b-146">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b868b-146">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="b868b-147">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b868b-147">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="b868b-148">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b868b-148">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b868b-149">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b868b-149">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="b868b-150">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b868b-150">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="b868b-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b868b-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
