---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
ms.openlocfilehash: b9d987dad0542f7637f7d061ee510c1601dc6e6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429007"
---
# <span data-ttu-id="2c177-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2c177-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="2c177-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c177-102">SYNOPSIS</span></span>
<span data-ttu-id="2c177-103">Remove o blob de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="2c177-103">Removes the specified storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c177-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c177-104">SYNTAX</span></span>

### <span data-ttu-id="2c177-105">NamePipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c177-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c177-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2c177-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c177-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="2c177-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c177-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c177-108">DESCRIPTION</span></span>
<span data-ttu-id="2c177-109">O cmdlet **Remove-AzureStorageBlob** remove o blob especificado de uma conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="2c177-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="2c177-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c177-110">EXAMPLES</span></span>

### <span data-ttu-id="2c177-111">Exemplo 1: remover um blob de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="2c177-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="2c177-112">Esse comando Remove um blob identificado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="2c177-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="2c177-113">Exemplo 2: remover um blob de armazenamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="2c177-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="2c177-114">Esse comando usa o pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c177-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="2c177-115">Exemplo 3: remover blobs de armazenamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="2c177-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="2c177-116">Esse comando usa o caractere curinga asterisco (\*) e o pipeline para recuperar o BLOB ou BLOBs e, em seguida, remove-os.</span><span class="sxs-lookup"><span data-stu-id="2c177-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="2c177-117">OS</span><span class="sxs-lookup"><span data-stu-id="2c177-117">PARAMETERS</span></span>

### <span data-ttu-id="2c177-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="2c177-118">-Blob</span></span>
<span data-ttu-id="2c177-119">Especifica o nome do blob que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="2c177-119">Specifies the name of the blob you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c177-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2c177-121">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c177-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2c177-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2c177-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2c177-123">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="2c177-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2c177-124">-CloudBlob</span></span>
<span data-ttu-id="2c177-125">Especifica um blob na nuvem.</span><span class="sxs-lookup"><span data-stu-id="2c177-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="2c177-126">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="2c177-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2c177-127">-CloudBlobContainer</span></span>
<span data-ttu-id="2c177-128">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c177-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="2c177-129">Você pode usar o cmdlet Get-AzureStorageContainer para obtê-lo.</span><span class="sxs-lookup"><span data-stu-id="2c177-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2c177-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2c177-131">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2c177-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2c177-132">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2c177-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2c177-133">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="2c177-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2c177-134">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="2c177-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2c177-135">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="2c177-135">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-136">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="2c177-136">-Container</span></span>
<span data-ttu-id="2c177-137">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="2c177-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-138">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2c177-138">-Context</span></span>
<span data-ttu-id="2c177-139">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c177-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2c177-140">Você pode usar o cmdlet New-AzureStorageContext para criá-lo.</span><span class="sxs-lookup"><span data-stu-id="2c177-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="2c177-141">-DeleteSnapshot</span></span>
<span data-ttu-id="2c177-142">Especifica que todos os instantâneos serão excluídos, mas não o blob base.</span><span class="sxs-lookup"><span data-stu-id="2c177-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="2c177-143">Se esse parâmetro não for especificado, o blob base e seus instantâneos serão excluídos juntos.</span><span class="sxs-lookup"><span data-stu-id="2c177-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="2c177-144">O usuário será solicitado a confirmar a operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="2c177-144">The user is prompted to confirm the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-145">-Force</span><span class="sxs-lookup"><span data-stu-id="2c177-145">-Force</span></span>
<span data-ttu-id="2c177-146">Indica que esse cmdlet Remove o blob e seu instantâneo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="2c177-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c177-147">-PassThru</span></span>
<span data-ttu-id="2c177-148">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="2c177-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2c177-149">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2c177-149">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c177-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2c177-151">Especifica o perfil do Azure para o cmdlet ler.</span><span class="sxs-lookup"><span data-stu-id="2c177-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="2c177-152">Se não for especificado, o cmdlet lerá do perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="2c177-152">If not specified, the cmdlet reads from the default profile.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c177-153">-Confirm</span></span>
<span data-ttu-id="2c177-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c177-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c177-155">-WhatIf</span></span>
<span data-ttu-id="2c177-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c177-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c177-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c177-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c177-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c177-158">CommonParameters</span></span>
<span data-ttu-id="2c177-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c177-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c177-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c177-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c177-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c177-161">INPUTS</span></span>

### <span data-ttu-id="2c177-162">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c177-162">IStorageContext</span></span>

<span data-ttu-id="2c177-163">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2c177-163">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="2c177-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c177-164">OUTPUTS</span></span>

### <span data-ttu-id="2c177-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c177-165">System.Boolean</span></span>

## <span data-ttu-id="2c177-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c177-166">NOTES</span></span>

## <span data-ttu-id="2c177-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c177-167">RELATED LINKS</span></span>

[<span data-ttu-id="2c177-168">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2c177-168">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="2c177-169">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2c177-169">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="2c177-170">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2c177-170">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)
