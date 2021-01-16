---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259172"
---
# <span data-ttu-id="a285a-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="a285a-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="a285a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a285a-102">SYNOPSIS</span></span>
<span data-ttu-id="a285a-103">Obtém um arquivo de nó de lote.</span><span class="sxs-lookup"><span data-stu-id="a285a-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="a285a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a285a-104">SYNTAX</span></span>

### <span data-ttu-id="a285a-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="a285a-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a285a-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="a285a-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a285a-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="a285a-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a285a-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="a285a-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a285a-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="a285a-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a285a-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="a285a-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a285a-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a285a-111">DESCRIPTION</span></span>
<span data-ttu-id="a285a-112">O cmdlet **Get-AzBatchNodeFileContent** Obtém um arquivo de nó de lote do Azure e o salva como um arquivo ou em um Stream.</span><span class="sxs-lookup"><span data-stu-id="a285a-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="a285a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a285a-113">EXAMPLES</span></span>

### <span data-ttu-id="a285a-114">Exemplo 1: obter um arquivo de nó de lote associado a uma tarefa e salvar o arquivo</span><span class="sxs-lookup"><span data-stu-id="a285a-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a285a-115">Esse comando obtém o arquivo de nó chamado StdOut.txt e salva-o no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="a285a-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="a285a-116">O arquivo de nó StdOut.txt está associado a uma tarefa que tem a ID Task01 para o trabalho que tem a ID Job01.</span><span class="sxs-lookup"><span data-stu-id="a285a-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="a285a-117">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="a285a-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a285a-118">Exemplo 2: obter um arquivo de nó de lote e salvá-lo em um caminho de arquivo especificado usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="a285a-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a285a-119">Esse comando obtém o arquivo de nó chamado StdErr.txt usando o cmdlet Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="a285a-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="a285a-120">O comando passa esse arquivo para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="a285a-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a285a-121">O cmdlet atual salva esse arquivo no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="a285a-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="a285a-122">O arquivo de nó StdOut.txt está associado à tarefa que tem a ID Task02 para o trabalho que tem a ID Job02.</span><span class="sxs-lookup"><span data-stu-id="a285a-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="a285a-123">Exemplo 3: obter um arquivo de nó de lote associado a uma tarefa e direcioná-lo a um fluxo</span><span class="sxs-lookup"><span data-stu-id="a285a-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="a285a-124">O primeiro comando cria um Stream usando o cmdlet New-Object e, em seguida, armazena-o na variável $Stream.</span><span class="sxs-lookup"><span data-stu-id="a285a-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="a285a-125">O segundo comando obtém o arquivo de nó chamado StdOut.txt da tarefa que tem a ID Task11 para o trabalho que tem a ID Job03.</span><span class="sxs-lookup"><span data-stu-id="a285a-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="a285a-126">O comando direciona o conteúdo do arquivo para o fluxo no $Stream.</span><span class="sxs-lookup"><span data-stu-id="a285a-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="a285a-127">Exemplo 4: obter um arquivo de nó de um nó de computação e salvá-lo</span><span class="sxs-lookup"><span data-stu-id="a285a-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a285a-128">Esse comando obtém o arquivo de nó Startup\StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="a285a-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a285a-129">O comando salva o arquivo no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="a285a-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="a285a-130">Exemplo 5: obter um arquivo de nó de um nó de computação e salvá-lo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="a285a-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a285a-131">Esse comando obtém o arquivo de nó Startup\StdOut.txt usando Get-AzBatchNodeFile do nó de computação que tem a ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="a285a-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="a285a-132">O nó de computação está no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="a285a-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a285a-133">O comando passa esse arquivo de nó para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="a285a-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="a285a-134">Esse cmdlet salva o arquivo para o caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="a285a-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="a285a-135">Exemplo 6: obter um arquivo de nó de um nó de computação e direcioná-lo para um fluxo</span><span class="sxs-lookup"><span data-stu-id="a285a-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="a285a-136">O primeiro comando cria um Stream usando o cmdlet New-Object e, em seguida, armazena-o na variável $Stream.</span><span class="sxs-lookup"><span data-stu-id="a285a-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="a285a-137">O segundo comando obtém o arquivo de nó chamado StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="a285a-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a285a-138">O comando direciona o conteúdo do arquivo para o fluxo no $Stream.</span><span class="sxs-lookup"><span data-stu-id="a285a-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="a285a-139">OS</span><span class="sxs-lookup"><span data-stu-id="a285a-139">PARAMETERS</span></span>

