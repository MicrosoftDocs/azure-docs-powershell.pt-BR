---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 92c485a743372eff7ddb8725172ac4d9bb030d22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610027"
---
# <span data-ttu-id="d3ff5-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="d3ff5-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="d3ff5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ff5-103">Obtém um arquivo de nó de lote.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3ff5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3ff5-104">SYNTAX</span></span>

### <span data-ttu-id="d3ff5-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="d3ff5-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3ff5-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="d3ff5-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3ff5-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="d3ff5-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3ff5-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="d3ff5-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3ff5-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="d3ff5-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3ff5-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="d3ff5-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3ff5-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3ff5-111">DESCRIPTION</span></span>
<span data-ttu-id="d3ff5-112">O cmdlet **Get-AzureBatchNodeFileContent** Obtém um arquivo de nó de lote do Azure e o salva como um arquivo ou em um Stream.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="d3ff5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3ff5-113">EXAMPLES</span></span>

### <span data-ttu-id="d3ff5-114">Exemplo 1: obter um arquivo de nó de lote associado a uma tarefa e salvar o arquivo</span><span class="sxs-lookup"><span data-stu-id="d3ff5-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Name "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="d3ff5-115">Esse comando obtém o arquivo de nó chamado StdOut.txt e salva-o no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="d3ff5-116">O arquivo de nó StdOut.txt está associado a uma tarefa que tem a ID Task01 para o trabalho que tem a ID Job01.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="d3ff5-117">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d3ff5-118">Exemplo 2: obter um arquivo de nó de lote e salvá-lo em um caminho de arquivo especificado usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d3ff5-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Name "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="d3ff5-119">Esse comando obtém o arquivo de nó chamado StdErr.txt usando o cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="d3ff5-120">O comando passa esse arquivo para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3ff5-121">O cmdlet atual salva esse arquivo no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="d3ff5-122">O arquivo de nó StdOut.txt está associado à tarefa que tem a ID Task02 para o trabalho que tem a ID Job02.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="d3ff5-123">Exemplo 3: obter um arquivo de nó de lote associado a uma tarefa e direcioná-lo a um fluxo</span><span class="sxs-lookup"><span data-stu-id="d3ff5-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Name "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="d3ff5-124">O primeiro comando cria um Stream usando o cmdlet New-Object e, em seguida, armazena-o na variável $Stream.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="d3ff5-125">O segundo comando obtém o arquivo de nó chamado StdOut.txt da tarefa que tem a ID Task11 para o trabalho que tem a ID Job03.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="d3ff5-126">O comando direciona o conteúdo do arquivo para o fluxo no $Stream.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="d3ff5-127">Exemplo 4: obter um arquivo de nó de um nó de computação e salvá-lo</span><span class="sxs-lookup"><span data-stu-id="d3ff5-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="d3ff5-128">Esse comando obtém o arquivo de nó Startup\StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="d3ff5-129">O comando salva o arquivo no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="d3ff5-130">Exemplo 5: obter um arquivo de nó de um nó de computação e salvá-lo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d3ff5-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="d3ff5-131">Esse comando obtém o arquivo de nó Startup\StdOut.txt usando Get-AzureBatchNodeFile do nó de computação que tem a ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="d3ff5-132">O nó de computação está no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="d3ff5-133">O comando passa esse arquivo de nó para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="d3ff5-134">Esse cmdlet salva o arquivo para o caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="d3ff5-135">Exemplo 6: obter um arquivo de nó de um nó de computação e direcioná-lo para um fluxo</span><span class="sxs-lookup"><span data-stu-id="d3ff5-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="d3ff5-136">O primeiro comando cria um Stream usando o cmdlet New-Object e, em seguida, armazena-o na variável $Stream.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="d3ff5-137">O segundo comando obtém o arquivo de nó chamado StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="d3ff5-138">O comando direciona o conteúdo do arquivo para o fluxo no $Stream.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="d3ff5-139">OS</span><span class="sxs-lookup"><span data-stu-id="d3ff5-139">PARAMETERS</span></span>

