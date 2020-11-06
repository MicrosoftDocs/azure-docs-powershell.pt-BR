---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 25c3d0c72539ecd74e25ed455b4afcf4211c0718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609380"
---
# <span data-ttu-id="7eed8-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7eed8-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="7eed8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7eed8-102">SYNOPSIS</span></span>
<span data-ttu-id="7eed8-103">Remover uma regra de firewall de um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="7eed8-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eed8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7eed8-104">SYNTAX</span></span>

### <span data-ttu-id="7eed8-105">NormalParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7eed8-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eed8-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="7eed8-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eed8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7eed8-107">DESCRIPTION</span></span>
<span data-ttu-id="7eed8-108">Remover uma regra de firewall de um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="7eed8-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="7eed8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7eed8-109">EXAMPLES</span></span>

### <span data-ttu-id="7eed8-110">Exemplo 1: remover uma única regra de firewall</span><span class="sxs-lookup"><span data-stu-id="7eed8-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="7eed8-111">Esse comando Remove uma regra de firewall chamada ruleone do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="7eed8-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="7eed8-112">OS</span><span class="sxs-lookup"><span data-stu-id="7eed8-112">PARAMETERS</span></span>

### <span data-ttu-id="7eed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eed8-113">-DefaultProfile</span></span>
<span data-ttu-id="7eed8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7eed8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eed8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eed8-115">-InputObject</span></span>
<span data-ttu-id="7eed8-116">objeto do tipo PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7eed8-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="7eed8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7eed8-117">-Name</span></span>
<span data-ttu-id="7eed8-118">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="7eed8-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="7eed8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7eed8-119">-PassThru</span></span>
<span data-ttu-id="7eed8-120">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="7eed8-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7eed8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eed8-121">-ResourceGroupName</span></span>
<span data-ttu-id="7eed8-122">Nome do grupo de recursos no qual existe o cache.</span><span class="sxs-lookup"><span data-stu-id="7eed8-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="7eed8-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7eed8-123">-RuleName</span></span>
<span data-ttu-id="7eed8-124">Nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="7eed8-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="7eed8-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7eed8-125">-Confirm</span></span>
<span data-ttu-id="7eed8-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eed8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eed8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eed8-127">-WhatIf</span></span>
<span data-ttu-id="7eed8-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7eed8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eed8-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7eed8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eed8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eed8-130">CommonParameters</span></span>
<span data-ttu-id="7eed8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eed8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eed8-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eed8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eed8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7eed8-133">INPUTS</span></span>

### <span data-ttu-id="7eed8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7eed8-134">System.String</span></span>

### <span data-ttu-id="7eed8-135">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7eed8-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>
<span data-ttu-id="7eed8-136">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7eed8-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7eed8-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7eed8-137">OUTPUTS</span></span>

### <span data-ttu-id="7eed8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7eed8-138">System.Boolean</span></span>

## <span data-ttu-id="7eed8-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7eed8-139">NOTES</span></span>

## <span data-ttu-id="7eed8-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7eed8-140">RELATED LINKS</span></span>

[<span data-ttu-id="7eed8-141">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7eed8-141">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="7eed8-142">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7eed8-142">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="7eed8-143">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eed8-143">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="7eed8-144">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eed8-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="7eed8-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eed8-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="7eed8-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eed8-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