### <span data-ttu-id="a285a-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a285a-140">-BatchContext</span></span>
<span data-ttu-id="a285a-141">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="a285a-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a285a-142">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="a285a-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a285a-143">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="a285a-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a285a-144">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="a285a-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a285a-145">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a285a-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a285a-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="a285a-146">-ByteRangeEnd</span></span>
<span data-ttu-id="a285a-147">O final do intervalo de bytes a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="a285a-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="a285a-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="a285a-148">-ByteRangeStart</span></span>
<span data-ttu-id="a285a-149">O início do intervalo de bytes a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="a285a-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="a285a-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="a285a-150">-ComputeNodeId</span></span>
<span data-ttu-id="a285a-151">Especifica a ID do nó de computação que contém o arquivo de nó que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="a285a-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="a285a-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a285a-152">-DefaultProfile</span></span>
<span data-ttu-id="a285a-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a285a-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a285a-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="a285a-154">-DestinationPath</span></span>
<span data-ttu-id="a285a-155">Especifica o caminho do arquivo em que esse cmdlet salva o arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="a285a-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="a285a-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="a285a-156">-DestinationStream</span></span>
<span data-ttu-id="a285a-157">Especifica o fluxo em que esse cmdlet grava o conteúdo do arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="a285a-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="a285a-158">Esse cmdlet não fecha ou rebobina o fluxo.</span><span class="sxs-lookup"><span data-stu-id="a285a-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="a285a-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a285a-159">-InputObject</span></span>
<span data-ttu-id="a285a-160">Especifica o arquivo que esse cmdlet obtém, como um objeto **PSNodeFile** .</span><span class="sxs-lookup"><span data-stu-id="a285a-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="a285a-161">Para obter um objeto de arquivo de nó, use o cmdlet Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="a285a-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="a285a-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="a285a-162">-JobId</span></span>
<span data-ttu-id="a285a-163">Especifica a ID do trabalho que contém a tarefa de destino.</span><span class="sxs-lookup"><span data-stu-id="a285a-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="a285a-164">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a285a-164">-Path</span></span>
<span data-ttu-id="a285a-165">O caminho do arquivo de nó a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="a285a-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a285a-166">-Poolid</span><span class="sxs-lookup"><span data-stu-id="a285a-166">-PoolId</span></span>
<span data-ttu-id="a285a-167">Especifica a ID do pool que contém o nó de computação que contém o arquivo de nó que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a285a-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a285a-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="a285a-168">-TaskId</span></span>
<span data-ttu-id="a285a-169">Especifica a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a285a-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="a285a-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a285a-170">CommonParameters</span></span>
<span data-ttu-id="a285a-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a285a-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a285a-172">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a285a-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a285a-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a285a-173">INPUTS</span></span>

### <span data-ttu-id="a285a-174">System. String</span><span class="sxs-lookup"><span data-stu-id="a285a-174">System.String</span></span>

### <span data-ttu-id="a285a-175">Microsoft.Azure.Commands.Batch. Modelos. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="a285a-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="a285a-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a285a-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a285a-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a285a-177">OUTPUTS</span></span>

### <span data-ttu-id="a285a-178">System. void</span><span class="sxs-lookup"><span data-stu-id="a285a-178">System.Void</span></span>

## <span data-ttu-id="a285a-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a285a-179">NOTES</span></span>

## <span data-ttu-id="a285a-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a285a-180">RELATED LINKS</span></span>

[<span data-ttu-id="a285a-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a285a-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a285a-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="a285a-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="a285a-183">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="a285a-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
