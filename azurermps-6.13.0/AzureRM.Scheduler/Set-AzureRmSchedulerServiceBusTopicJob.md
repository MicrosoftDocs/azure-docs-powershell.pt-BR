---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 6f1e92654c038cccf49e32b489ad5face70ae011
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611022"
---
# <span data-ttu-id="4d3be-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4d3be-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="4d3be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d3be-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3be-103">Modifica um trabalho de tópico de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="4d3be-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d3be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d3be-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d3be-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d3be-105">DESCRIPTION</span></span>
<span data-ttu-id="4d3be-106">O cmdlet **set-AzureRmSchedulerServiceBusTopicJob** modifica um trabalho de tópico de barramento de serviço no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3be-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>
<span data-ttu-id="4d3be-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base no parâmetro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="4d3be-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="4d3be-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4d3be-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="4d3be-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4d3be-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4d3be-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="4d3be-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4d3be-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d3be-111">EXAMPLES</span></span>

## <span data-ttu-id="4d3be-112">OS</span><span class="sxs-lookup"><span data-stu-id="4d3be-112">PARAMETERS</span></span>

### <span data-ttu-id="4d3be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3be-113">-DefaultProfile</span></span>
<span data-ttu-id="4d3be-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d3be-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4d3be-115">-EndTime</span></span>
<span data-ttu-id="4d3be-116">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d3be-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="4d3be-117">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="4d3be-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="4d3be-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="4d3be-118">-ErrorActionType</span></span>
<span data-ttu-id="4d3be-119">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d3be-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="4d3be-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4d3be-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d3be-121">Http</span><span class="sxs-lookup"><span data-stu-id="4d3be-121">Http</span></span> 
- <span data-ttu-id="4d3be-122">Https</span><span class="sxs-lookup"><span data-stu-id="4d3be-122">Https</span></span> 
- <span data-ttu-id="4d3be-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="4d3be-123">StorageQueue</span></span> 
- <span data-ttu-id="4d3be-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="4d3be-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="4d3be-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="4d3be-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="4d3be-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="4d3be-126">-ExecutionCount</span></span>
<span data-ttu-id="4d3be-127">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="4d3be-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="4d3be-128">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="4d3be-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="4d3be-129">-Frequency</span><span class="sxs-lookup"><span data-stu-id="4d3be-129">-Frequency</span></span>
<span data-ttu-id="4d3be-130">Especifica uma frequência máxima para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d3be-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="4d3be-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4d3be-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d3be-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="4d3be-132">Minute</span></span> 
- <span data-ttu-id="4d3be-133">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="4d3be-133">Hour</span></span> 
- <span data-ttu-id="4d3be-134">Contas</span><span class="sxs-lookup"><span data-stu-id="4d3be-134">Day</span></span> 
- <span data-ttu-id="4d3be-135">Emana</span><span class="sxs-lookup"><span data-stu-id="4d3be-135">Week</span></span> 
- <span data-ttu-id="4d3be-136">Mensais</span><span class="sxs-lookup"><span data-stu-id="4d3be-136">Month</span></span>

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

### <span data-ttu-id="4d3be-137">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="4d3be-137">-Interval</span></span>
<span data-ttu-id="4d3be-138">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d3be-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="4d3be-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4d3be-139">-JobCollectionName</span></span>
<span data-ttu-id="4d3be-140">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="4d3be-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="4d3be-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="4d3be-141">-JobName</span></span>
<span data-ttu-id="4d3be-142">Especifica o nome do trabalho que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="4d3be-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4d3be-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="4d3be-143">-JobState</span></span>
<span data-ttu-id="4d3be-144">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d3be-144">Specifies the state of the job.</span></span>
<span data-ttu-id="4d3be-145">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4d3be-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d3be-146">Possibilita</span><span class="sxs-lookup"><span data-stu-id="4d3be-146">Enabled</span></span> 
- <span data-ttu-id="4d3be-147">Ativo</span><span class="sxs-lookup"><span data-stu-id="4d3be-147">Disabled</span></span>

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

### <span data-ttu-id="4d3be-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3be-148">-ResourceGroupName</span></span>
<span data-ttu-id="4d3be-149">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="4d3be-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="4d3be-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="4d3be-150">-ServiceBusMessage</span></span>
<span data-ttu-id="4d3be-151">Especifica uma mensagem de tópico de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="4d3be-151">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="4d3be-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="4d3be-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="4d3be-153">Especifica um namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="4d3be-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="4d3be-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="4d3be-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="4d3be-155">Especifica um nome de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="4d3be-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="4d3be-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="4d3be-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="4d3be-157">Especifica um valor de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="4d3be-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="4d3be-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="4d3be-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="4d3be-159">Especifica um caminho de tópico de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="4d3be-159">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="4d3be-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="4d3be-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="4d3be-161">Especifica um tipo de transporte de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="4d3be-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="4d3be-162">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4d3be-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d3be-163">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="4d3be-163">NetMessaging</span></span>
- <span data-ttu-id="4d3be-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="4d3be-164">AMQP</span></span>

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

### <span data-ttu-id="4d3be-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4d3be-165">-StartTime</span></span>
<span data-ttu-id="4d3be-166">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d3be-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="4d3be-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4d3be-167">-Confirm</span></span>
<span data-ttu-id="4d3be-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d3be-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d3be-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d3be-169">-WhatIf</span></span>
<span data-ttu-id="4d3be-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d3be-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d3be-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d3be-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d3be-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3be-172">CommonParameters</span></span>
<span data-ttu-id="4d3be-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3be-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3be-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d3be-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3be-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d3be-175">INPUTS</span></span>

### <span data-ttu-id="4d3be-176">System. String</span><span class="sxs-lookup"><span data-stu-id="4d3be-176">System.String</span></span>

## <span data-ttu-id="4d3be-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d3be-177">OUTPUTS</span></span>

### <span data-ttu-id="4d3be-178">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4d3be-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="4d3be-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d3be-179">NOTES</span></span>

## <span data-ttu-id="4d3be-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d3be-180">RELATED LINKS</span></span>

[<span data-ttu-id="4d3be-181">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4d3be-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4d3be-182">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4d3be-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4d3be-183">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4d3be-183">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4d3be-184">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4d3be-184">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4d3be-185">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4d3be-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="4d3be-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4d3be-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4d3be-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4d3be-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4d3be-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4d3be-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4d3be-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4d3be-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


