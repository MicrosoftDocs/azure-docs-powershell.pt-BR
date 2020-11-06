---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 07bfc520cfabc33ed4f72f1d0d4c46c9104a5253
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427812"
---
# <span data-ttu-id="22313-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="22313-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="22313-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22313-102">SYNOPSIS</span></span>
<span data-ttu-id="22313-103">Cria uma entrada de cronograma.</span><span class="sxs-lookup"><span data-stu-id="22313-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22313-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22313-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22313-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22313-105">DESCRIPTION</span></span>
<span data-ttu-id="22313-106">O cmdlet **New-AzureRmRedisCacheScheduleEntry** cria um objeto **PSScheduleEntry** .</span><span class="sxs-lookup"><span data-stu-id="22313-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="22313-107">Cmdlets de agendamento do patch de cache do Redis do Azure, como o cmdlet New-AzureRmRedisCachePatchSchedule, exigem objetos de entrada de cronograma.</span><span class="sxs-lookup"><span data-stu-id="22313-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="22313-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22313-108">EXAMPLES</span></span>

### <span data-ttu-id="22313-109">Exemplo 1: criar uma entrada de cronograma para finais de semana</span><span class="sxs-lookup"><span data-stu-id="22313-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="22313-110">Esse comando cria um objeto **PSScheduleEntry** que representa um cronograma de final de semana que tem a hora e a hora de início especificadas.</span><span class="sxs-lookup"><span data-stu-id="22313-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="22313-111">OS</span><span class="sxs-lookup"><span data-stu-id="22313-111">PARAMETERS</span></span>

### <span data-ttu-id="22313-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="22313-112">-DayOfWeek</span></span>
<span data-ttu-id="22313-113">Especifica o dia da semana para a entrada de cronograma.</span><span class="sxs-lookup"><span data-stu-id="22313-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="22313-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="22313-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22313-115">Diário</span><span class="sxs-lookup"><span data-stu-id="22313-115">Everyday</span></span> 
- <span data-ttu-id="22313-116">Longa</span><span class="sxs-lookup"><span data-stu-id="22313-116">Weekend</span></span> 
- <span data-ttu-id="22313-117">Sexta</span><span class="sxs-lookup"><span data-stu-id="22313-117">Monday</span></span> 
- <span data-ttu-id="22313-118">-</span><span class="sxs-lookup"><span data-stu-id="22313-118">Tuesday</span></span> 
- <span data-ttu-id="22313-119">Feira</span><span class="sxs-lookup"><span data-stu-id="22313-119">Wednesday</span></span> 
- <span data-ttu-id="22313-120">Terça</span><span class="sxs-lookup"><span data-stu-id="22313-120">Thursday</span></span> 
- <span data-ttu-id="22313-121">Às</span><span class="sxs-lookup"><span data-stu-id="22313-121">Friday</span></span> 
- <span data-ttu-id="22313-122">Sábado</span><span class="sxs-lookup"><span data-stu-id="22313-122">Saturday</span></span> 
- <span data-ttu-id="22313-123">Domingo</span><span class="sxs-lookup"><span data-stu-id="22313-123">Sunday</span></span>

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

### <span data-ttu-id="22313-124">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="22313-124">-MaintenanceWindow</span></span>
<span data-ttu-id="22313-125">Especifica a quantidade de tempo permitida para atualizações.</span><span class="sxs-lookup"><span data-stu-id="22313-125">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="22313-126">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="22313-126">-StartHourUtc</span></span>
<span data-ttu-id="22313-127">Especifica uma hora do dia em que o cronograma começará.</span><span class="sxs-lookup"><span data-stu-id="22313-127">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="22313-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22313-128">-DefaultProfile</span></span>
<span data-ttu-id="22313-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22313-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22313-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22313-130">CommonParameters</span></span>
<span data-ttu-id="22313-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22313-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22313-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22313-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22313-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22313-133">INPUTS</span></span>

### <span data-ttu-id="22313-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="22313-134">None</span></span>
<span data-ttu-id="22313-135">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="22313-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="22313-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22313-136">OUTPUTS</span></span>

### <span data-ttu-id="22313-137">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="22313-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="22313-138">Esse cmdlet retorna um objeto de entrada de cronograma.</span><span class="sxs-lookup"><span data-stu-id="22313-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="22313-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22313-139">NOTES</span></span>
* <span data-ttu-id="22313-140">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="22313-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="22313-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22313-141">RELATED LINKS</span></span>

[<span data-ttu-id="22313-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="22313-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="22313-143">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="22313-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="22313-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="22313-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


