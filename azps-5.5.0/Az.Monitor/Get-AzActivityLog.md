---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113566"
---
# <span data-ttu-id="de08c-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="de08c-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="de08c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de08c-102">SYNOPSIS</span></span>
<span data-ttu-id="de08c-103">Recuperar eventos do Log de Atividades.</span><span class="sxs-lookup"><span data-stu-id="de08c-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="de08c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de08c-104">SYNTAX</span></span>

### <span data-ttu-id="de08c-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="de08c-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de08c-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de08c-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de08c-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de08c-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de08c-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="de08c-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de08c-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="de08c-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de08c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="de08c-110">DESCRIPTION</span></span>
<span data-ttu-id="de08c-111">O cmdlet Get-AzActivityLog recupera eventos do Log de Atividades.</span><span class="sxs-lookup"><span data-stu-id="de08c-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="de08c-112">Os eventos podem ser associados à ID de assinatura atual, À ID de correlação, ao grupo de recursos, à ID do recurso ou ao provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="de08c-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="de08c-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de08c-113">EXAMPLES</span></span>

### <span data-ttu-id="de08c-114">Exemplo 1: Obter um log de eventos por ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="de08c-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="de08c-115">Esse comando lista no máximo 1.000 eventos associados à ID de assinatura do usuário que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-116">Exemplo 2: Obter um log de eventos por ID de assinatura com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="de08c-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="de08c-117">Esse comando lista no máximo 100 eventos associados à ID de assinatura do usuário que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-118">Exemplo 3: Obter um log de eventos por ID de assinatura com uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="de08c-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="de08c-119">Esse comando lista no máximo 1.000 eventos associados à ID de assinatura do usuário que ocorreu em ou após 2017-06-01T10:30 hora local se essa data/hora não for mais antiga do que 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-120">Exemplo 4: Obter um log de eventos por ID de assinatura com uma hora de início e hora de término.</span><span class="sxs-lookup"><span data-stu-id="de08c-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="de08c-121">Esse comando lista no máximo 1.000 dos eventos associados à ID de assinatura do usuário que ocorreram no período local de 2017-04-01T10:30 e antes de 2017-04-14T11:30 local se o intervalo de data/hora inteiro não for mais antigo do que 90 dias a partir da data/hora atual, ou seja: o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="de08c-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="de08c-122">Exemplo 5: Obter um log de eventos por ID de correlação</span><span class="sxs-lookup"><span data-stu-id="de08c-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="de08c-123">Esse comando lista no máximo 1.000 eventos associados à ID de correlação especificada que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="de08c-124">**OBSERVAÇÃO:** geralmente é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="de08c-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="de08c-125">Exemplo 6: Obter um log de eventos por ID de correlação com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="de08c-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="de08c-126">Esse comando lista no máximo 100 eventos associados à ID de correlação especificada que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="de08c-127">**OBSERVAÇÃO:** geralmente é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="de08c-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="de08c-128">Exemplo 7: Obter um log de eventos por ID de correlação e hora de início</span><span class="sxs-lookup"><span data-stu-id="de08c-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="de08c-129">Esse comando lista no máximo 1.000 eventos associados à ID de correlação especificada que ocorreu em ou após 2017-05-22T04:30:00 hora local se a hora de início não for mais antiga do que 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="de08c-130">**OBSERVAÇÃO:** geralmente é apenas um evento.</span><span class="sxs-lookup"><span data-stu-id="de08c-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="de08c-131">Exemplo 8: Obter um log de eventos por ID de correlação com hora de início e hora de término</span><span class="sxs-lookup"><span data-stu-id="de08c-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="de08c-132">Esse comando lista no máximo 1000 eventos associados à ID de correlação especificada que ocorreu em ou após 2017-04-15T04:30 hora local, mas antes de 2017-04-25T12:30 hora local se o intervalo de data/hora inteiro não for mais antigo do que 90 dias a partir da data/hora atual, ou seja: o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="de08c-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="de08c-133">Exemplo 9: Obter um log de eventos para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="de08c-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="de08c-134">Esse comando lista no máximo 1.000 os eventos associados ao grupo de recursos especificado que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-135">Exemplo 10: Obter um log de eventos para um grupo de recursos com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="de08c-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="de08c-136">Esse comando lista no máximo 100 eventos associados ao grupo de recursos especificado que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-137">Exemplo 11: Obter um log de eventos para um grupo de recursos por hora de início</span><span class="sxs-lookup"><span data-stu-id="de08c-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="de08c-138">Esse comando lista no máximo 1.000 eventos associados ao grupo de recursos especificado que ocorreu em ou após 2017-05-22T04:30:00 hora local se a hora de início não for mais antiga do que 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-139">Exemplo 12: Obter um log de eventos para um grupo de recursos com uma hora de início e uma hora de término</span><span class="sxs-lookup"><span data-stu-id="de08c-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="de08c-140">Esse comando lista no máximo 1000 eventos associados ao grupo de recursos especificado que ocorreu em ou após 2017-04-15T04:30 hora local, mas antes de 2017-04-25T12:30 hora local se o intervalo de data/hora inteiro não for anterior a 90 dias a partir da data/hora atual, ou seja: o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="de08c-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="de08c-141">Exemplo 13: Obter um log de eventos por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="de08c-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="de08c-142">Esse comando lista no máximo 1.000 eventos associados à ID de recurso especificada que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-143">Exemplo 14: Obter um log de eventos por ID do recurso com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="de08c-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="de08c-144">Esse comando lista no máximo 100 eventos associados à ID de recurso especificada que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-145">Exemplo 15: Obter um log de eventos por ID do recurso com uma hora de início</span><span class="sxs-lookup"><span data-stu-id="de08c-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="de08c-146">Esse comando lista no máximo 1000 eventos associados à ID de recurso especificada que ocorreu em ou após 2017-05-22T04:30:00 hora local se a hora de início não for mais antiga do que 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-147">Exemplo 16: Obter um log de eventos por ID do recurso com uma hora de início e uma hora de término</span><span class="sxs-lookup"><span data-stu-id="de08c-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="de08c-148">Esse comando lista no máximo 1000 eventos associados à ID de recurso especificada que ocorreu em ou após 2017-04-15T04:30 hora local, mas antes de 2017-04-25T12:30 hora local se o intervalo de data/hora inteiro não for mais antigo do que 90 dias a partir da data/hora atual, ou seja: o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="de08c-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="de08c-149">Exemplo 17: Obter um log de eventos por provedor de recursos</span><span class="sxs-lookup"><span data-stu-id="de08c-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="de08c-150">Esse comando lista no máximo 1.000 eventos associados ao provedor de recursos especificado que ocorreram 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-151">Exemplo 18: Obter um log de eventos por provedor de recursos com um número máximo de eventos</span><span class="sxs-lookup"><span data-stu-id="de08c-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="de08c-152">Esse comando lista no máximo 100 eventos associados ao provedor de recursos especificado que ocorreu 7 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-153">Exemplo 19: Obter um log de eventos por provedor de recursos com uma hora de início</span><span class="sxs-lookup"><span data-stu-id="de08c-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="de08c-154">Esse comando lista no máximo 1.000 eventos associados ao provedor de recursos especificado que ocorreu em ou após 2017-05-22T04:30:00 hora local se a hora de início não for mais antiga do que 90 dias a partir da data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="de08c-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="de08c-155">Exemplo 20: Obter um log de eventos por provedor de recursos com uma hora de início e uma hora de término</span><span class="sxs-lookup"><span data-stu-id="de08c-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="de08c-156">Esse comando lista no máximo 1.000 eventos associados ao provedor de recursos especificado que ocorreu em ou após 2017-04-15T04:30 hora local, mas antes de 2017-04-25T12:30 hora local se o intervalo de data/hora inteiro não for mais antigo do que 90 dias a partir da data/hora atual, ou seja: o período de retenção.</span><span class="sxs-lookup"><span data-stu-id="de08c-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="de08c-157">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de08c-157">PARAMETERS</span></span>

