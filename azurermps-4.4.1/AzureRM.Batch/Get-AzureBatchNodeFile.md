---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: 0a027bd15d4b207baf9c69fcb9104428c2881872
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610029"
---
# <span data-ttu-id="c175d-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="c175d-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="c175d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c175d-102">SYNOPSIS</span></span>
<span data-ttu-id="c175d-103">Obtém as propriedades dos arquivos de nó de lote.</span><span class="sxs-lookup"><span data-stu-id="c175d-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c175d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c175d-104">SYNTAX</span></span>

### <span data-ttu-id="c175d-105">ComputeNode_Id (padrão)</span><span class="sxs-lookup"><span data-stu-id="c175d-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Name] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c175d-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="c175d-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Name] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c175d-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="c175d-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c175d-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="c175d-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c175d-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="c175d-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c175d-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="c175d-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c175d-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c175d-111">DESCRIPTION</span></span>
<span data-ttu-id="c175d-112">O cmdlet **Get-AzureBatchNodeFile** Obtém as propriedades dos arquivos de nó de lote do Azure de uma tarefa ou um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="c175d-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="c175d-113">Para restringir os resultados, você pode especificar um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="c175d-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="c175d-114">Se você especificar uma tarefa, mas não um filtro, esse cmdlet retornará Propriedades para todos os arquivos de nó dessa tarefa.</span><span class="sxs-lookup"><span data-stu-id="c175d-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="c175d-115">Se você especificar um nó de computação, mas não um filtro, esse cmdlet retornará Propriedades para todos os arquivos de nó desse nó de computação.</span><span class="sxs-lookup"><span data-stu-id="c175d-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="c175d-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c175d-116">EXAMPLES</span></span>

### <span data-ttu-id="c175d-117">Exemplo 1: obter as propriedades de um arquivo de nó associado a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="c175d-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="c175d-118">Esse comando obtém as propriedades do arquivo de nó StdOut.txt associado à tarefa com a ID Task26 no trabalho que tem o ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="c175d-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c175d-119">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="c175d-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c175d-120">Exemplo 2: obter as propriedades dos arquivos de nó associados a uma tarefa usando um filtro</span><span class="sxs-lookup"><span data-stu-id="c175d-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="c175d-121">Esse comando obtém as propriedades dos arquivos de nó cujos nomes começam com St e estão associados a Task com a ID Task26 em Job com o job ID-00002.</span><span class="sxs-lookup"><span data-stu-id="c175d-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="c175d-122">Exemplo 3: obter recursivamente as propriedades dos arquivos de nó associados a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="c175d-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
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

<span data-ttu-id="c175d-123">Esse comando obtém as propriedades de todos os arquivos associados à tarefa que tem a ID Task31 no trabalho da tarefa-00003.</span><span class="sxs-lookup"><span data-stu-id="c175d-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="c175d-124">Esse comando especifica o parâmetro *recursive* .</span><span class="sxs-lookup"><span data-stu-id="c175d-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="c175d-125">Portanto, o cmdlet executa uma pesquisa de arquivo recursiva é realizada e retorna o arquivo de nó wd\newFile.txt.</span><span class="sxs-lookup"><span data-stu-id="c175d-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="c175d-126">Exemplo 4: obter um único arquivo de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="c175d-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="c175d-127">Esse comando obtém o arquivo chamado Startup\StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="c175d-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="c175d-128">Exemplo 5: obter todos os arquivos em uma pasta a partir de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="c175d-128">Example 5: Get all files under a folder from a compute node</span></span>
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

<span data-ttu-id="c175d-129">Esse comando obtém todos os arquivos na pasta Startup do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="c175d-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="c175d-130">Esse cmdlet especifica o parâmetro *recursive* .</span><span class="sxs-lookup"><span data-stu-id="c175d-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="c175d-131">Exemplo 6: obter arquivos da pasta raiz de um nó de computação</span><span class="sxs-lookup"><span data-stu-id="c175d-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="c175d-132">Esse comando obtém todos os arquivos na pasta raiz do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="c175d-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="c175d-133">OS</span><span class="sxs-lookup"><span data-stu-id="c175d-133">PARAMETERS</span></span>

