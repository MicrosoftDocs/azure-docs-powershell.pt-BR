---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113358"
---
# <span data-ttu-id="32e05-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32e05-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="32e05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32e05-102">SYNOPSIS</span></span>
<span data-ttu-id="32e05-103">Reinicia os nós de um cache.</span><span class="sxs-lookup"><span data-stu-id="32e05-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="32e05-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32e05-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e05-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="32e05-105">DESCRIPTION</span></span>
<span data-ttu-id="32e05-106">O cmdlet **Reset-AzRedisCache** reinicia nós de uma instância do Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="32e05-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="32e05-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="32e05-107">EXAMPLES</span></span>

### <span data-ttu-id="32e05-108">Exemplo 1: Reiniciar ambos os nós</span><span class="sxs-lookup"><span data-stu-id="32e05-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="32e05-109">Esse comando reinicia os dois nós para o cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="32e05-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="32e05-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32e05-110">PARAMETERS</span></span>

### <span data-ttu-id="32e05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e05-111">-DefaultProfile</span></span>
<span data-ttu-id="32e05-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="32e05-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e05-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="32e05-113">-Force</span></span>
<span data-ttu-id="32e05-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="32e05-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32e05-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="32e05-115">-Name</span></span>
<span data-ttu-id="32e05-116">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="32e05-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="32e05-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32e05-117">-PassThru</span></span>
<span data-ttu-id="32e05-118">Indica que esse cmdlet retorna um boolano que indica se a operação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="32e05-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="32e05-119">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="32e05-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32e05-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="32e05-120">-RebootType</span></span>
<span data-ttu-id="32e05-121">Especifica quais nós ou nó reiniciar.</span><span class="sxs-lookup"><span data-stu-id="32e05-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="32e05-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="32e05-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32e05-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="32e05-123">PrimaryNode</span></span> 
- <span data-ttu-id="32e05-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="32e05-124">SecondaryNode</span></span> 
- <span data-ttu-id="32e05-125">Todos osNodes</span><span class="sxs-lookup"><span data-stu-id="32e05-125">AllNodes</span></span>

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

### <span data-ttu-id="32e05-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e05-126">-ResourceGroupName</span></span>
<span data-ttu-id="32e05-127">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="32e05-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="32e05-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="32e05-128">-ShardId</span></span>
<span data-ttu-id="32e05-129">Especifica a ID do fragmento que este cmdlet reinicia para um cache premium com cluster habilitado.</span><span class="sxs-lookup"><span data-stu-id="32e05-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="32e05-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="32e05-130">-Confirm</span></span>
<span data-ttu-id="32e05-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e05-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e05-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e05-132">-WhatIf</span></span>
<span data-ttu-id="32e05-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="32e05-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32e05-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32e05-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e05-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e05-135">CommonParameters</span></span>
<span data-ttu-id="32e05-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e05-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e05-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e05-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e05-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="32e05-138">INPUTS</span></span>

### <span data-ttu-id="32e05-139">System.String</span><span class="sxs-lookup"><span data-stu-id="32e05-139">System.String</span></span>

### <span data-ttu-id="32e05-140">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32e05-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="32e05-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="32e05-141">OUTPUTS</span></span>

### <span data-ttu-id="32e05-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32e05-142">System.Boolean</span></span>

## <span data-ttu-id="32e05-143">Notas</span><span class="sxs-lookup"><span data-stu-id="32e05-143">NOTES</span></span>
* <span data-ttu-id="32e05-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="32e05-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="32e05-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32e05-145">RELATED LINKS</span></span>

[<span data-ttu-id="32e05-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32e05-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="32e05-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32e05-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="32e05-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32e05-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="32e05-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32e05-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="32e05-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32e05-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


