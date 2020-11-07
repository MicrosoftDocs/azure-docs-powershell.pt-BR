---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: 2e34bc9a468a662db8dc4bba155cd70a1c24bcfe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772647"
---
# <span data-ttu-id="45e35-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45e35-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="45e35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45e35-102">SYNOPSIS</span></span>
<span data-ttu-id="45e35-103">Reinicia os nós de um cache.</span><span class="sxs-lookup"><span data-stu-id="45e35-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="45e35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45e35-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45e35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45e35-105">DESCRIPTION</span></span>
<span data-ttu-id="45e35-106">O cmdlet **Reset-AzRedisCache** reinicia os nós de uma instância de cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="45e35-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="45e35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45e35-107">EXAMPLES</span></span>

### <span data-ttu-id="45e35-108">Exemplo 1: reiniciar os dois nós</span><span class="sxs-lookup"><span data-stu-id="45e35-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="45e35-109">Esse comando reinicia os dois nós para o cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="45e35-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="45e35-110">OS</span><span class="sxs-lookup"><span data-stu-id="45e35-110">PARAMETERS</span></span>

### <span data-ttu-id="45e35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e35-111">-DefaultProfile</span></span>
<span data-ttu-id="45e35-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45e35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45e35-113">-Force</span><span class="sxs-lookup"><span data-stu-id="45e35-113">-Force</span></span>
<span data-ttu-id="45e35-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="45e35-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45e35-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="45e35-115">-Name</span></span>
<span data-ttu-id="45e35-116">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="45e35-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="45e35-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45e35-117">-PassThru</span></span>
<span data-ttu-id="45e35-118">Indica que esse cmdlet retorna um booliano que indica se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="45e35-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="45e35-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="45e35-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45e35-120">-Reboottype</span><span class="sxs-lookup"><span data-stu-id="45e35-120">-RebootType</span></span>
<span data-ttu-id="45e35-121">Especifica quais nós ou nós deseja reiniciar.</span><span class="sxs-lookup"><span data-stu-id="45e35-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="45e35-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="45e35-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45e35-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="45e35-123">PrimaryNode</span></span> 
- <span data-ttu-id="45e35-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="45e35-124">SecondaryNode</span></span> 
- <span data-ttu-id="45e35-125">Subnós</span><span class="sxs-lookup"><span data-stu-id="45e35-125">AllNodes</span></span>

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

### <span data-ttu-id="45e35-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e35-126">-ResourceGroupName</span></span>
<span data-ttu-id="45e35-127">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="45e35-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="45e35-128">-Fragmentaid</span><span class="sxs-lookup"><span data-stu-id="45e35-128">-ShardId</span></span>
<span data-ttu-id="45e35-129">Especifica a ID do fragmentador que este cmdlet reinicia para um cache Premium com cluster habilitado.</span><span class="sxs-lookup"><span data-stu-id="45e35-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="45e35-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45e35-130">-Confirm</span></span>
<span data-ttu-id="45e35-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e35-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e35-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e35-132">-WhatIf</span></span>
<span data-ttu-id="45e35-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45e35-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45e35-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45e35-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e35-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e35-135">CommonParameters</span></span>
<span data-ttu-id="45e35-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e35-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e35-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e35-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e35-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45e35-138">INPUTS</span></span>

### <span data-ttu-id="45e35-139">System. String</span><span class="sxs-lookup"><span data-stu-id="45e35-139">System.String</span></span>

### <span data-ttu-id="45e35-140">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="45e35-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="45e35-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45e35-141">OUTPUTS</span></span>

### <span data-ttu-id="45e35-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45e35-142">System.Boolean</span></span>

## <span data-ttu-id="45e35-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45e35-143">NOTES</span></span>
* <span data-ttu-id="45e35-144">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="45e35-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="45e35-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45e35-145">RELATED LINKS</span></span>

[<span data-ttu-id="45e35-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45e35-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="45e35-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45e35-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="45e35-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45e35-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="45e35-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45e35-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="45e35-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="45e35-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


