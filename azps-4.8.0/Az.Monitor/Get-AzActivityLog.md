---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955480"
---
# <span data-ttu-id="4b2e9-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="4b2e9-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="4b2e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2e9-103">Recuperar eventos do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="4b2e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b2e9-104">SYNTAX</span></span>

### <span data-ttu-id="4b2e9-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="4b2e9-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b2e9-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b2e9-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b2e9-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4b2e9-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b2e9-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4b2e9-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b2e9-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="4b2e9-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b2e9-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b2e9-110">DESCRIPTION</span></span>
<span data-ttu-id="4b2e9-111">O cmdlet Get-AzActivityLog recupera eventos do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="4b2e9-112">Os eventos podem ser associados à ID da assinatura atual, ID de correlação, grupo de recursos, ID do recurso ou provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="4b2e9-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b2e9-113">EXAMPLES</span></span>

### <span data-ttu-id="4b2e9-114">Exemplo 1: obter um log de eventos por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="4b2e9-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="4b2e9-115">Este comando lista os eventos mais recentes do 1000 associados à ID de assinatura do usuário que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-116">Exemplo 2: obter um log de eventos por ID de assinatura com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="4b2e9-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="4b2e9-117">Este comando lista os eventos mais recentes do 100 associados à ID de assinatura do usuário que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-118">Exemplo 3: obter um log de eventos por ID de assinatura com uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="4b2e9-119">Este comando lista os eventos mais recentes do 1000 associados à ID de assinatura do usuário que ocorreu em ou após 2017-06-01T10:30 Hora local se essa data/hora não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-120">Exemplo 4: obter um log de eventos por ID de assinatura com hora de início e hora de término.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="4b2e9-121">Este comando listará, no máximo, 1000 dos eventos associados à ID de assinatura do usuário que ocorreu em ou após 2017-04-01T10:30 Hora local e antes de 2017-04-14T11:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="4b2e9-122">Exemplo 5: obter um log de eventos por ID de correlação</span><span class="sxs-lookup"><span data-stu-id="4b2e9-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="4b2e9-123">Este comando lista os eventos mais recentes do 1000 associados à ID de correlação especificada que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="4b2e9-124">**Observação** : geralmente, esse é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="4b2e9-125">Exemplo 6: obter um log de eventos por ID de correlação com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="4b2e9-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="4b2e9-126">Este comando lista os eventos mais recentes do 100 associados à ID de correlação especificada que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="4b2e9-127">**Observação** : geralmente, esse é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="4b2e9-128">Exemplo 7: obter um log de eventos por ID de correlação e hora de início</span><span class="sxs-lookup"><span data-stu-id="4b2e9-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="4b2e9-129">Este comando lista os eventos da maioria 1000 associados à ID de correlação especificada que ocorreram em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="4b2e9-130">**Observação** : geralmente, esse é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="4b2e9-131">Exemplo 8: obter um log de eventos por ID de correlação com hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="4b2e9-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="4b2e9-132">Este comando lista os eventos mais recentes do 1000 associados à ID de correlação especificada que ocorreram em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="4b2e9-133">Exemplo 9: obter um log de eventos para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b2e9-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="4b2e9-134">Este comando lista no máximo 1000 os eventos associados ao grupo de recursos especificado que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-135">Exemplo 10: obter um log de eventos para um grupo de recursos com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="4b2e9-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="4b2e9-136">Este comando lista os eventos de no máximo 100 associados ao grupo de recursos especificado que levou 7 dias da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-137">Exemplo 11: obter um log de eventos para um grupo de recursos por hora de início</span><span class="sxs-lookup"><span data-stu-id="4b2e9-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="4b2e9-138">Este comando lista os eventos mais recentes do 1000 associados ao grupo de recursos especificado que ocorrerá em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-139">Exemplo 12: obter um log de eventos para um grupo de recursos com hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="4b2e9-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="4b2e9-140">Este comando lista os eventos de no máximo 1000 associados ao grupo de recursos especificado que ocorreu em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja: o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="4b2e9-141">Exemplo 13: obter um log de eventos por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="4b2e9-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="4b2e9-142">Este comando lista os eventos mais recentes do 1000 associados à ID do recurso especificado que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-143">Exemplo 14: obter um log de eventos por ID do recurso com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="4b2e9-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="4b2e9-144">Este comando lista os eventos mais recentes do 100 associados à ID do recurso especificado que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-145">Exemplo 15: obter um log de eventos por ID do recurso com uma hora de início</span><span class="sxs-lookup"><span data-stu-id="4b2e9-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="4b2e9-146">Este comando lista os eventos da maioria 1000 associados à ID do recurso especificada que ocorreram em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-147">Exemplo 16: obter um log de eventos por ID do recurso com hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="4b2e9-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="4b2e9-148">Este comando lista os eventos de no máximo 1000 associados à ID de recurso especificada que ocorreu em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="4b2e9-149">Exemplo 17: obter um log de eventos por provedor de recursos</span><span class="sxs-lookup"><span data-stu-id="4b2e9-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="4b2e9-150">Este comando lista os eventos mais recentes do 1000 associados ao provedor de recursos especificado que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-151">Exemplo 18: obter um log de eventos do provedor de recursos com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="4b2e9-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="4b2e9-152">Este comando lista os eventos mais recentes do 100 associados ao provedor de recursos especificado que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-153">Exemplo 19: obter um log de eventos do provedor de recursos com uma hora de início</span><span class="sxs-lookup"><span data-stu-id="4b2e9-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="4b2e9-154">Este comando lista os eventos do 1000 associados ao provedor de recursos especificado que ocorreram em ou depois de 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="4b2e9-155">Exemplo 20: obter um log de eventos do provedor de recursos com uma hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="4b2e9-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="4b2e9-156">Este comando lista os eventos mais recentes do 1000 associados ao provedor de recursos especificado que ocorreram em ou após 2017-04-15T04:30 Hora local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="4b2e9-157">OS</span><span class="sxs-lookup"><span data-stu-id="4b2e9-157">PARAMETERS</span></span>

