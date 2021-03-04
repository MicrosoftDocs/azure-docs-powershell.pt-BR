---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 4bc06ca07c95986f75062a64a0f86475f7720ff1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891995"
---
# <span data-ttu-id="905a0-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="905a0-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="905a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="905a0-102">SYNOPSIS</span></span>
<span data-ttu-id="905a0-103">Obtém o status de cópia de um blob armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="905a0-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="905a0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="905a0-104">SYNTAX</span></span>

### <span data-ttu-id="905a0-105">NamePipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="905a0-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="905a0-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="905a0-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="905a0-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="905a0-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="905a0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="905a0-108">DESCRIPTION</span></span>
<span data-ttu-id="905a0-109">O cmdlet **Get-AzStorageBlobCopyState** obtém o status de cópia de um blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="905a0-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="905a0-110">Ele deve ser executado no blob de destino de cópia.</span><span class="sxs-lookup"><span data-stu-id="905a0-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="905a0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="905a0-111">EXAMPLES</span></span>

### <span data-ttu-id="905a0-112">Exemplo 1: Obter o status de cópia de um blob</span><span class="sxs-lookup"><span data-stu-id="905a0-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="905a0-113">Este comando obtém o status de cópia do blob chamado ContosoPlanning2015 no contêiner ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="905a0-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="905a0-114">Exemplo 2: Obter o status de cópia de um blob usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="905a0-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="905a0-115">Este comando obtém o blob chamado ContosoPlanning2015 no contêiner chamado ContosoUploads usando o cmdlet **Get-AzStorageBlob** e, em seguida, passa o resultado para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="905a0-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="905a0-116">O cmdlet **Get-AzStorageBlobCopyState** obtém o status de cópia desse blob.</span><span class="sxs-lookup"><span data-stu-id="905a0-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="905a0-117">Exemplo 3: Obter o status de cópia de um blob em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="905a0-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="905a0-118">Esse comando obtém o contêiner nomeado usando o cmdlet **Get-AzStorageBlob** e passa o resultado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="905a0-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="905a0-119">O cmdlet **Get-AzStorageContainer** obtém o status de cópia do blob chamado ContosoPlanning2015 nesse contêiner.</span><span class="sxs-lookup"><span data-stu-id="905a0-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="905a0-120">Exemplo 4: Iniciar Cópia e pipeline para obter o status da cópia</span><span class="sxs-lookup"><span data-stu-id="905a0-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="905a0-121">O primeiro comando inicia a cópia do blob "ContosoPlanning2015" para "ContosoPlanning2015_copy", e saída do objeto blob de destiantion.</span><span class="sxs-lookup"><span data-stu-id="905a0-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="905a0-122">O segundo pipeline de comando do objeto blob de destiantion para Get-AzStorageBlobCopyState, para obter o estado de cópia de blob.</span><span class="sxs-lookup"><span data-stu-id="905a0-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="905a0-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="905a0-123">PARAMETERS</span></span>

### <span data-ttu-id="905a0-124">-Blob</span><span class="sxs-lookup"><span data-stu-id="905a0-124">-Blob</span></span>
<span data-ttu-id="905a0-125">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="905a0-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="905a0-126">Este cmdlet obtém o estado da operação de cópia de blob para o blob armazenamento do Azure especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="905a0-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="905a0-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="905a0-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="905a0-128">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="905a0-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="905a0-129">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="905a0-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="905a0-130">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="905a0-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="905a0-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="905a0-131">-CloudBlob</span></span>
<span data-ttu-id="905a0-132">Especifica um **objeto CloudBlob** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="905a0-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="905a0-133">Para obter um **objeto CloudBlob,** use Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="905a0-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="905a0-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="905a0-134">-CloudBlobContainer</span></span>
<span data-ttu-id="905a0-135">Especifica um **objeto CloudBlobContainer** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="905a0-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="905a0-136">Este cmdlet obtém o status de cópia de um blob no contêiner especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="905a0-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="905a0-137">Para obter um **objeto CloudBlobContainer,** use Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="905a0-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="905a0-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="905a0-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="905a0-139">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="905a0-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="905a0-140">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="905a0-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="905a0-141">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="905a0-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="905a0-142">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="905a0-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="905a0-143">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="905a0-143">The default value is 10.</span></span>

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

### <span data-ttu-id="905a0-144">-Container</span><span class="sxs-lookup"><span data-stu-id="905a0-144">-Container</span></span>
<span data-ttu-id="905a0-145">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="905a0-145">Specifies the name of a container.</span></span>
<span data-ttu-id="905a0-146">Este cmdlet obtém o status de cópia de um blob no contêiner especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="905a0-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="905a0-147">-Context</span><span class="sxs-lookup"><span data-stu-id="905a0-147">-Context</span></span>
<span data-ttu-id="905a0-148">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="905a0-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="905a0-149">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="905a0-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="905a0-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905a0-150">-DefaultProfile</span></span>
<span data-ttu-id="905a0-151">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="905a0-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="905a0-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="905a0-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="905a0-153">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="905a0-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="905a0-154">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="905a0-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="905a0-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="905a0-155">-WaitForComplete</span></span>
<span data-ttu-id="905a0-156">Indica que esse cmdlet aguarda o fim da cópia.</span><span class="sxs-lookup"><span data-stu-id="905a0-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="905a0-157">Se você não especificar esse parâmetro, este cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="905a0-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="905a0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905a0-158">CommonParameters</span></span>
<span data-ttu-id="905a0-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905a0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905a0-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905a0-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905a0-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="905a0-161">INPUTS</span></span>

### <span data-ttu-id="905a0-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="905a0-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="905a0-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="905a0-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="905a0-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="905a0-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="905a0-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="905a0-165">OUTPUTS</span></span>

### <span data-ttu-id="905a0-166">Microsoft.Azure.Storage.Blob.CopyState</span><span class="sxs-lookup"><span data-stu-id="905a0-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="905a0-167">NOTES</span><span class="sxs-lookup"><span data-stu-id="905a0-167">NOTES</span></span>

## <span data-ttu-id="905a0-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="905a0-168">RELATED LINKS</span></span>

[<span data-ttu-id="905a0-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="905a0-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="905a0-170">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="905a0-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


