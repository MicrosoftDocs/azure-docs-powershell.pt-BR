---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115670"
---
# <span data-ttu-id="2c1a7-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="2c1a7-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="2c1a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c1a7-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1a7-103">Aplica uma instrução SQL (Structured Query Language) simples ao conteúdo de um blob e salva apenas o subconjunto consultado dos dados em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="2c1a7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c1a7-104">SYNTAX</span></span>

### <span data-ttu-id="2c1a7-105">NamePipeline (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2c1a7-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c1a7-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2c1a7-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c1a7-107">ContainerLaline</span><span class="sxs-lookup"><span data-stu-id="2c1a7-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c1a7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c1a7-108">DESCRIPTION</span></span>
<span data-ttu-id="2c1a7-109">O cmdlet **Get-AzStorageBiedQueryResult** aplica uma instrução SQL (Linguagem de Consulta Estruturada) simples no conteúdo de um blob e salva o subconjunto consultado dos dados em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="2c1a7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c1a7-110">EXAMPLES</span></span>

### <span data-ttu-id="2c1a7-111">Exemplo 1: Consultar um blob</span><span class="sxs-lookup"><span data-stu-id="2c1a7-111">Example 1: Query a blob</span></span>
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

<span data-ttu-id="2c1a7-112">Esse comando consulta um blob de forma supositiva com a configuração de entrada como csv e a configuração de saída como json, e salva a saída no arquivo local "c:\resultfile.js".</span><span class="sxs-lookup"><span data-stu-id="2c1a7-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="2c1a7-113">Exemplo 2: Consultar um instantâneo de blob</span><span class="sxs-lookup"><span data-stu-id="2c1a7-113">Example 2: Query a blob snapshot</span></span>
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

<span data-ttu-id="2c1a7-114">Esse comando obtém primeiro um objeto de blob para instantâneo de blob, depois consulta o instantâneo de blob e mostra o resultado incluindo o erro de consulta.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="2c1a7-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c1a7-115">PARAMETERS</span></span>

### <span data-ttu-id="2c1a7-116">-Blob</span><span class="sxs-lookup"><span data-stu-id="2c1a7-116">-Blob</span></span>
<span data-ttu-id="2c1a7-117">Nome de blob</span><span class="sxs-lookup"><span data-stu-id="2c1a7-117">Blob name</span></span>

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

### <span data-ttu-id="2c1a7-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="2c1a7-118">-BlobBaseClient</span></span>
<span data-ttu-id="2c1a7-119">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="2c1a7-119">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="2c1a7-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="2c1a7-120">-BlobContainerClient</span></span>
<span data-ttu-id="2c1a7-121">Objeto BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="2c1a7-121">BlobContainerClient Object</span></span>

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

### <span data-ttu-id="2c1a7-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c1a7-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2c1a7-123">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="2c1a7-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2c1a7-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2c1a7-125">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="2c1a7-126">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-126">The default value is 10.</span></span>

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

### <span data-ttu-id="2c1a7-127">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="2c1a7-127">-Container</span></span>
<span data-ttu-id="2c1a7-128">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="2c1a7-128">Container name</span></span>

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

### <span data-ttu-id="2c1a7-129">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2c1a7-129">-Context</span></span>
<span data-ttu-id="2c1a7-130">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="2c1a7-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2c1a7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1a7-131">-DefaultProfile</span></span>
<span data-ttu-id="2c1a7-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c1a7-133">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2c1a7-133">-Force</span></span>
<span data-ttu-id="2c1a7-134">Forçar a substituir o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="2c1a7-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1a7-135">-InputTextConfiguration</span></span>
<span data-ttu-id="2c1a7-136">A configuração usada para lidar com o texto de entrada da consulta.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="2c1a7-137">Crie o objeto de configuração com o Novo-AzStorageB diamondQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="2c1a7-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1a7-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="2c1a7-139">A configuração usada para lidar com o texto de saída da consulta.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="2c1a7-140">Crie o objeto de configuração com o Novo-AzStorageB diamondQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="2c1a7-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c1a7-141">-PassThru</span></span>
<span data-ttu-id="2c1a7-142">Retorne se a blob especificada foi consultada com êxito.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="2c1a7-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="2c1a7-143">-QueryString</span></span>
<span data-ttu-id="2c1a7-144">Cadeia de caracteres de consulta, veja mais detalhes em: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="2c1a7-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

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

### <span data-ttu-id="2c1a7-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="2c1a7-145">-ResultFile</span></span>
<span data-ttu-id="2c1a7-146">Caminho de arquivo local para salvar o resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-146">Local file path to save the query result.</span></span>

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

### <span data-ttu-id="2c1a7-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c1a7-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2c1a7-148">O tempo de tempo de servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="2c1a7-149">-InstantâneoTime</span><span class="sxs-lookup"><span data-stu-id="2c1a7-149">-SnapshotTime</span></span>
<span data-ttu-id="2c1a7-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2c1a7-150">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="2c1a7-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="2c1a7-151">-VersionId</span></span>
<span data-ttu-id="2c1a7-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="2c1a7-152">Blob VersionId</span></span>

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

### <span data-ttu-id="2c1a7-153">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2c1a7-153">-Confirm</span></span>
<span data-ttu-id="2c1a7-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c1a7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c1a7-155">-WhatIf</span></span>
<span data-ttu-id="2c1a7-156">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c1a7-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c1a7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1a7-158">CommonParameters</span></span>
<span data-ttu-id="2c1a7-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c1a7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1a7-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c1a7-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1a7-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c1a7-161">INPUTS</span></span>

### <span data-ttu-id="2c1a7-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="2c1a7-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="2c1a7-163">Azure.Storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="2c1a7-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="2c1a7-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c1a7-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2c1a7-165">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c1a7-165">OUTPUTS</span></span>

### <span data-ttu-id="2c1a7-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c1a7-166">System.Boolean</span></span>

## <span data-ttu-id="2c1a7-167">Notas</span><span class="sxs-lookup"><span data-stu-id="2c1a7-167">NOTES</span></span>

## <span data-ttu-id="2c1a7-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c1a7-168">RELATED LINKS</span></span>
