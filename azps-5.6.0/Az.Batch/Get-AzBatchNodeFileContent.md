---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 5790d217a63b7c2ef3aa7011d5f8a708df1dfbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889318"
---
# <span data-ttu-id="f51c2-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="f51c2-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="f51c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f51c2-102">SYNOPSIS</span></span>
<span data-ttu-id="f51c2-103">Obtém um arquivo de nó Batch.</span><span class="sxs-lookup"><span data-stu-id="f51c2-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="f51c2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f51c2-104">SYNTAX</span></span>

### <span data-ttu-id="f51c2-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="f51c2-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f51c2-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="f51c2-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f51c2-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="f51c2-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f51c2-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="f51c2-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f51c2-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="f51c2-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f51c2-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="f51c2-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f51c2-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f51c2-111">DESCRIPTION</span></span>
<span data-ttu-id="f51c2-112">O cmdlet **Get-AzBatchNodeFileContent** obtém um arquivo de nó do Lote do Azure e o salva como um arquivo ou em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="f51c2-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="f51c2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f51c2-113">EXAMPLES</span></span>

### <span data-ttu-id="f51c2-114">Exemplo 1: Obter um arquivo de nó Batch associado a uma tarefa e salvar o arquivo</span><span class="sxs-lookup"><span data-stu-id="f51c2-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f51c2-115">Esse comando obtém o arquivo de nó chamado StdOut.txt e o salva no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.</span><span class="sxs-lookup"><span data-stu-id="f51c2-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="f51c2-116">O StdOut.txt de nó está associado à tarefa que tem a ID Task01 para o trabalho que tem a ID Job01.</span><span class="sxs-lookup"><span data-stu-id="f51c2-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="f51c2-117">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="f51c2-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f51c2-118">Exemplo 2: Obter um arquivo de nó Batch e salvá-lo em um caminho de arquivo especificado usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="f51c2-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f51c2-119">Esse comando obtém o arquivo de nó chamado StdErr.txt usando o cmdlet Get-AzBatchNodeFile de usuário.</span><span class="sxs-lookup"><span data-stu-id="f51c2-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="f51c2-120">O comando passa esse arquivo para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f51c2-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f51c2-121">O cmdlet atual salva esse arquivo no E:\PowerShell\StdOut.txt de arquivo no computador local.</span><span class="sxs-lookup"><span data-stu-id="f51c2-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="f51c2-122">O StdOut.txt de nó está associado à tarefa que tem a ID Task02 para o trabalho que tem a ID Job02.</span><span class="sxs-lookup"><span data-stu-id="f51c2-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="f51c2-123">Exemplo 3: Obter um arquivo de nó Batch associado a uma tarefa e direciona-lo para um fluxo</span><span class="sxs-lookup"><span data-stu-id="f51c2-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="f51c2-124">O primeiro comando cria um fluxo usando o cmdlet New-Object e o armazena na variável $Stream.</span><span class="sxs-lookup"><span data-stu-id="f51c2-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="f51c2-125">O segundo comando obtém o arquivo de nó chamado StdOut.txt da tarefa que tem a ID Task11 para o trabalho que tem a ID Job03.</span><span class="sxs-lookup"><span data-stu-id="f51c2-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="f51c2-126">O comando direciona o conteúdo do arquivo para o fluxo em $Stream.</span><span class="sxs-lookup"><span data-stu-id="f51c2-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="f51c2-127">Exemplo 4: obter um arquivo de nó de um nó de computação e salvá-lo</span><span class="sxs-lookup"><span data-stu-id="f51c2-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f51c2-128">Este comando obtém o arquivo de nó Startup\StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="f51c2-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f51c2-129">O comando salva o arquivo no E:\PowerShell\StdOut.txt de arquivo no computador local.</span><span class="sxs-lookup"><span data-stu-id="f51c2-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="f51c2-130">Exemplo 5: obter um arquivo de nó de um nó de computação e salvá-lo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="f51c2-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f51c2-131">Esse comando obtém o arquivo de nó Startup\StdOut.txt usando Get-AzBatchNodeFile do nó de computação que tem a ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="f51c2-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="f51c2-132">O nó de computação está no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="f51c2-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f51c2-133">O comando passa esse arquivo de nó para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="f51c2-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="f51c2-134">Esse cmdlet salva o arquivo no E:\PowerShell\StdOut.txt de arquivo no computador local.</span><span class="sxs-lookup"><span data-stu-id="f51c2-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="f51c2-135">Exemplo 6: obter um arquivo de nó de um nó de computação e direciona-lo para um fluxo</span><span class="sxs-lookup"><span data-stu-id="f51c2-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="f51c2-136">O primeiro comando cria um fluxo usando o cmdlet New-Object e o armazena na variável $Stream.</span><span class="sxs-lookup"><span data-stu-id="f51c2-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="f51c2-137">O segundo comando obtém o arquivo de nó chamado StdOut.txt do nó de computação que tem o ID ComputeNode01 no pool que tem a ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="f51c2-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f51c2-138">O comando direciona o conteúdo do arquivo para o fluxo em $Stream.</span><span class="sxs-lookup"><span data-stu-id="f51c2-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="f51c2-139">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f51c2-139">PARAMETERS</span></span>

