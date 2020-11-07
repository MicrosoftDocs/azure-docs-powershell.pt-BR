---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 403bcc5a85001b6d98c67f91d995eb05bc948752
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942423"
---
# <span data-ttu-id="07e03-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="07e03-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="07e03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07e03-102">SYNOPSIS</span></span>
<span data-ttu-id="07e03-103">Carregue arquivos de log do serviço de nó de computação em um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="07e03-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="07e03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07e03-104">SYNTAX</span></span>

### <span data-ttu-id="07e03-105">AzureBatchComputeNodeServiceLogUpload (padrão)</span><span class="sxs-lookup"><span data-stu-id="07e03-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07e03-106">%</span><span class="sxs-lookup"><span data-stu-id="07e03-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07e03-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="07e03-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07e03-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07e03-108">DESCRIPTION</span></span>
<span data-ttu-id="07e03-109">Esse cmdlet coleta os arquivos de log do serviço em lotes do Azure a partir de nós de computação se você estiver apresentando um erro e quiser escalonar para o suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="07e03-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="07e03-110">Os arquivos de log do serviço em lotes do Azure devem ser compartilhados com o suporte do Azure para auxiliar na depuração de problemas com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="07e03-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="07e03-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07e03-111">EXAMPLES</span></span>

### <span data-ttu-id="07e03-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07e03-112">Example 1</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="07e03-113">Carregue os logs do serviço de nó de computação gravados em ou após 1º de janeiro de 2018, a meia-noite, que foi obtida do nó de computação, determinada ID de pool do pool no qual o nó de computação reside e o ID do nó de computação.</span><span class="sxs-lookup"><span data-stu-id="07e03-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="07e03-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="07e03-114">Example 2</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="07e03-115">Carregue os logs do serviço de nó de computação gravados em ou após 1º de janeiro de 2018 e antes de 10 de janeiro de 2018 $ meia-noite, que foram obtidos do nó de computação, o ID de pool fornecido no qual o nó de computação reside e o ID do nó de computação.</span><span class="sxs-lookup"><span data-stu-id="07e03-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="07e03-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="07e03-116">Example 3</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="07e03-117">Carregue os logs do serviço de nó de computação gravados em ou após 1º de janeiro de 2018 e antes de 10 de janeiro de 2018 $ meia-noite, que foram obtidos do objeto do nó de computação.</span><span class="sxs-lookup"><span data-stu-id="07e03-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="07e03-118">OS</span><span class="sxs-lookup"><span data-stu-id="07e03-118">PARAMETERS</span></span>

### <span data-ttu-id="07e03-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="07e03-119">-BatchContext</span></span>
<span data-ttu-id="07e03-120">A instância BatchAccountContext a ser usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="07e03-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="07e03-121">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="07e03-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="07e03-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="07e03-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="07e03-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="07e03-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="07e03-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="07e03-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="07e03-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="07e03-125">-ComputeNode</span></span>
<span data-ttu-id="07e03-126">Especifica o objeto **PSComputeNode** a partir do qual os logs de serviço são recuperados.</span><span class="sxs-lookup"><span data-stu-id="07e03-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07e03-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="07e03-127">-ComputeNodeId</span></span>
<span data-ttu-id="07e03-128">A ID do nó de computação.</span><span class="sxs-lookup"><span data-stu-id="07e03-128">The id of the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e03-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="07e03-129">-ContainerUrl</span></span>
<span data-ttu-id="07e03-130">A URL do contêiner para o armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="07e03-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e03-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e03-131">-DefaultProfile</span></span>
<span data-ttu-id="07e03-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07e03-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07e03-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="07e03-133">-EndTime</span></span>
<span data-ttu-id="07e03-134">A hora de término do log de serviço a ser carregada (opcional).</span><span class="sxs-lookup"><span data-stu-id="07e03-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e03-135">-Poolid</span><span class="sxs-lookup"><span data-stu-id="07e03-135">-PoolId</span></span>
<span data-ttu-id="07e03-136">A ID do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="07e03-136">The id of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e03-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="07e03-137">-StartTime</span></span>
<span data-ttu-id="07e03-138">A hora de início do log de serviço a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="07e03-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e03-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07e03-139">-Confirm</span></span>
<span data-ttu-id="07e03-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e03-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e03-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07e03-141">-WhatIf</span></span>
<span data-ttu-id="07e03-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07e03-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07e03-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07e03-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e03-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e03-144">CommonParameters</span></span>
<span data-ttu-id="07e03-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e03-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e03-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07e03-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e03-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07e03-147">INPUTS</span></span>

### <span data-ttu-id="07e03-148">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="07e03-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="07e03-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="07e03-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="07e03-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07e03-150">OUTPUTS</span></span>

### <span data-ttu-id="07e03-151">Microsoft.Azure.Commands.Batch. Modelos. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="07e03-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="07e03-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07e03-152">NOTES</span></span>

## <span data-ttu-id="07e03-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07e03-153">RELATED LINKS</span></span>