### <span data-ttu-id="4b2e9-158">-Chamador</span><span class="sxs-lookup"><span data-stu-id="4b2e9-158">-Caller</span></span>
<span data-ttu-id="4b2e9-159">O chamador dos eventos a serem buscados</span><span class="sxs-lookup"><span data-stu-id="4b2e9-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="4b2e9-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="4b2e9-160">-CorrelationId</span></span>
<span data-ttu-id="4b2e9-161">A CorrelationId</span><span class="sxs-lookup"><span data-stu-id="4b2e9-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2e9-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b2e9-162">-DefaultProfile</span></span>
<span data-ttu-id="4b2e9-163">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b2e9-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="4b2e9-164">-DetailedOutput</span></span>
<span data-ttu-id="4b2e9-165">Objeto de retorno com todos os detalhes dos eventos (o padrão é retornar apenas alguns atributos, ou seja, nenhum detalhe)</span><span class="sxs-lookup"><span data-stu-id="4b2e9-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2e9-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4b2e9-166">-EndTime</span></span>
<span data-ttu-id="4b2e9-167">A endTime da consulta</span><span class="sxs-lookup"><span data-stu-id="4b2e9-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2e9-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="4b2e9-168">-MaxRecord</span></span>
<span data-ttu-id="4b2e9-169">O número máximo de registros a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="4b2e9-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="4b2e9-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2e9-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b2e9-171">-ResourceGroupName</span></span>
<span data-ttu-id="4b2e9-172">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b2e9-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2e9-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b2e9-173">-ResourceId</span></span>
<span data-ttu-id="4b2e9-174">A ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b2e9-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2e9-175">-Resourceprovider</span><span class="sxs-lookup"><span data-stu-id="4b2e9-175">-ResourceProvider</span></span>
<span data-ttu-id="4b2e9-176">O nome do resourceprovider</span><span class="sxs-lookup"><span data-stu-id="4b2e9-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2e9-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4b2e9-177">-StartTime</span></span>
<span data-ttu-id="4b2e9-178">A CorrelationId da consulta</span><span class="sxs-lookup"><span data-stu-id="4b2e9-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b2e9-179">-Status</span><span class="sxs-lookup"><span data-stu-id="4b2e9-179">-Status</span></span>
<span data-ttu-id="4b2e9-180">O status dos eventos a serem buscados</span><span class="sxs-lookup"><span data-stu-id="4b2e9-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="4b2e9-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2e9-181">CommonParameters</span></span>
<span data-ttu-id="4b2e9-182">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b2e9-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2e9-183">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b2e9-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2e9-184">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b2e9-184">INPUTS</span></span>

### <span data-ttu-id="4b2e9-185">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b2e9-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4b2e9-186">System. String</span><span class="sxs-lookup"><span data-stu-id="4b2e9-186">System.String</span></span>

### <span data-ttu-id="4b2e9-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4b2e9-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4b2e9-188">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4b2e9-188">System.Int32</span></span>

## <span data-ttu-id="4b2e9-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b2e9-189">OUTPUTS</span></span>

### <span data-ttu-id="4b2e9-190">Microsoft. Azure. Commands. insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="4b2e9-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="4b2e9-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b2e9-191">NOTES</span></span>

## <span data-ttu-id="4b2e9-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b2e9-192">RELATED LINKS</span></span>
