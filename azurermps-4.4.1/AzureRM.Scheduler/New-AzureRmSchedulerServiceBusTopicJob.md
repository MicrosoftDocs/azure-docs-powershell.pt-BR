---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 3a4c0cfb2e9ec3b41921e42b793a06163b9a8303
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433010"
---
# <span data-ttu-id="824ee-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="824ee-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="824ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="824ee-102">SYNOPSIS</span></span>
<span data-ttu-id="824ee-103">Cria um trabalho de tópico de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="824ee-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="824ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="824ee-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="824ee-105">DESCRIPTION</span></span>
<span data-ttu-id="824ee-106">O cmdlet **New-AzureRmSchedulerServiceBusTopicJob** cria um trabalho de tópico de barramento de serviço no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="824ee-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="824ee-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base no parâmetro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="824ee-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="824ee-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="824ee-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="824ee-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="824ee-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="824ee-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="824ee-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="824ee-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="824ee-111">EXAMPLES</span></span>

## <span data-ttu-id="824ee-112">OS</span><span class="sxs-lookup"><span data-stu-id="824ee-112">PARAMETERS</span></span>

### <span data-ttu-id="824ee-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="824ee-113">-EndTime</span></span>
<span data-ttu-id="824ee-114">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="824ee-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="824ee-115">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="824ee-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="824ee-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="824ee-116">-ErrorActionType</span></span>
<span data-ttu-id="824ee-117">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="824ee-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="824ee-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="824ee-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="824ee-119">Http</span><span class="sxs-lookup"><span data-stu-id="824ee-119">Http</span></span> 
- <span data-ttu-id="824ee-120">Https</span><span class="sxs-lookup"><span data-stu-id="824ee-120">Https</span></span> 
- <span data-ttu-id="824ee-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="824ee-121">StorageQueue</span></span> 
- <span data-ttu-id="824ee-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="824ee-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="824ee-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="824ee-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="824ee-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="824ee-124">-ExecutionCount</span></span>
<span data-ttu-id="824ee-125">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="824ee-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="824ee-126">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="824ee-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="824ee-127">-Frequency</span><span class="sxs-lookup"><span data-stu-id="824ee-127">-Frequency</span></span>
<span data-ttu-id="824ee-128">Especifica uma frequência máxima para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="824ee-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="824ee-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="824ee-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="824ee-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="824ee-130">Minute</span></span> 
- <span data-ttu-id="824ee-131">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="824ee-131">Hour</span></span> 
- <span data-ttu-id="824ee-132">Contas</span><span class="sxs-lookup"><span data-stu-id="824ee-132">Day</span></span> 
- <span data-ttu-id="824ee-133">Emana</span><span class="sxs-lookup"><span data-stu-id="824ee-133">Week</span></span> 
- <span data-ttu-id="824ee-134">Mensais</span><span class="sxs-lookup"><span data-stu-id="824ee-134">Month</span></span>

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

### <span data-ttu-id="824ee-135">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="824ee-135">-Interval</span></span>
<span data-ttu-id="824ee-136">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="824ee-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="824ee-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="824ee-137">-JobCollectionName</span></span>
<span data-ttu-id="824ee-138">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="824ee-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="824ee-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="824ee-139">-JobName</span></span>
<span data-ttu-id="824ee-140">Especifica um nome para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="824ee-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="824ee-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="824ee-141">-JobState</span></span>
<span data-ttu-id="824ee-142">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="824ee-142">Specifies the state of the job.</span></span>
<span data-ttu-id="824ee-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="824ee-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="824ee-144">Possibilita</span><span class="sxs-lookup"><span data-stu-id="824ee-144">Enabled</span></span> 
- <span data-ttu-id="824ee-145">Ativo</span><span class="sxs-lookup"><span data-stu-id="824ee-145">Disabled</span></span>

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

### <span data-ttu-id="824ee-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="824ee-146">-ResourceGroupName</span></span>
<span data-ttu-id="824ee-147">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="824ee-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="824ee-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="824ee-148">-ServiceBusMessage</span></span>
<span data-ttu-id="824ee-149">Especifica uma mensagem de tópico de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="824ee-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="824ee-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="824ee-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="824ee-151">Especifica um namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="824ee-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="824ee-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="824ee-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="824ee-153">Especifica um nome de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="824ee-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="824ee-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="824ee-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="824ee-155">Especifica um valor de chave de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="824ee-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="824ee-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="824ee-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="824ee-157">Especifica um caminho de tópico de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="824ee-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="824ee-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="824ee-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="824ee-159">Especifica um tipo de transporte de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="824ee-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="824ee-160">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="824ee-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="824ee-161">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="824ee-161">NetMessaging</span></span>
- <span data-ttu-id="824ee-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="824ee-162">AMQP</span></span>

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

### <span data-ttu-id="824ee-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="824ee-163">-StartTime</span></span>
<span data-ttu-id="824ee-164">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="824ee-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="824ee-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="824ee-165">-Confirm</span></span>
<span data-ttu-id="824ee-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824ee-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824ee-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824ee-167">-WhatIf</span></span>
<span data-ttu-id="824ee-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="824ee-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824ee-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="824ee-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824ee-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824ee-170">-DefaultProfile</span></span>
<span data-ttu-id="824ee-171">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="824ee-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="824ee-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824ee-172">CommonParameters</span></span>
<span data-ttu-id="824ee-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824ee-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824ee-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824ee-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824ee-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="824ee-175">INPUTS</span></span>

## <span data-ttu-id="824ee-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="824ee-176">OUTPUTS</span></span>

### <span data-ttu-id="824ee-177">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="824ee-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="824ee-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="824ee-178">NOTES</span></span>

## <span data-ttu-id="824ee-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="824ee-179">RELATED LINKS</span></span>

[<span data-ttu-id="824ee-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="824ee-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="824ee-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="824ee-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="824ee-182">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="824ee-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="824ee-183">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="824ee-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="824ee-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="824ee-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="824ee-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="824ee-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="824ee-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="824ee-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="824ee-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="824ee-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="824ee-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="824ee-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


