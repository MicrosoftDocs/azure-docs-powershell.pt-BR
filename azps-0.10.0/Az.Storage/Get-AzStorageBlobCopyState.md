---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: e6d5bcad88e50fcd166e2d7a8c37ca948ae355f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776271"
---
# <span data-ttu-id="cbae9-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="cbae9-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="cbae9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbae9-102">SYNOPSIS</span></span>
<span data-ttu-id="cbae9-103">Obtém o status da cópia de um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbae9-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="cbae9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbae9-104">SYNTAX</span></span>

### <span data-ttu-id="cbae9-105">NamePipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="cbae9-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cbae9-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="cbae9-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cbae9-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="cbae9-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cbae9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbae9-108">DESCRIPTION</span></span>
<span data-ttu-id="cbae9-109">O cmdlet **Get-AzStorageBlobCopyState** Obtém o status da cópia de um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbae9-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="cbae9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbae9-110">EXAMPLES</span></span>

### <span data-ttu-id="cbae9-111">Exemplo 1: obter o status da cópia de um blob</span><span class="sxs-lookup"><span data-stu-id="cbae9-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="cbae9-112">Esse comando obtém o status da cópia do blob chamado ContosoPlanning2015 na ContosoUploads do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cbae9-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="cbae9-113">Exemplo 2: obter o status da cópia de um BLOB usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="cbae9-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="cbae9-114">Esse comando obtém o blob chamado ContosoPlanning2015 no contêiner chamado ContosoUploads usando o cmdlet **Get-AzStorageBlob** e, em seguida, passa o resultado para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="cbae9-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cbae9-115">O cmdlet **Get-AzStorageBlobCopyState** Obtém o status de cópia desse blob.</span><span class="sxs-lookup"><span data-stu-id="cbae9-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="cbae9-116">Exemplo 3: obter o status da cópia de um blob em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="cbae9-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="cbae9-117">Esse comando obtém o contêiner nomeado usando o cmdlet **Get-AzStorageBlob** e, em seguida, passa o resultado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="cbae9-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="cbae9-118">O cmdlet **Get-AzStorageContainer** Obtém o status de cópia do blob chamado ContosoPlanning2015 nesse contêiner.</span><span class="sxs-lookup"><span data-stu-id="cbae9-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="cbae9-119">OS</span><span class="sxs-lookup"><span data-stu-id="cbae9-119">PARAMETERS</span></span>

### <span data-ttu-id="cbae9-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="cbae9-120">-Blob</span></span>
<span data-ttu-id="cbae9-121">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="cbae9-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="cbae9-122">Esse cmdlet obtém o estado da operação de cópia de BLOB para o blob de armazenamento do Azure que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cbae9-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbae9-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cbae9-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cbae9-124">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="cbae9-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cbae9-125">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="cbae9-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cbae9-126">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cbae9-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cbae9-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cbae9-127">-CloudBlob</span></span>
<span data-ttu-id="cbae9-128">Especifica um objeto **CloudBlob** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbae9-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="cbae9-129">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="cbae9-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbae9-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cbae9-130">-CloudBlobContainer</span></span>
<span data-ttu-id="cbae9-131">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbae9-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="cbae9-132">Esse cmdlet obtém o status da cópia de um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cbae9-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="cbae9-133">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="cbae9-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbae9-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cbae9-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cbae9-135">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cbae9-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cbae9-136">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cbae9-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cbae9-137">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="cbae9-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cbae9-138">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cbae9-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cbae9-139">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="cbae9-139">The default value is 10.</span></span>

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

### <span data-ttu-id="cbae9-140">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="cbae9-140">-Container</span></span>
<span data-ttu-id="cbae9-141">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="cbae9-141">Specifies the name of a container.</span></span>
<span data-ttu-id="cbae9-142">Esse cmdlet obtém o status da cópia de um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cbae9-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbae9-143">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cbae9-143">-Context</span></span>
<span data-ttu-id="cbae9-144">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbae9-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cbae9-145">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cbae9-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cbae9-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbae9-146">-DefaultProfile</span></span>
<span data-ttu-id="cbae9-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbae9-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbae9-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cbae9-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cbae9-149">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="cbae9-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="cbae9-150">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cbae9-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="cbae9-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="cbae9-151">-WaitForComplete</span></span>
<span data-ttu-id="cbae9-152">Indica que esse cmdlet aguarda a conclusão da cópia.</span><span class="sxs-lookup"><span data-stu-id="cbae9-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="cbae9-153">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cbae9-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="cbae9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbae9-154">CommonParameters</span></span>
<span data-ttu-id="cbae9-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbae9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbae9-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbae9-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbae9-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbae9-157">INPUTS</span></span>

### <span data-ttu-id="cbae9-158">Microsoft. WindowsAz. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cbae9-158">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="cbae9-159">Microsoft. WindowsAz. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cbae9-159">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="cbae9-160">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cbae9-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cbae9-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbae9-161">OUTPUTS</span></span>

### <span data-ttu-id="cbae9-162">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cbae9-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="cbae9-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbae9-163">NOTES</span></span>

## <span data-ttu-id="cbae9-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbae9-164">RELATED LINKS</span></span>

[<span data-ttu-id="cbae9-165">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cbae9-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="cbae9-166">Parar-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cbae9-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


