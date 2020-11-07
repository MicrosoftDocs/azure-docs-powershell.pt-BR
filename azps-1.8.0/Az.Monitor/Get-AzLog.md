---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: 6a217be0122a94aec7b247fbc7e8835155805ffe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770322"
---
# <span data-ttu-id="8c7db-101">Get-AzLog</span><span class="sxs-lookup"><span data-stu-id="8c7db-101">Get-AzLog</span></span>

## <span data-ttu-id="8c7db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c7db-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7db-103">Obtém um log de eventos.</span><span class="sxs-lookup"><span data-stu-id="8c7db-103">Gets a log of events.</span></span>

## <span data-ttu-id="8c7db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c7db-104">SYNTAX</span></span>

### <span data-ttu-id="8c7db-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="8c7db-105">GetByCorrelationId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c7db-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c7db-106">GetByResourceId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c7db-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c7db-107">GetByResourceGroup</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c7db-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="8c7db-108">GetByResourceProvider</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c7db-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="8c7db-109">GetBySubscription</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7db-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c7db-110">DESCRIPTION</span></span>
<span data-ttu-id="8c7db-111">O cmdlet **Get-AzLog** Obtém um log de eventos.</span><span class="sxs-lookup"><span data-stu-id="8c7db-111">The **Get-AzLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="8c7db-112">Os eventos podem ser associados à ID da assinatura atual, ID de correlação, grupo de recursos, ID do recurso ou provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c7db-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="8c7db-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c7db-113">EXAMPLES</span></span>

### <span data-ttu-id="8c7db-114">Exemplo 1: obter um log de eventos por ID de assinatura</span><span class="sxs-lookup"><span data-stu-id="8c7db-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzLog
```

<span data-ttu-id="8c7db-115">Este comando lista os eventos mais recentes do 1000 associados à ID de assinatura do usuário que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-116">Exemplo 2: obter um log de eventos por ID de assinatura com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="8c7db-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -MaxEvents 100
```

<span data-ttu-id="8c7db-117">Este comando lista os eventos mais recentes do 100 associados à ID de assinatura do usuário que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-118">Exemplo 3: obter um log de eventos por ID de assinatura com uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="8c7db-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="8c7db-119">Este comando lista os eventos mais recentes do 1000 associados à ID de assinatura do usuário que ocorreu em ou após 2017-06-01T10:30 Hora local se essa data/hora não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-120">Exemplo 4: obter um log de eventos por ID de assinatura com hora de início e hora de término.</span><span class="sxs-lookup"><span data-stu-id="8c7db-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="8c7db-121">Este comando listará, no máximo, 1000 dos eventos associados à ID de assinatura do usuário que ocorreu em ou após 2017-04-01T10:30 Hora local e antes de 2017-04-14T11:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="8c7db-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="8c7db-122">Exemplo 5: obter um log de eventos por ID de correlação</span><span class="sxs-lookup"><span data-stu-id="8c7db-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="8c7db-123">Este comando lista os eventos mais recentes do 1000 associados à ID de correlação especificada que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="8c7db-124">**Observação** : geralmente, esse é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="8c7db-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="8c7db-125">Exemplo 6: obter um log de eventos por ID de correlação com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="8c7db-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

<span data-ttu-id="8c7db-126">Este comando lista os eventos mais recentes do 100 associados à ID de correlação especificada que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="8c7db-127">**Observação** : geralmente, esse é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="8c7db-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="8c7db-128">Exemplo 7: obter um log de eventos por ID de correlação e hora de início</span><span class="sxs-lookup"><span data-stu-id="8c7db-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="8c7db-129">Este comando lista os eventos da maioria 1000 associados à ID de correlação especificada que ocorreram em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="8c7db-130">**Observação** : geralmente, esse é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="8c7db-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="8c7db-131">Exemplo 8: obter um log de eventos por ID de correlação com hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="8c7db-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="8c7db-132">Este comando lista os eventos mais recentes do 1000 associados à ID de correlação especificada que ocorreram em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="8c7db-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="8c7db-133">Exemplo 9: obter um log de eventos para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8c7db-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="8c7db-134">Este comando lista no máximo 1000 os eventos associados ao grupo de recursos especificado que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-135">Exemplo 10: obter um log de eventos para um grupo de recursos com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="8c7db-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

<span data-ttu-id="8c7db-136">Este comando lista os eventos de no máximo 100 associados ao grupo de recursos especificado que levou 7 dias da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-137">Exemplo 11: obter um log de eventos para um grupo de recursos por hora de início</span><span class="sxs-lookup"><span data-stu-id="8c7db-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="8c7db-138">Este comando lista no máximo 1000 Evetns associados ao grupo de recursos especificado que ocorreria em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-138">This command lists at most 1000 evetns associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-139">Exemplo 12: obter um log de eventos para um grupo de recursos com hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="8c7db-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="8c7db-140">Este comando lista os eventos de no máximo 1000 associados ao grupo de recursos especificado que ocorreu em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja: o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="8c7db-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="8c7db-141">Exemplo 13: obter um log de eventos por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="8c7db-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="8c7db-142">Este comando lista os eventos mais recentes do 1000 associados à ID do recurso especificado que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-143">Exemplo 14: obter um log de eventos por ID do recurso com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="8c7db-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

