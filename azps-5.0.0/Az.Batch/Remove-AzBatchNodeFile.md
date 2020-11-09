---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282082"
---
# <span data-ttu-id="993a0-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="993a0-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="993a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="993a0-102">SYNOPSIS</span></span>
<span data-ttu-id="993a0-103">Exclui um arquivo de nó para uma tarefa ou um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="993a0-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="993a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="993a0-104">SYNTAX</span></span>

### <span data-ttu-id="993a0-105">Ela</span><span class="sxs-lookup"><span data-stu-id="993a0-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="993a0-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="993a0-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="993a0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="993a0-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="993a0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="993a0-108">DESCRIPTION</span></span>
<span data-ttu-id="993a0-109">O cmdlet **Remove-AzBatchNodeFile** exclui um arquivo de nó de lote do Azure para uma tarefa ou um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="993a0-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="993a0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="993a0-110">EXAMPLES</span></span>

### <span data-ttu-id="993a0-111">Exemplo 1: excluir um arquivo associado a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="993a0-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="993a0-112">Esse comando exclui o arquivo de nó chamado wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="993a0-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="993a0-113">Esse arquivo está associado à tarefa que tem a ID Task26 sob o job job-000001.</span><span class="sxs-lookup"><span data-stu-id="993a0-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="993a0-114">Exemplo 2: excluir um arquivo de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="993a0-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="993a0-115">Esse comando exclui o arquivo de nó que é chamado startup\testFile.txt do nó de computação especificado no pool que tem a ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="993a0-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="993a0-116">Exemplo 3: remover um arquivo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="993a0-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="993a0-117">Esse comando obtém o arquivo de nó usando **Get-AzBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="993a0-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="993a0-118">Esse arquivo está associado à tarefa que tem a ID Task26 sob o job job-000001.</span><span class="sxs-lookup"><span data-stu-id="993a0-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="993a0-119">O comando passa esse arquivo para o cmdlet atual usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="993a0-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="993a0-120">O cmdlet atual remove o arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="993a0-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="993a0-121">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="993a0-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="993a0-122">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="993a0-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="993a0-123">OS</span><span class="sxs-lookup"><span data-stu-id="993a0-123">PARAMETERS</span></span>

### <span data-ttu-id="993a0-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="993a0-124">-BatchContext</span></span>
<span data-ttu-id="993a0-125">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="993a0-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="993a0-126">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="993a0-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="993a0-127">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="993a0-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="993a0-128">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="993a0-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="993a0-129">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="993a0-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="993a0-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="993a0-130">-ComputeNodeId</span></span>
<span data-ttu-id="993a0-131">Especifica a ID do nó de computação que contém o arquivo de nó de lote que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="993a0-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="993a0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993a0-132">-DefaultProfile</span></span>
<span data-ttu-id="993a0-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="993a0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="993a0-134">-Force</span><span class="sxs-lookup"><span data-stu-id="993a0-134">-Force</span></span>
<span data-ttu-id="993a0-135">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="993a0-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="993a0-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="993a0-136">-InputObject</span></span>
<span data-ttu-id="993a0-137">Especifica o objeto **PSNodeFile** que representa o arquivo de nó que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="993a0-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="993a0-138">Para obter um **PSNodeFile** , use o cmdlet Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="993a0-138">To obtain a **PSNodeFile** , use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="993a0-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="993a0-139">-JobId</span></span>
<span data-ttu-id="993a0-140">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="993a0-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="993a0-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="993a0-141">-Path</span></span>
<span data-ttu-id="993a0-142">O caminho do arquivo do nó a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="993a0-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="993a0-143">-Poolid</span><span class="sxs-lookup"><span data-stu-id="993a0-143">-PoolId</span></span>
<span data-ttu-id="993a0-144">Especifica a ID do pool que contém os nós de computação para os quais esse cmdlet Remove um arquivo.</span><span class="sxs-lookup"><span data-stu-id="993a0-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="993a0-145">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="993a0-145">-Recursive</span></span>
<span data-ttu-id="993a0-146">Indica que esse cmdlet exclui a pasta e todas as subpastas e arquivos sob o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="993a0-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="993a0-147">Este cmdlet é relevante apenas se o caminho for uma pasta.</span><span class="sxs-lookup"><span data-stu-id="993a0-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="993a0-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="993a0-148">-TaskId</span></span>
<span data-ttu-id="993a0-149">Especifica a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="993a0-149">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="993a0-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="993a0-150">-Confirm</span></span>
<span data-ttu-id="993a0-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="993a0-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="993a0-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="993a0-152">-WhatIf</span></span>
<span data-ttu-id="993a0-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="993a0-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="993a0-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="993a0-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="993a0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993a0-155">CommonParameters</span></span>
<span data-ttu-id="993a0-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="993a0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993a0-157">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="993a0-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993a0-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="993a0-158">INPUTS</span></span>

### <span data-ttu-id="993a0-159">System. String</span><span class="sxs-lookup"><span data-stu-id="993a0-159">System.String</span></span>

### <span data-ttu-id="993a0-160">Microsoft.Azure.Commands.Batch. Modelos. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="993a0-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="993a0-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="993a0-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="993a0-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="993a0-162">OUTPUTS</span></span>

### <span data-ttu-id="993a0-163">System. void</span><span class="sxs-lookup"><span data-stu-id="993a0-163">System.Void</span></span>

## <span data-ttu-id="993a0-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="993a0-164">NOTES</span></span>

## <span data-ttu-id="993a0-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="993a0-165">RELATED LINKS</span></span>

[<span data-ttu-id="993a0-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="993a0-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="993a0-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="993a0-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="993a0-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="993a0-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


