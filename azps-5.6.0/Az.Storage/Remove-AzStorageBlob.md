---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 12bfa9ab7e35bab3421bee71cf5ea0787c95a86d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885240"
---
# <span data-ttu-id="6d246-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6d246-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="6d246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d246-102">SYNOPSIS</span></span>
<span data-ttu-id="6d246-103">Remove o blob de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="6d246-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="6d246-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6d246-104">SYNTAX</span></span>

### <span data-ttu-id="6d246-105">NamePipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d246-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d246-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="6d246-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d246-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6d246-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d246-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d246-108">DESCRIPTION</span></span>
<span data-ttu-id="6d246-109">O cmdlet **Remove-AzStorageBlob** remove o blob especificado de uma conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="6d246-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="6d246-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d246-110">EXAMPLES</span></span>

### <span data-ttu-id="6d246-111">Exemplo 1: Remover um blob de armazenamento pelo nome</span><span class="sxs-lookup"><span data-stu-id="6d246-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="6d246-112">Este comando remove um blob identificado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="6d246-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="6d246-113">Exemplo 2: Remover um blob de armazenamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="6d246-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="6d246-114">Este comando usa o pipeline.</span><span class="sxs-lookup"><span data-stu-id="6d246-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="6d246-115">Exemplo 3: Remover blobs de armazenamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="6d246-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="6d246-116">Este comando usa o caractere curinga asterisco (\*) e o pipeline para recuperar o blob ou blobs e, em seguida, remove-os.</span><span class="sxs-lookup"><span data-stu-id="6d246-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="6d246-117">Exemplo 4: Remover uma única versão de blob</span><span class="sxs-lookup"><span data-stu-id="6d246-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="6d246-118">Este comando remove um único vértice de blobs com VersionId.</span><span class="sxs-lookup"><span data-stu-id="6d246-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="6d246-119">Exemplo 5: Remover um único instantâneo de blob</span><span class="sxs-lookup"><span data-stu-id="6d246-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="6d246-120">Este comando remove um único instantâneo de blobs com InstantâneoTime.</span><span class="sxs-lookup"><span data-stu-id="6d246-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="6d246-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6d246-121">PARAMETERS</span></span>

### <span data-ttu-id="6d246-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="6d246-122">-Blob</span></span>
<span data-ttu-id="6d246-123">Especifica o nome do blob que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="6d246-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="6d246-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6d246-124">-BlobBaseClient</span></span>
<span data-ttu-id="6d246-125">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6d246-125">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d246-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6d246-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6d246-127">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="6d246-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6d246-128">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6d246-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6d246-129">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6d246-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6d246-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6d246-130">-CloudBlob</span></span>
<span data-ttu-id="6d246-131">Especifica um blob de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6d246-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="6d246-132">Para obter um **objeto CloudBlob,** use Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d246-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6d246-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6d246-133">-CloudBlobContainer</span></span>
<span data-ttu-id="6d246-134">Especifica um **objeto CloudBlobContainer** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d246-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6d246-135">Você pode usar o cmdlet Get-AzStorageContainer para obter.</span><span class="sxs-lookup"><span data-stu-id="6d246-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="6d246-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6d246-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6d246-137">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="6d246-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6d246-138">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="6d246-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6d246-139">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="6d246-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6d246-140">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="6d246-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6d246-141">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="6d246-141">The default value is 10.</span></span>

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

### <span data-ttu-id="6d246-142">-Container</span><span class="sxs-lookup"><span data-stu-id="6d246-142">-Container</span></span>
<span data-ttu-id="6d246-143">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="6d246-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="6d246-144">-Context</span><span class="sxs-lookup"><span data-stu-id="6d246-144">-Context</span></span>
<span data-ttu-id="6d246-145">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d246-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6d246-146">Você pode usar o cmdlet New-AzStorageContext para cria-lo.</span><span class="sxs-lookup"><span data-stu-id="6d246-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="6d246-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d246-147">-DefaultProfile</span></span>
<span data-ttu-id="6d246-148">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d246-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d246-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="6d246-149">-DeleteSnapshot</span></span>
<span data-ttu-id="6d246-150">Especifica que todos os instantâneos sejam excluídos, mas não o blob base.</span><span class="sxs-lookup"><span data-stu-id="6d246-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="6d246-151">Se esse parâmetro não for especificado, o blob base e seus instantâneos serão excluídos juntos.</span><span class="sxs-lookup"><span data-stu-id="6d246-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="6d246-152">O usuário é solicitado a confirmar a operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="6d246-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="6d246-153">-Force</span><span class="sxs-lookup"><span data-stu-id="6d246-153">-Force</span></span>
<span data-ttu-id="6d246-154">Indica que esse cmdlet remove o blob e seu instantâneo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="6d246-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="6d246-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d246-155">-PassThru</span></span>
<span data-ttu-id="6d246-156">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="6d246-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6d246-157">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6d246-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6d246-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6d246-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6d246-159">Especifica o perfil do Azure para o cmdlet ler.</span><span class="sxs-lookup"><span data-stu-id="6d246-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="6d246-160">Se não for especificado, o cmdlet será lido do perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="6d246-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="6d246-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="6d246-161">-SnapshotTime</span></span>
<span data-ttu-id="6d246-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="6d246-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d246-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="6d246-163">-VersionId</span></span>
<span data-ttu-id="6d246-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="6d246-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d246-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d246-165">-Confirm</span></span>
<span data-ttu-id="6d246-166">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d246-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d246-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d246-167">-WhatIf</span></span>
<span data-ttu-id="6d246-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d246-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d246-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d246-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d246-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d246-170">CommonParameters</span></span>
<span data-ttu-id="6d246-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d246-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d246-172">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d246-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d246-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d246-173">INPUTS</span></span>

### <span data-ttu-id="6d246-174">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6d246-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6d246-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6d246-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="6d246-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d246-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6d246-177">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6d246-177">OUTPUTS</span></span>

### <span data-ttu-id="6d246-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d246-178">System.Boolean</span></span>

## <span data-ttu-id="6d246-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="6d246-179">NOTES</span></span>

## <span data-ttu-id="6d246-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d246-180">RELATED LINKS</span></span>

[<span data-ttu-id="6d246-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6d246-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6d246-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d246-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="6d246-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d246-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
