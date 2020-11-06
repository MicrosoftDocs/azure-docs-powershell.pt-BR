---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: d93ceb91ded5161dc962f902434cefe0f2070ae5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602141"
---
# <span data-ttu-id="33b8b-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="33b8b-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="33b8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="33b8b-103">Modifica um trabalho em fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="33b8b-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33b8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33b8b-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33b8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="33b8b-106">O cmdlet **set-AzureRmSchedulerStorageQueueJob** modifica um trabalho de fila de armazenamento no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="33b8b-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="33b8b-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base no parâmetro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="33b8b-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="33b8b-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="33b8b-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="33b8b-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="33b8b-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="33b8b-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="33b8b-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="33b8b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33b8b-111">EXAMPLES</span></span>

## <span data-ttu-id="33b8b-112">OS</span><span class="sxs-lookup"><span data-stu-id="33b8b-112">PARAMETERS</span></span>

### <span data-ttu-id="33b8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b8b-113">-DefaultProfile</span></span>
<span data-ttu-id="33b8b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33b8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33b8b-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="33b8b-115">-EndTime</span></span>
<span data-ttu-id="33b8b-116">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33b8b-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="33b8b-117">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="33b8b-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="33b8b-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="33b8b-118">-ErrorActionType</span></span>
<span data-ttu-id="33b8b-119">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33b8b-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="33b8b-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33b8b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33b8b-121">Http</span><span class="sxs-lookup"><span data-stu-id="33b8b-121">Http</span></span> 
- <span data-ttu-id="33b8b-122">Https</span><span class="sxs-lookup"><span data-stu-id="33b8b-122">Https</span></span> 
- <span data-ttu-id="33b8b-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="33b8b-123">StorageQueue</span></span> 
- <span data-ttu-id="33b8b-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="33b8b-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="33b8b-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="33b8b-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="33b8b-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="33b8b-126">-ExecutionCount</span></span>
<span data-ttu-id="33b8b-127">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="33b8b-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="33b8b-128">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="33b8b-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="33b8b-129">-Frequency</span><span class="sxs-lookup"><span data-stu-id="33b8b-129">-Frequency</span></span>
<span data-ttu-id="33b8b-130">Especifica uma frequência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33b8b-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="33b8b-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33b8b-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33b8b-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="33b8b-132">Minute</span></span> 
- <span data-ttu-id="33b8b-133">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="33b8b-133">Hour</span></span> 
- <span data-ttu-id="33b8b-134">Contas</span><span class="sxs-lookup"><span data-stu-id="33b8b-134">Day</span></span> 
- <span data-ttu-id="33b8b-135">Emana</span><span class="sxs-lookup"><span data-stu-id="33b8b-135">Week</span></span> 
- <span data-ttu-id="33b8b-136">Mensais</span><span class="sxs-lookup"><span data-stu-id="33b8b-136">Month</span></span>

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

### <span data-ttu-id="33b8b-137">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="33b8b-137">-Interval</span></span>
<span data-ttu-id="33b8b-138">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33b8b-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="33b8b-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="33b8b-139">-JobCollectionName</span></span>
<span data-ttu-id="33b8b-140">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="33b8b-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="33b8b-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="33b8b-141">-JobName</span></span>
<span data-ttu-id="33b8b-142">Especifica o nome do trabalho que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="33b8b-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="33b8b-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="33b8b-143">-JobState</span></span>
<span data-ttu-id="33b8b-144">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="33b8b-144">Specifies the state of the job.</span></span>
<span data-ttu-id="33b8b-145">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33b8b-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33b8b-146">Possibilita</span><span class="sxs-lookup"><span data-stu-id="33b8b-146">Enabled</span></span> 
- <span data-ttu-id="33b8b-147">Ativo</span><span class="sxs-lookup"><span data-stu-id="33b8b-147">Disabled</span></span>

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

### <span data-ttu-id="33b8b-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b8b-148">-ResourceGroupName</span></span>
<span data-ttu-id="33b8b-149">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="33b8b-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="33b8b-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="33b8b-150">-StartTime</span></span>
<span data-ttu-id="33b8b-151">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="33b8b-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="33b8b-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="33b8b-152">-StorageQueueAccount</span></span>
<span data-ttu-id="33b8b-153">Especifica um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="33b8b-153">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b8b-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="33b8b-154">-StorageQueueMessage</span></span>
<span data-ttu-id="33b8b-155">Especifica uma mensagem de fila para o trabalho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="33b8b-155">Specifies a queue message for storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b8b-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="33b8b-156">-StorageQueueName</span></span>
<span data-ttu-id="33b8b-157">Especifica o nome da fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="33b8b-157">Specifies a storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b8b-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="33b8b-158">-StorageSASToken</span></span>
<span data-ttu-id="33b8b-159">Especifica um token de assinatura de acesso compartilhado para uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="33b8b-159">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b8b-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33b8b-160">-Confirm</span></span>
<span data-ttu-id="33b8b-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33b8b-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33b8b-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33b8b-162">-WhatIf</span></span>
<span data-ttu-id="33b8b-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33b8b-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33b8b-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33b8b-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33b8b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b8b-165">CommonParameters</span></span>
<span data-ttu-id="33b8b-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b8b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b8b-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b8b-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b8b-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33b8b-168">INPUTS</span></span>

### <span data-ttu-id="33b8b-169">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="33b8b-169">None</span></span>
<span data-ttu-id="33b8b-170">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="33b8b-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33b8b-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33b8b-171">OUTPUTS</span></span>

### <span data-ttu-id="33b8b-172">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="33b8b-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="33b8b-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33b8b-173">NOTES</span></span>

## <span data-ttu-id="33b8b-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33b8b-174">RELATED LINKS</span></span>

[<span data-ttu-id="33b8b-175">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="33b8b-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="33b8b-176">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="33b8b-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="33b8b-177">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="33b8b-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="33b8b-178">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="33b8b-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="33b8b-179">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="33b8b-179">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="33b8b-180">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="33b8b-180">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="33b8b-181">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="33b8b-181">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="33b8b-182">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="33b8b-182">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="33b8b-183">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="33b8b-183">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


