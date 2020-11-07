---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942439"
---
# <span data-ttu-id="e2791-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="e2791-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="e2791-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2791-102">SYNOPSIS</span></span>
<span data-ttu-id="e2791-103">Cria um arquivo de recursos para uso `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="e2791-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="e2791-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2791-104">SYNTAX</span></span>

### <span data-ttu-id="e2791-105">HttpUrl (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2791-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2791-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="e2791-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2791-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="e2791-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2791-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2791-108">DESCRIPTION</span></span>
<span data-ttu-id="e2791-109">Cria um arquivo de recursos para uso `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="e2791-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="e2791-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2791-110">EXAMPLES</span></span>

### <span data-ttu-id="e2791-111">Exemplo 1: criar um arquivo de recurso a partir de uma URL HTTP apontando para um único arquivo</span><span class="sxs-lookup"><span data-stu-id="e2791-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e2791-112">Cria uma `PSResourceFile` referência a uma URL http.</span><span class="sxs-lookup"><span data-stu-id="e2791-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="e2791-113">Exemplo 2: criar um arquivo de recursos a partir de uma URL do contêiner de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="e2791-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e2791-114">Cria uma `PSResourceFile` referência a uma URL do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2791-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="e2791-115">Todos os arquivos no contêiner serão baixados para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="e2791-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="e2791-116">Exemplo 3: criar um arquivo de recurso a partir de um nome de contêiner de armazenamento automático</span><span class="sxs-lookup"><span data-stu-id="e2791-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e2791-117">Cria uma `PSResourceFile` referência a um nome de contêiner de armazenamento automático.</span><span class="sxs-lookup"><span data-stu-id="e2791-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="e2791-118">Todos os arquivos no contêiner serão baixados para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="e2791-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="e2791-119">OS</span><span class="sxs-lookup"><span data-stu-id="e2791-119">PARAMETERS</span></span>

### <span data-ttu-id="e2791-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="e2791-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="e2791-121">O nome do contêiner de armazenamento na conta de armazenamento automático.</span><span class="sxs-lookup"><span data-stu-id="e2791-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2791-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="e2791-122">-BlobPrefix</span></span>
<span data-ttu-id="e2791-123">Obtém o prefixo de blob a ser usado ao baixar blobs de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2791-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="e2791-124">Somente os BLOBs cujos nomes começam com o prefixo especificado serão baixados.</span><span class="sxs-lookup"><span data-stu-id="e2791-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="e2791-125">Esse prefixo pode ser um nome de arquivo parcial ou um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="e2791-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="e2791-126">Se um prefixo não for especificado, todos os arquivos no contêiner serão baixados.</span><span class="sxs-lookup"><span data-stu-id="e2791-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2791-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2791-127">-DefaultProfile</span></span>
<span data-ttu-id="e2791-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2791-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2791-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="e2791-129">-FileMode</span></span>
<span data-ttu-id="e2791-130">Obtém o atributo do modo de permissão de arquivo em formato octal.</span><span class="sxs-lookup"><span data-stu-id="e2791-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="e2791-131">Essa propriedade é aplicável apenas se o arquivo de recurso é baixado para um nó Linux.</span><span class="sxs-lookup"><span data-stu-id="e2791-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="e2791-132">Se essa propriedade não for especificada para um nó Linux, o valor padrão será 0770.</span><span class="sxs-lookup"><span data-stu-id="e2791-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="e2791-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e2791-133">-FilePath</span></span>
<span data-ttu-id="e2791-134">O local no nó de computação para o qual baixar o (s) arquivo (s), em relação ao diretório de trabalho da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e2791-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="e2791-135">Se o parâmetro HttpUrl for especificado, o FilePath será necessário e descreverá o caminho para o qual o arquivo será baixado, incluindo o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2791-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="e2791-136">Caso contrário, se os parâmetros AutoStorageContainerName ou StorageContainerUrl forem especificados, FilePath será opcional e será o diretório para o qual baixar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="e2791-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="e2791-137">Caso o FilePath seja usado como um diretório, qualquer estrutura de diretório já associada aos dados de entrada será mantida em total e acrescentada ao diretório FilePath especificado.</span><span class="sxs-lookup"><span data-stu-id="e2791-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="e2791-138">O caminho relativo especificado não pode ser desfeito do diretório de trabalho da tarefa (por exemplo, usando '.. ').</span><span class="sxs-lookup"><span data-stu-id="e2791-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2791-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="e2791-139">-HttpUrl</span></span>
<span data-ttu-id="e2791-140">A URL do arquivo a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="e2791-140">The URL of the file to download.</span></span>
<span data-ttu-id="e2791-141">Se a URL for Azure Blob Storage, ela deverá ser legível usando o acesso anônimo; ou seja, o serviço em lotes não apresenta nenhuma credencial durante o download do blob.</span><span class="sxs-lookup"><span data-stu-id="e2791-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="e2791-142">Há duas maneiras de obter tal URL para um blob no armazenamento do Azure: inclua uma assinatura de acesso compartilhado (SAS) que conceda permissões de leitura ao BLOB ou defina a ACL para o BLOB ou seu contêiner para permitir acesso público.</span><span class="sxs-lookup"><span data-stu-id="e2791-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2791-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="e2791-143">-StorageContainerUrl</span></span>
<span data-ttu-id="e2791-144">A URL do contêiner de blob no armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2791-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="e2791-145">Esta URL deve ser legível e ser listada usando o acesso anônimo; ou seja, o serviço em lotes não apresenta nenhuma credencial durante o download de BLOBs do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e2791-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="e2791-146">Há duas maneiras de obter tal URL para um contêiner no armazenamento do Azure: inclua uma assinatura de acesso compartilhado (SAS) que conceda permissões de leitura no contêiner ou defina a ACL do contêiner para permitir acesso público.</span><span class="sxs-lookup"><span data-stu-id="e2791-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2791-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2791-147">CommonParameters</span></span>
<span data-ttu-id="e2791-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2791-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2791-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2791-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2791-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2791-150">INPUTS</span></span>

### <span data-ttu-id="e2791-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e2791-151">None</span></span>

## <span data-ttu-id="e2791-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2791-152">OUTPUTS</span></span>

### <span data-ttu-id="e2791-153">Microsoft.Azure.Commands.Batch. Modelos. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="e2791-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="e2791-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2791-154">NOTES</span></span>

## <span data-ttu-id="e2791-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2791-155">RELATED LINKS</span></span>

[<span data-ttu-id="e2791-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e2791-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)