---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: 797ea800962e00dfd94e1be14e39293fc303ef38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891767"
---
# <span data-ttu-id="e086a-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e086a-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="e086a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e086a-102">SYNOPSIS</span></span>
<span data-ttu-id="e086a-103">Reinicia nós de um cache.</span><span class="sxs-lookup"><span data-stu-id="e086a-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="e086a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e086a-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e086a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e086a-105">DESCRIPTION</span></span>
<span data-ttu-id="e086a-106">O cmdlet **Reset-AzRedisCache** reinicia os nós de uma instância do Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e086a-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="e086a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e086a-107">EXAMPLES</span></span>

### <span data-ttu-id="e086a-108">Exemplo 1: Reiniciar ambos os nós</span><span class="sxs-lookup"><span data-stu-id="e086a-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="e086a-109">Este comando reinicia os dois nós para o cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="e086a-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="e086a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e086a-110">PARAMETERS</span></span>

### <span data-ttu-id="e086a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e086a-111">-DefaultProfile</span></span>
<span data-ttu-id="e086a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e086a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e086a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e086a-113">-Force</span></span>
<span data-ttu-id="e086a-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e086a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e086a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e086a-115">-Name</span></span>
<span data-ttu-id="e086a-116">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="e086a-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="e086a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e086a-117">-PassThru</span></span>
<span data-ttu-id="e086a-118">Indica que esse cmdlet retorna um Boolean que indica se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e086a-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="e086a-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e086a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e086a-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="e086a-120">-RebootType</span></span>
<span data-ttu-id="e086a-121">Especifica qual nó ou nós reiniciar.</span><span class="sxs-lookup"><span data-stu-id="e086a-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="e086a-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e086a-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e086a-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="e086a-123">PrimaryNode</span></span> 
- <span data-ttu-id="e086a-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="e086a-124">SecondaryNode</span></span> 
- <span data-ttu-id="e086a-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="e086a-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e086a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e086a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e086a-127">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="e086a-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="e086a-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="e086a-128">-ShardId</span></span>
<span data-ttu-id="e086a-129">Especifica a ID do fragmento que este cmdlet reinicia para um cache premium com clustering habilitado.</span><span class="sxs-lookup"><span data-stu-id="e086a-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e086a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e086a-130">-Confirm</span></span>
<span data-ttu-id="e086a-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e086a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e086a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e086a-132">-WhatIf</span></span>
<span data-ttu-id="e086a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e086a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e086a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e086a-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e086a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e086a-135">CommonParameters</span></span>
<span data-ttu-id="e086a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e086a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e086a-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e086a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e086a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e086a-138">INPUTS</span></span>

### <span data-ttu-id="e086a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e086a-139">System.String</span></span>

### <span data-ttu-id="e086a-140">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e086a-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e086a-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e086a-141">OUTPUTS</span></span>

### <span data-ttu-id="e086a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e086a-142">System.Boolean</span></span>

## <span data-ttu-id="e086a-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="e086a-143">NOTES</span></span>
* <span data-ttu-id="e086a-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="e086a-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e086a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e086a-145">RELATED LINKS</span></span>

[<span data-ttu-id="e086a-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e086a-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="e086a-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e086a-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="e086a-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e086a-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="e086a-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e086a-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="e086a-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e086a-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


