---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 5e17eced3525a7aa318cbba19b632d3ae11d79a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901442"
---
# <span data-ttu-id="6fd06-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6fd06-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6fd06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fd06-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd06-103">Obter regras de firewall definidas no Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="6fd06-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="6fd06-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6fd06-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fd06-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6fd06-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd06-106">Se **o parâmetro RuleName** for fornecido, o cmdlet **Get-AzRedisCacheFirewallRule** obterá detalhes sobre a regra de firewall especificada no Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="6fd06-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="6fd06-107">Se somente **Name** for especificado, essa operação obtém todas as regras de firewall disponíveis nesse Cache redis.</span><span class="sxs-lookup"><span data-stu-id="6fd06-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="6fd06-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fd06-108">EXAMPLES</span></span>

### <span data-ttu-id="6fd06-109">Exemplo 1: Obter uma única regra de firewall</span><span class="sxs-lookup"><span data-stu-id="6fd06-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="6fd06-110">Este comando obtém uma regra de firewall chamada ruleone de Redis Cache chamada mycache.</span><span class="sxs-lookup"><span data-stu-id="6fd06-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="6fd06-111">Exemplo 2: Obter todas as regras de firewall</span><span class="sxs-lookup"><span data-stu-id="6fd06-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="6fd06-112">Este comando obtém todas as regras de firewall do Cache Redis chamado mycache.</span><span class="sxs-lookup"><span data-stu-id="6fd06-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="6fd06-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6fd06-113">PARAMETERS</span></span>

### <span data-ttu-id="6fd06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd06-114">-DefaultProfile</span></span>
<span data-ttu-id="6fd06-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6fd06-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fd06-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6fd06-116">-Name</span></span>
<span data-ttu-id="6fd06-117">Nome do cache redis.</span><span class="sxs-lookup"><span data-stu-id="6fd06-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="6fd06-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd06-118">-ResourceGroupName</span></span>
<span data-ttu-id="6fd06-119">Nome do grupo de recursos no qual o cache existe.</span><span class="sxs-lookup"><span data-stu-id="6fd06-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd06-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6fd06-120">-RuleName</span></span>
<span data-ttu-id="6fd06-121">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="6fd06-121">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd06-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd06-122">CommonParameters</span></span>
<span data-ttu-id="6fd06-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd06-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd06-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd06-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd06-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fd06-125">INPUTS</span></span>

### <span data-ttu-id="6fd06-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6fd06-126">System.String</span></span>

## <span data-ttu-id="6fd06-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6fd06-127">OUTPUTS</span></span>

### <span data-ttu-id="6fd06-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6fd06-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="6fd06-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="6fd06-129">NOTES</span></span>

## <span data-ttu-id="6fd06-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fd06-130">RELATED LINKS</span></span>

[<span data-ttu-id="6fd06-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6fd06-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6fd06-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6fd06-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6fd06-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd06-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6fd06-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd06-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6fd06-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd06-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6fd06-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6fd06-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)