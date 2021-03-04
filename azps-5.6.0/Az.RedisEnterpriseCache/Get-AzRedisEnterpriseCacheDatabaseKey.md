---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ff635c55600c6528ecad537b74a843e2d1da830e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891751"
---
# <span data-ttu-id="829bb-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="829bb-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="829bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="829bb-102">SYNOPSIS</span></span>
<span data-ttu-id="829bb-103">Recupera as chaves de acesso para o banco de dados RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="829bb-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="829bb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="829bb-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="829bb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="829bb-105">DESCRIPTION</span></span>
<span data-ttu-id="829bb-106">Recupera as chaves de acesso para o banco de dados RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="829bb-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="829bb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="829bb-107">EXAMPLES</span></span>

### <span data-ttu-id="829bb-108">Exemplo 1: Obter chaves de acesso ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="829bb-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="829bb-109">Este comando obtém as chaves de acesso secreto usadas para autenticar conexões ao banco de dados do Cache da Empresa Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="829bb-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="829bb-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="829bb-110">PARAMETERS</span></span>

### <span data-ttu-id="829bb-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="829bb-111">-ClusterName</span></span>
<span data-ttu-id="829bb-112">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="829bb-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="829bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829bb-113">-DefaultProfile</span></span>
<span data-ttu-id="829bb-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="829bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="829bb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="829bb-115">-ResourceGroupName</span></span>
<span data-ttu-id="829bb-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="829bb-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="829bb-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="829bb-117">-SubscriptionId</span></span>
<span data-ttu-id="829bb-118">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="829bb-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="829bb-119">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="829bb-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829bb-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="829bb-120">-Confirm</span></span>
<span data-ttu-id="829bb-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="829bb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="829bb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="829bb-122">-WhatIf</span></span>
<span data-ttu-id="829bb-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="829bb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="829bb-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="829bb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="829bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829bb-125">CommonParameters</span></span>
<span data-ttu-id="829bb-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="829bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829bb-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="829bb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829bb-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="829bb-128">INPUTS</span></span>

## <span data-ttu-id="829bb-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="829bb-129">OUTPUTS</span></span>

### <span data-ttu-id="829bb-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="829bb-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="829bb-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="829bb-131">NOTES</span></span>

<span data-ttu-id="829bb-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="829bb-132">ALIASES</span></span>

## <span data-ttu-id="829bb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="829bb-133">RELATED LINKS</span></span>

