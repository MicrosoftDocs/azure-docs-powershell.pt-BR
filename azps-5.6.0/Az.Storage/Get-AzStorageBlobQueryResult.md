---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: 7a790610d9ff3334494276eee7bb85af5b9ba3fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891990"
---
# <span data-ttu-id="eea24-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="eea24-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="eea24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea24-102">SYNOPSIS</span></span>
<span data-ttu-id="eea24-103">Aplica uma instrução linguagem SQL (SQL) simples no conteúdo de um blob e salva apenas o subconjunto consultado dos dados em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="eea24-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="eea24-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eea24-104">SYNTAX</span></span>

### <span data-ttu-id="eea24-105">NamePipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eea24-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eea24-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="eea24-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eea24-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="eea24-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eea24-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eea24-108">DESCRIPTION</span></span>
<span data-ttu-id="eea24-109">O cmdlet **Get-AzStorageBlobQueryResult** aplica uma instrução linguagem SQL simples (SQL) no conteúdo de um blob e salva o subconjunto consultado dos dados em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="eea24-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="eea24-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eea24-110">EXAMPLES</span></span>

### <span data-ttu-id="eea24-111">Exemplo 1: Consultar um blob</span><span class="sxs-lookup"><span data-stu-id="eea24-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="eea24-112">Este comando consulta um blob succsssfully com config de entrada como csv e config de saída como json e salva a saída no arquivo local "c:\resultfile.json".</span><span class="sxs-lookup"><span data-stu-id="eea24-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="eea24-113">Exemplo 2: Consultar um instantâneo blob</span><span class="sxs-lookup"><span data-stu-id="eea24-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="eea24-114">Este comando primeiro obtém um objeto blob para o instantâneo blob, em seguida, consulta o instantâneo blob e mostra o resultado incluir erro de consulta.</span><span class="sxs-lookup"><span data-stu-id="eea24-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="eea24-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eea24-115">PARAMETERS</span></span>

### <span data-ttu-id="eea24-116">-Blob</span><span class="sxs-lookup"><span data-stu-id="eea24-116">-Blob</span></span>
<span data-ttu-id="eea24-117">Nome de blob</span><span class="sxs-lookup"><span data-stu-id="eea24-117">Blob name</span></span>

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

### <span data-ttu-id="eea24-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="eea24-118">-BlobBaseClient</span></span>
<span data-ttu-id="eea24-119">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="eea24-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eea24-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="eea24-120">-BlobContainerClient</span></span>
<span data-ttu-id="eea24-121">Objeto BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="eea24-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eea24-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eea24-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eea24-123">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="eea24-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="eea24-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eea24-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eea24-125">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="eea24-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="eea24-126">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="eea24-126">The default value is 10.</span></span>

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

### <span data-ttu-id="eea24-127">-Container</span><span class="sxs-lookup"><span data-stu-id="eea24-127">-Container</span></span>
<span data-ttu-id="eea24-128">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="eea24-128">Container name</span></span>

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

### <span data-ttu-id="eea24-129">-Context</span><span class="sxs-lookup"><span data-stu-id="eea24-129">-Context</span></span>
<span data-ttu-id="eea24-130">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="eea24-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="eea24-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea24-131">-DefaultProfile</span></span>
<span data-ttu-id="eea24-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eea24-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea24-133">-Force</span><span class="sxs-lookup"><span data-stu-id="eea24-133">-Force</span></span>
<span data-ttu-id="eea24-134">Force a substituir o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="eea24-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="eea24-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="eea24-135">-InputTextConfiguration</span></span>
<span data-ttu-id="eea24-136">A configuração usada para lidar com o texto de entrada de consulta.</span><span class="sxs-lookup"><span data-stu-id="eea24-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="eea24-137">Crie o objeto de configuração com New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="eea24-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea24-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="eea24-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="eea24-139">A configuração usada para lidar com o texto de saída da consulta.</span><span class="sxs-lookup"><span data-stu-id="eea24-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="eea24-140">Crie o objeto de configuração com New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="eea24-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea24-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eea24-141">-PassThru</span></span>
<span data-ttu-id="eea24-142">Retorne se o blob especificado foi consultado com êxito.</span><span class="sxs-lookup"><span data-stu-id="eea24-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="eea24-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="eea24-143">-QueryString</span></span>
<span data-ttu-id="eea24-144">Cadeia de caracteres de consulta, confira mais detalhes em: https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="eea24-144">Query string, see more details in: https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea24-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="eea24-145">-ResultFile</span></span>
<span data-ttu-id="eea24-146">Caminho do arquivo local para salvar o resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="eea24-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea24-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eea24-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eea24-148">O tempo de tempo de servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="eea24-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="eea24-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="eea24-149">-SnapshotTime</span></span>
<span data-ttu-id="eea24-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="eea24-150">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="eea24-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="eea24-151">-VersionId</span></span>
<span data-ttu-id="eea24-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="eea24-152">Blob VersionId</span></span>

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

### <span data-ttu-id="eea24-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eea24-153">-Confirm</span></span>
<span data-ttu-id="eea24-154">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eea24-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea24-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea24-155">-WhatIf</span></span>
<span data-ttu-id="eea24-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eea24-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea24-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eea24-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea24-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea24-158">CommonParameters</span></span>
<span data-ttu-id="eea24-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea24-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea24-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea24-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea24-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eea24-161">INPUTS</span></span>

### <span data-ttu-id="eea24-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="eea24-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="eea24-163">Azure.Storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="eea24-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="eea24-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eea24-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eea24-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eea24-165">OUTPUTS</span></span>

### <span data-ttu-id="eea24-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eea24-166">System.Boolean</span></span>

## <span data-ttu-id="eea24-167">NOTES</span><span class="sxs-lookup"><span data-stu-id="eea24-167">NOTES</span></span>

## <span data-ttu-id="eea24-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eea24-168">RELATED LINKS</span></span>
