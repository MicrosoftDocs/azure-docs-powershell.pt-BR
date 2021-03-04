---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9033082093d571fc60cd9b4c495688d11d87aea8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891752"
---
# <span data-ttu-id="f049b-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="f049b-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="f049b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f049b-102">SYNOPSIS</span></span>
<span data-ttu-id="f049b-103">Obtém informações sobre um banco de dados em um cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="f049b-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="f049b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f049b-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f049b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f049b-105">DESCRIPTION</span></span>
<span data-ttu-id="f049b-106">Obtém informações sobre um banco de dados em um cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="f049b-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="f049b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f049b-107">EXAMPLES</span></span>

### <span data-ttu-id="f049b-108">Exemplo 1: Obter banco de dados</span><span class="sxs-lookup"><span data-stu-id="f049b-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="f049b-109">Este comando obtém o banco de dados do Cache da Empresa Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="f049b-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="f049b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f049b-110">PARAMETERS</span></span>

### <span data-ttu-id="f049b-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f049b-111">-ClusterName</span></span>
<span data-ttu-id="f049b-112">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="f049b-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="f049b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f049b-113">-DefaultProfile</span></span>
<span data-ttu-id="f049b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f049b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f049b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f049b-115">-ResourceGroupName</span></span>
<span data-ttu-id="f049b-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f049b-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="f049b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f049b-117">-SubscriptionId</span></span>
<span data-ttu-id="f049b-118">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f049b-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f049b-119">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f049b-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f049b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f049b-120">CommonParameters</span></span>
<span data-ttu-id="f049b-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f049b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f049b-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f049b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f049b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f049b-123">INPUTS</span></span>

## <span data-ttu-id="f049b-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f049b-124">OUTPUTS</span></span>

### <span data-ttu-id="f049b-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="f049b-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="f049b-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="f049b-126">NOTES</span></span>

<span data-ttu-id="f049b-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f049b-127">ALIASES</span></span>

## <span data-ttu-id="f049b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f049b-128">RELATED LINKS</span></span>

