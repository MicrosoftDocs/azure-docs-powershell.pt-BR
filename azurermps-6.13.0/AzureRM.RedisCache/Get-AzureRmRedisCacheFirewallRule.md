---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 91eff9b6a096263b96ecae0cf9901f6dbce26c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432758"
---
# <span data-ttu-id="79cd8-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="79cd8-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="79cd8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="79cd8-103">Obter regras de firewall definidas no cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="79cd8-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79cd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79cd8-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79cd8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="79cd8-106">Se o parâmetro **RuleName** se fornecido, o cmdlet **Get-AzureRmRedisCacheFirewallRule** obterá detalhes sobre a regra de firewall especificada no cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="79cd8-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="79cd8-107">Se apenas o **nome** for especificado, essa operação obterá todas as regras de firewall disponíveis nesse cache Redis.</span><span class="sxs-lookup"><span data-stu-id="79cd8-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="79cd8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79cd8-108">EXAMPLES</span></span>

### <span data-ttu-id="79cd8-109">Exemplo 1: obter uma única regra de firewall</span><span class="sxs-lookup"><span data-stu-id="79cd8-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="79cd8-110">Este comando obtém a regra de firewall chamada ruleone do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="79cd8-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="79cd8-111">Exemplo 2: obter todas as regras de firewall</span><span class="sxs-lookup"><span data-stu-id="79cd8-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="79cd8-112">Esse comando obtém todas as regras de firewall do cache Redis chamado de myCache.</span><span class="sxs-lookup"><span data-stu-id="79cd8-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="79cd8-113">OS</span><span class="sxs-lookup"><span data-stu-id="79cd8-113">PARAMETERS</span></span>

### <span data-ttu-id="79cd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79cd8-114">-DefaultProfile</span></span>
<span data-ttu-id="79cd8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79cd8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79cd8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="79cd8-116">-Name</span></span>
<span data-ttu-id="79cd8-117">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="79cd8-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="79cd8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79cd8-118">-ResourceGroupName</span></span>
<span data-ttu-id="79cd8-119">Nome do grupo de recursos no qual existe o cache.</span><span class="sxs-lookup"><span data-stu-id="79cd8-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="79cd8-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="79cd8-120">-RuleName</span></span>
<span data-ttu-id="79cd8-121">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="79cd8-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="79cd8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79cd8-122">CommonParameters</span></span>
<span data-ttu-id="79cd8-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79cd8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79cd8-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79cd8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79cd8-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79cd8-125">INPUTS</span></span>

### <span data-ttu-id="79cd8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="79cd8-126">System.String</span></span>

## <span data-ttu-id="79cd8-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79cd8-127">OUTPUTS</span></span>

### <span data-ttu-id="79cd8-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="79cd8-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="79cd8-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79cd8-129">NOTES</span></span>

## <span data-ttu-id="79cd8-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79cd8-130">RELATED LINKS</span></span>

[<span data-ttu-id="79cd8-131">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="79cd8-131">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="79cd8-132">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="79cd8-132">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="79cd8-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="79cd8-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="79cd8-134">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="79cd8-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="79cd8-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="79cd8-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="79cd8-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="79cd8-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
