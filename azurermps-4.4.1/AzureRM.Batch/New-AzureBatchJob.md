---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: 94a35c3923debf5ea983e9d1ad276b124ae8c89c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431152"
---
# <span data-ttu-id="356da-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="356da-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="356da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="356da-102">SYNOPSIS</span></span>
<span data-ttu-id="356da-103">Cria um trabalho no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="356da-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="356da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="356da-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="356da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="356da-105">DESCRIPTION</span></span>
<span data-ttu-id="356da-106">O cmdlet **New-AzureBatchJob** cria um trabalho no serviço de lote do Azure na conta especificada pelo parâmetro *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="356da-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="356da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="356da-107">EXAMPLES</span></span>

### <span data-ttu-id="356da-108">Exemplo 1: criar um trabalho</span><span class="sxs-lookup"><span data-stu-id="356da-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="356da-109">O primeiro comando cria um objeto **PSPoolInformation** usando o cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="356da-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="356da-110">O comando armazena esse objeto na variável $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="356da-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="356da-111">O segundo comando atribui a ID Pool22 à propriedade **poolid** do objeto em $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="356da-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="356da-112">O comando final cria um trabalho com a ID ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="356da-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="356da-113">Tarefas adicionadas ao trabalho são executadas no pool que tem a ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="356da-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="356da-114">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="356da-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="356da-115">OS</span><span class="sxs-lookup"><span data-stu-id="356da-115">PARAMETERS</span></span>

### <span data-ttu-id="356da-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="356da-116">-BatchContext</span></span>
<span data-ttu-id="356da-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="356da-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="356da-118">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="356da-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="356da-119">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="356da-119">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="356da-120">Especifica as variáveis de ambiente comuns, como pares de chave/valor, que esse cmdlet define para todas as tarefas no trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-120">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="356da-121">A chave é o nome da variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="356da-121">The key is the environment variable name.</span></span>
<span data-ttu-id="356da-122">O valor é o valor da variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="356da-122">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-123">-Restrições</span><span class="sxs-lookup"><span data-stu-id="356da-123">-Constraints</span></span>
<span data-ttu-id="356da-124">Especifica as restrições de execução para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-124">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="356da-125">-DisplayName</span></span>
<span data-ttu-id="356da-126">Especifica o nome de exibição do trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-126">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="356da-127">-ID</span><span class="sxs-lookup"><span data-stu-id="356da-127">-Id</span></span>
<span data-ttu-id="356da-128">Especifica uma ID para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-128">Specifies an ID for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="356da-129">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="356da-129">-JobManagerTask</span></span>
<span data-ttu-id="356da-130">Especifica a tarefa do Gerenciador de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="356da-130">Specifies the Job Manager task.</span></span>
<span data-ttu-id="356da-131">O serviço em lotes executa a tarefa do Gerenciador de trabalhos quando o trabalho é iniciado.</span><span class="sxs-lookup"><span data-stu-id="356da-131">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-132">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="356da-132">-JobPreparationTask</span></span>
<span data-ttu-id="356da-133">Especifica a tarefa de preparação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-133">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="356da-134">O serviço em lotes executa a tarefa de preparação do trabalho em um nó de computação antes de iniciar qualquer tarefa desse trabalho nesse nó de computação.</span><span class="sxs-lookup"><span data-stu-id="356da-134">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-135">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="356da-135">-JobReleaseTask</span></span>
<span data-ttu-id="356da-136">Especifica a tarefa de liberação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-136">Specifies the Job Release task.</span></span>
<span data-ttu-id="356da-137">O serviço em lotes executa a tarefa de liberação do trabalho quando o trabalho terminar.</span><span class="sxs-lookup"><span data-stu-id="356da-137">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="356da-138">O serviço em lotes executa a tarefa de versão do trabalho em cada nó de computação em que executou qualquer tarefa do trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-138">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-139">-Metadados</span><span class="sxs-lookup"><span data-stu-id="356da-139">-Metadata</span></span>
<span data-ttu-id="356da-140">Especifica os metadados, como pares de chave/valor, a serem adicionados ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-140">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="356da-141">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="356da-141">The key is the metadata name.</span></span>
<span data-ttu-id="356da-142">O valor é o valor dos metadados.</span><span class="sxs-lookup"><span data-stu-id="356da-142">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-143">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="356da-143">-OnAllTasksComplete</span></span>
<span data-ttu-id="356da-144">Especifica uma ação a ser executada pelo serviço em lotes se todas as tarefas no trabalho estiverem em estado concluído.</span><span class="sxs-lookup"><span data-stu-id="356da-144">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-145">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="356da-145">-OnTaskFailure</span></span>
<span data-ttu-id="356da-146">Especifica uma ação a ser executada pelo serviço em lotes se qualquer tarefa no trabalho falhar.</span><span class="sxs-lookup"><span data-stu-id="356da-146">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-147">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="356da-147">-PoolInformation</span></span>
<span data-ttu-id="356da-148">Especifica os detalhes do pool em que o serviço de lote executa as tarefas do trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-148">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-149">-Priority</span><span class="sxs-lookup"><span data-stu-id="356da-149">-Priority</span></span>
<span data-ttu-id="356da-150">Especifica a prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="356da-150">Specifies the priority of the job.</span></span>
<span data-ttu-id="356da-151">Os valores válidos são: inteiros de-1000 a 1000.</span><span class="sxs-lookup"><span data-stu-id="356da-151">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="356da-152">Um valor de-1000 é a prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="356da-152">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="356da-153">Um valor de 1000 é a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="356da-153">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="356da-154">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="356da-154">The default value is 0.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-155">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="356da-155">-UsesTaskDependencies</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356da-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356da-156">-DefaultProfile</span></span>
<span data-ttu-id="356da-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="356da-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="356da-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356da-158">CommonParameters</span></span>
<span data-ttu-id="356da-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356da-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356da-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="356da-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356da-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="356da-161">INPUTS</span></span>

### <span data-ttu-id="356da-162">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="356da-162">BatchAccountContext</span></span>
<span data-ttu-id="356da-163">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="356da-163">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="356da-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="356da-164">OUTPUTS</span></span>

## <span data-ttu-id="356da-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="356da-165">NOTES</span></span>

## <span data-ttu-id="356da-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="356da-166">RELATED LINKS</span></span>

[<span data-ttu-id="356da-167">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="356da-167">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="356da-168">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="356da-168">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="356da-169">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="356da-169">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="356da-170">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="356da-170">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="356da-171">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="356da-171">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="356da-172">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="356da-172">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="356da-173">Parar-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="356da-173">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="356da-174">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="356da-174">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


