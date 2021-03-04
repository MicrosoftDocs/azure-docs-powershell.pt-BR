---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: fd127005107586e31798d215d7f54888b26705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891756"
---
# <span data-ttu-id="1741f-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="1741f-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="1741f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1741f-102">SYNOPSIS</span></span>
<span data-ttu-id="1741f-103">Obtém informações sobre um cluster RedisEnterprise e seu banco de dados associado</span><span class="sxs-lookup"><span data-stu-id="1741f-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="1741f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1741f-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1741f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1741f-105">DESCRIPTION</span></span>
<span data-ttu-id="1741f-106">Obtém informações sobre um cluster RedisEnterprise e seu banco de dados associado</span><span class="sxs-lookup"><span data-stu-id="1741f-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="1741f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1741f-107">EXAMPLES</span></span>

### <span data-ttu-id="1741f-108">Exemplo 1: Obter um Cache da Empresa Redis pelo nome</span><span class="sxs-lookup"><span data-stu-id="1741f-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="1741f-109">Este comando obtém o Cache da Empresa Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="1741f-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="1741f-110">Exemplo 2: Obter todos os Redis Enterprise Cache em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1741f-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="1741f-111">Este comando obtém todos os Redis Enterprise Cache no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="1741f-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="1741f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1741f-112">PARAMETERS</span></span>

### <span data-ttu-id="1741f-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1741f-113">-ClusterName</span></span>
<span data-ttu-id="1741f-114">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1741f-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1741f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1741f-115">-DefaultProfile</span></span>
<span data-ttu-id="1741f-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1741f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1741f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1741f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1741f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1741f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="1741f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1741f-119">-SubscriptionId</span></span>
<span data-ttu-id="1741f-120">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1741f-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1741f-121">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1741f-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1741f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1741f-122">CommonParameters</span></span>
<span data-ttu-id="1741f-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1741f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1741f-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1741f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1741f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1741f-125">INPUTS</span></span>

## <span data-ttu-id="1741f-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1741f-126">OUTPUTS</span></span>

### <span data-ttu-id="1741f-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="1741f-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="1741f-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="1741f-128">NOTES</span></span>

<span data-ttu-id="1741f-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1741f-129">ALIASES</span></span>

## <span data-ttu-id="1741f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1741f-130">RELATED LINKS</span></span>

