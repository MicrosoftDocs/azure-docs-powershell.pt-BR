---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: d96ccfb2160d7121ffda4802a0fd8afa43ea4589
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889886"
---
# <span data-ttu-id="32e7b-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="32e7b-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="32e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="32e7b-103">Cria uma entrada de agendamento.</span><span class="sxs-lookup"><span data-stu-id="32e7b-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="32e7b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32e7b-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32e7b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="32e7b-106">O cmdlet **New-AzRedisCacheScheduleEntry** cria um **objeto PSScheduleEntry.**</span><span class="sxs-lookup"><span data-stu-id="32e7b-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="32e7b-107">Os cmdlets de agendamento de patch do Cache do Azure Redis, como o cmdlet New-AzRedisCachePatchSchedule, exigem objetos de entrada de agendamento.</span><span class="sxs-lookup"><span data-stu-id="32e7b-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="32e7b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32e7b-108">EXAMPLES</span></span>

### <span data-ttu-id="32e7b-109">Exemplo 1: Criar uma entrada de agendamento para fins de semana</span><span class="sxs-lookup"><span data-stu-id="32e7b-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="32e7b-110">Este comando cria um **objeto PSScheduleEntry** que representa um cronograma de fim de semana que tem a hora de início e a janela especificadas.</span><span class="sxs-lookup"><span data-stu-id="32e7b-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="32e7b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32e7b-111">PARAMETERS</span></span>

### <span data-ttu-id="32e7b-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="32e7b-112">-DayOfWeek</span></span>
<span data-ttu-id="32e7b-113">Especifica o dia da semana para a entrada de agendamento.</span><span class="sxs-lookup"><span data-stu-id="32e7b-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="32e7b-114">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="32e7b-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32e7b-115">Todos os dias</span><span class="sxs-lookup"><span data-stu-id="32e7b-115">Everyday</span></span> 
- <span data-ttu-id="32e7b-116">Fim de semana</span><span class="sxs-lookup"><span data-stu-id="32e7b-116">Weekend</span></span> 
- <span data-ttu-id="32e7b-117">Segunda-feira</span><span class="sxs-lookup"><span data-stu-id="32e7b-117">Monday</span></span> 
- <span data-ttu-id="32e7b-118">Terça-feira</span><span class="sxs-lookup"><span data-stu-id="32e7b-118">Tuesday</span></span> 
- <span data-ttu-id="32e7b-119">Quarta-feira</span><span class="sxs-lookup"><span data-stu-id="32e7b-119">Wednesday</span></span> 
- <span data-ttu-id="32e7b-120">Quinta-feira</span><span class="sxs-lookup"><span data-stu-id="32e7b-120">Thursday</span></span> 
- <span data-ttu-id="32e7b-121">Sexta-feira</span><span class="sxs-lookup"><span data-stu-id="32e7b-121">Friday</span></span> 
- <span data-ttu-id="32e7b-122">Sábado</span><span class="sxs-lookup"><span data-stu-id="32e7b-122">Saturday</span></span> 
- <span data-ttu-id="32e7b-123">Domingo</span><span class="sxs-lookup"><span data-stu-id="32e7b-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e7b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e7b-124">-DefaultProfile</span></span>
<span data-ttu-id="32e7b-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="32e7b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e7b-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="32e7b-126">-MaintenanceWindow</span></span>
<span data-ttu-id="32e7b-127">Especifica o período de tempo permitido para atualizações.</span><span class="sxs-lookup"><span data-stu-id="32e7b-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e7b-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="32e7b-128">-StartHourUtc</span></span>
<span data-ttu-id="32e7b-129">Especifica uma hora do dia em que a agenda é iniciada.</span><span class="sxs-lookup"><span data-stu-id="32e7b-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e7b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e7b-130">CommonParameters</span></span>
<span data-ttu-id="32e7b-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e7b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e7b-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e7b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e7b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32e7b-133">INPUTS</span></span>

### <span data-ttu-id="32e7b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="32e7b-134">System.String</span></span>

### <span data-ttu-id="32e7b-135">System.Int32</span><span class="sxs-lookup"><span data-stu-id="32e7b-135">System.Int32</span></span>

### <span data-ttu-id="32e7b-136">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32e7b-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="32e7b-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32e7b-137">OUTPUTS</span></span>

### <span data-ttu-id="32e7b-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="32e7b-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="32e7b-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="32e7b-139">NOTES</span></span>
* <span data-ttu-id="32e7b-140">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="32e7b-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="32e7b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32e7b-141">RELATED LINKS</span></span>

[<span data-ttu-id="32e7b-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="32e7b-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="32e7b-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="32e7b-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="32e7b-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="32e7b-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


