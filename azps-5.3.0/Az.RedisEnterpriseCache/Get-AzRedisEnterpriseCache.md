---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427398"
---
# <span data-ttu-id="f1428-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="f1428-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="f1428-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1428-102">SYNOPSIS</span></span>
<span data-ttu-id="f1428-103">Obtém informações sobre um cluster do RedisEnterprise e seu banco de dados associado</span><span class="sxs-lookup"><span data-stu-id="f1428-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="f1428-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1428-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f1428-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1428-105">DESCRIPTION</span></span>
<span data-ttu-id="f1428-106">Obtém informações sobre um cluster do RedisEnterprise e seu banco de dados associado</span><span class="sxs-lookup"><span data-stu-id="f1428-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="f1428-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1428-107">EXAMPLES</span></span>

### <span data-ttu-id="f1428-108">Exemplo 1: obter um cache corporativo Redis por nome</span><span class="sxs-lookup"><span data-stu-id="f1428-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="f1428-109">Esse comando obtém o cache corporativo Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="f1428-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="f1428-110">Exemplo 2: obter cada cache corporativo do Redis em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f1428-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="f1428-111">Esse comando obtém todos os Redis Enterprise cache do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f1428-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="f1428-112">OS</span><span class="sxs-lookup"><span data-stu-id="f1428-112">PARAMETERS</span></span>

### <span data-ttu-id="f1428-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f1428-113">-ClusterName</span></span>
<span data-ttu-id="f1428-114">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="f1428-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="f1428-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1428-115">-DefaultProfile</span></span>
<span data-ttu-id="f1428-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1428-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1428-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1428-117">-ResourceGroupName</span></span>
<span data-ttu-id="f1428-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1428-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1428-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1428-119">-SubscriptionId</span></span>
<span data-ttu-id="f1428-120">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f1428-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f1428-121">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f1428-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f1428-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1428-122">CommonParameters</span></span>
<span data-ttu-id="f1428-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1428-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1428-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1428-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1428-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1428-125">INPUTS</span></span>

## <span data-ttu-id="f1428-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1428-126">OUTPUTS</span></span>

### <span data-ttu-id="f1428-127">Microsoft. Azure. PowerShell. cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="f1428-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="f1428-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1428-128">NOTES</span></span>

<span data-ttu-id="f1428-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f1428-129">ALIASES</span></span>

## <span data-ttu-id="f1428-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1428-130">RELATED LINKS</span></span>

