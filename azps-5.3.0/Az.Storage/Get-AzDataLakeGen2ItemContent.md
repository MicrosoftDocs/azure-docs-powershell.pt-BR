---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271335"
---
# <span data-ttu-id="2ef93-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="2ef93-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="2ef93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ef93-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef93-103">Baixar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ef93-103">Download a file.</span></span>

## <span data-ttu-id="2ef93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ef93-104">SYNTAX</span></span>

### <span data-ttu-id="2ef93-105">ReceiveManual (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ef93-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ef93-106">Hiperencanamento</span><span class="sxs-lookup"><span data-stu-id="2ef93-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ef93-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ef93-107">DESCRIPTION</span></span>
<span data-ttu-id="2ef93-108">O cmdlet **Get-AzDataLakeGen2ItemContent** baixa um arquivo em um sistema de arquivos em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2ef93-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="2ef93-109">Este cmdlet só funcionará se o namespace hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2ef93-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="2ef93-110">Esse tipo de conta pode ser criado por meio da execução do cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="2ef93-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="2ef93-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ef93-111">EXAMPLES</span></span>

### <span data-ttu-id="2ef93-112">Exemplo 1: baixar um arquivo sem avisar</span><span class="sxs-lookup"><span data-stu-id="2ef93-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="2ef93-113">Esse comando baixa um arquivo para um arquivo local sem avisar.</span><span class="sxs-lookup"><span data-stu-id="2ef93-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="2ef93-114">Exemplo 2: obter um arquivo e, em seguida, fazer o pipeline para baixar o arquivo para um arquivo local</span><span class="sxs-lookup"><span data-stu-id="2ef93-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="2ef93-115">Esse comando primeiro obtém um arquivo e, em seguida, o pipeline para baixar o arquivo para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="2ef93-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="2ef93-116">OS</span><span class="sxs-lookup"><span data-stu-id="2ef93-116">PARAMETERS</span></span>

### <span data-ttu-id="2ef93-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ef93-117">-AsJob</span></span>
<span data-ttu-id="2ef93-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2ef93-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ef93-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="2ef93-119">-CheckMd5</span></span>
<span data-ttu-id="2ef93-120">Verifique o md5sum</span><span class="sxs-lookup"><span data-stu-id="2ef93-120">check the md5sum</span></span>

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

### <span data-ttu-id="2ef93-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2ef93-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2ef93-122">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2ef93-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="2ef93-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="2ef93-123">The default value is 10.</span></span>

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

### <span data-ttu-id="2ef93-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2ef93-124">-Context</span></span>
<span data-ttu-id="2ef93-125">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="2ef93-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2ef93-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef93-126">-DefaultProfile</span></span>
<span data-ttu-id="2ef93-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ef93-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ef93-128">-Destino</span><span class="sxs-lookup"><span data-stu-id="2ef93-128">-Destination</span></span>
<span data-ttu-id="2ef93-129">Caminho do arquivo de destino local.</span><span class="sxs-lookup"><span data-stu-id="2ef93-129">Destination local file path.</span></span>

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

### <span data-ttu-id="2ef93-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="2ef93-130">-FileSystem</span></span>
<span data-ttu-id="2ef93-131">Nome do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="2ef93-131">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ef93-132">-Force</span><span class="sxs-lookup"><span data-stu-id="2ef93-132">-Force</span></span>
<span data-ttu-id="2ef93-133">Forçar a substituição do arquivo ou BLOB existente</span><span class="sxs-lookup"><span data-stu-id="2ef93-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="2ef93-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ef93-134">-InputObject</span></span>
<span data-ttu-id="2ef93-135">Objeto de item Gen2 do Azure datalake para download.</span><span class="sxs-lookup"><span data-stu-id="2ef93-135">Azure Datalake Gen2 Item Object to download.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ef93-136">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2ef93-136">-Path</span></span>
<span data-ttu-id="2ef93-137">O caminho no sistema de arquivos especificado que deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="2ef93-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="2ef93-138">Pode ser um arquivo ou diretório no formato ' diretório/file.txt ' ou ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="2ef93-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ef93-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2ef93-139">-Confirm</span></span>
<span data-ttu-id="2ef93-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ef93-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef93-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef93-141">-WhatIf</span></span>
<span data-ttu-id="2ef93-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2ef93-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ef93-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ef93-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef93-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef93-144">CommonParameters</span></span>
<span data-ttu-id="2ef93-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ef93-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef93-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ef93-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef93-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ef93-147">INPUTS</span></span>

### <span data-ttu-id="2ef93-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2ef93-148">System.String</span></span>

### <span data-ttu-id="2ef93-149">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2ef93-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="2ef93-150">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2ef93-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2ef93-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ef93-151">OUTPUTS</span></span>

### <span data-ttu-id="2ef93-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2ef93-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="2ef93-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ef93-153">NOTES</span></span>

## <span data-ttu-id="2ef93-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ef93-154">RELATED LINKS</span></span>
