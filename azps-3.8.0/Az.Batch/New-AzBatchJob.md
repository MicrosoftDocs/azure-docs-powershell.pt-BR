---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: afd89951c85022ac8b6fccbaccd734458f029c5f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947257"
---
# <span data-ttu-id="b4e9e-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4e9e-101">New-AzBatchJob</span></span>

## <span data-ttu-id="b4e9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e9e-103">Cria um trabalho no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="b4e9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4e9e-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4e9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e9e-106">O cmdlet **New-AzBatchJob** cria um trabalho no serviço de lote do Azure na conta especificada pelo parâmetro *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="b4e9e-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="b4e9e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4e9e-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e9e-108">Exemplo 1: criar um trabalho</span><span class="sxs-lookup"><span data-stu-id="b4e9e-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="b4e9e-109">O primeiro comando cria um objeto **PSPoolInformation** usando o cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="b4e9e-110">O comando armazena esse objeto na variável $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="b4e9e-111">O segundo comando atribui a ID Pool22 à propriedade **poolid** do objeto em $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="b4e9e-112">O comando final cria um trabalho com a ID ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="b4e9e-113">Tarefas adicionadas ao trabalho são executadas no pool que tem a ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="b4e9e-114">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b4e9e-115">OS</span><span class="sxs-lookup"><span data-stu-id="b4e9e-115">PARAMETERS</span></span>

### <span data-ttu-id="b4e9e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4e9e-116">-BatchContext</span></span>
<span data-ttu-id="b4e9e-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4e9e-118">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4e9e-119">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4e9e-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4e9e-121">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b4e9e-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="b4e9e-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="b4e9e-123">Especifica as variáveis de ambiente comuns, como pares de chave/valor, que esse cmdlet define para todas as tarefas no trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="b4e9e-124">A chave é o nome da variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-124">The key is the environment variable name.</span></span>
<span data-ttu-id="b4e9e-125">O valor é o valor da variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e9e-126">-Restrições</span><span class="sxs-lookup"><span data-stu-id="b4e9e-126">-Constraints</span></span>
<span data-ttu-id="b4e9e-127">Especifica as restrições de execução para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="b4e9e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e9e-128">-DefaultProfile</span></span>
<span data-ttu-id="b4e9e-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4e9e-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b4e9e-130">-DisplayName</span></span>
<span data-ttu-id="b4e9e-131">Especifica o nome de exibição do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="b4e9e-132">-ID</span><span class="sxs-lookup"><span data-stu-id="b4e9e-132">-Id</span></span>
<span data-ttu-id="b4e9e-133">Especifica uma ID para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="b4e9e-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="b4e9e-134">-JobManagerTask</span></span>
<span data-ttu-id="b4e9e-135">Especifica a tarefa do Gerenciador de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="b4e9e-136">O serviço em lotes executa a tarefa do Gerenciador de trabalhos quando o trabalho é iniciado.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="b4e9e-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="b4e9e-137">-JobPreparationTask</span></span>
<span data-ttu-id="b4e9e-138">Especifica a tarefa de preparação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="b4e9e-139">O serviço em lotes executa a tarefa de preparação do trabalho em um nó de computação antes de iniciar qualquer tarefa desse trabalho nesse nó de computação.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="b4e9e-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="b4e9e-140">-JobReleaseTask</span></span>
<span data-ttu-id="b4e9e-141">Especifica a tarefa de liberação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="b4e9e-142">O serviço em lotes executa a tarefa de liberação do trabalho quando o trabalho terminar.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="b4e9e-143">O serviço em lotes executa a tarefa de versão do trabalho em cada nó de computação em que executou qualquer tarefa do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="b4e9e-144">-Metadados</span><span class="sxs-lookup"><span data-stu-id="b4e9e-144">-Metadata</span></span>
<span data-ttu-id="b4e9e-145">Especifica os metadados, como pares de chave/valor, a serem adicionados ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="b4e9e-146">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-146">The key is the metadata name.</span></span>
<span data-ttu-id="b4e9e-147">O valor é o valor dos metadados.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="b4e9e-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="b4e9e-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="b4e9e-149">Especifica uma ação a ser executada pelo serviço em lotes se todas as tarefas no trabalho estiverem em estado concluído.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="b4e9e-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="b4e9e-150">-OnTaskFailure</span></span>
<span data-ttu-id="b4e9e-151">Especifica uma ação a ser executada pelo serviço em lotes se qualquer tarefa no trabalho falhar.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="b4e9e-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="b4e9e-152">-PoolInformation</span></span>
<span data-ttu-id="b4e9e-153">Especifica os detalhes do pool em que o serviço de lote executa as tarefas do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="b4e9e-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="b4e9e-154">-Priority</span></span>
<span data-ttu-id="b4e9e-155">Especifica a prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="b4e9e-156">Os valores válidos são: inteiros de-1000 a 1000.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="b4e9e-157">Um valor de-1000 é a prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="b4e9e-158">Um valor de 1000 é a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="b4e9e-159">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-159">The default value is 0.</span></span>

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

### <span data-ttu-id="b4e9e-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="b4e9e-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="b4e9e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e9e-161">CommonParameters</span></span>
<span data-ttu-id="b4e9e-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e9e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e9e-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4e9e-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e9e-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4e9e-164">INPUTS</span></span>

### <span data-ttu-id="b4e9e-165">System. String</span><span class="sxs-lookup"><span data-stu-id="b4e9e-165">System.String</span></span>

### <span data-ttu-id="b4e9e-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4e9e-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b4e9e-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4e9e-167">OUTPUTS</span></span>

### <span data-ttu-id="b4e9e-168">System. void</span><span class="sxs-lookup"><span data-stu-id="b4e9e-168">System.Void</span></span>

## <span data-ttu-id="b4e9e-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4e9e-169">NOTES</span></span>

## <span data-ttu-id="b4e9e-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4e9e-170">RELATED LINKS</span></span>

[<span data-ttu-id="b4e9e-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4e9e-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="b4e9e-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4e9e-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="b4e9e-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4e9e-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b4e9e-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4e9e-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="b4e9e-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4e9e-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="b4e9e-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4e9e-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="b4e9e-177">Parar-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4e9e-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="b4e9e-178">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="b4e9e-178">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


