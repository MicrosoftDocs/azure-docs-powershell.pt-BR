---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: 3d28515ede93abf2ebb5be8bad2e961f2e22b572
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891746"
---
# <span data-ttu-id="2b568-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="2b568-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="2b568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b568-102">SYNOPSIS</span></span>
<span data-ttu-id="2b568-103">Regenera as chaves de acesso do banco de dados RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2b568-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="2b568-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b568-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b568-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b568-105">DESCRIPTION</span></span>
<span data-ttu-id="2b568-106">Regenera as chaves de acesso do banco de dados RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2b568-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="2b568-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b568-107">EXAMPLES</span></span>

### <span data-ttu-id="2b568-108">Exemplo 1: Regenerar a chave de acesso principal</span><span class="sxs-lookup"><span data-stu-id="2b568-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="2b568-109">Este comando regenera a chave de acesso secreta primária usada para autenticar conexões ao banco de dados do Cache corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="2b568-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="2b568-110">Exemplo 2: Regenerar chave de acesso secundário</span><span class="sxs-lookup"><span data-stu-id="2b568-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="2b568-111">Este comando regenera a chave de acesso secreta secundária usada para autenticar conexões ao banco de dados do Cache da Empresa Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="2b568-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="2b568-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b568-112">PARAMETERS</span></span>

### <span data-ttu-id="2b568-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b568-113">-AsJob</span></span>
<span data-ttu-id="2b568-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2b568-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2b568-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2b568-115">-ClusterName</span></span>
<span data-ttu-id="2b568-116">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2b568-116">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b568-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b568-117">-DefaultProfile</span></span>
<span data-ttu-id="2b568-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b568-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b568-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2b568-119">-KeyType</span></span>
<span data-ttu-id="2b568-120">Qual tecla de acesso deve ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="2b568-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b568-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2b568-121">-NoWait</span></span>
<span data-ttu-id="2b568-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2b568-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2b568-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b568-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b568-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b568-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b568-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b568-125">-SubscriptionId</span></span>
<span data-ttu-id="2b568-126">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2b568-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2b568-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2b568-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b568-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b568-128">-Confirm</span></span>
<span data-ttu-id="2b568-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b568-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b568-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b568-130">-WhatIf</span></span>
<span data-ttu-id="2b568-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b568-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b568-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b568-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b568-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b568-133">CommonParameters</span></span>
<span data-ttu-id="2b568-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b568-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b568-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b568-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b568-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b568-136">INPUTS</span></span>

## <span data-ttu-id="2b568-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b568-137">OUTPUTS</span></span>

### <span data-ttu-id="2b568-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2b568-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="2b568-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b568-139">NOTES</span></span>

<span data-ttu-id="2b568-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2b568-140">ALIASES</span></span>

## <span data-ttu-id="2b568-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b568-141">RELATED LINKS</span></span>

