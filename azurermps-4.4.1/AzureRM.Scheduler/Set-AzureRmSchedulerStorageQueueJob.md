---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: c752b4fd96ec001467e051fc01be24f592241182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610465"
---
# <span data-ttu-id="66a75-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="66a75-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="66a75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66a75-102">SYNOPSIS</span></span>
<span data-ttu-id="66a75-103">Modifica um trabalho em fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="66a75-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66a75-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a75-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66a75-105">DESCRIPTION</span></span>
<span data-ttu-id="66a75-106">O cmdlet **set-AzureRmSchedulerStorageQueueJob** modifica um trabalho de fila de armazenamento no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="66a75-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="66a75-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base no parâmetro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="66a75-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="66a75-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="66a75-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="66a75-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="66a75-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="66a75-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="66a75-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="66a75-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66a75-111">EXAMPLES</span></span>

## <span data-ttu-id="66a75-112">OS</span><span class="sxs-lookup"><span data-stu-id="66a75-112">PARAMETERS</span></span>

### <span data-ttu-id="66a75-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="66a75-113">-EndTime</span></span>
<span data-ttu-id="66a75-114">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="66a75-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="66a75-115">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="66a75-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="66a75-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="66a75-116">-ErrorActionType</span></span>
<span data-ttu-id="66a75-117">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="66a75-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="66a75-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="66a75-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66a75-119">Http</span><span class="sxs-lookup"><span data-stu-id="66a75-119">Http</span></span> 
- <span data-ttu-id="66a75-120">Https</span><span class="sxs-lookup"><span data-stu-id="66a75-120">Https</span></span> 
- <span data-ttu-id="66a75-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="66a75-121">StorageQueue</span></span> 
- <span data-ttu-id="66a75-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="66a75-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="66a75-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="66a75-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="66a75-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="66a75-124">-ExecutionCount</span></span>
<span data-ttu-id="66a75-125">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="66a75-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="66a75-126">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="66a75-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="66a75-127">-Frequency</span><span class="sxs-lookup"><span data-stu-id="66a75-127">-Frequency</span></span>
<span data-ttu-id="66a75-128">Especifica uma frequência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="66a75-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="66a75-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="66a75-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66a75-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="66a75-130">Minute</span></span> 
- <span data-ttu-id="66a75-131">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="66a75-131">Hour</span></span> 
- <span data-ttu-id="66a75-132">Contas</span><span class="sxs-lookup"><span data-stu-id="66a75-132">Day</span></span> 
- <span data-ttu-id="66a75-133">Emana</span><span class="sxs-lookup"><span data-stu-id="66a75-133">Week</span></span> 
- <span data-ttu-id="66a75-134">Mensais</span><span class="sxs-lookup"><span data-stu-id="66a75-134">Month</span></span>

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

### <span data-ttu-id="66a75-135">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="66a75-135">-Interval</span></span>
<span data-ttu-id="66a75-136">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="66a75-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="66a75-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="66a75-137">-JobCollectionName</span></span>
<span data-ttu-id="66a75-138">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="66a75-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="66a75-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="66a75-139">-JobName</span></span>
<span data-ttu-id="66a75-140">Especifica o nome do trabalho que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="66a75-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="66a75-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="66a75-141">-JobState</span></span>
<span data-ttu-id="66a75-142">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="66a75-142">Specifies the state of the job.</span></span>
<span data-ttu-id="66a75-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="66a75-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66a75-144">Possibilita</span><span class="sxs-lookup"><span data-stu-id="66a75-144">Enabled</span></span> 
- <span data-ttu-id="66a75-145">Ativo</span><span class="sxs-lookup"><span data-stu-id="66a75-145">Disabled</span></span>

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

### <span data-ttu-id="66a75-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a75-146">-ResourceGroupName</span></span>
<span data-ttu-id="66a75-147">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="66a75-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="66a75-148">-StartTime</span><span class="sxs-lookup"><span data-stu-id="66a75-148">-StartTime</span></span>
<span data-ttu-id="66a75-149">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="66a75-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="66a75-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="66a75-150">-StorageQueueAccount</span></span>
<span data-ttu-id="66a75-151">Especifica um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="66a75-151">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="66a75-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="66a75-152">-StorageQueueMessage</span></span>
<span data-ttu-id="66a75-153">Especifica uma mensagem de fila para o trabalho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="66a75-153">Specifies a queue message for storage job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a75-154">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="66a75-154">-StorageQueueName</span></span>
<span data-ttu-id="66a75-155">Especifica o nome da fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="66a75-155">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="66a75-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="66a75-156">-StorageSASToken</span></span>
<span data-ttu-id="66a75-157">Especifica um token de assinatura de acesso compartilhado para uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="66a75-157">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="66a75-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66a75-158">-Confirm</span></span>
<span data-ttu-id="66a75-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a75-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a75-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a75-160">-WhatIf</span></span>
<span data-ttu-id="66a75-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66a75-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a75-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66a75-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a75-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a75-163">-DefaultProfile</span></span>
<span data-ttu-id="66a75-164">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66a75-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a75-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a75-165">CommonParameters</span></span>
<span data-ttu-id="66a75-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a75-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a75-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a75-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a75-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66a75-168">INPUTS</span></span>

## <span data-ttu-id="66a75-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66a75-169">OUTPUTS</span></span>

### <span data-ttu-id="66a75-170">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="66a75-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="66a75-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66a75-171">NOTES</span></span>

## <span data-ttu-id="66a75-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66a75-172">RELATED LINKS</span></span>

[<span data-ttu-id="66a75-173">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="66a75-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="66a75-174">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="66a75-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="66a75-175">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="66a75-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="66a75-176">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="66a75-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="66a75-177">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="66a75-177">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="66a75-178">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="66a75-178">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="66a75-179">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="66a75-179">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="66a75-180">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="66a75-180">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="66a75-181">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="66a75-181">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


