---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271612"
---
# <span data-ttu-id="f54c8-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="f54c8-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="f54c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f54c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f54c8-103">Obtém o status da operação.</span><span class="sxs-lookup"><span data-stu-id="f54c8-103">Gets the status of operation.</span></span>

## <span data-ttu-id="f54c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f54c8-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f54c8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f54c8-105">DESCRIPTION</span></span>
<span data-ttu-id="f54c8-106">Obtém o status da operação.</span><span class="sxs-lookup"><span data-stu-id="f54c8-106">Gets the status of operation.</span></span>

## <span data-ttu-id="f54c8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f54c8-107">EXAMPLES</span></span>

### <span data-ttu-id="f54c8-108">Exemplo 1: obter o status da operação</span><span class="sxs-lookup"><span data-stu-id="f54c8-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="f54c8-109">Esse comando obtém o status de uma operação.</span><span class="sxs-lookup"><span data-stu-id="f54c8-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="f54c8-110">OS</span><span class="sxs-lookup"><span data-stu-id="f54c8-110">PARAMETERS</span></span>

### <span data-ttu-id="f54c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54c8-111">-DefaultProfile</span></span>
<span data-ttu-id="f54c8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f54c8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f54c8-113">-Local</span><span class="sxs-lookup"><span data-stu-id="f54c8-113">-Location</span></span>
<span data-ttu-id="f54c8-114">A região em que a operação se encontra.</span><span class="sxs-lookup"><span data-stu-id="f54c8-114">The region the operation is in.</span></span>

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

### <span data-ttu-id="f54c8-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f54c8-115">-OperationId</span></span>
<span data-ttu-id="f54c8-116">O identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="f54c8-116">The operation's unique identifier.</span></span>

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

### <span data-ttu-id="f54c8-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f54c8-117">-SubscriptionId</span></span>
<span data-ttu-id="f54c8-118">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f54c8-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f54c8-119">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f54c8-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f54c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54c8-120">CommonParameters</span></span>
<span data-ttu-id="f54c8-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54c8-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f54c8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54c8-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f54c8-123">INPUTS</span></span>

## <span data-ttu-id="f54c8-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f54c8-124">OUTPUTS</span></span>

### <span data-ttu-id="f54c8-125">Microsoft. Azure. PowerShell. cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="f54c8-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="f54c8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f54c8-126">NOTES</span></span>

<span data-ttu-id="f54c8-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f54c8-127">ALIASES</span></span>

## <span data-ttu-id="f54c8-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f54c8-128">RELATED LINKS</span></span>