### <span data-ttu-id="de08c-158">-Chamador</span><span class="sxs-lookup"><span data-stu-id="de08c-158">-Caller</span></span>
<span data-ttu-id="de08c-159">O chamador dos eventos a buscar</span><span class="sxs-lookup"><span data-stu-id="de08c-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="de08c-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="de08c-160">-CorrelationId</span></span>
<span data-ttu-id="de08c-161">A CorrelationId</span><span class="sxs-lookup"><span data-stu-id="de08c-161">The CorrelationId</span></span>

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

### <span data-ttu-id="de08c-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de08c-162">-DefaultProfile</span></span>
<span data-ttu-id="de08c-163">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de08c-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de08c-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="de08c-164">-DetailedOutput</span></span>
<span data-ttu-id="de08c-165">Retornar objeto com todos os detalhes dos eventos (o padrão é retornar apenas alguns atributos, ou seja, nenhum detalhe)</span><span class="sxs-lookup"><span data-stu-id="de08c-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="de08c-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="de08c-166">-EndTime</span></span>
<span data-ttu-id="de08c-167">O tempo de término da consulta</span><span class="sxs-lookup"><span data-stu-id="de08c-167">The endTime of the query</span></span>

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

### <span data-ttu-id="de08c-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="de08c-168">-MaxRecord</span></span>
<span data-ttu-id="de08c-169">O número máximo de registros a buscar.</span><span class="sxs-lookup"><span data-stu-id="de08c-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="de08c-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="de08c-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="de08c-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de08c-171">-ResourceGroupName</span></span>
<span data-ttu-id="de08c-172">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="de08c-172">The resource group name</span></span>

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