### <span data-ttu-id="c175d-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c175d-134">-BatchContext</span></span>
<span data-ttu-id="c175d-135">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c175d-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c175d-136">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="c175d-136">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c175d-137">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c175d-137">-ComputeNode</span></span>
<span data-ttu-id="c175d-138">Especifica o nó de computação, como um objeto **PSComputeNode** , que contém os arquivos de nó de lote.</span><span class="sxs-lookup"><span data-stu-id="c175d-138">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="c175d-139">Para obter um objeto do nó de computação, use o cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="c175d-139">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-140">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c175d-140">-ComputeNodeId</span></span>
<span data-ttu-id="c175d-141">Especifica a ID do nó de computação que contém os arquivos de nó de lote.</span><span class="sxs-lookup"><span data-stu-id="c175d-141">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-142">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c175d-142">-Filter</span></span>
<span data-ttu-id="c175d-143">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="c175d-143">Specifies an OData filter clause.</span></span>
<span data-ttu-id="c175d-144">Esse cmdlet retorna propriedades dos arquivos de nó que correspondem ao filtro especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c175d-144">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="c175d-145">-JobId</span></span>
<span data-ttu-id="c175d-146">Especifica a ID do trabalho que contém a tarefa de destino.</span><span class="sxs-lookup"><span data-stu-id="c175d-146">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c175d-147">-MaxCount</span></span>
<span data-ttu-id="c175d-148">Especifica o número máximo de arquivos de nó para os quais esse cmdlet retorna propriedades.</span><span class="sxs-lookup"><span data-stu-id="c175d-148">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="c175d-149">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="c175d-149">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c175d-150">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="c175d-150">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="c175d-151">-Name</span></span>
<span data-ttu-id="c175d-152">Especifica o nome do arquivo de nó para o qual esse cmdlet recupera propriedades.</span><span class="sxs-lookup"><span data-stu-id="c175d-152">Specifies the name of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="c175d-153">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="c175d-153">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-154">-Poolid</span><span class="sxs-lookup"><span data-stu-id="c175d-154">-PoolId</span></span>
<span data-ttu-id="c175d-155">Especifica a ID do pool que contém o nó de computação do qual obter propriedades de arquivos de nó.</span><span class="sxs-lookup"><span data-stu-id="c175d-155">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-156">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="c175d-156">-Recursive</span></span>
<span data-ttu-id="c175d-157">Indica que esse cmdlet retorna uma lista recursiva de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c175d-157">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="c175d-158">Caso contrário, ele retornará somente os arquivos na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="c175d-158">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-159">-Tarefa</span><span class="sxs-lookup"><span data-stu-id="c175d-159">-Task</span></span>
<span data-ttu-id="c175d-160">Especifica a tarefa, como um objeto **PSCloudTask** , com o qual os arquivos de nó estão associados.</span><span class="sxs-lookup"><span data-stu-id="c175d-160">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="c175d-161">Para obter um objeto Task, use o cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c175d-161">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-162">-TaskId</span><span class="sxs-lookup"><span data-stu-id="c175d-162">-TaskId</span></span>
<span data-ttu-id="c175d-163">Especifica a ID da tarefa para a qual esse cmdlet obtém Propriedades de arquivos de nó.</span><span class="sxs-lookup"><span data-stu-id="c175d-163">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c175d-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c175d-164">-DefaultProfile</span></span>
<span data-ttu-id="c175d-165">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c175d-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c175d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c175d-166">CommonParameters</span></span>
<span data-ttu-id="c175d-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c175d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c175d-168">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c175d-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c175d-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c175d-169">INPUTS</span></span>

### <span data-ttu-id="c175d-170">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c175d-170">BatchAccountContext</span></span>
<span data-ttu-id="c175d-171">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c175d-171">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c175d-172">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c175d-172">PSComputeNode</span></span>
<span data-ttu-id="c175d-173">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c175d-173">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="c175d-174">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c175d-174">PSCloudTask</span></span>
<span data-ttu-id="c175d-175">O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="c175d-175">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="c175d-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c175d-176">OUTPUTS</span></span>

### <span data-ttu-id="c175d-177">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="c175d-177">PSNodeFile</span></span>

## <span data-ttu-id="c175d-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c175d-178">NOTES</span></span>

## <span data-ttu-id="c175d-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c175d-179">RELATED LINKS</span></span>

[<span data-ttu-id="c175d-180">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c175d-180">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c175d-181">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c175d-181">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="c175d-182">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="c175d-182">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="c175d-183">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c175d-183">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="c175d-184">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="c175d-184">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


