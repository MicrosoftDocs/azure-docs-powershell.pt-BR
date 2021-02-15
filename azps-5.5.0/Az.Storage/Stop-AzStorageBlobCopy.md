---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 979cfd1241910cb98bebee3b80bc0a1ab6b8da71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112501"
---
# <span data-ttu-id="03039-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="03039-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="03039-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03039-102">SYNOPSIS</span></span>
<span data-ttu-id="03039-103">Interrompe uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="03039-103">Stops a copy operation.</span></span>

## <span data-ttu-id="03039-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03039-104">SYNTAX</span></span>

### <span data-ttu-id="03039-105">NamePipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="03039-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03039-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="03039-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03039-107">ContainerLaline</span><span class="sxs-lookup"><span data-stu-id="03039-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03039-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="03039-108">DESCRIPTION</span></span>
<span data-ttu-id="03039-109">O cmdlet **Stop-AzStorageBcopy** interrompe uma operação de cópia para o blob de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="03039-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="03039-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="03039-110">EXAMPLES</span></span>

### <span data-ttu-id="03039-111">Exemplo 1: interromper a operação de cópia por nome</span><span class="sxs-lookup"><span data-stu-id="03039-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="03039-112">Esse comando interrompe a operação de cópia por nome.</span><span class="sxs-lookup"><span data-stu-id="03039-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="03039-113">Exemplo 2: interromper a operação de cópia usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="03039-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="03039-114">Esse comando interrompe a operação de cópia passando o contêiner no pipeline **do Get-AzStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="03039-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="03039-115">Exemplo 3: interromper a operação de cópia usando o pipeline e o Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="03039-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="03039-116">Este exemplo interrompe a operação de cópia passando o contêiner no pipeline Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03039-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="03039-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03039-117">PARAMETERS</span></span>

### <span data-ttu-id="03039-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="03039-118">-Blob</span></span>
<span data-ttu-id="03039-119">Especifica o nome do blob.</span><span class="sxs-lookup"><span data-stu-id="03039-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="03039-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03039-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="03039-121">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="03039-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="03039-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="03039-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="03039-123">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="03039-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="03039-124">-CloudBlab</span><span class="sxs-lookup"><span data-stu-id="03039-124">-CloudBlob</span></span>
<span data-ttu-id="03039-125">Especifica um objeto **CloudB object** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="03039-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="03039-126">Para obter um **objeto CloudB ltd,** use o cmdlet Get-AzStorageBlob nuvem.</span><span class="sxs-lookup"><span data-stu-id="03039-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="03039-127">-CloudBltContainer</span><span class="sxs-lookup"><span data-stu-id="03039-127">-CloudBlobContainer</span></span>
<span data-ttu-id="03039-128">Especifica um objeto **CloudBltContainer** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="03039-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="03039-129">Você pode criar o objeto ou usar o Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03039-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="03039-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="03039-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="03039-131">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="03039-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="03039-132">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="03039-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="03039-133">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="03039-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="03039-134">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="03039-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="03039-135">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="03039-135">The default value is 10.</span></span>

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

### <span data-ttu-id="03039-136">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="03039-136">-Container</span></span>
<span data-ttu-id="03039-137">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="03039-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="03039-138">-Contexto</span><span class="sxs-lookup"><span data-stu-id="03039-138">-Context</span></span>
<span data-ttu-id="03039-139">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="03039-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="03039-140">Você pode criar o contexto usando o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03039-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="03039-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="03039-141">-CopyId</span></span>
<span data-ttu-id="03039-142">Especifica a ID de cópia.</span><span class="sxs-lookup"><span data-stu-id="03039-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="03039-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03039-143">-DefaultProfile</span></span>
<span data-ttu-id="03039-144">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03039-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03039-145">-Forçar</span><span class="sxs-lookup"><span data-stu-id="03039-145">-Force</span></span>
<span data-ttu-id="03039-146">Interrompe a tarefa de cópia atual no blob especificado sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="03039-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="03039-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03039-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="03039-148">Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="03039-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="03039-149">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="03039-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="03039-150">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="03039-150">-Confirm</span></span>
<span data-ttu-id="03039-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03039-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03039-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03039-152">-WhatIf</span></span>
<span data-ttu-id="03039-153">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="03039-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03039-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03039-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03039-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03039-155">CommonParameters</span></span>
<span data-ttu-id="03039-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03039-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03039-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03039-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03039-158">Entradas</span><span class="sxs-lookup"><span data-stu-id="03039-158">INPUTS</span></span>

### <span data-ttu-id="03039-159">Microsoft.Azure.Storage.Blob.CloudBlab</span><span class="sxs-lookup"><span data-stu-id="03039-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="03039-160">Microsoft.Azure.Storage.Blob.CloudBltContainer</span><span class="sxs-lookup"><span data-stu-id="03039-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="03039-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="03039-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="03039-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="03039-162">OUTPUTS</span></span>

### <span data-ttu-id="03039-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlab</span><span class="sxs-lookup"><span data-stu-id="03039-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="03039-164">Notas</span><span class="sxs-lookup"><span data-stu-id="03039-164">NOTES</span></span>

## <span data-ttu-id="03039-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03039-165">RELATED LINKS</span></span>

[<span data-ttu-id="03039-166">Get-AzStorageB ltd</span><span class="sxs-lookup"><span data-stu-id="03039-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="03039-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="03039-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="03039-168">Start-AzStorageBcopy</span><span class="sxs-lookup"><span data-stu-id="03039-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="03039-169">Get-AzStorageBcopyState</span><span class="sxs-lookup"><span data-stu-id="03039-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
