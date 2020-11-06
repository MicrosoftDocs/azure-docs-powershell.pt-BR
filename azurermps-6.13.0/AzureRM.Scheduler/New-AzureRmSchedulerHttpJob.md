---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 1d0c66d3442d6db03897140849f5713d3107f8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440263"
---
# <span data-ttu-id="1a4b8-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="1a4b8-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="1a4b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4b8-103">Cria um trabalho HTTP.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a4b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a4b8-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a4b8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="1a4b8-106">O cmdlet **New-AzureRmSchedulerHttpJob** cria um trabalho http no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="1a4b8-107">Esse cmdlet dá suporte a parâmetros dinâmicos com base nos parâmetros *ErrorActionType* e *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="1a4b8-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="1a4b8-108">Os parâmetros dinâmicos ficam disponíveis com base em outros valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="1a4b8-109">Para descobrir os nomes dos parâmetros dinâmicos depois de especificar os outros parâmetros, digite um hífen (-) e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1a4b8-110">Se você omitir um parâmetro obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1a4b8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a4b8-111">EXAMPLES</span></span>

## <span data-ttu-id="1a4b8-112">OS</span><span class="sxs-lookup"><span data-stu-id="1a4b8-112">PARAMETERS</span></span>

### <span data-ttu-id="1a4b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a4b8-113">-DefaultProfile</span></span>
<span data-ttu-id="1a4b8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a4b8-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1a4b8-115">-EndTime</span></span>
<span data-ttu-id="1a4b8-116">Especifica uma hora de término, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="1a4b8-117">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="1a4b8-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="1a4b8-118">-ErrorActionType</span></span>
<span data-ttu-id="1a4b8-119">Especifica uma configuração de ação de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="1a4b8-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a4b8-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a4b8-121">Http</span><span class="sxs-lookup"><span data-stu-id="1a4b8-121">Http</span></span> 
- <span data-ttu-id="1a4b8-122">Https</span><span class="sxs-lookup"><span data-stu-id="1a4b8-122">Https</span></span> 
- <span data-ttu-id="1a4b8-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="1a4b8-123">StorageQueue</span></span> 
- <span data-ttu-id="1a4b8-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="1a4b8-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="1a4b8-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="1a4b8-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="1a4b8-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="1a4b8-126">-ExecutionCount</span></span>
<span data-ttu-id="1a4b8-127">Especifica o número de vezes que o trabalho é executado.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="1a4b8-128">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="1a4b8-129">-Frequency</span><span class="sxs-lookup"><span data-stu-id="1a4b8-129">-Frequency</span></span>
<span data-ttu-id="1a4b8-130">Especifica uma frequência máxima para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="1a4b8-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a4b8-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a4b8-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="1a4b8-132">Minute</span></span> 
- <span data-ttu-id="1a4b8-133">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="1a4b8-133">Hour</span></span> 
- <span data-ttu-id="1a4b8-134">Contas</span><span class="sxs-lookup"><span data-stu-id="1a4b8-134">Day</span></span> 
- <span data-ttu-id="1a4b8-135">Emana</span><span class="sxs-lookup"><span data-stu-id="1a4b8-135">Week</span></span> 
- <span data-ttu-id="1a4b8-136">Mensais</span><span class="sxs-lookup"><span data-stu-id="1a4b8-136">Month</span></span>

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

### <span data-ttu-id="1a4b8-137">-Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="1a4b8-137">-Headers</span></span>
<span data-ttu-id="1a4b8-138">Especifica uma tabela de hash que contém cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-138">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="1a4b8-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="1a4b8-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="1a4b8-140">Especifica o tipo de autenticação HTTP.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="1a4b8-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a4b8-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a4b8-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1a4b8-142">None</span></span> 
- <span data-ttu-id="1a4b8-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1a4b8-143">ClientCertificate</span></span> 
- <span data-ttu-id="1a4b8-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="1a4b8-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="1a4b8-145">Basic</span><span class="sxs-lookup"><span data-stu-id="1a4b8-145">Basic</span></span>

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

