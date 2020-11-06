---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: a12cf84d90ecbcc948ac13745b38438766582aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440560"
---
# <span data-ttu-id="ae014-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ae014-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="ae014-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae014-102">SYNOPSIS</span></span>
<span data-ttu-id="ae014-103">Modifica um trabalho de tópico de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="ae014-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae014-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae014-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae014-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae014-105">DESCRIPTION</span></span>
<span data-ttu-id="ae014-106">O cmdlet **set-AzureRmSchedulerServiceBusTopicJob** modifica um trabalho de tópico de barramento de serviço no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae014-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="ae014-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base no parâmetro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="ae014-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="ae014-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ae014-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="ae014-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ae014-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ae014-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="ae014-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ae014-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae014-111">EXAMPLES</span></span>

## <span data-ttu-id="ae014-112">OS</span><span class="sxs-lookup"><span data-stu-id="ae014-112">PARAMETERS</span></span>

### <span data-ttu-id="ae014-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ae014-113">-EndTime</span></span>
<span data-ttu-id="ae014-114">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ae014-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="ae014-115">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ae014-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ae014-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="ae014-116">-ErrorActionType</span></span>
<span data-ttu-id="ae014-117">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ae014-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="ae014-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ae014-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae014-119">Http</span><span class="sxs-lookup"><span data-stu-id="ae014-119">Http</span></span> 
- <span data-ttu-id="ae014-120">Https</span><span class="sxs-lookup"><span data-stu-id="ae014-120">Https</span></span> 
- <span data-ttu-id="ae014-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="ae014-121">StorageQueue</span></span> 
- <span data-ttu-id="ae014-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ae014-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="ae014-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ae014-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="ae014-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="ae014-124">-ExecutionCount</span></span>
<span data-ttu-id="ae014-125">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="ae014-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="ae014-126">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="ae014-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="ae014-127">-Frequency</span><span class="sxs-lookup"><span data-stu-id="ae014-127">-Frequency</span></span>
<span data-ttu-id="ae014-128">Especifica uma frequência máxima para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ae014-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="ae014-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ae014-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae014-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="ae014-130">Minute</span></span> 
- <span data-ttu-id="ae014-131">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="ae014-131">Hour</span></span> 
- <span data-ttu-id="ae014-132">Contas</span><span class="sxs-lookup"><span data-stu-id="ae014-132">Day</span></span> 
- <span data-ttu-id="ae014-133">Emana</span><span class="sxs-lookup"><span data-stu-id="ae014-133">Week</span></span> 
- <span data-ttu-id="ae014-134">Mensais</span><span class="sxs-lookup"><span data-stu-id="ae014-134">Month</span></span>

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

### <span data-ttu-id="ae014-135">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="ae014-135">-Interval</span></span>
<span data-ttu-id="ae014-136">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ae014-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="ae014-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ae014-137">-JobCollectionName</span></span>
<span data-ttu-id="ae014-138">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="ae014-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="ae014-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="ae014-139">-JobName</span></span>
<span data-ttu-id="ae014-140">Especifica o nome do trabalho que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ae014-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ae014-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="ae014-141">-JobState</span></span>
<span data-ttu-id="ae014-142">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ae014-142">Specifies the state of the job.</span></span>
<span data-ttu-id="ae014-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ae014-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae014-144">Possibilita</span><span class="sxs-lookup"><span data-stu-id="ae014-144">Enabled</span></span> 
- <span data-ttu-id="ae014-145">Ativo</span><span class="sxs-lookup"><span data-stu-id="ae014-145">Disabled</span></span>

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

### <span data-ttu-id="ae014-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae014-146">-ResourceGroupName</span></span>
<span data-ttu-id="ae014-147">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="ae014-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="ae014-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="ae014-148">-ServiceBusMessage</span></span>
<span data-ttu-id="ae014-149">Especifica uma mensagem de tópico de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="ae014-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="ae014-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ae014-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="ae014-151">Especifica um namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="ae014-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="ae014-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="ae014-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="ae014-153">Especifica um nome de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ae014-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="ae014-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="ae014-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="ae014-155">Especifica um valor de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ae014-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="ae014-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="ae014-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="ae014-157">Especifica um caminho de tópico de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="ae014-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="ae014-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="ae014-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="ae014-159">Especifica um tipo de transporte de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="ae014-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="ae014-160">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ae014-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae014-161">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="ae014-161">NetMessaging</span></span>
- <span data-ttu-id="ae014-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="ae014-162">AMQP</span></span>

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

### <span data-ttu-id="ae014-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ae014-163">-StartTime</span></span>
<span data-ttu-id="ae014-164">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ae014-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="ae014-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae014-165">-Confirm</span></span>
<span data-ttu-id="ae014-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae014-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae014-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae014-167">-WhatIf</span></span>
<span data-ttu-id="ae014-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae014-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae014-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae014-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae014-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae014-170">-DefaultProfile</span></span>
<span data-ttu-id="ae014-171">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae014-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae014-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae014-172">CommonParameters</span></span>
<span data-ttu-id="ae014-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae014-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae014-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae014-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae014-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae014-175">INPUTS</span></span>

## <span data-ttu-id="ae014-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae014-176">OUTPUTS</span></span>

### <span data-ttu-id="ae014-177">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ae014-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ae014-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae014-178">NOTES</span></span>

## <span data-ttu-id="ae014-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae014-179">RELATED LINKS</span></span>

[<span data-ttu-id="ae014-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ae014-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ae014-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ae014-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ae014-182">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae014-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ae014-183">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ae014-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ae014-184">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae014-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ae014-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ae014-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ae014-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ae014-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ae014-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae014-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ae014-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae014-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


