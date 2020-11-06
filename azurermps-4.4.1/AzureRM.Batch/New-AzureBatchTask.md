---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431149"
---
# <span data-ttu-id="b8d30-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8d30-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="b8d30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8d30-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d30-103">Cria uma tarefa em lotes em um trabalho.</span><span class="sxs-lookup"><span data-stu-id="b8d30-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8d30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8d30-104">SYNTAX</span></span>

### <span data-ttu-id="b8d30-105">JobId_Single (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8d30-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8d30-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="b8d30-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8d30-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="b8d30-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8d30-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="b8d30-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8d30-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8d30-109">DESCRIPTION</span></span>
<span data-ttu-id="b8d30-110">O cmdlet **New-AzureBatchTask** cria uma tarefa em lotes do Azure sob o trabalho especificado pelo parâmetro *JobID* ou o parâmetro *Job* .</span><span class="sxs-lookup"><span data-stu-id="b8d30-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="b8d30-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8d30-111">EXAMPLES</span></span>

### <span data-ttu-id="b8d30-112">Exemplo 1: criar uma tarefa em lote</span><span class="sxs-lookup"><span data-stu-id="b8d30-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="b8d30-113">Esse comando cria uma tarefa com a ID Task23 sob o trabalho que tem o ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="b8d30-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="b8d30-114">A tarefa executa o comando especificado.</span><span class="sxs-lookup"><span data-stu-id="b8d30-114">The task runs the specified command.</span></span>
<span data-ttu-id="b8d30-115">Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="b8d30-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b8d30-116">Exemplo 2: criar uma tarefa em lote</span><span class="sxs-lookup"><span data-stu-id="b8d30-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="b8d30-117">Esse comando obtém o trabalho em lotes que tem o ID Job-000001 usando o cmdlet **Get-AzureBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="b8d30-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="b8d30-118">O comando passa aquele trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8d30-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b8d30-119">O comando cria uma tarefa com a ID Task26 sob esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="b8d30-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="b8d30-120">A tarefa executa o comando especificado usando permissões elevadas.</span><span class="sxs-lookup"><span data-stu-id="b8d30-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="b8d30-121">Exemplo 3: adicionar um conjunto de tarefas ao trabalho especificado usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="b8d30-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="b8d30-122">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="b8d30-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="b8d30-123">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="b8d30-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="b8d30-124">Os próximos dois comandos criam objetos **PSCloudTask** usando o cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="b8d30-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="b8d30-125">Os comandos armazenam as tarefas nas variáveis $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="b8d30-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="b8d30-126">O comando final Obtém o trabalho em lotes com o ID Job-000001 usando **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="b8d30-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="b8d30-127">Em seguida, o comando passa esse trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8d30-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b8d30-128">O comando adiciona uma coleção de tarefas sob esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="b8d30-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="b8d30-129">O comando usa o contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="b8d30-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="b8d30-130">Exemplo 4: adicionar um conjunto de tarefas ao trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="b8d30-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="b8d30-131">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="b8d30-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="b8d30-132">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="b8d30-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="b8d30-133">Os próximos dois comandos criam objetos **PSCloudTask** usando o cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="b8d30-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="b8d30-134">Os comandos armazenam as tarefas nas variáveis $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="b8d30-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="b8d30-135">O comando final adiciona as tarefas armazenadas em $Task 01 e $Task 02 sob o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="b8d30-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="b8d30-136">OS</span><span class="sxs-lookup"><span data-stu-id="b8d30-136">PARAMETERS</span></span>

