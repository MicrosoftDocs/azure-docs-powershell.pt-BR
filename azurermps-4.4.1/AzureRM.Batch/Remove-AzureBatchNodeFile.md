---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431145"
---
# <span data-ttu-id="64173-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="64173-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="64173-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64173-102">SYNOPSIS</span></span>
<span data-ttu-id="64173-103">Exclui um arquivo de nó para uma tarefa ou um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="64173-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64173-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64173-104">SYNTAX</span></span>

### <span data-ttu-id="64173-105">Ela</span><span class="sxs-lookup"><span data-stu-id="64173-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64173-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="64173-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64173-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="64173-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64173-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64173-108">DESCRIPTION</span></span>
<span data-ttu-id="64173-109">O cmdlet **Remove-AzureBatchNodeFile** exclui um arquivo de nó de lote do Azure para uma tarefa ou um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="64173-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="64173-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64173-110">EXAMPLES</span></span>

### <span data-ttu-id="64173-111">Exemplo 1: excluir um arquivo assocated com uma tarefa</span><span class="sxs-lookup"><span data-stu-id="64173-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="64173-112">Esse comando exclui o arquivo de nó chamado wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="64173-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="64173-113">Esse arquivo está associado à tarefa que tem a ID Task26 sob o job job-000001.</span><span class="sxs-lookup"><span data-stu-id="64173-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="64173-114">Exemplo 2: excluir um arquivo de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="64173-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="64173-115">Esse comando exclui o arquivo de nó que é chamado startup\testFile.txt do nó de computação especificado no pool que tem a ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="64173-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="64173-116">Exemplo 3: remover um arquivo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="64173-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="64173-117">Esse comando obtém o arquivo de nó usando **Get-AzureBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="64173-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="64173-118">Esse arquivo está associado à tarefa que tem a ID Task26 sob o job job-000001.</span><span class="sxs-lookup"><span data-stu-id="64173-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="64173-119">O comando passa esse arquivo para o cmdlet atual usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="64173-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="64173-120">O cmdlet atual remove o arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="64173-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="64173-121">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="64173-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="64173-122">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="64173-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="64173-123">OS</span><span class="sxs-lookup"><span data-stu-id="64173-123">PARAMETERS</span></span>

### <span data-ttu-id="64173-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="64173-124">-BatchContext</span></span>
<span data-ttu-id="64173-125">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="64173-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="64173-126">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="64173-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="64173-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="64173-127">-ComputeNodeId</span></span>
<span data-ttu-id="64173-128">Especifica a ID do nó de computação que contém o arquivo de nó de lote que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="64173-128">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="64173-129">-Force</span><span class="sxs-lookup"><span data-stu-id="64173-129">-Force</span></span>
<span data-ttu-id="64173-130">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="64173-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64173-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64173-131">-InputObject</span></span>
<span data-ttu-id="64173-132">Especifica o objeto **PSNodeFile** que representa o arquivo de nó que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="64173-132">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="64173-133">Para obter um **PSNodeFile** , use o cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="64173-133">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="64173-134">-JobId</span><span class="sxs-lookup"><span data-stu-id="64173-134">-JobId</span></span>
<span data-ttu-id="64173-135">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="64173-135">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="64173-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="64173-136">-Name</span></span>
<span data-ttu-id="64173-137">Especifica o nome do arquivo de nó que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="64173-137">Specifies the name of the node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64173-138">-Poolid</span><span class="sxs-lookup"><span data-stu-id="64173-138">-PoolId</span></span>
<span data-ttu-id="64173-139">Especifica a ID do pool que contém os nós de computação para os quais esse cmdlet Remove um arquivo.</span><span class="sxs-lookup"><span data-stu-id="64173-139">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="64173-140">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="64173-140">-Recursive</span></span>
<span data-ttu-id="64173-141">Indica que esse cmdlet exclui a pasta e todas as subpastas e arquivos sob o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="64173-141">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="64173-142">Este cmdlet é relevante apenas se o caminho for uma pasta.</span><span class="sxs-lookup"><span data-stu-id="64173-142">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="64173-143">-TaskId</span><span class="sxs-lookup"><span data-stu-id="64173-143">-TaskId</span></span>
<span data-ttu-id="64173-144">Especifica a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="64173-144">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="64173-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64173-145">-Confirm</span></span>
<span data-ttu-id="64173-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64173-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64173-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64173-147">-WhatIf</span></span>
<span data-ttu-id="64173-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64173-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64173-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64173-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64173-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64173-150">-DefaultProfile</span></span>
<span data-ttu-id="64173-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64173-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64173-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64173-152">CommonParameters</span></span>
<span data-ttu-id="64173-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64173-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64173-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64173-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64173-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64173-155">INPUTS</span></span>

### <span data-ttu-id="64173-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="64173-156">BatchAccountContext</span></span>
<span data-ttu-id="64173-157">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="64173-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="64173-158">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="64173-158">PSNodeFile</span></span>
<span data-ttu-id="64173-159">O parâmetro ' InputObject ' aceita o valor do tipo ' PSNodeFile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="64173-159">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="64173-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64173-160">OUTPUTS</span></span>

## <span data-ttu-id="64173-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64173-161">NOTES</span></span>

## <span data-ttu-id="64173-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64173-162">RELATED LINKS</span></span>

[<span data-ttu-id="64173-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="64173-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="64173-164">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="64173-164">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="64173-165">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="64173-165">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


