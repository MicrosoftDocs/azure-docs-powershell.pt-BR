---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 7d2363f0fc9955ac75444c18da137dcfee345664
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598580"
---
# <span data-ttu-id="d3fc5-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d3fc5-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="d3fc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fc5-103">Remove o blob de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="d3fc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3fc5-104">SYNTAX</span></span>

### <span data-ttu-id="d3fc5-105">NamePipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3fc5-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3fc5-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="d3fc5-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3fc5-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="d3fc5-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3fc5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3fc5-108">DESCRIPTION</span></span>
<span data-ttu-id="d3fc5-109">O cmdlet **Remove-AzStorageBlob** remove o blob especificado de uma conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="d3fc5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3fc5-110">EXAMPLES</span></span>

### <span data-ttu-id="d3fc5-111">Exemplo 1: remover um blob de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="d3fc5-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="d3fc5-112">Esse comando Remove um blob identificado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="d3fc5-113">Exemplo 2: remover um blob de armazenamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d3fc5-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="d3fc5-114">Esse comando usa o pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="d3fc5-115">Exemplo 3: remover blobs de armazenamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d3fc5-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="d3fc5-116">Esse comando usa o caractere curinga asterisco (\*) e o pipeline para recuperar o BLOB ou BLOBs e, em seguida, remove-os.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="d3fc5-117">OS</span><span class="sxs-lookup"><span data-stu-id="d3fc5-117">PARAMETERS</span></span>

### <span data-ttu-id="d3fc5-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="d3fc5-118">-Blob</span></span>
<span data-ttu-id="d3fc5-119">Especifica o nome do blob que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="d3fc5-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3fc5-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d3fc5-121">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d3fc5-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d3fc5-123">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d3fc5-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d3fc5-124">-CloudBlob</span></span>
<span data-ttu-id="d3fc5-125">Especifica um blob na nuvem.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="d3fc5-126">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fc5-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d3fc5-127">-CloudBlobContainer</span></span>
<span data-ttu-id="d3fc5-128">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="d3fc5-129">Você pode usar o cmdlet Get-AzStorageContainer para obtê-lo.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-129">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fc5-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d3fc5-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d3fc5-131">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d3fc5-132">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d3fc5-133">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d3fc5-134">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d3fc5-135">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-135">The default value is 10.</span></span>

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

### <span data-ttu-id="d3fc5-136">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="d3fc5-136">-Container</span></span>
<span data-ttu-id="d3fc5-137">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="d3fc5-138">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d3fc5-138">-Context</span></span>
<span data-ttu-id="d3fc5-139">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d3fc5-140">Você pode usar o cmdlet New-AzStorageContext para criá-lo.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-140">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="d3fc5-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3fc5-141">-DefaultProfile</span></span>
<span data-ttu-id="d3fc5-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3fc5-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="d3fc5-143">-DeleteSnapshot</span></span>
<span data-ttu-id="d3fc5-144">Especifica que todos os instantâneos serão excluídos, mas não o blob base.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="d3fc5-145">Se esse parâmetro não for especificado, o blob base e seus instantâneos serão excluídos juntos.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="d3fc5-146">O usuário será solicitado a confirmar a operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="d3fc5-147">-Force</span><span class="sxs-lookup"><span data-stu-id="d3fc5-147">-Force</span></span>
<span data-ttu-id="d3fc5-148">Indica que esse cmdlet Remove o blob e seu instantâneo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="d3fc5-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3fc5-149">-PassThru</span></span>
<span data-ttu-id="d3fc5-150">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d3fc5-151">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d3fc5-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3fc5-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d3fc5-153">Especifica o perfil do Azure para o cmdlet ler.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="d3fc5-154">Se não for especificado, o cmdlet lerá do perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="d3fc5-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3fc5-155">-Confirm</span></span>
<span data-ttu-id="d3fc5-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3fc5-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3fc5-157">-WhatIf</span></span>
<span data-ttu-id="d3fc5-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3fc5-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3fc5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fc5-160">CommonParameters</span></span>
<span data-ttu-id="d3fc5-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3fc5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fc5-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3fc5-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fc5-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3fc5-163">INPUTS</span></span>

### <span data-ttu-id="d3fc5-164">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d3fc5-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="d3fc5-165">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d3fc5-165">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="d3fc5-166">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3fc5-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d3fc5-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3fc5-167">OUTPUTS</span></span>

### <span data-ttu-id="d3fc5-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3fc5-168">System.Boolean</span></span>

## <span data-ttu-id="d3fc5-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3fc5-169">NOTES</span></span>

## <span data-ttu-id="d3fc5-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3fc5-170">RELATED LINKS</span></span>

[<span data-ttu-id="d3fc5-171">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d3fc5-171">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="d3fc5-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d3fc5-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="d3fc5-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d3fc5-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
