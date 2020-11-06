---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: ac9a49b52dd2fecea12e3084e4d86077ddb06cb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431729"
---
# <span data-ttu-id="28be8-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="28be8-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="28be8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28be8-102">SYNOPSIS</span></span>
<span data-ttu-id="28be8-103">Obtém as propriedades dos arquivos de nó de lote.</span><span class="sxs-lookup"><span data-stu-id="28be8-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28be8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28be8-104">SYNTAX</span></span>

### <span data-ttu-id="28be8-105">ComputeNode_Id (padrão)</span><span class="sxs-lookup"><span data-stu-id="28be8-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28be8-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="28be8-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28be8-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="28be8-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28be8-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="28be8-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28be8-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="28be8-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28be8-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="28be8-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28be8-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28be8-111">DESCRIPTION</span></span>
<span data-ttu-id="28be8-112">O cmdlet **Get-AzureBatchNodeFile** Obtém as propriedades dos arquivos de nó de lote do Azure de uma tarefa ou um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="28be8-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="28be8-113">Para restringir os resultados, você pode especificar um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="28be8-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="28be8-114">Se você especificar uma tarefa, mas não um filtro, esse cmdlet retornará Propriedades para todos os arquivos de nó dessa tarefa.</span><span class="sxs-lookup"><span data-stu-id="28be8-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="28be8-115">Se você especificar um nó de computação, mas não um filtro, esse cmdlet retornará Propriedades para todos os arquivos de nó desse nó de computação.</span><span class="sxs-lookup"><span data-stu-id="28be8-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="28be8-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28be8-116">EXAMPLES</span></span>

### <span data-ttu-id="28be8-117">Exemplo 1: obter as propriedades de um arquivo de nó associado a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="28be8-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="28be8-118">Esse comando obtém as propriedades do arquivo de nó StdOut.txt associado à tarefa com a ID Task26 no trabalho que tem o ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="28be8-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="28be8-119">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="28be8-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="28be8-120">Exemplo 2: obter as propriedades dos arquivos de nó associados a uma tarefa usando um filtro</span><span class="sxs-lookup"><span data-stu-id="28be8-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="28be8-121">Esse comando obtém as propriedades dos arquivos de nó cujos nomes começam com St e estão associados a Task com a ID Task26 em Job com o job ID-00002.</span><span class="sxs-lookup"><span data-stu-id="28be8-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="28be8-122">Exemplo 3: obter recursivamente as propriedades dos arquivos de nó associados a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="28be8-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="28be8-123">Esse comando obtém as propriedades de todos os arquivos associados à tarefa que tem a ID Task31 no trabalho da tarefa-00003.</span><span class="sxs-lookup"><span data-stu-id="28be8-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="28be8-124">Esse comando especifica o parâmetro *recursive* .</span><span class="sxs-lookup"><span data-stu-id="28be8-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="28be8-125">Portanto, o cmdlet executa uma pesquisa de arquivo recursiva é realizada e retorna o arquivo de nó wd\newFile.txt.</span><span class="sxs-lookup"><span data-stu-id="28be8-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="28be8-126">Exemplo 4: obter um único arquivo de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="28be8-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="28be8-127">Esse comando obtém o arquivo chamado Startup\StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="28be8-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="28be8-128">Exemplo 5: obter todos os arquivos em uma pasta a partir de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="28be8-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="28be8-129">Esse comando obtém todos os arquivos na pasta Startup do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="28be8-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="28be8-130">Esse cmdlet especifica o parâmetro *recursive* .</span><span class="sxs-lookup"><span data-stu-id="28be8-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="28be8-131">Exemplo 6: obter arquivos da pasta raiz de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="28be8-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="28be8-132">Esse comando obtém todos os arquivos na pasta raiz do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="28be8-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="28be8-133">OS</span><span class="sxs-lookup"><span data-stu-id="28be8-133">PARAMETERS</span></span>