### <span data-ttu-id="de08c-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de08c-173">-ResourceId</span></span>
<span data-ttu-id="de08c-174">A ResourceId</span><span class="sxs-lookup"><span data-stu-id="de08c-174">The ResourceId</span></span>

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

### <span data-ttu-id="de08c-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="de08c-175">-ResourceProvider</span></span>
<span data-ttu-id="de08c-176">O nome do ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="de08c-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="de08c-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="de08c-177">-StartTime</span></span>
<span data-ttu-id="de08c-178">A ID de correlação da consulta</span><span class="sxs-lookup"><span data-stu-id="de08c-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="de08c-179">-Status</span><span class="sxs-lookup"><span data-stu-id="de08c-179">-Status</span></span>
<span data-ttu-id="de08c-180">O status dos eventos a buscar</span><span class="sxs-lookup"><span data-stu-id="de08c-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="de08c-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de08c-181">CommonParameters</span></span>
<span data-ttu-id="de08c-182">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de08c-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de08c-183">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de08c-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de08c-184">Entradas</span><span class="sxs-lookup"><span data-stu-id="de08c-184">INPUTS</span></span>

### <span data-ttu-id="de08c-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="de08c-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="de08c-186">System.String</span><span class="sxs-lookup"><span data-stu-id="de08c-186">System.String</span></span>

### <span data-ttu-id="de08c-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="de08c-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="de08c-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="de08c-188">System.Int32</span></span>

## <span data-ttu-id="de08c-189">Saídas</span><span class="sxs-lookup"><span data-stu-id="de08c-189">OUTPUTS</span></span>

### <span data-ttu-id="de08c-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="de08c-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="de08c-191">Notas</span><span class="sxs-lookup"><span data-stu-id="de08c-191">NOTES</span></span>

## <span data-ttu-id="de08c-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de08c-192">RELATED LINKS</span></span>
