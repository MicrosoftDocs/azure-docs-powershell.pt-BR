---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 1be012a9a9c5a62cbd08451849f8d50e9a5d52a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886394"
---
# <span data-ttu-id="801c2-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="801c2-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="801c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="801c2-102">SYNOPSIS</span></span>
<span data-ttu-id="801c2-103">Interrompe uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="801c2-103">Stops a copy operation.</span></span>

## <span data-ttu-id="801c2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="801c2-104">SYNTAX</span></span>

### <span data-ttu-id="801c2-105">NamePipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="801c2-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="801c2-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="801c2-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="801c2-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="801c2-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="801c2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="801c2-108">DESCRIPTION</span></span>
<span data-ttu-id="801c2-109">O cmdlet **Stop-AzStorageBlobCopy** interrompe uma operação de cópia para o blob de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="801c2-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="801c2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="801c2-110">EXAMPLES</span></span>

### <span data-ttu-id="801c2-111">Exemplo 1: Interromper a operação de cópia por nome</span><span class="sxs-lookup"><span data-stu-id="801c2-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="801c2-112">Este comando interrompe a operação de cópia por nome.</span><span class="sxs-lookup"><span data-stu-id="801c2-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="801c2-113">Exemplo 2: interromper a operação de cópia usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="801c2-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="801c2-114">Este comando interrompe a operação de cópia passando o contêiner no pipeline de **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="801c2-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="801c2-115">Exemplo 3: interromper a operação de cópia usando o pipeline e o Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="801c2-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="801c2-116">Este exemplo interrompe a operação de cópia passando o contêiner no pipeline Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="801c2-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="801c2-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="801c2-117">PARAMETERS</span></span>

### <span data-ttu-id="801c2-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="801c2-118">-Blob</span></span>
<span data-ttu-id="801c2-119">Especifica o nome do blob.</span><span class="sxs-lookup"><span data-stu-id="801c2-119">Specifies the name of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="801c2-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="801c2-121">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="801c2-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="801c2-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="801c2-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="801c2-123">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="801c2-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="801c2-124">-CloudBlob</span></span>
<span data-ttu-id="801c2-125">Especifica um **objeto CloudBlob** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="801c2-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="801c2-126">Para obter um **objeto CloudBlob,** use Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="801c2-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="801c2-127">-CloudBlobContainer</span></span>
<span data-ttu-id="801c2-128">Especifica um **objeto CloudBlobContainer** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="801c2-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="801c2-129">Você pode criar o objeto ou usar o Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="801c2-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="801c2-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="801c2-131">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="801c2-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="801c2-132">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="801c2-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="801c2-133">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="801c2-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="801c2-134">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="801c2-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="801c2-135">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="801c2-135">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-136">-Container</span><span class="sxs-lookup"><span data-stu-id="801c2-136">-Container</span></span>
<span data-ttu-id="801c2-137">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="801c2-137">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-138">-Context</span><span class="sxs-lookup"><span data-stu-id="801c2-138">-Context</span></span>
<span data-ttu-id="801c2-139">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="801c2-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="801c2-140">Você pode criar o contexto usando o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="801c2-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="801c2-141">-CopyId</span></span>
<span data-ttu-id="801c2-142">Especifica a ID da cópia.</span><span class="sxs-lookup"><span data-stu-id="801c2-142">Specifies the copy ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801c2-143">-DefaultProfile</span></span>
<span data-ttu-id="801c2-144">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="801c2-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-145">-Force</span><span class="sxs-lookup"><span data-stu-id="801c2-145">-Force</span></span>
<span data-ttu-id="801c2-146">Interrompe a tarefa de cópia atual no blob especificado sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="801c2-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="801c2-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="801c2-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="801c2-148">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="801c2-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="801c2-149">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="801c2-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="801c2-150">-Confirm</span></span>
<span data-ttu-id="801c2-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="801c2-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="801c2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="801c2-152">-WhatIf</span></span>
<span data-ttu-id="801c2-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="801c2-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="801c2-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="801c2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="801c2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801c2-155">CommonParameters</span></span>
<span data-ttu-id="801c2-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="801c2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801c2-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="801c2-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801c2-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="801c2-158">INPUTS</span></span>

### <span data-ttu-id="801c2-159">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="801c2-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="801c2-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="801c2-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="801c2-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="801c2-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="801c2-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="801c2-162">OUTPUTS</span></span>

### <span data-ttu-id="801c2-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="801c2-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="801c2-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="801c2-164">NOTES</span></span>

## <span data-ttu-id="801c2-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="801c2-165">RELATED LINKS</span></span>

[<span data-ttu-id="801c2-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="801c2-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="801c2-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="801c2-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="801c2-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="801c2-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="801c2-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="801c2-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
