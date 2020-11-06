---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: adb3a44a5d913d636d216750358ebd96c8fc5a29
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601849"
---
# <span data-ttu-id="ff67f-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ff67f-101">New-AzBatchTask</span></span>

## <span data-ttu-id="ff67f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff67f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff67f-103">Cria uma tarefa em lotes em um trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff67f-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="ff67f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff67f-104">SYNTAX</span></span>

### <span data-ttu-id="ff67f-105">JobId_Single (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff67f-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff67f-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="ff67f-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff67f-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="ff67f-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff67f-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="ff67f-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff67f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff67f-109">DESCRIPTION</span></span>
<span data-ttu-id="ff67f-110">O cmdlet **New-AzBatchTask** cria uma tarefa em lotes do Azure sob o trabalho especificado pelo parâmetro *JobID* ou o parâmetro *Job* .</span><span class="sxs-lookup"><span data-stu-id="ff67f-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="ff67f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff67f-111">EXAMPLES</span></span>

### <span data-ttu-id="ff67f-112">Exemplo 1: criar uma tarefa em lote</span><span class="sxs-lookup"><span data-stu-id="ff67f-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="ff67f-113">Esse comando cria uma tarefa com a ID Task23 sob o trabalho que tem o ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="ff67f-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ff67f-114">A tarefa executa o comando especificado.</span><span class="sxs-lookup"><span data-stu-id="ff67f-114">The task runs the specified command.</span></span>
<span data-ttu-id="ff67f-115">Use o cmdlet **Get-AzBatchAccountKeys** para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="ff67f-115">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ff67f-116">Exemplo 2: criar uma tarefa em lote</span><span class="sxs-lookup"><span data-stu-id="ff67f-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="ff67f-117">Esse comando obtém o trabalho em lotes que tem o ID Job-000001 usando o cmdlet **Get-AzBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="ff67f-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="ff67f-118">O comando passa aquele trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff67f-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff67f-119">O comando cria uma tarefa com a ID Task26 sob esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff67f-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="ff67f-120">A tarefa executa o comando especificado usando permissões elevadas.</span><span class="sxs-lookup"><span data-stu-id="ff67f-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="ff67f-121">Exemplo 3: adicionar um conjunto de tarefas ao trabalho especificado usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="ff67f-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="ff67f-122">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="ff67f-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="ff67f-123">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="ff67f-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="ff67f-124">Os próximos dois comandos criam objetos **PSCloudTask** usando o cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="ff67f-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="ff67f-125">Os comandos armazenam as tarefas nas variáveis $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="ff67f-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="ff67f-126">O comando final Obtém o trabalho em lotes com o ID Job-000001 usando **Get-AzBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="ff67f-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="ff67f-127">Em seguida, o comando passa esse trabalho para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff67f-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff67f-128">O comando adiciona uma coleção de tarefas sob esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff67f-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="ff67f-129">O comando usa o contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="ff67f-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="ff67f-130">Exemplo 4: adicionar um conjunto de tarefas ao trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="ff67f-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="ff67f-131">O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="ff67f-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="ff67f-132">O comando armazena essa referência de objeto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="ff67f-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="ff67f-133">Os próximos dois comandos criam objetos **PSCloudTask** usando o cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="ff67f-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="ff67f-134">Os comandos armazenam as tarefas nas variáveis $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="ff67f-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="ff67f-135">O comando final adiciona as tarefas armazenadas em $Task 01 e $Task 02 sob o trabalho que tem o job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="ff67f-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="ff67f-136">Exemplo 5: adicionar uma tarefa com arquivos de saída</span><span class="sxs-lookup"><span data-stu-id="ff67f-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="ff67f-137">Exemplo 6: adicionar uma tarefa com configurações de token de autenticação</span><span class="sxs-lookup"><span data-stu-id="ff67f-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="ff67f-138">Exemplo 7: adicionar uma tarefa que é executada em um contêiner</span><span class="sxs-lookup"><span data-stu-id="ff67f-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="ff67f-139">OS</span><span class="sxs-lookup"><span data-stu-id="ff67f-139">PARAMETERS</span></span>

