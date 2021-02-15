---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116100"
---
# <span data-ttu-id="61dcb-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="61dcb-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="61dcb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="61dcb-103">Remove o blob de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="61dcb-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="61dcb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61dcb-104">SYNTAX</span></span>

### <span data-ttu-id="61dcb-105">NamePipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="61dcb-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61dcb-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="61dcb-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61dcb-107">ContainerLaline</span><span class="sxs-lookup"><span data-stu-id="61dcb-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61dcb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="61dcb-108">DESCRIPTION</span></span>
<span data-ttu-id="61dcb-109">O cmdlet **Remove-AzStorageB ltd remove** o blob especificado de uma conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="61dcb-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="61dcb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61dcb-110">EXAMPLES</span></span>

### <span data-ttu-id="61dcb-111">Exemplo 1: Remover um blob de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="61dcb-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="61dcb-112">Esse comando remove um blob identificado por seu nome.</span><span class="sxs-lookup"><span data-stu-id="61dcb-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="61dcb-113">Exemplo 2: Remover um blob de armazenamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="61dcb-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="61dcb-114">Esse comando usa o pipeline.</span><span class="sxs-lookup"><span data-stu-id="61dcb-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="61dcb-115">Exemplo 3: Remover blobs de armazenamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="61dcb-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="61dcb-116">Esse comando usa o caractere curinga asterisco (\*) e o pipeline para recuperar o blob ou blobs e depois removê-los.</span><span class="sxs-lookup"><span data-stu-id="61dcb-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="61dcb-117">Exemplo 4: Remover uma única versão de blob</span><span class="sxs-lookup"><span data-stu-id="61dcb-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="61dcb-118">Esse comando remove um único verão de blobs com VersionId.</span><span class="sxs-lookup"><span data-stu-id="61dcb-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="61dcb-119">Exemplo 5: Remover um único instantâneo de blob</span><span class="sxs-lookup"><span data-stu-id="61dcb-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="61dcb-120">Esse comando remove um único instantâneo de blobs com InstantâneoTime.</span><span class="sxs-lookup"><span data-stu-id="61dcb-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="61dcb-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61dcb-121">PARAMETERS</span></span>

### <span data-ttu-id="61dcb-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="61dcb-122">-Blob</span></span>
<span data-ttu-id="61dcb-123">Especifica o nome do blob que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="61dcb-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="61dcb-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="61dcb-124">-BlobBaseClient</span></span>
<span data-ttu-id="61dcb-125">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="61dcb-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="61dcb-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61dcb-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="61dcb-127">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="61dcb-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="61dcb-128">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="61dcb-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="61dcb-129">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se elapse, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="61dcb-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="61dcb-130">-CloudBlab</span><span class="sxs-lookup"><span data-stu-id="61dcb-130">-CloudBlob</span></span>
<span data-ttu-id="61dcb-131">Especifica um blob de nuvem.</span><span class="sxs-lookup"><span data-stu-id="61dcb-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="61dcb-132">Para obter um **objeto CloudB ltd,** use o cmdlet Get-AzStorageBlob nuvem.</span><span class="sxs-lookup"><span data-stu-id="61dcb-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="61dcb-133">-CloudBltContainer</span><span class="sxs-lookup"><span data-stu-id="61dcb-133">-CloudBlobContainer</span></span>
<span data-ttu-id="61dcb-134">Especifica um objeto **CloudBltContainer** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="61dcb-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="61dcb-135">Você pode usar o cmdlet Get-AzStorageContainer-lo.</span><span class="sxs-lookup"><span data-stu-id="61dcb-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="61dcb-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="61dcb-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="61dcb-137">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="61dcb-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="61dcb-138">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="61dcb-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="61dcb-139">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="61dcb-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="61dcb-140">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="61dcb-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="61dcb-141">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="61dcb-141">The default value is 10.</span></span>

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

