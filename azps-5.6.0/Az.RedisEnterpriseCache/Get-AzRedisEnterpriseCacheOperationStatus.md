---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: fd2662af291b8c5c3372f27a3de89f7e18bfd35e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891750"
---
# <span data-ttu-id="d3eca-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d3eca-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="d3eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3eca-102">SYNOPSIS</span></span>
<span data-ttu-id="d3eca-103">Obtém o status da operação.</span><span class="sxs-lookup"><span data-stu-id="d3eca-103">Gets the status of operation.</span></span>

## <span data-ttu-id="d3eca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3eca-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d3eca-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3eca-105">DESCRIPTION</span></span>
<span data-ttu-id="d3eca-106">Obtém o status da operação.</span><span class="sxs-lookup"><span data-stu-id="d3eca-106">Gets the status of operation.</span></span>

## <span data-ttu-id="d3eca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3eca-107">EXAMPLES</span></span>

### <span data-ttu-id="d3eca-108">Exemplo 1: obter o status da operação</span><span class="sxs-lookup"><span data-stu-id="d3eca-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="d3eca-109">Este comando obtém o status de uma operação.</span><span class="sxs-lookup"><span data-stu-id="d3eca-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="d3eca-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3eca-110">PARAMETERS</span></span>

### <span data-ttu-id="d3eca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3eca-111">-DefaultProfile</span></span>
<span data-ttu-id="d3eca-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3eca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3eca-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d3eca-113">-Location</span></span>
<span data-ttu-id="d3eca-114">A região em que a operação está.</span><span class="sxs-lookup"><span data-stu-id="d3eca-114">The region the operation is in.</span></span>

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

### <span data-ttu-id="d3eca-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d3eca-115">-OperationId</span></span>
<span data-ttu-id="d3eca-116">Identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="d3eca-116">The operation's unique identifier.</span></span>

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

### <span data-ttu-id="d3eca-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3eca-117">-SubscriptionId</span></span>
<span data-ttu-id="d3eca-118">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d3eca-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3eca-119">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d3eca-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d3eca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3eca-120">CommonParameters</span></span>
<span data-ttu-id="d3eca-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3eca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3eca-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3eca-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3eca-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3eca-123">INPUTS</span></span>

## <span data-ttu-id="d3eca-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3eca-124">OUTPUTS</span></span>

### <span data-ttu-id="d3eca-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d3eca-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="d3eca-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3eca-126">NOTES</span></span>

<span data-ttu-id="d3eca-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d3eca-127">ALIASES</span></span>

## <span data-ttu-id="d3eca-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3eca-128">RELATED LINKS</span></span>

