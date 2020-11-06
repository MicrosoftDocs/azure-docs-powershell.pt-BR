---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: ecd801cff6a6cc67a4187e7f89b26e8b5edb3784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431617"
---
# <span data-ttu-id="33aa6-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="33aa6-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="33aa6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="33aa6-103">Cria um trabalho de tópico de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="33aa6-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33aa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33aa6-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33aa6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="33aa6-106">O cmdlet **New-AzureRmSchedulerServiceBusTopicJob** cria um trabalho de tópico de barramento de serviço no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="33aa6-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="33aa6-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base no parâmetro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="33aa6-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="33aa6-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="33aa6-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="33aa6-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="33aa6-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="33aa6-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="33aa6-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="33aa6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33aa6-111">EXAMPLES</span></span>

## <span data-ttu-id="33aa6-112">OS</span><span class="sxs-lookup"><span data-stu-id="33aa6-112">PARAMETERS</span></span>

### <span data-ttu-id="33aa6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33aa6-113">-DefaultProfile</span></span>
<span data-ttu-id="33aa6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33aa6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="33aa6-115">-EndTime</span></span>
<span data-ttu-id="33aa6-116">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33aa6-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="33aa6-117">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="33aa6-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="33aa6-118">-ErrorActionType</span></span>
<span data-ttu-id="33aa6-119">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33aa6-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="33aa6-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33aa6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33aa6-121">Http</span><span class="sxs-lookup"><span data-stu-id="33aa6-121">Http</span></span> 
- <span data-ttu-id="33aa6-122">Https</span><span class="sxs-lookup"><span data-stu-id="33aa6-122">Https</span></span> 
- <span data-ttu-id="33aa6-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="33aa6-123">StorageQueue</span></span> 
- <span data-ttu-id="33aa6-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="33aa6-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="33aa6-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="33aa6-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="33aa6-126">-ExecutionCount</span></span>
<span data-ttu-id="33aa6-127">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="33aa6-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="33aa6-128">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="33aa6-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-129">-Frequency</span><span class="sxs-lookup"><span data-stu-id="33aa6-129">-Frequency</span></span>
<span data-ttu-id="33aa6-130">Especifica uma frequência máxima para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33aa6-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="33aa6-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33aa6-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33aa6-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="33aa6-132">Minute</span></span> 
- <span data-ttu-id="33aa6-133">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="33aa6-133">Hour</span></span> 
- <span data-ttu-id="33aa6-134">Contas</span><span class="sxs-lookup"><span data-stu-id="33aa6-134">Day</span></span> 
- <span data-ttu-id="33aa6-135">Emana</span><span class="sxs-lookup"><span data-stu-id="33aa6-135">Week</span></span> 
- <span data-ttu-id="33aa6-136">Mensais</span><span class="sxs-lookup"><span data-stu-id="33aa6-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-137">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="33aa6-137">-Interval</span></span>
<span data-ttu-id="33aa6-138">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33aa6-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="33aa6-139">-JobCollectionName</span></span>
<span data-ttu-id="33aa6-140">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="33aa6-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="33aa6-141">-JobName</span></span>
<span data-ttu-id="33aa6-142">Especifica um nome para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33aa6-142">Specifies a name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="33aa6-143">-JobState</span></span>
<span data-ttu-id="33aa6-144">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="33aa6-144">Specifies the state of the job.</span></span>
<span data-ttu-id="33aa6-145">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33aa6-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33aa6-146">Possibilita</span><span class="sxs-lookup"><span data-stu-id="33aa6-146">Enabled</span></span> 
- <span data-ttu-id="33aa6-147">Ativo</span><span class="sxs-lookup"><span data-stu-id="33aa6-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33aa6-148">-ResourceGroupName</span></span>
<span data-ttu-id="33aa6-149">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="33aa6-149">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="33aa6-150">-ServiceBusMessage</span></span>
<span data-ttu-id="33aa6-151">Especifica uma mensagem de tópico de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="33aa6-151">Specifies a service bus topic message.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="33aa6-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="33aa6-153">Especifica um namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="33aa6-153">Specifies a service bus namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="33aa6-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="33aa6-155">Especifica um nome de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="33aa6-155">Specifies a shared access signature key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="33aa6-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="33aa6-157">Especifica um valor de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="33aa6-157">Specifies a shared access signature key value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="33aa6-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="33aa6-159">Especifica um caminho de tópico de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="33aa6-159">Specifies a service bus topic path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="33aa6-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="33aa6-161">Especifica um tipo de transporte de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="33aa6-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="33aa6-162">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33aa6-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33aa6-163">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="33aa6-163">NetMessaging</span></span>
- <span data-ttu-id="33aa6-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="33aa6-164">AMQP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="33aa6-165">-StartTime</span></span>
<span data-ttu-id="33aa6-166">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33aa6-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33aa6-167">-Confirm</span></span>
<span data-ttu-id="33aa6-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33aa6-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33aa6-169">-WhatIf</span></span>
<span data-ttu-id="33aa6-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33aa6-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33aa6-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33aa6-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33aa6-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33aa6-172">CommonParameters</span></span>
<span data-ttu-id="33aa6-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33aa6-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33aa6-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33aa6-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33aa6-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33aa6-175">INPUTS</span></span>

### <span data-ttu-id="33aa6-176">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="33aa6-176">None</span></span>
<span data-ttu-id="33aa6-177">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="33aa6-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33aa6-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33aa6-178">OUTPUTS</span></span>

### <span data-ttu-id="33aa6-179">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="33aa6-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="33aa6-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33aa6-180">NOTES</span></span>

## <span data-ttu-id="33aa6-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33aa6-181">RELATED LINKS</span></span>

[<span data-ttu-id="33aa6-182">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="33aa6-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="33aa6-183">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="33aa6-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="33aa6-184">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="33aa6-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="33aa6-185">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="33aa6-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="33aa6-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="33aa6-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="33aa6-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="33aa6-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="33aa6-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="33aa6-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="33aa6-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="33aa6-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="33aa6-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="33aa6-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


