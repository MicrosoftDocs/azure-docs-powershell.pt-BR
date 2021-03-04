---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: 97b6d2c332b4bc59df165599fe49d38fe496008c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889808"
---
# <span data-ttu-id="41490-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41490-101">New-AzBatchJob</span></span>

## <span data-ttu-id="41490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41490-102">SYNOPSIS</span></span>
<span data-ttu-id="41490-103">Cria um trabalho no serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="41490-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="41490-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="41490-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41490-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="41490-105">DESCRIPTION</span></span>
<span data-ttu-id="41490-106">O cmdlet **New-AzBatchJob** cria um trabalho no serviço lote do Azure na conta especificada pelo parâmetro *BatchAccountContext.*</span><span class="sxs-lookup"><span data-stu-id="41490-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="41490-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41490-107">EXAMPLES</span></span>

### <span data-ttu-id="41490-108">Exemplo 1: Criar um trabalho</span><span class="sxs-lookup"><span data-stu-id="41490-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="41490-109">O primeiro comando cria um **objeto PSPoolInformation** usando o cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="41490-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="41490-110">O comando armazena esse objeto na variável $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="41490-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="41490-111">O segundo comando atribui o Pool de ID22 à **propriedade PoolId** do objeto em $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="41490-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="41490-112">O comando final cria um trabalho que tem a ID ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="41490-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="41490-113">Tarefas adicionadas ao trabalho executado no pool que tem o Pool de ID22.</span><span class="sxs-lookup"><span data-stu-id="41490-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="41490-114">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="41490-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="41490-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="41490-115">PARAMETERS</span></span>

### <span data-ttu-id="41490-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="41490-116">-BatchContext</span></span>
<span data-ttu-id="41490-117">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="41490-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="41490-118">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="41490-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="41490-119">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="41490-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="41490-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="41490-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="41490-121">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="41490-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="41490-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="41490-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="41490-123">Especifica as variáveis de ambiente comuns, como pares de chave/valor, que esse cmdlet define para todas as tarefas no trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="41490-124">A chave é o nome da variável do ambiente.</span><span class="sxs-lookup"><span data-stu-id="41490-124">The key is the environment variable name.</span></span>
<span data-ttu-id="41490-125">O valor é o valor da variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="41490-125">The value is the environment variable value.</span></span>

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

### <span data-ttu-id="41490-126">-Constraints</span><span class="sxs-lookup"><span data-stu-id="41490-126">-Constraints</span></span>
<span data-ttu-id="41490-127">Especifica as restrições de execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="41490-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41490-128">-DefaultProfile</span></span>
<span data-ttu-id="41490-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="41490-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41490-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="41490-130">-DisplayName</span></span>
<span data-ttu-id="41490-131">Especifica o nome de exibição do trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="41490-132">-Id</span><span class="sxs-lookup"><span data-stu-id="41490-132">-Id</span></span>
<span data-ttu-id="41490-133">Especifica uma ID do trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="41490-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="41490-134">-JobManagerTask</span></span>
<span data-ttu-id="41490-135">Especifica a tarefa do Gerenciador de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="41490-136">O serviço Batch executa a tarefa Gerenciador de Trabalho quando o trabalho é iniciado.</span><span class="sxs-lookup"><span data-stu-id="41490-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="41490-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="41490-137">-JobPreparationTask</span></span>
<span data-ttu-id="41490-138">Especifica a tarefa Preparação do Trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="41490-139">O serviço Batch executa a tarefa Preparação do Trabalho em um nó de computação antes de iniciar qualquer tarefa desse trabalho nesse nó de computação.</span><span class="sxs-lookup"><span data-stu-id="41490-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="41490-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="41490-140">-JobReleaseTask</span></span>
<span data-ttu-id="41490-141">Especifica a tarefa Liberação de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="41490-142">O serviço Batch executa a tarefa Liberação de Trabalho quando o trabalho termina.</span><span class="sxs-lookup"><span data-stu-id="41490-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="41490-143">O serviço Batch executa a tarefa Liberar Trabalho em cada nó de computação onde ele executa qualquer tarefa do trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="41490-144">-Metadados</span><span class="sxs-lookup"><span data-stu-id="41490-144">-Metadata</span></span>
<span data-ttu-id="41490-145">Especifica metadados, como pares de chave/valor, para adicionar ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="41490-146">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="41490-146">The key is the metadata name.</span></span>
<span data-ttu-id="41490-147">O valor é o valor de metadados.</span><span class="sxs-lookup"><span data-stu-id="41490-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="41490-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="41490-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="41490-149">Especifica uma ação que o serviço Batch realizará se todas as tarefas do trabalho estão no estado concluído.</span><span class="sxs-lookup"><span data-stu-id="41490-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="41490-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="41490-150">-OnTaskFailure</span></span>
<span data-ttu-id="41490-151">Especifica uma ação que o serviço Batch assume se qualquer tarefa no trabalho falhar.</span><span class="sxs-lookup"><span data-stu-id="41490-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="41490-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="41490-152">-PoolInformation</span></span>
<span data-ttu-id="41490-153">Especifica os detalhes do pool no qual o serviço Batch executa as tarefas do trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="41490-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="41490-154">-Priority</span></span>
<span data-ttu-id="41490-155">Especifica a prioridade do trabalho.</span><span class="sxs-lookup"><span data-stu-id="41490-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="41490-156">Os valores válidos são: inteiros de -1000 a 1000.</span><span class="sxs-lookup"><span data-stu-id="41490-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="41490-157">Um valor de -1000 é a prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="41490-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="41490-158">Um valor de 1000 é a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="41490-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="41490-159">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="41490-159">The default value is 0.</span></span>

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

### <span data-ttu-id="41490-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="41490-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="41490-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41490-161">CommonParameters</span></span>
<span data-ttu-id="41490-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41490-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41490-163">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41490-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41490-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41490-164">INPUTS</span></span>

### <span data-ttu-id="41490-165">System.String</span><span class="sxs-lookup"><span data-stu-id="41490-165">System.String</span></span>

### <span data-ttu-id="41490-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="41490-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="41490-167">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="41490-167">OUTPUTS</span></span>

### <span data-ttu-id="41490-168">System.Void</span><span class="sxs-lookup"><span data-stu-id="41490-168">System.Void</span></span>

## <span data-ttu-id="41490-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="41490-169">NOTES</span></span>

## <span data-ttu-id="41490-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41490-170">RELATED LINKS</span></span>

[<span data-ttu-id="41490-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41490-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="41490-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41490-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="41490-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="41490-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="41490-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41490-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="41490-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="41490-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="41490-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41490-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="41490-177">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="41490-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="41490-178">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="41490-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