### <span data-ttu-id="f51c2-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f51c2-140">-BatchContext</span></span>
<span data-ttu-id="f51c2-141">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="f51c2-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f51c2-142">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="f51c2-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f51c2-143">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="f51c2-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f51c2-144">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="f51c2-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f51c2-145">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f51c2-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f51c2-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="f51c2-146">-ByteRangeEnd</span></span>
<span data-ttu-id="f51c2-147">O final do intervalo de byte a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="f51c2-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="f51c2-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="f51c2-148">-ByteRangeStart</span></span>
<span data-ttu-id="f51c2-149">O início do intervalo de byte a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="f51c2-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="f51c2-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="f51c2-150">-ComputeNodeId</span></span>
<span data-ttu-id="f51c2-151">Especifica a ID do nó de computação que contém o arquivo de nó que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="f51c2-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="f51c2-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f51c2-152">-DefaultProfile</span></span>
<span data-ttu-id="f51c2-153">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f51c2-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f51c2-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="f51c2-154">-DestinationPath</span></span>
<span data-ttu-id="f51c2-155">Especifica o caminho do arquivo onde esse cmdlet salva o arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="f51c2-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="f51c2-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="f51c2-156">-DestinationStream</span></span>
<span data-ttu-id="f51c2-157">Especifica o fluxo no qual esse cmdlet grava o conteúdo do arquivo de nó.</span><span class="sxs-lookup"><span data-stu-id="f51c2-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="f51c2-158">Este cmdlet não fecha nem rebobina esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="f51c2-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="f51c2-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f51c2-159">-InputObject</span></span>
<span data-ttu-id="f51c2-160">Especifica o arquivo que este cmdlet obtém, como um **objeto PSNodeFile.**</span><span class="sxs-lookup"><span data-stu-id="f51c2-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="f51c2-161">Para obter um objeto de arquivo de nó, use o cmdlet Get-AzBatchNodeFile nó.</span><span class="sxs-lookup"><span data-stu-id="f51c2-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="f51c2-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="f51c2-162">-JobId</span></span>
<span data-ttu-id="f51c2-163">Especifica a ID do trabalho que contém a tarefa de destino.</span><span class="sxs-lookup"><span data-stu-id="f51c2-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="f51c2-164">-Path</span><span class="sxs-lookup"><span data-stu-id="f51c2-164">-Path</span></span>
<span data-ttu-id="f51c2-165">O caminho do arquivo de nó a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="f51c2-165">The path of the node file to download.</span></span>

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

### <span data-ttu-id="f51c2-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f51c2-166">-PoolId</span></span>
<span data-ttu-id="f51c2-167">Especifica a ID do pool que contém o nó de computação que contém o arquivo de nó que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f51c2-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f51c2-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="f51c2-168">-TaskId</span></span>
<span data-ttu-id="f51c2-169">Especifica a ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f51c2-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="f51c2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51c2-170">CommonParameters</span></span>
<span data-ttu-id="f51c2-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f51c2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51c2-172">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f51c2-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51c2-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f51c2-173">INPUTS</span></span>

### <span data-ttu-id="f51c2-174">System.String</span><span class="sxs-lookup"><span data-stu-id="f51c2-174">System.String</span></span>

### <span data-ttu-id="f51c2-175">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="f51c2-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="f51c2-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f51c2-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f51c2-177">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f51c2-177">OUTPUTS</span></span>

### <span data-ttu-id="f51c2-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="f51c2-178">System.Void</span></span>

## <span data-ttu-id="f51c2-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="f51c2-179">NOTES</span></span>

## <span data-ttu-id="f51c2-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f51c2-180">RELATED LINKS</span></span>

[<span data-ttu-id="f51c2-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f51c2-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f51c2-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="f51c2-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="f51c2-183">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="f51c2-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
