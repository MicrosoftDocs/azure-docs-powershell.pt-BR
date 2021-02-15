---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118160"
---
# <span data-ttu-id="8025c-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="8025c-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="8025c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8025c-102">SYNOPSIS</span></span>
<span data-ttu-id="8025c-103">Obtém informações sobre um cluster RedisEnterprise e seu banco de dados associado</span><span class="sxs-lookup"><span data-stu-id="8025c-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="8025c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8025c-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8025c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8025c-105">DESCRIPTION</span></span>
<span data-ttu-id="8025c-106">Obtém informações sobre um cluster RedisEnterprise e seu banco de dados associado</span><span class="sxs-lookup"><span data-stu-id="8025c-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="8025c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8025c-107">EXAMPLES</span></span>

### <span data-ttu-id="8025c-108">Exemplo 1: Obter um Cache Corporativo Redis por nome</span><span class="sxs-lookup"><span data-stu-id="8025c-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="8025c-109">Esse comando obtém o Cache Corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="8025c-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="8025c-110">Exemplo 2: Obter todos os Caches Corporativos Redis em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8025c-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="8025c-111">Esse comando obtém todos os Caches Corporativos Redis no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="8025c-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="8025c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8025c-112">PARAMETERS</span></span>

### <span data-ttu-id="8025c-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8025c-113">-ClusterName</span></span>
<span data-ttu-id="8025c-114">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="8025c-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="8025c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8025c-115">-DefaultProfile</span></span>
<span data-ttu-id="8025c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8025c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8025c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8025c-117">-ResourceGroupName</span></span>
<span data-ttu-id="8025c-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8025c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8025c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8025c-119">-SubscriptionId</span></span>
<span data-ttu-id="8025c-120">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8025c-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8025c-121">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8025c-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8025c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8025c-122">CommonParameters</span></span>
<span data-ttu-id="8025c-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8025c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8025c-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8025c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8025c-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="8025c-125">INPUTS</span></span>

## <span data-ttu-id="8025c-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="8025c-126">OUTPUTS</span></span>

### <span data-ttu-id="8025c-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="8025c-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="8025c-128">Notas</span><span class="sxs-lookup"><span data-stu-id="8025c-128">NOTES</span></span>

<span data-ttu-id="8025c-129">Aliases</span><span class="sxs-lookup"><span data-stu-id="8025c-129">ALIASES</span></span>

## <span data-ttu-id="8025c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8025c-130">RELATED LINKS</span></span>

