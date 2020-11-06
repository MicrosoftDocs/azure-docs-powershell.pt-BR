---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 3d40a74af8b1f7b3dbb44a53d08b169501af704d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440126"
---
# <span data-ttu-id="71788-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="71788-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="71788-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71788-102">SYNOPSIS</span></span>
<span data-ttu-id="71788-103">Exclui um arquivo de nó para uma tarefa ou um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="71788-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71788-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71788-104">SYNTAX</span></span>

### <span data-ttu-id="71788-105">Ela</span><span class="sxs-lookup"><span data-stu-id="71788-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71788-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="71788-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71788-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="71788-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71788-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71788-108">DESCRIPTION</span></span>
<span data-ttu-id="71788-109">O cmdlet **Remove-AzureBatchNodeFile** exclui um arquivo de nó de lote do Azure para uma tarefa ou um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="71788-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="71788-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71788-110">EXAMPLES</span></span>

### <span data-ttu-id="71788-111">Exemplo 1: excluir um arquivo assocated com uma tarefa</span><span class="sxs-lookup"><span data-stu-id="71788-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="71788-112">Esse comando exclui o arquivo de nó chamado wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="71788-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="71788-113">Esse arquivo está associado à tarefa que tem a ID Task26 sob o job job-000001.</span><span class="sxs-lookup"><span data-stu-id="71788-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="71788-114">Exemplo 2: excluir um arquivo de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="71788-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="71788-115">Esse comando exclui o arquivo de nó que é chamado startup\testFile.txt do nó de computação especificado no pool que tem a ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="71788-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="71788-116">Exemplo 3: remover um arquivo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="71788-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="71788-117">Esse comando obtém o arquivo de nó usando **Get-AzureBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="71788-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="71788-118">Esse arquivo está associado à tarefa que tem a ID Task26 sob o job job-000001.</span><span class="sxs-lookup"><span data-stu-id="71788-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="71788-119">O comando passa esse arquivo para o cmdlet atual usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="71788-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="71788-120">O cmdlet atual remove o arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="71788-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="71788-121">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="71788-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="71788-122">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="71788-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="71788-123">OS</span><span class="sxs-lookup"><span data-stu-id="71788-123">PARAMETERS</span></span>

### <span data-ttu-id="71788-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="71788-124">-BatchContext</span></span>
<span data-ttu-id="71788-125">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="71788-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="71788-126">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="71788-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="71788-127">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="71788-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="71788-128">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="71788-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="71788-129">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="71788-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71788-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="71788-130">-ComputeNodeId</span></span>
<span data-ttu-id="71788-131">Especifica a ID do nó de computação que contém o arquivo de nó de lote que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="71788-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71788-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71788-132">-DefaultProfile</span></span>
<span data-ttu-id="71788-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71788-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71788-134">-Force</span><span class="sxs-lookup"><span data-stu-id="71788-134">-Force</span></span>
<span data-ttu-id="71788-135">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="71788-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71788-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71788-136">-InputObject</span></span>
<span data-ttu-id="71788-137">Especifica o objeto **PSNodeFile** que representa o arquivo de nó que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="71788-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="71788-138">Para obter um **PSNodeFile** , use o cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="71788-138">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: PSNodeFile
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71788-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="71788-139">-JobId</span></span>
<span data-ttu-id="71788-140">Especifica a ID do trabalho que contém a tarefa.</span><span class="sxs-lookup"><span data-stu-id="71788-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71788-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="71788-141">-Path</span></span>
<span data-ttu-id="71788-142">O caminho do arquivo do nó a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="71788-142">The file path of the node file to delete.</span></span>

```yaml
Type: String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71788-143">-Poolid</span><span class="sxs-lookup"><span data-stu-id="71788-143">-PoolId</span></span>
<span data-ttu-id="71788-144">Especifica a ID do pool que contém os nós de computação para os quais esse cmdlet Remove um arquivo.</span><span class="sxs-lookup"><span data-stu-id="71788-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71788-145">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="71788-145">-Recursive</span></span>
<span data-ttu-id="71788-146">Indica que esse cmdlet exclui a pasta e todas as subpastas e arquivos sob o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="71788-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="71788-147">Este cmdlet é relevante apenas se o caminho for uma pasta.</span><span class="sxs-lookup"><span data-stu-id="71788-147">This cmdlet is relevant only if the path is a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71788-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="71788-148">-TaskId</span></span>
<span data-ttu-id="71788-149">Especifica a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="71788-149">Specifies the ID of the task.</span></span>

```yaml
Type: String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71788-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71788-150">-Confirm</span></span>
<span data-ttu-id="71788-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71788-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71788-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71788-152">-WhatIf</span></span>
<span data-ttu-id="71788-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71788-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71788-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71788-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71788-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71788-155">CommonParameters</span></span>
<span data-ttu-id="71788-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71788-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71788-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71788-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71788-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71788-158">INPUTS</span></span>

### <span data-ttu-id="71788-159">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="71788-159">BatchAccountContext</span></span>
<span data-ttu-id="71788-160">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="71788-160">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="71788-161">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="71788-161">PSNodeFile</span></span>
<span data-ttu-id="71788-162">O parâmetro ' InputObject ' aceita o valor do tipo ' PSNodeFile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="71788-162">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="71788-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71788-163">OUTPUTS</span></span>

## <span data-ttu-id="71788-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71788-164">NOTES</span></span>

## <span data-ttu-id="71788-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71788-165">RELATED LINKS</span></span>

[<span data-ttu-id="71788-166">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="71788-166">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="71788-167">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="71788-167">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="71788-168">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="71788-168">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

