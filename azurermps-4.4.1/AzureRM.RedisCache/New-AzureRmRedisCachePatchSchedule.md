---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602418"
---
# <span data-ttu-id="8053f-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8053f-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="8053f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8053f-102">SYNOPSIS</span></span>
<span data-ttu-id="8053f-103">Adiciona um cronograma de correção.</span><span class="sxs-lookup"><span data-stu-id="8053f-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8053f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8053f-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8053f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8053f-105">DESCRIPTION</span></span>
<span data-ttu-id="8053f-106">O cmdlet **New-AzureRmRedisCachePatchSchedule** adiciona um cronograma de patches a um cache no Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="8053f-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="8053f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8053f-107">EXAMPLES</span></span>

### <span data-ttu-id="8053f-108">Exemplo 1: criar e adicionar um cronograma de patch em um cache</span><span class="sxs-lookup"><span data-stu-id="8053f-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="8053f-109">Esse comando adiciona um cronograma de patches ao cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="8053f-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="8053f-110">O parâmetro Entries usa como seu valor um comando que usa **New-AzureRmRedisCacheScheduleEntry** para criar um cronograma.</span><span class="sxs-lookup"><span data-stu-id="8053f-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="8053f-111">OS</span><span class="sxs-lookup"><span data-stu-id="8053f-111">PARAMETERS</span></span>

### <span data-ttu-id="8053f-112">-Entradas</span><span class="sxs-lookup"><span data-stu-id="8053f-112">-Entries</span></span>
<span data-ttu-id="8053f-113">Especifica uma matriz de agendas que esse cmdlet define em um cache.</span><span class="sxs-lookup"><span data-stu-id="8053f-113">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="8053f-114">Para obter um objeto **PSScheduleEntry** , use o cmdlet New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="8053f-114">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8053f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8053f-115">-Name</span></span>
<span data-ttu-id="8053f-116">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="8053f-116">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="8053f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8053f-117">-ResourceGroupName</span></span>
<span data-ttu-id="8053f-118">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="8053f-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="8053f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8053f-119">-DefaultProfile</span></span>
<span data-ttu-id="8053f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8053f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8053f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8053f-121">CommonParameters</span></span>
<span data-ttu-id="8053f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8053f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8053f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8053f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8053f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8053f-124">INPUTS</span></span>

### <span data-ttu-id="8053f-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8053f-125">None</span></span>
<span data-ttu-id="8053f-126">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="8053f-126">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="8053f-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8053f-127">OUTPUTS</span></span>

### <span data-ttu-id="8053f-128">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="8053f-128">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="8053f-129">Esse cmdlet retorna as entradas de agendamento de patch definidas no cache.</span><span class="sxs-lookup"><span data-stu-id="8053f-129">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="8053f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8053f-130">NOTES</span></span>
* <span data-ttu-id="8053f-131">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="8053f-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8053f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8053f-132">RELATED LINKS</span></span>

[<span data-ttu-id="8053f-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8053f-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="8053f-134">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="8053f-134">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="8053f-135">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8053f-135">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


