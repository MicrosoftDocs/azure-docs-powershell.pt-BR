---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 1bf6394621435293be1d00d4a9e9f435c160e668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772945"
---
# <span data-ttu-id="d40bd-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d40bd-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="d40bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d40bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d40bd-103">Obter regras de firewall definidas no cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="d40bd-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="d40bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d40bd-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d40bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d40bd-105">DESCRIPTION</span></span>
<span data-ttu-id="d40bd-106">Se o parâmetro **RuleName** se fornecido, o cmdlet **Get-AzRedisCacheFirewallRule** obterá detalhes sobre a regra de firewall especificada no cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d40bd-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="d40bd-107">Se apenas o **nome** for especificado, essa operação obterá todas as regras de firewall disponíveis nesse cache Redis.</span><span class="sxs-lookup"><span data-stu-id="d40bd-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="d40bd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d40bd-108">EXAMPLES</span></span>

### <span data-ttu-id="d40bd-109">Exemplo 1: obter uma única regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d40bd-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="d40bd-110">Este comando obtém a regra de firewall chamada ruleone do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="d40bd-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="d40bd-111">Exemplo 2: obter todas as regras de firewall</span><span class="sxs-lookup"><span data-stu-id="d40bd-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="d40bd-112">Esse comando obtém todas as regras de firewall do cache Redis chamado de myCache.</span><span class="sxs-lookup"><span data-stu-id="d40bd-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="d40bd-113">OS</span><span class="sxs-lookup"><span data-stu-id="d40bd-113">PARAMETERS</span></span>

### <span data-ttu-id="d40bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d40bd-114">-DefaultProfile</span></span>
<span data-ttu-id="d40bd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d40bd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d40bd-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d40bd-116">-Name</span></span>
<span data-ttu-id="d40bd-117">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="d40bd-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="d40bd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d40bd-118">-ResourceGroupName</span></span>
<span data-ttu-id="d40bd-119">Nome do grupo de recursos no qual existe o cache.</span><span class="sxs-lookup"><span data-stu-id="d40bd-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="d40bd-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d40bd-120">-RuleName</span></span>
<span data-ttu-id="d40bd-121">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="d40bd-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="d40bd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40bd-122">CommonParameters</span></span>
<span data-ttu-id="d40bd-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d40bd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40bd-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d40bd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40bd-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d40bd-125">INPUTS</span></span>

### <span data-ttu-id="d40bd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d40bd-126">System.String</span></span>

## <span data-ttu-id="d40bd-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d40bd-127">OUTPUTS</span></span>

### <span data-ttu-id="d40bd-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d40bd-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="d40bd-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d40bd-129">NOTES</span></span>

## <span data-ttu-id="d40bd-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d40bd-130">RELATED LINKS</span></span>

[<span data-ttu-id="d40bd-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d40bd-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d40bd-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d40bd-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d40bd-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d40bd-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d40bd-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d40bd-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d40bd-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d40bd-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d40bd-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d40bd-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)