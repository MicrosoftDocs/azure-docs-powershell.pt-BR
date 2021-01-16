---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426714"
---
# <span data-ttu-id="1cb53-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="1cb53-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="1cb53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cb53-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb53-103">Obtém o status da cópia de um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb53-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="1cb53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cb53-104">SYNTAX</span></span>

### <span data-ttu-id="1cb53-105">NamePipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="1cb53-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1cb53-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="1cb53-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1cb53-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="1cb53-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1cb53-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cb53-108">DESCRIPTION</span></span>
<span data-ttu-id="1cb53-109">O cmdlet **Get-AzStorageBlobCopyState** Obtém o status da cópia de um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb53-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="1cb53-110">Ele deve ser executado no blob de destino da cópia.</span><span class="sxs-lookup"><span data-stu-id="1cb53-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="1cb53-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cb53-111">EXAMPLES</span></span>

### <span data-ttu-id="1cb53-112">Exemplo 1: obter o status da cópia de um blob</span><span class="sxs-lookup"><span data-stu-id="1cb53-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="1cb53-113">Esse comando obtém o status da cópia do blob chamado ContosoPlanning2015 na ContosoUploads do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1cb53-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="1cb53-114">Exemplo 2: obter o status da cópia de um BLOB usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="1cb53-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="1cb53-115">Esse comando obtém o blob chamado ContosoPlanning2015 no contêiner chamado ContosoUploads usando o cmdlet **Get-AzStorageBlob** e, em seguida, passa o resultado para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="1cb53-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1cb53-116">O cmdlet **Get-AzStorageBlobCopyState** Obtém o status de cópia desse blob.</span><span class="sxs-lookup"><span data-stu-id="1cb53-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="1cb53-117">Exemplo 3: obter o status da cópia de um blob em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="1cb53-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="1cb53-118">Esse comando obtém o contêiner nomeado usando o cmdlet **Get-AzStorageBlob** e, em seguida, passa o resultado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1cb53-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="1cb53-119">O cmdlet **Get-AzStorageContainer** Obtém o status de cópia do blob chamado ContosoPlanning2015 nesse contêiner.</span><span class="sxs-lookup"><span data-stu-id="1cb53-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="1cb53-120">Exemplo 4: Iniciar cópia e pipeline para obter o status da cópia</span><span class="sxs-lookup"><span data-stu-id="1cb53-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="1cb53-121">O primeiro comando começa copiar blob "ContosoPlanning2015" para "ContosoPlanning2015_copy" e gerar o objeto BLOB destiantion.</span><span class="sxs-lookup"><span data-stu-id="1cb53-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="1cb53-122">O segundo pipeline de comando do objeto BLOB destiantion para obter-AzStorageBlobCopyState, para obter o estado de cópia de BLOB.</span><span class="sxs-lookup"><span data-stu-id="1cb53-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="1cb53-123">OS</span><span class="sxs-lookup"><span data-stu-id="1cb53-123">PARAMETERS</span></span>

### <span data-ttu-id="1cb53-124">-Blob</span><span class="sxs-lookup"><span data-stu-id="1cb53-124">-Blob</span></span>
<span data-ttu-id="1cb53-125">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="1cb53-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="1cb53-126">Esse cmdlet obtém o estado da operação de cópia de BLOB para o blob de armazenamento do Azure que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1cb53-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="1cb53-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1cb53-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1cb53-128">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1cb53-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1cb53-129">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1cb53-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1cb53-130">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1cb53-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1cb53-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1cb53-131">-CloudBlob</span></span>
<span data-ttu-id="1cb53-132">Especifica um objeto **CloudBlob** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb53-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1cb53-133">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="1cb53-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="1cb53-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1cb53-134">-CloudBlobContainer</span></span>
<span data-ttu-id="1cb53-135">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb53-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="1cb53-136">Esse cmdlet obtém o status da cópia de um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1cb53-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="1cb53-137">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="1cb53-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="1cb53-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1cb53-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1cb53-139">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1cb53-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1cb53-140">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1cb53-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1cb53-141">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="1cb53-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1cb53-142">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1cb53-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1cb53-143">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="1cb53-143">The default value is 10.</span></span>

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

### <span data-ttu-id="1cb53-144">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="1cb53-144">-Container</span></span>
<span data-ttu-id="1cb53-145">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="1cb53-145">Specifies the name of a container.</span></span>
<span data-ttu-id="1cb53-146">Esse cmdlet obtém o status da cópia de um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1cb53-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="1cb53-147">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1cb53-147">-Context</span></span>
<span data-ttu-id="1cb53-148">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb53-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1cb53-149">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1cb53-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1cb53-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb53-150">-DefaultProfile</span></span>
<span data-ttu-id="1cb53-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb53-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cb53-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1cb53-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1cb53-153">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="1cb53-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1cb53-154">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1cb53-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1cb53-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="1cb53-155">-WaitForComplete</span></span>
<span data-ttu-id="1cb53-156">Indica que esse cmdlet aguarda a conclusão da cópia.</span><span class="sxs-lookup"><span data-stu-id="1cb53-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="1cb53-157">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1cb53-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="1cb53-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb53-158">CommonParameters</span></span>
<span data-ttu-id="1cb53-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb53-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb53-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb53-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb53-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cb53-161">INPUTS</span></span>

### <span data-ttu-id="1cb53-162">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1cb53-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="1cb53-163">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1cb53-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="1cb53-164">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1cb53-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1cb53-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cb53-165">OUTPUTS</span></span>

### <span data-ttu-id="1cb53-166">Microsoft. Azure. Storage. blob. CopyState</span><span class="sxs-lookup"><span data-stu-id="1cb53-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="1cb53-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cb53-167">NOTES</span></span>

## <span data-ttu-id="1cb53-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cb53-168">RELATED LINKS</span></span>

[<span data-ttu-id="1cb53-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1cb53-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="1cb53-170">Parar-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1cb53-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