### <span data-ttu-id="b8d30-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="b8d30-137">-AffinityInformation</span></span>
<span data-ttu-id="b8d30-138">Especifica uma dica de localidade que o serviço de lote usa para selecionar um nó no qual executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b8d30-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="b8d30-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b8d30-140">-BatchContext</span></span>
<span data-ttu-id="b8d30-141">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="b8d30-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b8d30-142">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="b8d30-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b8d30-143">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="b8d30-143">-CommandLine</span></span>
<span data-ttu-id="b8d30-144">Especifica a linha de comando para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b8d30-144">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-145">-Restrições</span><span class="sxs-lookup"><span data-stu-id="b8d30-145">-Constraints</span></span>
<span data-ttu-id="b8d30-146">Especifica as restrições de execução que se aplicam a essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="b8d30-146">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-147">-Depende</span><span class="sxs-lookup"><span data-stu-id="b8d30-147">-DependsOn</span></span>
<span data-ttu-id="b8d30-148">Especifica que a tarefa depende de outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="b8d30-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="b8d30-149">A tarefa não será agendada até que todas as tarefas depends tenham sido concluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="b8d30-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b8d30-150">-DisplayName</span></span>
<span data-ttu-id="b8d30-151">Especifica o nome de exibição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b8d30-151">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="b8d30-152">-EnvironmentSettings</span></span>
<span data-ttu-id="b8d30-153">Especifica as configurações de ambiente, como pares de chave/valor, que esse cmdlet adiciona à tarefa.</span><span class="sxs-lookup"><span data-stu-id="b8d30-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="b8d30-154">A chave é o nome da configuração do ambiente.</span><span class="sxs-lookup"><span data-stu-id="b8d30-154">The key is the environment setting name.</span></span>
<span data-ttu-id="b8d30-155">O valor é a configuração do ambiente.</span><span class="sxs-lookup"><span data-stu-id="b8d30-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="b8d30-156">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-157">-ID</span><span class="sxs-lookup"><span data-stu-id="b8d30-157">-Id</span></span>
<span data-ttu-id="b8d30-158">Especifica a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b8d30-158">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-159">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="b8d30-159">-Job</span></span>
<span data-ttu-id="b8d30-160">Especifica o trabalho sob o qual esse cmdlet cria a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b8d30-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="b8d30-161">Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="b8d30-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="b8d30-162">-JobId</span></span>
<span data-ttu-id="b8d30-163">Especifica a ID do trabalho sob a qual esse cmdlet cria a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b8d30-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="b8d30-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="b8d30-165">Especifica informações sobre como executar uma tarefa de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="b8d30-165">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="b8d30-166">-ResourceFiles</span></span>
<span data-ttu-id="b8d30-167">Especifica os arquivos de recurso, como pares chave/valor, que a tarefa requer.</span><span class="sxs-lookup"><span data-stu-id="b8d30-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="b8d30-168">A chave é o caminho do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b8d30-168">The key is the resource file path.</span></span>
<span data-ttu-id="b8d30-169">O valor é a fonte de blob do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b8d30-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="b8d30-170">-RunElevated</span></span>
<span data-ttu-id="b8d30-171">Indica que o processo da tarefa é executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="b8d30-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-172">-Tarefas</span><span class="sxs-lookup"><span data-stu-id="b8d30-172">-Tasks</span></span>
<span data-ttu-id="b8d30-173">Especifica a coleção de tarefas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="b8d30-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="b8d30-174">Cada tarefa deve ter uma ID exclusiva.</span><span class="sxs-lookup"><span data-stu-id="b8d30-174">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d30-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d30-175">-DefaultProfile</span></span>
<span data-ttu-id="b8d30-176">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d30-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8d30-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d30-177">CommonParameters</span></span>
<span data-ttu-id="b8d30-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d30-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d30-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d30-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d30-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8d30-180">INPUTS</span></span>

### <span data-ttu-id="b8d30-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b8d30-181">BatchAccountContext</span></span>
<span data-ttu-id="b8d30-182">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b8d30-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b8d30-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b8d30-183">PSCloudJob</span></span>
<span data-ttu-id="b8d30-184">O parâmetro ' Job ' aceita o valor do tipo ' PSCloudJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="b8d30-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="b8d30-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8d30-185">OUTPUTS</span></span>

## <span data-ttu-id="b8d30-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8d30-186">NOTES</span></span>

## <span data-ttu-id="b8d30-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8d30-187">RELATED LINKS</span></span>

[<span data-ttu-id="b8d30-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b8d30-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b8d30-189">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b8d30-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="b8d30-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8d30-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="b8d30-191">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8d30-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="b8d30-192">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8d30-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="b8d30-193">Parar-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b8d30-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="b8d30-194">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="b8d30-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


