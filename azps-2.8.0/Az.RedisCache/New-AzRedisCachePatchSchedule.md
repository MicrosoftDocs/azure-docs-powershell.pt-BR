---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 367327e19ff95132b7b7d6bc2d86970892ab6e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773416"
---
# <span data-ttu-id="31a17-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31a17-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="31a17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31a17-102">SYNOPSIS</span></span>
<span data-ttu-id="31a17-103">Adiciona um cronograma de correção.</span><span class="sxs-lookup"><span data-stu-id="31a17-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="31a17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31a17-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31a17-105">DESCRIPTION</span></span>
<span data-ttu-id="31a17-106">O cmdlet **New-AzRedisCachePatchSchedule** adiciona um cronograma de patches a um cache no Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="31a17-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="31a17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31a17-107">EXAMPLES</span></span>

### <span data-ttu-id="31a17-108">Exemplo 1: criar e adicionar um cronograma de patch em um cache</span><span class="sxs-lookup"><span data-stu-id="31a17-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="31a17-109">Esse comando adiciona um cronograma de patches ao cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="31a17-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="31a17-110">O parâmetro Entries usa como seu valor um comando que usa **New-AzRedisCacheScheduleEntry** para criar um cronograma.</span><span class="sxs-lookup"><span data-stu-id="31a17-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="31a17-111">OS</span><span class="sxs-lookup"><span data-stu-id="31a17-111">PARAMETERS</span></span>

### <span data-ttu-id="31a17-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a17-112">-DefaultProfile</span></span>
<span data-ttu-id="31a17-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31a17-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a17-114">-Entradas</span><span class="sxs-lookup"><span data-stu-id="31a17-114">-Entries</span></span>
<span data-ttu-id="31a17-115">Especifica uma matriz de agendas que esse cmdlet define em um cache.</span><span class="sxs-lookup"><span data-stu-id="31a17-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="31a17-116">Para obter um objeto **PSScheduleEntry** , use o cmdlet New-AzRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="31a17-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="31a17-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="31a17-117">-Name</span></span>
<span data-ttu-id="31a17-118">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="31a17-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="31a17-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a17-119">-ResourceGroupName</span></span>
<span data-ttu-id="31a17-120">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="31a17-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="31a17-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="31a17-121">-Confirm</span></span>
<span data-ttu-id="31a17-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31a17-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a17-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a17-123">-WhatIf</span></span>
<span data-ttu-id="31a17-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31a17-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31a17-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31a17-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a17-126">CommonParameters</span></span>
<span data-ttu-id="31a17-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a17-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a17-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a17-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31a17-129">INPUTS</span></span>

### <span data-ttu-id="31a17-130">System. String</span><span class="sxs-lookup"><span data-stu-id="31a17-130">System.String</span></span>

### <span data-ttu-id="31a17-131">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="31a17-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="31a17-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31a17-132">OUTPUTS</span></span>

### <span data-ttu-id="31a17-133">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="31a17-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="31a17-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31a17-134">NOTES</span></span>
* <span data-ttu-id="31a17-135">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="31a17-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="31a17-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31a17-136">RELATED LINKS</span></span>

[<span data-ttu-id="31a17-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31a17-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="31a17-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="31a17-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="31a17-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31a17-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


