---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 9f43780cc7684c897b7b6d42e381e47f6ff8e106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432899"
---
# <span data-ttu-id="8530b-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="8530b-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="8530b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8530b-102">SYNOPSIS</span></span>
<span data-ttu-id="8530b-103">Modifica um trabalho de Agendador HTTP.</span><span class="sxs-lookup"><span data-stu-id="8530b-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8530b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8530b-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8530b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8530b-105">DESCRIPTION</span></span>
<span data-ttu-id="8530b-106">O cmdlet **set-AzureRmSchedulerHttpJob** modifica um trabalho http no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="8530b-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="8530b-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base nos parâmetros *ErrorActionType* e *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="8530b-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="8530b-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8530b-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="8530b-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8530b-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8530b-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="8530b-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8530b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8530b-111">EXAMPLES</span></span>

## <span data-ttu-id="8530b-112">OS</span><span class="sxs-lookup"><span data-stu-id="8530b-112">PARAMETERS</span></span>

### <span data-ttu-id="8530b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8530b-113">-DefaultProfile</span></span>
<span data-ttu-id="8530b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8530b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8530b-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8530b-115">-EndTime</span></span>
<span data-ttu-id="8530b-116">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="8530b-117">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="8530b-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="8530b-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="8530b-118">-ErrorActionType</span></span>
<span data-ttu-id="8530b-119">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="8530b-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8530b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8530b-121">Http</span><span class="sxs-lookup"><span data-stu-id="8530b-121">Http</span></span> 
- <span data-ttu-id="8530b-122">Https</span><span class="sxs-lookup"><span data-stu-id="8530b-122">Https</span></span> 
- <span data-ttu-id="8530b-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="8530b-123">StorageQueue</span></span> 
- <span data-ttu-id="8530b-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="8530b-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="8530b-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="8530b-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="8530b-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="8530b-126">-ExecutionCount</span></span>
<span data-ttu-id="8530b-127">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="8530b-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="8530b-128">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="8530b-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="8530b-129">-Frequency</span><span class="sxs-lookup"><span data-stu-id="8530b-129">-Frequency</span></span>
<span data-ttu-id="8530b-130">Especifica a frequência máxima do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="8530b-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8530b-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8530b-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="8530b-132">Minute</span></span> 
- <span data-ttu-id="8530b-133">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="8530b-133">Hour</span></span> 
- <span data-ttu-id="8530b-134">Contas</span><span class="sxs-lookup"><span data-stu-id="8530b-134">Day</span></span> 
- <span data-ttu-id="8530b-135">Emana</span><span class="sxs-lookup"><span data-stu-id="8530b-135">Week</span></span> 
- <span data-ttu-id="8530b-136">Mensais</span><span class="sxs-lookup"><span data-stu-id="8530b-136">Month</span></span>

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

### <span data-ttu-id="8530b-137">-Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="8530b-137">-Headers</span></span>
<span data-ttu-id="8530b-138">Especifica uma tabela de hash que contém cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="8530b-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8530b-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8530b-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="8530b-140">Especifica o tipo de autenticação HTTP.</span><span class="sxs-lookup"><span data-stu-id="8530b-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="8530b-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8530b-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8530b-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8530b-142">None</span></span> 
- <span data-ttu-id="8530b-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8530b-143">ClientCertificate</span></span> 
- <span data-ttu-id="8530b-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="8530b-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="8530b-145">Basic</span><span class="sxs-lookup"><span data-stu-id="8530b-145">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8530b-146">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="8530b-146">-Interval</span></span>
<span data-ttu-id="8530b-147">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="8530b-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8530b-148">-JobCollectionName</span></span>
<span data-ttu-id="8530b-149">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="8530b-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="8530b-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="8530b-150">-JobName</span></span>
<span data-ttu-id="8530b-151">Especifica o nome do trabalho que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8530b-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8530b-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="8530b-152">-JobState</span></span>
<span data-ttu-id="8530b-153">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-153">Specifies the state of the job.</span></span>
<span data-ttu-id="8530b-154">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8530b-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8530b-155">Possibilita</span><span class="sxs-lookup"><span data-stu-id="8530b-155">Enabled</span></span> 
- <span data-ttu-id="8530b-156">Ativo</span><span class="sxs-lookup"><span data-stu-id="8530b-156">Disabled</span></span>

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

### <span data-ttu-id="8530b-157">-Método</span><span class="sxs-lookup"><span data-stu-id="8530b-157">-Method</span></span>
<span data-ttu-id="8530b-158">Especifica o método para os tipos de ação para esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="8530b-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8530b-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8530b-160">Obter</span><span class="sxs-lookup"><span data-stu-id="8530b-160">GET</span></span> 
- <span data-ttu-id="8530b-161">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="8530b-161">PUT</span></span> 
- <span data-ttu-id="8530b-162">Postar</span><span class="sxs-lookup"><span data-stu-id="8530b-162">POST</span></span> 
- <span data-ttu-id="8530b-163">REMOVER</span><span class="sxs-lookup"><span data-stu-id="8530b-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8530b-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="8530b-164">-RequestBody</span></span>
<span data-ttu-id="8530b-165">Especifica o valor do corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="8530b-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8530b-166">-ResourceGroupName</span></span>
<span data-ttu-id="8530b-167">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="8530b-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="8530b-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8530b-168">-StartTime</span></span>
<span data-ttu-id="8530b-169">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="8530b-170">-URI</span><span class="sxs-lookup"><span data-stu-id="8530b-170">-Uri</span></span>
<span data-ttu-id="8530b-171">Especifica um URI para a ação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8530b-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8530b-172">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8530b-172">-Confirm</span></span>
<span data-ttu-id="8530b-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8530b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8530b-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8530b-174">-WhatIf</span></span>
<span data-ttu-id="8530b-175">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8530b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8530b-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8530b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8530b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8530b-177">CommonParameters</span></span>
<span data-ttu-id="8530b-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8530b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8530b-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8530b-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8530b-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8530b-180">INPUTS</span></span>

### <span data-ttu-id="8530b-181">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8530b-181">None</span></span>
<span data-ttu-id="8530b-182">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8530b-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8530b-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8530b-183">OUTPUTS</span></span>

### <span data-ttu-id="8530b-184">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8530b-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="8530b-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8530b-185">NOTES</span></span>

## <span data-ttu-id="8530b-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8530b-186">RELATED LINKS</span></span>

[<span data-ttu-id="8530b-187">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="8530b-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="8530b-188">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8530b-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8530b-189">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="8530b-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="8530b-190">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="8530b-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="8530b-191">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="8530b-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="8530b-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8530b-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8530b-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="8530b-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="8530b-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="8530b-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="8530b-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="8530b-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