### <span data-ttu-id="61dcb-142">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="61dcb-142">-Container</span></span>
<span data-ttu-id="61dcb-143">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="61dcb-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="61dcb-144">-Contexto</span><span class="sxs-lookup"><span data-stu-id="61dcb-144">-Context</span></span>
<span data-ttu-id="61dcb-145">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="61dcb-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="61dcb-146">Você pode usar o cmdlet New-AzStorageContext para criar.</span><span class="sxs-lookup"><span data-stu-id="61dcb-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="61dcb-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dcb-147">-DefaultProfile</span></span>
<span data-ttu-id="61dcb-148">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61dcb-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61dcb-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="61dcb-149">-DeleteSnapshot</span></span>
<span data-ttu-id="61dcb-150">Especifica que todos os instantâneos serão excluídos, mas não o blob base.</span><span class="sxs-lookup"><span data-stu-id="61dcb-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="61dcb-151">Se esse parâmetro não for especificado, o blob base e seus instantâneos serão excluídos juntos.</span><span class="sxs-lookup"><span data-stu-id="61dcb-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="61dcb-152">O usuário será solicitado a confirmar a operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="61dcb-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="61dcb-153">-Forçar</span><span class="sxs-lookup"><span data-stu-id="61dcb-153">-Force</span></span>
<span data-ttu-id="61dcb-154">Indica que esse cmdlet remove o blob e seu instantâneo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="61dcb-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="61dcb-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61dcb-155">-PassThru</span></span>
<span data-ttu-id="61dcb-156">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="61dcb-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="61dcb-157">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="61dcb-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="61dcb-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61dcb-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="61dcb-159">Especifica o perfil do Azure para que o cmdlet seja lido.</span><span class="sxs-lookup"><span data-stu-id="61dcb-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="61dcb-160">Se não especificado, o cmdlet será lido do perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="61dcb-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="61dcb-161">-InstantâneoTime</span><span class="sxs-lookup"><span data-stu-id="61dcb-161">-SnapshotTime</span></span>
<span data-ttu-id="61dcb-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="61dcb-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="61dcb-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="61dcb-163">-VersionId</span></span>
<span data-ttu-id="61dcb-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="61dcb-164">Blob VersionId</span></span>

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

### <span data-ttu-id="61dcb-165">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="61dcb-165">-Confirm</span></span>
<span data-ttu-id="61dcb-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61dcb-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61dcb-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61dcb-167">-WhatIf</span></span>
<span data-ttu-id="61dcb-168">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="61dcb-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61dcb-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61dcb-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61dcb-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dcb-170">CommonParameters</span></span>
<span data-ttu-id="61dcb-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61dcb-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dcb-172">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61dcb-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dcb-173">Entradas</span><span class="sxs-lookup"><span data-stu-id="61dcb-173">INPUTS</span></span>

### <span data-ttu-id="61dcb-174">Microsoft.Azure.Storage.Blob.CloudBlab</span><span class="sxs-lookup"><span data-stu-id="61dcb-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="61dcb-175">Microsoft.Azure.Storage.Blob.CloudBltContainer</span><span class="sxs-lookup"><span data-stu-id="61dcb-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="61dcb-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="61dcb-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="61dcb-177">Saídas</span><span class="sxs-lookup"><span data-stu-id="61dcb-177">OUTPUTS</span></span>

### <span data-ttu-id="61dcb-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61dcb-178">System.Boolean</span></span>

## <span data-ttu-id="61dcb-179">Notas</span><span class="sxs-lookup"><span data-stu-id="61dcb-179">NOTES</span></span>

## <span data-ttu-id="61dcb-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61dcb-180">RELATED LINKS</span></span>

[<span data-ttu-id="61dcb-181">Get-AzStorageB ltd</span><span class="sxs-lookup"><span data-stu-id="61dcb-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="61dcb-182">Get-AzStorageBcontent</span><span class="sxs-lookup"><span data-stu-id="61dcb-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="61dcb-183">Set-AzStorageBcontent</span><span class="sxs-lookup"><span data-stu-id="61dcb-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
