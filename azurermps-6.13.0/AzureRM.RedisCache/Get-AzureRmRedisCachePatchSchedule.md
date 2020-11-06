---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: ac1184dcdcc55a0b5cac28f996c29c3476ba3613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609755"
---
# <span data-ttu-id="7d2ec-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7d2ec-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="7d2ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2ec-103">Obtém um cronograma de correção.</span><span class="sxs-lookup"><span data-stu-id="7d2ec-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d2ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d2ec-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d2ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d2ec-105">DESCRIPTION</span></span>
<span data-ttu-id="7d2ec-106">O cmdlet **Get-AzureRmRedisCachePatchSchedule** Obtém um cronograma de patch para um cache no Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="7d2ec-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="7d2ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d2ec-107">EXAMPLES</span></span>

### <span data-ttu-id="7d2ec-108">Exemplo 1: obter o cronograma do patch</span><span class="sxs-lookup"><span data-stu-id="7d2ec-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="7d2ec-109">Esse comando obtém o cronograma do patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="7d2ec-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="7d2ec-110">OS</span><span class="sxs-lookup"><span data-stu-id="7d2ec-110">PARAMETERS</span></span>

### <span data-ttu-id="7d2ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2ec-111">-DefaultProfile</span></span>
<span data-ttu-id="7d2ec-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2ec-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d2ec-113">-Name</span></span>
<span data-ttu-id="7d2ec-114">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="7d2ec-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="7d2ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="7d2ec-116">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="7d2ec-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="7d2ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2ec-117">CommonParameters</span></span>
<span data-ttu-id="7d2ec-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2ec-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2ec-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2ec-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d2ec-120">INPUTS</span></span>

### <span data-ttu-id="7d2ec-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2ec-121">System.String</span></span>

## <span data-ttu-id="7d2ec-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d2ec-122">OUTPUTS</span></span>

### <span data-ttu-id="7d2ec-123">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="7d2ec-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="7d2ec-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d2ec-124">NOTES</span></span>
* <span data-ttu-id="7d2ec-125">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="7d2ec-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7d2ec-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d2ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="7d2ec-127">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7d2ec-127">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="7d2ec-128">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="7d2ec-128">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="7d2ec-129">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7d2ec-129">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