### <span data-ttu-id="1a4b8-146">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="1a4b8-146">-Interval</span></span>
<span data-ttu-id="1a4b8-147">Especifica um intervalo de recorrência para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="1a4b8-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="1a4b8-148">-JobCollectionName</span></span>
<span data-ttu-id="1a4b8-149">Especifica o nome da coleção de trabalhos à qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="1a4b8-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="1a4b8-150">-JobName</span></span>
<span data-ttu-id="1a4b8-151">Especifica um nome para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="1a4b8-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="1a4b8-152">-JobState</span></span>
<span data-ttu-id="1a4b8-153">Especifica o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-153">Specifies the state of the job.</span></span>
<span data-ttu-id="1a4b8-154">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a4b8-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a4b8-155">Possibilita</span><span class="sxs-lookup"><span data-stu-id="1a4b8-155">Enabled</span></span> 
- <span data-ttu-id="1a4b8-156">Ativo</span><span class="sxs-lookup"><span data-stu-id="1a4b8-156">Disabled</span></span>

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

### <span data-ttu-id="1a4b8-157">-Método</span><span class="sxs-lookup"><span data-stu-id="1a4b8-157">-Method</span></span>
<span data-ttu-id="1a4b8-158">Especifica o método para os tipos de ação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="1a4b8-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a4b8-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a4b8-160">Obter</span><span class="sxs-lookup"><span data-stu-id="1a4b8-160">GET</span></span> 
- <span data-ttu-id="1a4b8-161">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="1a4b8-161">PUT</span></span> 
- <span data-ttu-id="1a4b8-162">Postar</span><span class="sxs-lookup"><span data-stu-id="1a4b8-162">POST</span></span> 
- <span data-ttu-id="1a4b8-163">REMOVER</span><span class="sxs-lookup"><span data-stu-id="1a4b8-163">DELETE</span></span>

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

### <span data-ttu-id="1a4b8-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="1a4b8-164">-RequestBody</span></span>
<span data-ttu-id="1a4b8-165">Especifica o valor do corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="1a4b8-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a4b8-166">-ResourceGroupName</span></span>
<span data-ttu-id="1a4b8-167">Especifica o grupo de recursos ao qual o trabalho pertence.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="1a4b8-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1a4b8-168">-StartTime</span></span>
<span data-ttu-id="1a4b8-169">Especifica a hora de início, como um objeto **DateTime** , para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="1a4b8-170">-URI</span><span class="sxs-lookup"><span data-stu-id="1a4b8-170">-Uri</span></span>
<span data-ttu-id="1a4b8-171">Especifica um URI para a ação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-171">Specifies a URI for the job action.</span></span>

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

### <span data-ttu-id="1a4b8-172">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a4b8-172">-Confirm</span></span>
<span data-ttu-id="1a4b8-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a4b8-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a4b8-174">-WhatIf</span></span>
<span data-ttu-id="1a4b8-175">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a4b8-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a4b8-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4b8-177">CommonParameters</span></span>
<span data-ttu-id="1a4b8-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a4b8-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4b8-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a4b8-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4b8-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a4b8-180">INPUTS</span></span>

### <span data-ttu-id="1a4b8-181">System. String</span><span class="sxs-lookup"><span data-stu-id="1a4b8-181">System.String</span></span>

### <span data-ttu-id="1a4b8-182">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1a4b8-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1a4b8-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a4b8-183">OUTPUTS</span></span>

### <span data-ttu-id="1a4b8-184">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1a4b8-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="1a4b8-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a4b8-185">NOTES</span></span>

## <span data-ttu-id="1a4b8-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a4b8-186">RELATED LINKS</span></span>

[<span data-ttu-id="1a4b8-187">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1a4b8-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1a4b8-188">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="1a4b8-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="1a4b8-189">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="1a4b8-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="1a4b8-190">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="1a4b8-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="1a4b8-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="1a4b8-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="1a4b8-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1a4b8-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1a4b8-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="1a4b8-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="1a4b8-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="1a4b8-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="1a4b8-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="1a4b8-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


