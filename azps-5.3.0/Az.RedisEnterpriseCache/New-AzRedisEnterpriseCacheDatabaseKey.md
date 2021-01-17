---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427396"
---
# <span data-ttu-id="2dcf7-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="2dcf7-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="2dcf7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dcf7-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcf7-103">Gera novamente as teclas de acesso do banco de dados RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="2dcf7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dcf7-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2dcf7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dcf7-105">DESCRIPTION</span></span>
<span data-ttu-id="2dcf7-106">Gera novamente as teclas de acesso do banco de dados RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="2dcf7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dcf7-107">EXAMPLES</span></span>

### <span data-ttu-id="2dcf7-108">Exemplo 1: regenerar a chave de acesso primária</span><span class="sxs-lookup"><span data-stu-id="2dcf7-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="2dcf7-109">Esse comando regenera a chave de acesso de segredo primário usada para autenticar conexões para o banco de dados do cache corporativo do Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="2dcf7-110">Exemplo 2: regenerar a chave de acesso secundário</span><span class="sxs-lookup"><span data-stu-id="2dcf7-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="2dcf7-111">Esse comando regenera a chave de acesso de segredo secundário usada para autenticar conexões para o banco de dados do cache corporativo do Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="2dcf7-112">OS</span><span class="sxs-lookup"><span data-stu-id="2dcf7-112">PARAMETERS</span></span>

### <span data-ttu-id="2dcf7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dcf7-113">-AsJob</span></span>
<span data-ttu-id="2dcf7-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2dcf7-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2dcf7-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2dcf7-115">-ClusterName</span></span>
<span data-ttu-id="2dcf7-116">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="2dcf7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcf7-117">-DefaultProfile</span></span>
<span data-ttu-id="2dcf7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dcf7-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2dcf7-119">-KeyType</span></span>
<span data-ttu-id="2dcf7-120">Qual tecla de acesso deve ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-120">Which access key to regenerate.</span></span>

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

### <span data-ttu-id="2dcf7-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2dcf7-121">-NoWait</span></span>
<span data-ttu-id="2dcf7-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2dcf7-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2dcf7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dcf7-123">-ResourceGroupName</span></span>
<span data-ttu-id="2dcf7-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2dcf7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2dcf7-125">-SubscriptionId</span></span>
<span data-ttu-id="2dcf7-126">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2dcf7-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2dcf7-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2dcf7-128">-Confirm</span></span>
<span data-ttu-id="2dcf7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dcf7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dcf7-130">-WhatIf</span></span>
<span data-ttu-id="2dcf7-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dcf7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dcf7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcf7-133">CommonParameters</span></span>
<span data-ttu-id="2dcf7-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dcf7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcf7-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dcf7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcf7-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dcf7-136">INPUTS</span></span>

## <span data-ttu-id="2dcf7-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dcf7-137">OUTPUTS</span></span>

### <span data-ttu-id="2dcf7-138">Microsoft. Azure. PowerShell. cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2dcf7-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="2dcf7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dcf7-139">NOTES</span></span>

<span data-ttu-id="2dcf7-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2dcf7-140">ALIASES</span></span>

## <span data-ttu-id="2dcf7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dcf7-141">RELATED LINKS</span></span>