### <span data-ttu-id="ff67f-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="ff67f-140">-AffinityInformation</span></span>
<span data-ttu-id="ff67f-141">Especifica uma dica de localidade que o serviço de lote usa para selecionar um nó no qual executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff67f-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="ff67f-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="ff67f-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff67f-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="ff67f-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="ff67f-144">As configurações de um token de autenticação que a tarefa pode usar para realizar operações de serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="ff67f-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="ff67f-145">Se estiver definido, o serviço em lotes fornece a tarefa com um token de autenticação que pode ser usado para autenticar operações de serviço em lotes sem exigir uma chave de acesso à conta.</span><span class="sxs-lookup"><span data-stu-id="ff67f-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="ff67f-146">O token é fornecido por meio da variável de ambiente AZ_BATCH_AUTHENTICATION_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="ff67f-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="ff67f-147">As operações que a tarefa pode realizar usando o token dependem das configurações.</span><span class="sxs-lookup"><span data-stu-id="ff67f-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="ff67f-148">Por exemplo, uma tarefa pode solicitar permissões de trabalho para adicionar outras tarefas ao trabalho ou verificar o status do trabalho ou de outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="ff67f-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff67f-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ff67f-149">-BatchContext</span></span>
<span data-ttu-id="ff67f-150">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="ff67f-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ff67f-151">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="ff67f-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ff67f-152">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="ff67f-152">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ff67f-153">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="ff67f-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ff67f-154">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ff67f-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ff67f-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="ff67f-155">-CommandLine</span></span>
<span data-ttu-id="ff67f-156">Especifica a linha de comando para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff67f-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="ff67f-157">-Restrições</span><span class="sxs-lookup"><span data-stu-id="ff67f-157">-Constraints</span></span>
<span data-ttu-id="ff67f-158">Especifica as restrições de execução que se aplicam a essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff67f-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="ff67f-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="ff67f-159">-ContainerSettings</span></span>
<span data-ttu-id="ff67f-160">As configurações para o contêiner em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="ff67f-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="ff67f-161">Se o pool que executar essa tarefa tiver containerConfiguration definido, isso também deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="ff67f-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="ff67f-162">Se o pool que executar essa tarefa não tiver o containerConfiguration definido, isso não deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="ff67f-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="ff67f-163">Quando isso é especificado, todas as pastas recursivamente abaixo do AZ_BATCH_NODE_ROOT_DIR (a raiz dos diretórios do Azure batch no nó) são mapeadas para o contêiner, todas as variáveis de ambiente de tarefa são mapeadas para o contêiner e a linha de comando da tarefa é executada no contêiner.</span><span class="sxs-lookup"><span data-stu-id="ff67f-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff67f-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff67f-164">-DefaultProfile</span></span>
<span data-ttu-id="ff67f-165">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff67f-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff67f-166">-Depende</span><span class="sxs-lookup"><span data-stu-id="ff67f-166">-DependsOn</span></span>
<span data-ttu-id="ff67f-167">Especifica que a tarefa depende de outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="ff67f-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="ff67f-168">A tarefa não será agendada até que todas as tarefas depends tenham sido concluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="ff67f-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="ff67f-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ff67f-169">-DisplayName</span></span>
<span data-ttu-id="ff67f-170">Especifica o nome de exibição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff67f-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="ff67f-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="ff67f-171">-EnvironmentSettings</span></span>
<span data-ttu-id="ff67f-172">Especifica as configurações de ambiente, como pares de chave/valor, que esse cmdlet adiciona à tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff67f-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="ff67f-173">A chave é o nome da configuração do ambiente.</span><span class="sxs-lookup"><span data-stu-id="ff67f-173">The key is the environment setting name.</span></span>
<span data-ttu-id="ff67f-174">O valor é a configuração do ambiente.</span><span class="sxs-lookup"><span data-stu-id="ff67f-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff67f-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="ff67f-175">-ExitConditions</span></span>
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

### <span data-ttu-id="ff67f-176">-ID</span><span class="sxs-lookup"><span data-stu-id="ff67f-176">-Id</span></span>
<span data-ttu-id="ff67f-177">Especifica a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff67f-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="ff67f-178">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="ff67f-178">-Job</span></span>
<span data-ttu-id="ff67f-179">Especifica o trabalho sob o qual esse cmdlet cria a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff67f-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="ff67f-180">Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="ff67f-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="ff67f-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="ff67f-181">-JobId</span></span>
<span data-ttu-id="ff67f-182">Especifica a ID do trabalho sob a qual esse cmdlet cria a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ff67f-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="ff67f-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="ff67f-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="ff67f-184">Especifica informações sobre como executar uma tarefa de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="ff67f-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="ff67f-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ff67f-185">-OutputFile</span></span>
<span data-ttu-id="ff67f-186">Obtém ou define uma lista de arquivos que o serviço em lotes carregará do nó de computação após a execução da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ff67f-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="ff67f-187">Para tarefas de várias instâncias, os arquivos só serão carregados do nó de computação no qual a tarefa principal será executada.</span><span class="sxs-lookup"><span data-stu-id="ff67f-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff67f-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="ff67f-188">-ResourceFiles</span></span>
<span data-ttu-id="ff67f-189">Especifica os arquivos de recurso, como pares chave/valor, que a tarefa requer.</span><span class="sxs-lookup"><span data-stu-id="ff67f-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="ff67f-190">A chave é o caminho do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ff67f-190">The key is the resource file path.</span></span>
<span data-ttu-id="ff67f-191">O valor é a fonte de blob do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ff67f-191">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff67f-192">-Tarefas</span><span class="sxs-lookup"><span data-stu-id="ff67f-192">-Tasks</span></span>
<span data-ttu-id="ff67f-193">Especifica a coleção de tarefas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="ff67f-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="ff67f-194">Cada tarefa deve ter uma ID exclusiva.</span><span class="sxs-lookup"><span data-stu-id="ff67f-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="ff67f-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="ff67f-195">-UserIdentity</span></span>
<span data-ttu-id="ff67f-196">A identidade do usuário na qual a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="ff67f-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff67f-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff67f-197">CommonParameters</span></span>
<span data-ttu-id="ff67f-198">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff67f-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff67f-199">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff67f-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff67f-200">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff67f-200">INPUTS</span></span>

### <span data-ttu-id="ff67f-201">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="ff67f-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="ff67f-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ff67f-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ff67f-203">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff67f-203">OUTPUTS</span></span>

### <span data-ttu-id="ff67f-204">System. void</span><span class="sxs-lookup"><span data-stu-id="ff67f-204">System.Void</span></span>

## <span data-ttu-id="ff67f-205">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff67f-205">NOTES</span></span>

## <span data-ttu-id="ff67f-206">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff67f-206">RELATED LINKS</span></span>

[<span data-ttu-id="ff67f-207">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ff67f-207">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ff67f-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ff67f-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="ff67f-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ff67f-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="ff67f-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ff67f-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="ff67f-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ff67f-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="ff67f-212">Parar-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="ff67f-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="ff67f-213">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="ff67f-213">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


