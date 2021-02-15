---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 403bcc5a85001b6d98c67f91d995eb05bc948752
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112231"
---
# <span data-ttu-id="392e4-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="392e4-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="392e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="392e4-102">SYNOPSIS</span></span>
<span data-ttu-id="392e4-103">Carregue arquivos de log de serviço de nó de computação em um contêiner de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="392e4-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="392e4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="392e4-104">SYNTAX</span></span>

### <span data-ttu-id="392e4-105">AzureBatchComputeNodeServiceLogUpload (Padrão)</span><span class="sxs-lookup"><span data-stu-id="392e4-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="392e4-106">Id</span><span class="sxs-lookup"><span data-stu-id="392e4-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="392e4-107">Parentobject</span><span class="sxs-lookup"><span data-stu-id="392e4-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="392e4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="392e4-108">DESCRIPTION</span></span>
<span data-ttu-id="392e4-109">Este cmdlet reúne arquivos de log de serviço do Azure Batch de nós de computação se você estiver enfrentando um erro e deseja escalonar para o suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="392e4-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="392e4-110">Os arquivos de log de serviço do Azure Batch devem ser compartilhados com o suporte do Azure para auxiliar em problemas de depuração com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="392e4-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="392e4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="392e4-111">EXAMPLES</span></span>

### <span data-ttu-id="392e4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="392e4-112">Example 1</span></span>
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

<span data-ttu-id="392e4-113">Carregue logs de serviço de nó de computação escritos em ou após 1º de janeiro de 2018, que foram obtidos do nó de computação, uma ID do pool no qual o nó de computação reside e a ID do nó de computação.</span><span class="sxs-lookup"><span data-stu-id="392e4-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="392e4-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="392e4-114">Example 2</span></span>
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

<span data-ttu-id="392e4-115">Carregue logs de serviço de nó de computação escritos em ou após 1º de janeiro de 2018, meia-noite e antes de 10 de janeiro de 2018, que foram obtidos do nó de computação, com a ID do pool no qual o nó de computação reside e a ID do nó de computação.</span><span class="sxs-lookup"><span data-stu-id="392e4-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="392e4-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="392e4-116">Example 3</span></span>
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

<span data-ttu-id="392e4-117">Carregue logs de serviço de nó de computação escritos em ou após 1º de janeiro de 2018, meia-noite e antes de 10 de janeiro de 2018, que foram obtidos do objeto de nó de computação.</span><span class="sxs-lookup"><span data-stu-id="392e4-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="392e4-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="392e4-118">PARAMETERS</span></span>

### <span data-ttu-id="392e4-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="392e4-119">-BatchContext</span></span>
<span data-ttu-id="392e4-120">A instância BatchAccountContext a ser usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="392e4-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="392e4-121">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="392e4-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="392e4-122">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="392e4-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="392e4-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="392e4-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="392e4-124">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="392e4-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="392e4-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="392e4-125">-ComputeNode</span></span>
<span data-ttu-id="392e4-126">Especifica o **objeto PSComputeNode** a partir do qual logs de serviço são recuperados.</span><span class="sxs-lookup"><span data-stu-id="392e4-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

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

### <span data-ttu-id="392e4-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="392e4-127">-ComputeNodeId</span></span>
<span data-ttu-id="392e4-128">A iD do nó de computação.</span><span class="sxs-lookup"><span data-stu-id="392e4-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="392e4-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="392e4-129">-ContainerUrl</span></span>
<span data-ttu-id="392e4-130">A URL do contêiner para o Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="392e4-130">The container url to Azure Storage.</span></span>

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

### <span data-ttu-id="392e4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="392e4-131">-DefaultProfile</span></span>
<span data-ttu-id="392e4-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="392e4-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="392e4-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="392e4-133">-EndTime</span></span>
<span data-ttu-id="392e4-134">O horário de término do log de serviço a ser carregado (opcional).</span><span class="sxs-lookup"><span data-stu-id="392e4-134">The end time of service log to be uploaded (optional).</span></span>

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

### <span data-ttu-id="392e4-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="392e4-135">-PoolId</span></span>
<span data-ttu-id="392e4-136">A id do pool que contém o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="392e4-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="392e4-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="392e4-137">-StartTime</span></span>
<span data-ttu-id="392e4-138">A hora de início do log de serviço a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="392e4-138">The start time of service log to be uploaded.</span></span>

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

### <span data-ttu-id="392e4-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="392e4-139">-Confirm</span></span>
<span data-ttu-id="392e4-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="392e4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="392e4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="392e4-141">-WhatIf</span></span>
<span data-ttu-id="392e4-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="392e4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="392e4-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="392e4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="392e4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392e4-144">CommonParameters</span></span>
<span data-ttu-id="392e4-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="392e4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392e4-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="392e4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392e4-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="392e4-147">INPUTS</span></span>

### <span data-ttu-id="392e4-148">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="392e4-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="392e4-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="392e4-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="392e4-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="392e4-150">OUTPUTS</span></span>

### <span data-ttu-id="392e4-151">Microsoft.Azure.Commands.Batch. Models.PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="392e4-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="392e4-152">Notas</span><span class="sxs-lookup"><span data-stu-id="392e4-152">NOTES</span></span>

## <span data-ttu-id="392e4-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="392e4-153">RELATED LINKS</span></span>
