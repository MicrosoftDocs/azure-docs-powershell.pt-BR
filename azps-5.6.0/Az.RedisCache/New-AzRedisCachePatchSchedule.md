---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: ebc51005bcffdde2ad5f64764e90440e8d1e7583
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886601"
---
# <span data-ttu-id="b2b21-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b2b21-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="b2b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2b21-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b21-103">Adiciona um cronograma de patch.</span><span class="sxs-lookup"><span data-stu-id="b2b21-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="b2b21-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b2b21-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2b21-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b2b21-105">DESCRIPTION</span></span>
<span data-ttu-id="b2b21-106">O cmdlet **New-AzRedisCachePatchSchedule** adiciona uma agenda de patch a um cache no Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="b2b21-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="b2b21-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2b21-107">EXAMPLES</span></span>

### <span data-ttu-id="b2b21-108">Exemplo 1: Criar e adicionar um agendamento de patch em um cache</span><span class="sxs-lookup"><span data-stu-id="b2b21-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="b2b21-109">Este comando adiciona um cronograma de patch ao cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="b2b21-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="b2b21-110">O parâmetro Entries tem como valor um comando que usa **New-AzRedisCacheScheduleEntry** para criar uma agenda.</span><span class="sxs-lookup"><span data-stu-id="b2b21-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="b2b21-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b2b21-111">PARAMETERS</span></span>

### <span data-ttu-id="b2b21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b21-112">-DefaultProfile</span></span>
<span data-ttu-id="b2b21-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b2b21-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2b21-114">-Entradas</span><span class="sxs-lookup"><span data-stu-id="b2b21-114">-Entries</span></span>
<span data-ttu-id="b2b21-115">Especifica uma matriz de agendamentos que esse cmdlet define em um cache.</span><span class="sxs-lookup"><span data-stu-id="b2b21-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="b2b21-116">Para obter um **objeto PSScheduleEntry,** use o cmdlet New-AzRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="b2b21-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="b2b21-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b2b21-117">-Name</span></span>
<span data-ttu-id="b2b21-118">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="b2b21-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="b2b21-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b21-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2b21-120">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="b2b21-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="b2b21-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2b21-121">-Confirm</span></span>
<span data-ttu-id="b2b21-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2b21-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2b21-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2b21-123">-WhatIf</span></span>
<span data-ttu-id="b2b21-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2b21-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2b21-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2b21-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2b21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b21-126">CommonParameters</span></span>
<span data-ttu-id="b2b21-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b21-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b21-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b21-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2b21-129">INPUTS</span></span>

### <span data-ttu-id="b2b21-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b2b21-130">System.String</span></span>

### <span data-ttu-id="b2b21-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="b2b21-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="b2b21-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b2b21-132">OUTPUTS</span></span>

### <span data-ttu-id="b2b21-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b2b21-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="b2b21-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="b2b21-134">NOTES</span></span>
* <span data-ttu-id="b2b21-135">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="b2b21-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b2b21-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2b21-136">RELATED LINKS</span></span>

[<span data-ttu-id="b2b21-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b2b21-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b2b21-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b2b21-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="b2b21-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b2b21-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


