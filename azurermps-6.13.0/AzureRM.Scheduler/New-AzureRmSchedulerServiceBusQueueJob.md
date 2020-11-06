---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 0382362c16ba65aa194029677cf8ca846e93db54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427172"
---
# <span data-ttu-id="ad4ed-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ad4ed-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="ad4ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad4ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4ed-103">Cria um trabalho na fila do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad4ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad4ed-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad4ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad4ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4ed-106">O cmdlet **New-AzureRmSchedulerServiceBusQueueJob** cria um trabalho da fila de barramento do serviço no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>
<span data-ttu-id="ad4ed-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base no parâmetro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="ad4ed-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="ad4ed-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="ad4ed-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad4ed-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ad4ed-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad4ed-111">EXAMPLES</span></span>

## <span data-ttu-id="ad4ed-112">OS</span><span class="sxs-lookup"><span data-stu-id="ad4ed-112">PARAMETERS</span></span>

### <span data-ttu-id="ad4ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4ed-113">-DefaultProfile</span></span>
<span data-ttu-id="ad4ed-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad4ed-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ad4ed-115">-EndTime</span></span>
<span data-ttu-id="ad4ed-116">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="ad4ed-117">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="ad4ed-118">-ErrorActionType</span></span>
<span data-ttu-id="ad4ed-119">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="ad4ed-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ad4ed-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad4ed-121">Http</span><span class="sxs-lookup"><span data-stu-id="ad4ed-121">Http</span></span> 
- <span data-ttu-id="ad4ed-122">Https</span><span class="sxs-lookup"><span data-stu-id="ad4ed-122">Https</span></span> 
- <span data-ttu-id="ad4ed-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="ad4ed-123">StorageQueue</span></span> 
- <span data-ttu-id="ad4ed-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ad4ed-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="ad4ed-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ad4ed-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="ad4ed-126">-ExecutionCount</span></span>
<span data-ttu-id="ad4ed-127">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="ad4ed-128">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-129">-Frequency</span><span class="sxs-lookup"><span data-stu-id="ad4ed-129">-Frequency</span></span>
<span data-ttu-id="ad4ed-130">Especifica uma frequência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="ad4ed-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ad4ed-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad4ed-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="ad4ed-132">Minute</span></span> 
- <span data-ttu-id="ad4ed-133">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="ad4ed-133">Hour</span></span> 
- <span data-ttu-id="ad4ed-134">Contas</span><span class="sxs-lookup"><span data-stu-id="ad4ed-134">Day</span></span> 
- <span data-ttu-id="ad4ed-135">Emana</span><span class="sxs-lookup"><span data-stu-id="ad4ed-135">Week</span></span> 
- <span data-ttu-id="ad4ed-136">Mensais</span><span class="sxs-lookup"><span data-stu-id="ad4ed-136">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-137">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad4ed-137">-Interval</span></span>
<span data-ttu-id="ad4ed-138">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ad4ed-139">-JobCollectionName</span></span>
<span data-ttu-id="ad4ed-140">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="ad4ed-141">-JobName</span></span>
<span data-ttu-id="ad4ed-142">Especifica um nome para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="ad4ed-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="ad4ed-143">-JobState</span></span>
<span data-ttu-id="ad4ed-144">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-144">Specifies the state of the job.</span></span>
<span data-ttu-id="ad4ed-145">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ad4ed-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad4ed-146">Possibilita</span><span class="sxs-lookup"><span data-stu-id="ad4ed-146">Enabled</span></span> 
- <span data-ttu-id="ad4ed-147">Ativo</span><span class="sxs-lookup"><span data-stu-id="ad4ed-147">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4ed-148">-ResourceGroupName</span></span>
<span data-ttu-id="ad4ed-149">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="ad4ed-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="ad4ed-150">-ServiceBusMessage</span></span>
<span data-ttu-id="ad4ed-151">Especifica uma mensagem na fila do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-151">Specifies a service bus queue message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ad4ed-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="ad4ed-153">Especifica um namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-153">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="ad4ed-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="ad4ed-155">Especifica o nome da fila do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-155">Specifies a service bus queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="ad4ed-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="ad4ed-157">Especifica um nome de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-157">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="ad4ed-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="ad4ed-159">Especifica um valor de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-159">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="ad4ed-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="ad4ed-161">Especifica um tipo de transporte de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="ad4ed-162">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ad4ed-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad4ed-163">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="ad4ed-163">NetMessaging</span></span> 
- <span data-ttu-id="ad4ed-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="ad4ed-164">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ad4ed-165">-StartTime</span></span>
<span data-ttu-id="ad4ed-166">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ad4ed-167">-Confirm</span></span>
<span data-ttu-id="ad4ed-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4ed-169">-WhatIf</span></span>
<span data-ttu-id="ad4ed-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad4ed-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-171">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ed-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4ed-172">CommonParameters</span></span>
<span data-ttu-id="ad4ed-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4ed-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4ed-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4ed-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4ed-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad4ed-175">INPUTS</span></span>

### <span data-ttu-id="ad4ed-176">System. String</span><span class="sxs-lookup"><span data-stu-id="ad4ed-176">System.String</span></span>

## <span data-ttu-id="ad4ed-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad4ed-177">OUTPUTS</span></span>

### <span data-ttu-id="ad4ed-178">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ad4ed-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ad4ed-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad4ed-179">NOTES</span></span>

## <span data-ttu-id="ad4ed-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad4ed-180">RELATED LINKS</span></span>

[<span data-ttu-id="ad4ed-181">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ad4ed-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ad4ed-182">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ad4ed-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ad4ed-183">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ad4ed-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ad4ed-184">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ad4ed-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ad4ed-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ad4ed-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ad4ed-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ad4ed-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ad4ed-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ad4ed-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ad4ed-188">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ad4ed-188">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ad4ed-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ad4ed-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


