---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: e24ea6e0b5bf88b17a6209f2ea69634200a10a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773403"
---
# <span data-ttu-id="db1df-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="db1df-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="db1df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db1df-102">SYNOPSIS</span></span>
<span data-ttu-id="db1df-103">Remover uma regra de firewall de um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="db1df-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="db1df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db1df-104">SYNTAX</span></span>

### <span data-ttu-id="db1df-105">NormalParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="db1df-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1df-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="db1df-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db1df-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db1df-107">DESCRIPTION</span></span>
<span data-ttu-id="db1df-108">Remover uma regra de firewall de um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="db1df-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="db1df-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db1df-109">EXAMPLES</span></span>

### <span data-ttu-id="db1df-110">Exemplo 1: remover uma única regra de firewall</span><span class="sxs-lookup"><span data-stu-id="db1df-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="db1df-111">Esse comando Remove uma regra de firewall chamada ruleone do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="db1df-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="db1df-112">OS</span><span class="sxs-lookup"><span data-stu-id="db1df-112">PARAMETERS</span></span>

### <span data-ttu-id="db1df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db1df-113">-DefaultProfile</span></span>
<span data-ttu-id="db1df-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db1df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db1df-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db1df-115">-InputObject</span></span>
<span data-ttu-id="db1df-116">objeto do tipo PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="db1df-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="db1df-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="db1df-117">-Name</span></span>
<span data-ttu-id="db1df-118">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="db1df-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="db1df-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db1df-119">-PassThru</span></span>
<span data-ttu-id="db1df-120">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="db1df-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="db1df-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1df-121">-ResourceGroupName</span></span>
<span data-ttu-id="db1df-122">Nome do grupo de recursos no qual existe o cache.</span><span class="sxs-lookup"><span data-stu-id="db1df-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="db1df-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="db1df-123">-RuleName</span></span>
<span data-ttu-id="db1df-124">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="db1df-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="db1df-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db1df-125">-Confirm</span></span>
<span data-ttu-id="db1df-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db1df-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db1df-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db1df-127">-WhatIf</span></span>
<span data-ttu-id="db1df-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db1df-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db1df-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db1df-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db1df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1df-130">CommonParameters</span></span>
<span data-ttu-id="db1df-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1df-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db1df-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1df-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db1df-133">INPUTS</span></span>

### <span data-ttu-id="db1df-134">System. String</span><span class="sxs-lookup"><span data-stu-id="db1df-134">System.String</span></span>

### <span data-ttu-id="db1df-135">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="db1df-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="db1df-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db1df-136">OUTPUTS</span></span>

### <span data-ttu-id="db1df-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db1df-137">System.Boolean</span></span>

## <span data-ttu-id="db1df-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db1df-138">NOTES</span></span>

## <span data-ttu-id="db1df-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db1df-139">RELATED LINKS</span></span>

[<span data-ttu-id="db1df-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="db1df-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="db1df-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="db1df-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="db1df-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="db1df-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="db1df-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="db1df-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="db1df-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="db1df-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="db1df-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="db1df-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)