---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112662"
---
# <span data-ttu-id="09e78-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="09e78-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="09e78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09e78-102">SYNOPSIS</span></span>
<span data-ttu-id="09e78-103">Obtém informações sobre um banco de dados em um cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="09e78-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="09e78-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09e78-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="09e78-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="09e78-105">DESCRIPTION</span></span>
<span data-ttu-id="09e78-106">Obtém informações sobre um banco de dados em um cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="09e78-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="09e78-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09e78-107">EXAMPLES</span></span>

### <span data-ttu-id="09e78-108">Exemplo 1: Obter banco de dados</span><span class="sxs-lookup"><span data-stu-id="09e78-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="09e78-109">Esse comando obtém o banco de dados do Cache Corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="09e78-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="09e78-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09e78-110">PARAMETERS</span></span>

### <span data-ttu-id="09e78-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="09e78-111">-ClusterName</span></span>
<span data-ttu-id="09e78-112">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="09e78-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="09e78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e78-113">-DefaultProfile</span></span>
<span data-ttu-id="09e78-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09e78-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09e78-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e78-115">-ResourceGroupName</span></span>
<span data-ttu-id="09e78-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09e78-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="09e78-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09e78-117">-SubscriptionId</span></span>
<span data-ttu-id="09e78-118">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="09e78-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="09e78-119">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="09e78-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="09e78-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e78-120">CommonParameters</span></span>
<span data-ttu-id="09e78-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e78-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e78-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09e78-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e78-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="09e78-123">INPUTS</span></span>

## <span data-ttu-id="09e78-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="09e78-124">OUTPUTS</span></span>

### <span data-ttu-id="09e78-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="09e78-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="09e78-126">Notas</span><span class="sxs-lookup"><span data-stu-id="09e78-126">NOTES</span></span>

<span data-ttu-id="09e78-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="09e78-127">ALIASES</span></span>

## <span data-ttu-id="09e78-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09e78-128">RELATED LINKS</span></span>

