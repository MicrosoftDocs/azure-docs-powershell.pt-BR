---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 2b352c649d01e2fceb42f99a6c4dad20859a2adc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602416"
---
# <span data-ttu-id="19e7f-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="19e7f-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="19e7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="19e7f-103">Reinicia os nós de um cache.</span><span class="sxs-lookup"><span data-stu-id="19e7f-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19e7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19e7f-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19e7f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19e7f-105">DESCRIPTION</span></span>
<span data-ttu-id="19e7f-106">O cmdlet **Reset-AzureRmRedisCache** reinicia os nós de uma instância de cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="19e7f-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="19e7f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19e7f-107">EXAMPLES</span></span>

### <span data-ttu-id="19e7f-108">Exemplo 1: reiniciar os dois nós</span><span class="sxs-lookup"><span data-stu-id="19e7f-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="19e7f-109">Esse comando reinicia os dois nós para o cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="19e7f-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="19e7f-110">OS</span><span class="sxs-lookup"><span data-stu-id="19e7f-110">PARAMETERS</span></span>

### <span data-ttu-id="19e7f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="19e7f-111">-Force</span></span>
<span data-ttu-id="19e7f-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="19e7f-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19e7f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="19e7f-113">-Name</span></span>
<span data-ttu-id="19e7f-114">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="19e7f-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="19e7f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19e7f-115">-PassThru</span></span>
<span data-ttu-id="19e7f-116">Indica que esse cmdlet retorna um booliano que indica se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="19e7f-116">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="19e7f-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="19e7f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19e7f-118">-Reboottype</span><span class="sxs-lookup"><span data-stu-id="19e7f-118">-RebootType</span></span>
<span data-ttu-id="19e7f-119">Especifica quais nós ou nós deseja reiniciar.</span><span class="sxs-lookup"><span data-stu-id="19e7f-119">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="19e7f-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="19e7f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19e7f-121">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="19e7f-121">PrimaryNode</span></span> 
- <span data-ttu-id="19e7f-122">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="19e7f-122">SecondaryNode</span></span> 
- <span data-ttu-id="19e7f-123">Subnós</span><span class="sxs-lookup"><span data-stu-id="19e7f-123">AllNodes</span></span>

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

### <span data-ttu-id="19e7f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19e7f-124">-ResourceGroupName</span></span>
<span data-ttu-id="19e7f-125">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="19e7f-125">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="19e7f-126">-Fragmentaid</span><span class="sxs-lookup"><span data-stu-id="19e7f-126">-ShardId</span></span>
<span data-ttu-id="19e7f-127">Especifica a ID do fragmentador que este cmdlet reinicia para um cache Premium com cluster habilitado.</span><span class="sxs-lookup"><span data-stu-id="19e7f-127">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="19e7f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19e7f-128">-Confirm</span></span>
<span data-ttu-id="19e7f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e7f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19e7f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e7f-130">-WhatIf</span></span>
<span data-ttu-id="19e7f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19e7f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19e7f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19e7f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19e7f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e7f-133">-DefaultProfile</span></span>
<span data-ttu-id="19e7f-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19e7f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19e7f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e7f-135">CommonParameters</span></span>
<span data-ttu-id="19e7f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e7f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e7f-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19e7f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e7f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19e7f-138">INPUTS</span></span>

### <span data-ttu-id="19e7f-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="19e7f-139">None</span></span>
<span data-ttu-id="19e7f-140">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="19e7f-140">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="19e7f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19e7f-141">OUTPUTS</span></span>

### <span data-ttu-id="19e7f-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="19e7f-142">None</span></span>

## <span data-ttu-id="19e7f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19e7f-143">NOTES</span></span>
* <span data-ttu-id="19e7f-144">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="19e7f-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="19e7f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19e7f-145">RELATED LINKS</span></span>

[<span data-ttu-id="19e7f-146">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="19e7f-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="19e7f-147">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="19e7f-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="19e7f-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="19e7f-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="19e7f-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="19e7f-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="19e7f-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="19e7f-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