<span data-ttu-id="8c7db-144">Este comando lista os eventos mais recentes do 100 associados à ID do recurso especificado que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-145">Exemplo 15: obter um log de eventos por ID do recurso com uma hora de início</span><span class="sxs-lookup"><span data-stu-id="8c7db-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="8c7db-146">Este comando lista os eventos da maioria 1000 associados à ID do recurso especificada que ocorreram em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-147">Exemplo 16: obter um log de eventos por ID do recurso com hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="8c7db-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="8c7db-148">Este comando lista os eventos de no máximo 1000 associados à ID de recurso especificada que ocorreu em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="8c7db-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="8c7db-149">Exemplo 17: obter um log de eventos por provedor de recursos</span><span class="sxs-lookup"><span data-stu-id="8c7db-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="8c7db-150">Este comando lista os eventos mais recentes do 1000 associados ao provedor de recursos especificado que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-151">Exemplo 18: obter um log de eventos do provedor de recursos com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="8c7db-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

<span data-ttu-id="8c7db-152">Este comando lista os eventos mais recentes do 100 associados ao provedor de recursos especificado que levaram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-153">Exemplo 19: obter um log de eventos do provedor de recursos com uma hora de início</span><span class="sxs-lookup"><span data-stu-id="8c7db-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="8c7db-154">Este comando lista os eventos do 1000 associados ao provedor de recursos especificado que ocorreram em ou depois de 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="8c7db-155">Exemplo 20: obter um log de eventos do provedor de recursos com uma hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="8c7db-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="8c7db-156">Este comando lista os eventos mais recentes do 1000 associados ao provedor de recursos especificado que ocorreram em ou após 2017-04-15T04:30 Hora local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="8c7db-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="8c7db-157">OS</span><span class="sxs-lookup"><span data-stu-id="8c7db-157">PARAMETERS</span></span>

### <span data-ttu-id="8c7db-158">-Chamador</span><span class="sxs-lookup"><span data-stu-id="8c7db-158">-Caller</span></span>
<span data-ttu-id="8c7db-159">Especifica um chamador.</span><span class="sxs-lookup"><span data-stu-id="8c7db-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="8c7db-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="8c7db-160">-CorrelationId</span></span>
<span data-ttu-id="8c7db-161">Especifica a ID de correlação.</span><span class="sxs-lookup"><span data-stu-id="8c7db-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="8c7db-162">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8c7db-162">This parameter is required.</span></span>

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

### <span data-ttu-id="8c7db-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7db-163">-DefaultProfile</span></span>
<span data-ttu-id="8c7db-164">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8c7db-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c7db-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="8c7db-165">-DetailedOutput</span></span>
<span data-ttu-id="8c7db-166">Indica que esse cmdlet exibe a saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="8c7db-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="8c7db-167">Por padrão, a saída é resumida.</span><span class="sxs-lookup"><span data-stu-id="8c7db-167">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7db-168">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8c7db-168">-EndTime</span></span>
<span data-ttu-id="8c7db-169">Especifica a hora de término da consulta na hora local.</span><span class="sxs-lookup"><span data-stu-id="8c7db-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="8c7db-170">O valor padrão é a hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c7db-170">The default value is the current time.</span></span>
<span data-ttu-id="8c7db-171">O valor deve ser posterior a *StartTime*.</span><span class="sxs-lookup"><span data-stu-id="8c7db-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="8c7db-172">Você pode usar o cmdlet Get-Date para obter um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="8c7db-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7db-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="8c7db-173">-MaxRecord</span></span>
<span data-ttu-id="8c7db-174">Especifica o número total de registros a serem recuperados para o filtro especificado.</span><span class="sxs-lookup"><span data-stu-id="8c7db-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="8c7db-175">O valor padrão é 1000 e o valor máximo aceito é 100000.</span><span class="sxs-lookup"><span data-stu-id="8c7db-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="8c7db-176">Os valores negativos e 0 são ignorados e o valor padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="8c7db-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7db-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7db-177">-ResourceGroupName</span></span>
<span data-ttu-id="8c7db-178">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c7db-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8c7db-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c7db-179">-ResourceId</span></span>
<span data-ttu-id="8c7db-180">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8c7db-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="8c7db-181">-Resourceprovider</span><span class="sxs-lookup"><span data-stu-id="8c7db-181">-ResourceProvider</span></span>
<span data-ttu-id="8c7db-182">Especifica um provedor de recurso filtrar por.</span><span class="sxs-lookup"><span data-stu-id="8c7db-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="8c7db-183">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8c7db-183">-StartTime</span></span>
<span data-ttu-id="8c7db-184">Especifica a hora de início da consulta na hora local.</span><span class="sxs-lookup"><span data-stu-id="8c7db-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="8c7db-185">O valor padrão é *EndTime* menos sete dias.</span><span class="sxs-lookup"><span data-stu-id="8c7db-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="8c7db-186">Você pode usar o cmdlet Get-Date para obter um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="8c7db-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7db-187">-Status</span><span class="sxs-lookup"><span data-stu-id="8c7db-187">-Status</span></span>
<span data-ttu-id="8c7db-188">Especifica o status.</span><span class="sxs-lookup"><span data-stu-id="8c7db-188">Specifies the status.</span></span>

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

### <span data-ttu-id="8c7db-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7db-189">CommonParameters</span></span>
<span data-ttu-id="8c7db-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7db-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7db-191">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7db-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7db-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c7db-192">INPUTS</span></span>

### <span data-ttu-id="8c7db-193">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8c7db-193">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8c7db-194">System. String</span><span class="sxs-lookup"><span data-stu-id="8c7db-194">System.String</span></span>

### <span data-ttu-id="8c7db-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c7db-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8c7db-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8c7db-196">System.Int32</span></span>

## <span data-ttu-id="8c7db-197">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c7db-197">OUTPUTS</span></span>

### <span data-ttu-id="8c7db-198">Microsoft. Azure. Commands. insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="8c7db-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="8c7db-199">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c7db-199">NOTES</span></span>

## <span data-ttu-id="8c7db-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c7db-200">RELATED LINKS</span></span>
