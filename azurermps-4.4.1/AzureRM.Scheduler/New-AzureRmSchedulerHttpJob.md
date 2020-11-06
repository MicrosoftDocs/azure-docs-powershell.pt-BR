---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 5fc591ff5d24211b8af464dab46bfb81360f83e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609567"
---
# <span data-ttu-id="36a50-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="36a50-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="36a50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36a50-102">SYNOPSIS</span></span>
<span data-ttu-id="36a50-103">Cria um trabalho HTTP.</span><span class="sxs-lookup"><span data-stu-id="36a50-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36a50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36a50-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36a50-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36a50-105">DESCRIPTION</span></span>
<span data-ttu-id="36a50-106">O cmdlet **New-AzureRmSchedulerHttpJob** cria um trabalho http no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="36a50-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="36a50-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base nos parâmetros *ErrorActionType* e *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="36a50-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="36a50-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="36a50-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="36a50-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="36a50-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="36a50-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="36a50-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="36a50-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36a50-111">EXAMPLES</span></span>

## <span data-ttu-id="36a50-112">OS</span><span class="sxs-lookup"><span data-stu-id="36a50-112">PARAMETERS</span></span>

### <span data-ttu-id="36a50-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="36a50-113">-EndTime</span></span>
<span data-ttu-id="36a50-114">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="36a50-115">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="36a50-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="36a50-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="36a50-116">-ErrorActionType</span></span>
<span data-ttu-id="36a50-117">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="36a50-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="36a50-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36a50-119">Http</span><span class="sxs-lookup"><span data-stu-id="36a50-119">Http</span></span> 
- <span data-ttu-id="36a50-120">Https</span><span class="sxs-lookup"><span data-stu-id="36a50-120">Https</span></span> 
- <span data-ttu-id="36a50-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="36a50-121">StorageQueue</span></span> 
- <span data-ttu-id="36a50-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="36a50-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="36a50-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="36a50-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="36a50-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="36a50-124">-ExecutionCount</span></span>
<span data-ttu-id="36a50-125">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="36a50-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="36a50-126">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="36a50-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="36a50-127">-Frequency</span><span class="sxs-lookup"><span data-stu-id="36a50-127">-Frequency</span></span>
<span data-ttu-id="36a50-128">Especifica uma frequência máxima para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="36a50-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="36a50-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36a50-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="36a50-130">Minute</span></span> 
- <span data-ttu-id="36a50-131">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="36a50-131">Hour</span></span> 
- <span data-ttu-id="36a50-132">Contas</span><span class="sxs-lookup"><span data-stu-id="36a50-132">Day</span></span> 
- <span data-ttu-id="36a50-133">Emana</span><span class="sxs-lookup"><span data-stu-id="36a50-133">Week</span></span> 
- <span data-ttu-id="36a50-134">Mensais</span><span class="sxs-lookup"><span data-stu-id="36a50-134">Month</span></span>

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

### <span data-ttu-id="36a50-135">-Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="36a50-135">-Headers</span></span>
<span data-ttu-id="36a50-136">Especifica uma tabela de hash que contém cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="36a50-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="36a50-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="36a50-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="36a50-138">Especifica o tipo de autenticação HTTP.</span><span class="sxs-lookup"><span data-stu-id="36a50-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="36a50-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="36a50-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36a50-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="36a50-140">None</span></span> 
- <span data-ttu-id="36a50-141">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="36a50-141">ClientCertificate</span></span> 
- <span data-ttu-id="36a50-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="36a50-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="36a50-143">Basic</span><span class="sxs-lookup"><span data-stu-id="36a50-143">Basic</span></span>

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

### <span data-ttu-id="36a50-144">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="36a50-144">-Interval</span></span>
<span data-ttu-id="36a50-145">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="36a50-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="36a50-146">-JobCollectionName</span></span>
<span data-ttu-id="36a50-147">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="36a50-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="36a50-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="36a50-148">-JobName</span></span>
<span data-ttu-id="36a50-149">Especifica um nome para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-149">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="36a50-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="36a50-150">-JobState</span></span>
<span data-ttu-id="36a50-151">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-151">Specifies the state of the job.</span></span>
<span data-ttu-id="36a50-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="36a50-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36a50-153">Possibilita</span><span class="sxs-lookup"><span data-stu-id="36a50-153">Enabled</span></span> 
- <span data-ttu-id="36a50-154">Ativo</span><span class="sxs-lookup"><span data-stu-id="36a50-154">Disabled</span></span>

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

### <span data-ttu-id="36a50-155">-Método</span><span class="sxs-lookup"><span data-stu-id="36a50-155">-Method</span></span>
<span data-ttu-id="36a50-156">Especifica o método para os tipos de ação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-156">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="36a50-157">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="36a50-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36a50-158">Obter</span><span class="sxs-lookup"><span data-stu-id="36a50-158">GET</span></span> 
- <span data-ttu-id="36a50-159">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="36a50-159">PUT</span></span> 
- <span data-ttu-id="36a50-160">Postar</span><span class="sxs-lookup"><span data-stu-id="36a50-160">POST</span></span> 
- <span data-ttu-id="36a50-161">REMOVER</span><span class="sxs-lookup"><span data-stu-id="36a50-161">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a50-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="36a50-162">-RequestBody</span></span>
<span data-ttu-id="36a50-163">Especifica o valor do corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="36a50-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a50-164">-ResourceGroupName</span></span>
<span data-ttu-id="36a50-165">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="36a50-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="36a50-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="36a50-166">-StartTime</span></span>
<span data-ttu-id="36a50-167">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="36a50-168">-URI</span><span class="sxs-lookup"><span data-stu-id="36a50-168">-Uri</span></span>
<span data-ttu-id="36a50-169">Especifica um URI para a ação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="36a50-169">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a50-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36a50-170">-Confirm</span></span>
<span data-ttu-id="36a50-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36a50-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36a50-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36a50-172">-WhatIf</span></span>
<span data-ttu-id="36a50-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36a50-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36a50-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36a50-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36a50-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a50-175">-DefaultProfile</span></span>
<span data-ttu-id="36a50-176">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36a50-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36a50-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a50-177">CommonParameters</span></span>
<span data-ttu-id="36a50-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a50-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a50-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a50-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a50-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36a50-180">INPUTS</span></span>

## <span data-ttu-id="36a50-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36a50-181">OUTPUTS</span></span>

### <span data-ttu-id="36a50-182">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="36a50-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="36a50-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36a50-183">NOTES</span></span>

## <span data-ttu-id="36a50-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36a50-184">RELATED LINKS</span></span>

[<span data-ttu-id="36a50-185">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="36a50-185">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="36a50-186">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="36a50-186">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="36a50-187">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="36a50-187">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="36a50-188">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="36a50-188">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="36a50-189">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="36a50-189">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="36a50-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="36a50-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="36a50-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="36a50-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="36a50-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="36a50-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="36a50-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="36a50-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