### <span data-ttu-id="28be8-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="28be8-134">-BatchContext</span></span>
<span data-ttu-id="28be8-135">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="28be8-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="28be8-136">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="28be8-136">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="28be8-137">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="28be8-137">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="28be8-138">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="28be8-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="28be8-139">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="28be8-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="28be8-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="28be8-140">-ComputeNode</span></span>
<span data-ttu-id="28be8-141">Especifica o nó de computação, como um objeto **PSComputeNode** , que contém os arquivos de nó de lote.</span><span class="sxs-lookup"><span data-stu-id="28be8-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="28be8-142">Para obter um objeto do nó de computação, use o cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="28be8-142">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: ParentComputeNode
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="28be8-143">-ComputeNodeId</span></span>
<span data-ttu-id="28be8-144">Especifica a ID do nó de computação que contém os arquivos de nó de lote.</span><span class="sxs-lookup"><span data-stu-id="28be8-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28be8-145">-DefaultProfile</span></span>
<span data-ttu-id="28be8-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28be8-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28be8-147">-Filtro</span><span class="sxs-lookup"><span data-stu-id="28be8-147">-Filter</span></span>
<span data-ttu-id="28be8-148">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="28be8-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="28be8-149">Esse cmdlet retorna propriedades dos arquivos de nó que correspondem ao filtro especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="28be8-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="28be8-150">-JobId</span></span>
<span data-ttu-id="28be8-151">Especifica a ID do trabalho que contém a tarefa de destino.</span><span class="sxs-lookup"><span data-stu-id="28be8-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="28be8-152">-MaxCount</span></span>
<span data-ttu-id="28be8-153">Especifica o número máximo de arquivos de nó para os quais esse cmdlet retorna propriedades.</span><span class="sxs-lookup"><span data-stu-id="28be8-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="28be8-154">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="28be8-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="28be8-155">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="28be8-155">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-156">-Caminho</span><span class="sxs-lookup"><span data-stu-id="28be8-156">-Path</span></span>
<span data-ttu-id="28be8-157">Especifica o caminho do arquivo de nó para o qual esse cmdlet recupera propriedades.</span><span class="sxs-lookup"><span data-stu-id="28be8-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="28be8-158">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="28be8-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-159">-Poolid</span><span class="sxs-lookup"><span data-stu-id="28be8-159">-PoolId</span></span>
<span data-ttu-id="28be8-160">Especifica a ID do pool que contém o nó de computação do qual obter propriedades de arquivos de nó.</span><span class="sxs-lookup"><span data-stu-id="28be8-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-161">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="28be8-161">-Recursive</span></span>
<span data-ttu-id="28be8-162">Indica que esse cmdlet retorna uma lista recursiva de arquivos.</span><span class="sxs-lookup"><span data-stu-id="28be8-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="28be8-163">Caso contrário, ele retornará somente os arquivos na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="28be8-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-164">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="28be8-164">-Task</span></span>
<span data-ttu-id="28be8-165">Especifica a tarefa, como um objeto **PSCloudTask** , com o qual os arquivos de nó estão associados.</span><span class="sxs-lookup"><span data-stu-id="28be8-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="28be8-166">Para obter um objeto Task, use o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="28be8-166">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: ParentTask
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="28be8-167">-TaskId</span></span>
<span data-ttu-id="28be8-168">Especifica a ID da tarefa para a qual esse cmdlet obtém Propriedades de arquivos de nó.</span><span class="sxs-lookup"><span data-stu-id="28be8-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28be8-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28be8-169">CommonParameters</span></span>
<span data-ttu-id="28be8-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28be8-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28be8-171">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28be8-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28be8-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28be8-172">INPUTS</span></span>

### <span data-ttu-id="28be8-173">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="28be8-173">BatchAccountContext</span></span>
<span data-ttu-id="28be8-174">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="28be8-174">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="28be8-175">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="28be8-175">PSComputeNode</span></span>
<span data-ttu-id="28be8-176">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="28be8-176">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="28be8-177">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="28be8-177">PSCloudTask</span></span>
<span data-ttu-id="28be8-178">O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="28be8-178">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="28be8-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28be8-179">OUTPUTS</span></span>

### <span data-ttu-id="28be8-180">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="28be8-180">PSNodeFile</span></span>

## <span data-ttu-id="28be8-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28be8-181">NOTES</span></span>

## <span data-ttu-id="28be8-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28be8-182">RELATED LINKS</span></span>

[<span data-ttu-id="28be8-183">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="28be8-183">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="28be8-184">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="28be8-184">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="28be8-185">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="28be8-185">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="28be8-186">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="28be8-186">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="28be8-187">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="28be8-187">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