### <span data-ttu-id="d3ff5-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d3ff5-140">-BatchContext</span></span>
<span data-ttu-id="d3ff5-141">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d3ff5-142">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d3ff5-143">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="d3ff5-143">-ByteRangeEnd</span></span>
<span data-ttu-id="d3ff5-144">O final do intervalo de bytes a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-144">The end of the byte range to be downloaded.</span></span>
```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-145">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="d3ff5-145">-ByteRangeStart</span></span>
<span data-ttu-id="d3ff5-146">O início do intervalo de bytes a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-146">The start of the byte range to be downloaded.</span></span>
```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-147">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d3ff5-147">-ComputeNodeId</span></span>
<span data-ttu-id="d3ff5-148">Especifica a ID do nó de computação que contém o arquivo de nó que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-148">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-149">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="d3ff5-149">-DestinationPath</span></span>
<span data-ttu-id="d3ff5-150">Especifica o caminho do arquivo em que esse cmdlet salva o arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-150">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-151">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="d3ff5-151">-DestinationStream</span></span>
<span data-ttu-id="d3ff5-152">Especifica o fluxo em que esse cmdlet grava o conteúdo do arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-152">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="d3ff5-153">Esse cmdlet não fecha ou rebobina o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-153">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3ff5-154">-InputObject</span></span>
<span data-ttu-id="d3ff5-155">Especifica o arquivo que esse cmdlet obtém, como um objeto **PSNodeFile** .</span><span class="sxs-lookup"><span data-stu-id="d3ff5-155">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="d3ff5-156">Para obter um objeto de arquivo de nó, use o cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-156">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-157">-JobId</span><span class="sxs-lookup"><span data-stu-id="d3ff5-157">-JobId</span></span>
<span data-ttu-id="d3ff5-158">Especifica a ID do trabalho que contém a tarefa de destino.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-158">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3ff5-159">-Name</span></span>
<span data-ttu-id="d3ff5-160">Especifica o nome do arquivo de nó que este cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-160">Specifies the name of the node file that this cmdlet retrieves.</span></span>
<span data-ttu-id="d3ff5-161">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-161">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-162">-Poolid</span><span class="sxs-lookup"><span data-stu-id="d3ff5-162">-PoolId</span></span>
<span data-ttu-id="d3ff5-163">Especifica a ID do pool que contém o nó de computação que contém o arquivo de nó que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-163">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-164">-TaskId</span><span class="sxs-lookup"><span data-stu-id="d3ff5-164">-TaskId</span></span>
<span data-ttu-id="d3ff5-165">Especifica a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-165">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ff5-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ff5-166">-DefaultProfile</span></span>
<span data-ttu-id="d3ff5-167">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3ff5-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ff5-168">CommonParameters</span></span>
<span data-ttu-id="d3ff5-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ff5-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ff5-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ff5-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ff5-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3ff5-171">INPUTS</span></span>

### <span data-ttu-id="d3ff5-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d3ff5-172">BatchAccountContext</span></span>
<span data-ttu-id="d3ff5-173">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d3ff5-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d3ff5-174">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="d3ff5-174">PSNodeFile</span></span>
<span data-ttu-id="d3ff5-175">O parâmetro ' InputObject ' aceita o valor do tipo ' PSNodeFile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d3ff5-175">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="d3ff5-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3ff5-176">OUTPUTS</span></span>

## <span data-ttu-id="d3ff5-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3ff5-177">NOTES</span></span>

## <span data-ttu-id="d3ff5-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3ff5-178">RELATED LINKS</span></span>

[<span data-ttu-id="d3ff5-179">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d3ff5-179">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d3ff5-180">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="d3ff5-180">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="d3ff5-181">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="d3ff5-181">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


