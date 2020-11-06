---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: a3fdbb3732def98bbf885cb58bf6f00dcb61eb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427444"
---
# <span data-ttu-id="c166f-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c166f-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="c166f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c166f-102">SYNOPSIS</span></span>
<span data-ttu-id="c166f-103">Cria um trabalho HTTP.</span><span class="sxs-lookup"><span data-stu-id="c166f-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c166f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c166f-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c166f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c166f-105">DESCRIPTION</span></span>
<span data-ttu-id="c166f-106">O cmdlet **New-AzureRmSchedulerHttpJob** cria um trabalho http no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="c166f-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="c166f-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base nos parâmetros *ErrorActionType* e *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="c166f-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="c166f-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c166f-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="c166f-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c166f-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c166f-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="c166f-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c166f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c166f-111">EXAMPLES</span></span>

## <span data-ttu-id="c166f-112">OS</span><span class="sxs-lookup"><span data-stu-id="c166f-112">PARAMETERS</span></span>

### <span data-ttu-id="c166f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c166f-113">-DefaultProfile</span></span>
<span data-ttu-id="c166f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c166f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c166f-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c166f-115">-EndTime</span></span>
<span data-ttu-id="c166f-116">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="c166f-117">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="c166f-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="c166f-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="c166f-118">-ErrorActionType</span></span>
<span data-ttu-id="c166f-119">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="c166f-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c166f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c166f-121">Http</span><span class="sxs-lookup"><span data-stu-id="c166f-121">Http</span></span> 
- <span data-ttu-id="c166f-122">Https</span><span class="sxs-lookup"><span data-stu-id="c166f-122">Https</span></span> 
- <span data-ttu-id="c166f-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="c166f-123">StorageQueue</span></span> 
- <span data-ttu-id="c166f-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c166f-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="c166f-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c166f-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="c166f-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="c166f-126">-ExecutionCount</span></span>
<span data-ttu-id="c166f-127">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="c166f-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="c166f-128">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="c166f-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="c166f-129">-Frequency</span><span class="sxs-lookup"><span data-stu-id="c166f-129">-Frequency</span></span>
<span data-ttu-id="c166f-130">Especifica uma frequência máxima para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="c166f-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c166f-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c166f-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="c166f-132">Minute</span></span> 
- <span data-ttu-id="c166f-133">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="c166f-133">Hour</span></span> 
- <span data-ttu-id="c166f-134">Contas</span><span class="sxs-lookup"><span data-stu-id="c166f-134">Day</span></span> 
- <span data-ttu-id="c166f-135">Emana</span><span class="sxs-lookup"><span data-stu-id="c166f-135">Week</span></span> 
- <span data-ttu-id="c166f-136">Mensais</span><span class="sxs-lookup"><span data-stu-id="c166f-136">Month</span></span>

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

### <span data-ttu-id="c166f-137">-Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="c166f-137">-Headers</span></span>
<span data-ttu-id="c166f-138">Especifica uma tabela de hash que contém cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="c166f-138">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="c166f-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="c166f-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="c166f-140">Especifica o tipo de autenticação HTTP.</span><span class="sxs-lookup"><span data-stu-id="c166f-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="c166f-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c166f-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c166f-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c166f-142">None</span></span> 
- <span data-ttu-id="c166f-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c166f-143">ClientCertificate</span></span> 
- <span data-ttu-id="c166f-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="c166f-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="c166f-145">Basic</span><span class="sxs-lookup"><span data-stu-id="c166f-145">Basic</span></span>

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

### <span data-ttu-id="c166f-146">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="c166f-146">-Interval</span></span>
<span data-ttu-id="c166f-147">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="c166f-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c166f-148">-JobCollectionName</span></span>
<span data-ttu-id="c166f-149">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="c166f-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="c166f-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="c166f-150">-JobName</span></span>
<span data-ttu-id="c166f-151">Especifica um nome para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="c166f-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="c166f-152">-JobState</span></span>
<span data-ttu-id="c166f-153">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-153">Specifies the state of the job.</span></span>
<span data-ttu-id="c166f-154">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c166f-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c166f-155">Possibilita</span><span class="sxs-lookup"><span data-stu-id="c166f-155">Enabled</span></span> 
- <span data-ttu-id="c166f-156">Ativo</span><span class="sxs-lookup"><span data-stu-id="c166f-156">Disabled</span></span>

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

### <span data-ttu-id="c166f-157">-Método</span><span class="sxs-lookup"><span data-stu-id="c166f-157">-Method</span></span>
<span data-ttu-id="c166f-158">Especifica o método para os tipos de ação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="c166f-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c166f-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c166f-160">Obter</span><span class="sxs-lookup"><span data-stu-id="c166f-160">GET</span></span> 
- <span data-ttu-id="c166f-161">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="c166f-161">PUT</span></span> 
- <span data-ttu-id="c166f-162">Postar</span><span class="sxs-lookup"><span data-stu-id="c166f-162">POST</span></span> 
- <span data-ttu-id="c166f-163">REMOVER</span><span class="sxs-lookup"><span data-stu-id="c166f-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c166f-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="c166f-164">-RequestBody</span></span>
<span data-ttu-id="c166f-165">Especifica o valor do corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="c166f-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c166f-166">-ResourceGroupName</span></span>
<span data-ttu-id="c166f-167">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="c166f-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="c166f-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c166f-168">-StartTime</span></span>
<span data-ttu-id="c166f-169">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="c166f-170">-URI</span><span class="sxs-lookup"><span data-stu-id="c166f-170">-Uri</span></span>
<span data-ttu-id="c166f-171">Especifica um URI para a ação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="c166f-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c166f-172">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c166f-172">-Confirm</span></span>
<span data-ttu-id="c166f-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c166f-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c166f-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c166f-174">-WhatIf</span></span>
<span data-ttu-id="c166f-175">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c166f-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c166f-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c166f-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c166f-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c166f-177">CommonParameters</span></span>
<span data-ttu-id="c166f-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c166f-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c166f-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c166f-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c166f-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c166f-180">INPUTS</span></span>

### <span data-ttu-id="c166f-181">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c166f-181">None</span></span>
<span data-ttu-id="c166f-182">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c166f-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c166f-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c166f-183">OUTPUTS</span></span>

### <span data-ttu-id="c166f-184">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c166f-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="c166f-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c166f-185">NOTES</span></span>

## <span data-ttu-id="c166f-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c166f-186">RELATED LINKS</span></span>

[<span data-ttu-id="c166f-187">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c166f-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c166f-188">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c166f-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c166f-189">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c166f-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c166f-190">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c166f-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="c166f-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c166f-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c166f-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c166f-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c166f-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c166f-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c166f-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c166f-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c166f-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c166f-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


