---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281684"
---
# <span data-ttu-id="8e831-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="8e831-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="8e831-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e831-102">SYNOPSIS</span></span>
<span data-ttu-id="8e831-103">Obtém um arquivo RDP de um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="8e831-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="8e831-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e831-104">SYNTAX</span></span>

### <span data-ttu-id="8e831-105">Id_Path (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e831-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e831-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="8e831-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e831-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="8e831-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e831-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="8e831-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e831-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e831-109">DESCRIPTION</span></span>
<span data-ttu-id="8e831-110">O cmdlet **Get-AzBatchRemoteDesktopProtocolFile** Obtém um arquivo RDP (protocolo de área de trabalho remota) de um nó de computação e salva-o como um arquivo ou um fluxo fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8e831-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="8e831-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e831-111">EXAMPLES</span></span>

### <span data-ttu-id="8e831-112">Exemplo 1: obter um arquivo RDP de um nó de computação especificado e salvar o arquivo</span><span class="sxs-lookup"><span data-stu-id="8e831-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="8e831-113">Esse comando obtém um arquivo RDP do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="8e831-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="8e831-114">O comando salva o arquivo. rdp como C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="8e831-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="8e831-115">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="8e831-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8e831-116">Exemplo 2: obter um arquivo RDP de um nó de computação e salvar o arquivo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="8e831-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="8e831-117">Esse comando obtém o nó de computação que tem a ID ComputeNode02 no pool que tem a ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="8e831-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="8e831-118">O comando passa aquele nó COMPUTE para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e831-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e831-119">O cmdlet atual Obtém um arquivo. RPD do nó de computação e, em seguida, salva o conteúdo como um arquivo chamado C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="8e831-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="8e831-120">Exemplo 3: obter um arquivo RDP de um nó de computação especificado e direcioná-lo para um fluxo</span><span class="sxs-lookup"><span data-stu-id="8e831-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="8e831-121">O primeiro comando cria um Stream usando o cmdlet New-Object e, em seguida, armazena-o na variável $Stream.</span><span class="sxs-lookup"><span data-stu-id="8e831-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="8e831-122">O segundo comando obtém um arquivo. rdp do nó de computação que tem a ID ComputeNode03 no pool que tem a ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="8e831-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="8e831-123">O comando direciona o conteúdo do arquivo para o fluxo no $Stream.</span><span class="sxs-lookup"><span data-stu-id="8e831-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="8e831-124">OS</span><span class="sxs-lookup"><span data-stu-id="8e831-124">PARAMETERS</span></span>

### <span data-ttu-id="8e831-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8e831-125">-BatchContext</span></span>
<span data-ttu-id="8e831-126">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8e831-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e831-127">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8e831-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8e831-128">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="8e831-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8e831-129">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="8e831-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8e831-130">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8e831-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8e831-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e831-131">-ComputeNode</span></span>
<span data-ttu-id="8e831-132">Especifica um nó de computação, como um objeto **PSComputeNode** , ao qual o arquivo. rdp aponta.</span><span class="sxs-lookup"><span data-stu-id="8e831-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="8e831-133">Para obter um objeto do nó de computação, use o cmdlet Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="8e831-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e831-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="8e831-134">-ComputeNodeId</span></span>
<span data-ttu-id="8e831-135">Especifica a ID do nó de computação para o qual o arquivo. rdp aponta.</span><span class="sxs-lookup"><span data-stu-id="8e831-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e831-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e831-136">-DefaultProfile</span></span>
<span data-ttu-id="8e831-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e831-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e831-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="8e831-138">-DestinationPath</span></span>
<span data-ttu-id="8e831-139">Especifica o caminho do arquivo em que esse cmdlet salva o arquivo. rdp.</span><span class="sxs-lookup"><span data-stu-id="8e831-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e831-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="8e831-140">-DestinationStream</span></span>
<span data-ttu-id="8e831-141">Especifica o fluxo em que esse cmdlet direciona os dados RDP.</span><span class="sxs-lookup"><span data-stu-id="8e831-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="8e831-142">Esse cmdlet não fecha ou rebobina o fluxo.</span><span class="sxs-lookup"><span data-stu-id="8e831-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e831-143">-Poolid</span><span class="sxs-lookup"><span data-stu-id="8e831-143">-PoolId</span></span>
<span data-ttu-id="8e831-144">Especifica a ID do pool que contém o nó de computação do qual esse cmdlet obtém um arquivo. rdp.</span><span class="sxs-lookup"><span data-stu-id="8e831-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e831-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e831-145">CommonParameters</span></span>
<span data-ttu-id="8e831-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e831-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e831-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e831-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e831-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e831-148">INPUTS</span></span>

### <span data-ttu-id="8e831-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8e831-149">System.String</span></span>

### <span data-ttu-id="8e831-150">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e831-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="8e831-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e831-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e831-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e831-152">OUTPUTS</span></span>

### <span data-ttu-id="8e831-153">System. void</span><span class="sxs-lookup"><span data-stu-id="8e831-153">System.Void</span></span>

## <span data-ttu-id="8e831-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e831-154">NOTES</span></span>

## <span data-ttu-id="8e831-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e831-155">RELATED LINKS</span></span>

[<span data-ttu-id="8e831-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8e831-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8e831-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e831-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="8e831-158">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="8e831-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
