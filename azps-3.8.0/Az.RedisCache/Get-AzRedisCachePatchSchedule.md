---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943564"
---
# <span data-ttu-id="6ede1-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6ede1-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="6ede1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ede1-102">SYNOPSIS</span></span>
<span data-ttu-id="6ede1-103">Obtém um cronograma de correção.</span><span class="sxs-lookup"><span data-stu-id="6ede1-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="6ede1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ede1-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ede1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ede1-105">DESCRIPTION</span></span>
<span data-ttu-id="6ede1-106">O cmdlet **Get-AzRedisCachePatchSchedule** Obtém um cronograma de patch para um cache no Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="6ede1-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="6ede1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ede1-107">EXAMPLES</span></span>

### <span data-ttu-id="6ede1-108">Exemplo 1: obter o cronograma do patch</span><span class="sxs-lookup"><span data-stu-id="6ede1-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="6ede1-109">Esse comando obtém o cronograma do patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="6ede1-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="6ede1-110">OS</span><span class="sxs-lookup"><span data-stu-id="6ede1-110">PARAMETERS</span></span>

### <span data-ttu-id="6ede1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ede1-111">-DefaultProfile</span></span>
<span data-ttu-id="6ede1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ede1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ede1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ede1-113">-Name</span></span>
<span data-ttu-id="6ede1-114">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="6ede1-114">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ede1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ede1-115">-ResourceGroupName</span></span>
<span data-ttu-id="6ede1-116">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="6ede1-116">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ede1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ede1-117">CommonParameters</span></span>
<span data-ttu-id="6ede1-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ede1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ede1-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ede1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ede1-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ede1-120">INPUTS</span></span>

### <span data-ttu-id="6ede1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6ede1-121">System.String</span></span>

## <span data-ttu-id="6ede1-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ede1-122">OUTPUTS</span></span>

### <span data-ttu-id="6ede1-123">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="6ede1-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="6ede1-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ede1-124">NOTES</span></span>
* <span data-ttu-id="6ede1-125">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="6ede1-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6ede1-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ede1-126">RELATED LINKS</span></span>

[<span data-ttu-id="6ede1-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6ede1-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="6ede1-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="6ede1-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="6ede1-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6ede1-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


