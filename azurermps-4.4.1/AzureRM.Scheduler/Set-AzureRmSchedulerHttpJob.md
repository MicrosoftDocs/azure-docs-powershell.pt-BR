---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2debabbcd4ae9b5418436e7846e8490926f37b1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430650"
---
# <span data-ttu-id="cca02-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="cca02-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="cca02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cca02-102">SYNOPSIS</span></span>
<span data-ttu-id="cca02-103">Modifica um trabalho de Agendador HTTP.</span><span class="sxs-lookup"><span data-stu-id="cca02-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cca02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cca02-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cca02-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cca02-105">DESCRIPTION</span></span>
<span data-ttu-id="cca02-106">O cmdlet **set-AzureRmSchedulerHttpJob** modifica um trabalho http no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="cca02-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="cca02-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base nos parâmetros *ErrorActionType* e *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="cca02-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="cca02-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cca02-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="cca02-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cca02-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cca02-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="cca02-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cca02-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cca02-111">EXAMPLES</span></span>

## <span data-ttu-id="cca02-112">OS</span><span class="sxs-lookup"><span data-stu-id="cca02-112">PARAMETERS</span></span>

### <span data-ttu-id="cca02-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="cca02-113">-EndTime</span></span>
<span data-ttu-id="cca02-114">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="cca02-115">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="cca02-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="cca02-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="cca02-116">-ErrorActionType</span></span>
<span data-ttu-id="cca02-117">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="cca02-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cca02-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cca02-119">Http</span><span class="sxs-lookup"><span data-stu-id="cca02-119">Http</span></span> 
- <span data-ttu-id="cca02-120">Https</span><span class="sxs-lookup"><span data-stu-id="cca02-120">Https</span></span> 
- <span data-ttu-id="cca02-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="cca02-121">StorageQueue</span></span> 
- <span data-ttu-id="cca02-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="cca02-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="cca02-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="cca02-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="cca02-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="cca02-124">-ExecutionCount</span></span>
<span data-ttu-id="cca02-125">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="cca02-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="cca02-126">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="cca02-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="cca02-127">-Frequency</span><span class="sxs-lookup"><span data-stu-id="cca02-127">-Frequency</span></span>
<span data-ttu-id="cca02-128">Especifica a frequência máxima do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-128">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="cca02-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cca02-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cca02-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="cca02-130">Minute</span></span> 
- <span data-ttu-id="cca02-131">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="cca02-131">Hour</span></span> 
- <span data-ttu-id="cca02-132">Contas</span><span class="sxs-lookup"><span data-stu-id="cca02-132">Day</span></span> 
- <span data-ttu-id="cca02-133">Emana</span><span class="sxs-lookup"><span data-stu-id="cca02-133">Week</span></span> 
- <span data-ttu-id="cca02-134">Mensais</span><span class="sxs-lookup"><span data-stu-id="cca02-134">Month</span></span>

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

### <span data-ttu-id="cca02-135">-Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="cca02-135">-Headers</span></span>
<span data-ttu-id="cca02-136">Especifica uma tabela de hash que contém cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="cca02-136">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca02-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="cca02-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="cca02-138">Especifica o tipo de autenticação HTTP.</span><span class="sxs-lookup"><span data-stu-id="cca02-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="cca02-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cca02-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cca02-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cca02-140">None</span></span> 
- <span data-ttu-id="cca02-141">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cca02-141">ClientCertificate</span></span> 
- <span data-ttu-id="cca02-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="cca02-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="cca02-143">Basic</span><span class="sxs-lookup"><span data-stu-id="cca02-143">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca02-144">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="cca02-144">-Interval</span></span>
<span data-ttu-id="cca02-145">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="cca02-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="cca02-146">-JobCollectionName</span></span>
<span data-ttu-id="cca02-147">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="cca02-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="cca02-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="cca02-148">-JobName</span></span>
<span data-ttu-id="cca02-149">Especifica o nome do trabalho que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="cca02-149">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cca02-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="cca02-150">-JobState</span></span>
<span data-ttu-id="cca02-151">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-151">Specifies the state of the job.</span></span>
<span data-ttu-id="cca02-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cca02-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cca02-153">Possibilita</span><span class="sxs-lookup"><span data-stu-id="cca02-153">Enabled</span></span> 
- <span data-ttu-id="cca02-154">Ativo</span><span class="sxs-lookup"><span data-stu-id="cca02-154">Disabled</span></span>

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

### <span data-ttu-id="cca02-155">-Método</span><span class="sxs-lookup"><span data-stu-id="cca02-155">-Method</span></span>
<span data-ttu-id="cca02-156">Especifica o método para os tipos de ação para esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-156">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="cca02-157">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cca02-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cca02-158">Obter</span><span class="sxs-lookup"><span data-stu-id="cca02-158">GET</span></span> 
- <span data-ttu-id="cca02-159">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="cca02-159">PUT</span></span> 
- <span data-ttu-id="cca02-160">Postar</span><span class="sxs-lookup"><span data-stu-id="cca02-160">POST</span></span> 
- <span data-ttu-id="cca02-161">REMOVER</span><span class="sxs-lookup"><span data-stu-id="cca02-161">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca02-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="cca02-162">-RequestBody</span></span>
<span data-ttu-id="cca02-163">Especifica o valor do corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="cca02-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca02-164">-ResourceGroupName</span></span>
<span data-ttu-id="cca02-165">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="cca02-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="cca02-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cca02-166">-StartTime</span></span>
<span data-ttu-id="cca02-167">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="cca02-168">-URI</span><span class="sxs-lookup"><span data-stu-id="cca02-168">-Uri</span></span>
<span data-ttu-id="cca02-169">Especifica um URI para a ação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca02-169">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca02-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cca02-170">-Confirm</span></span>
<span data-ttu-id="cca02-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cca02-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cca02-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cca02-172">-WhatIf</span></span>
<span data-ttu-id="cca02-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cca02-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cca02-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cca02-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cca02-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca02-175">-DefaultProfile</span></span>
<span data-ttu-id="cca02-176">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cca02-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cca02-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca02-177">CommonParameters</span></span>
<span data-ttu-id="cca02-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca02-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca02-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca02-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca02-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cca02-180">INPUTS</span></span>

## <span data-ttu-id="cca02-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cca02-181">OUTPUTS</span></span>

### <span data-ttu-id="cca02-182">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cca02-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="cca02-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cca02-183">NOTES</span></span>

## <span data-ttu-id="cca02-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cca02-184">RELATED LINKS</span></span>

[<span data-ttu-id="cca02-185">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="cca02-185">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="cca02-186">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cca02-186">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="cca02-187">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="cca02-187">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="cca02-188">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="cca02-188">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="cca02-189">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="cca02-189">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="cca02-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cca02-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="cca02-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="cca02-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="cca02-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="cca02-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="cca02-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="cca02-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


