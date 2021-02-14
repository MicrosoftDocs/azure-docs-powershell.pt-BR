---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111284"
---
# <span data-ttu-id="bdd20-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="bdd20-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="bdd20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdd20-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd20-103">Baixar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bdd20-103">Download a file.</span></span>

## <span data-ttu-id="bdd20-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdd20-104">SYNTAX</span></span>

### <span data-ttu-id="bdd20-105">ReceiveManual (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bdd20-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdd20-106">ItemEsqueleque</span><span class="sxs-lookup"><span data-stu-id="bdd20-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdd20-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdd20-107">DESCRIPTION</span></span>
<span data-ttu-id="bdd20-108">O cmdlet **Get-AzDataLakeGen2ItemContent** baixou um arquivo em um sistema de arquivos em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd20-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="bdd20-109">Esse cmdlet só funcionará se o Namespace Hierárquico estiver habilitado para a conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdd20-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="bdd20-110">Esse tipo de conta pode ser criado por meio do cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="bdd20-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="bdd20-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bdd20-111">EXAMPLES</span></span>

### <span data-ttu-id="bdd20-112">Exemplo 1: Baixar um arquivo sem aviso</span><span class="sxs-lookup"><span data-stu-id="bdd20-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="bdd20-113">Esse comando baixa um arquivo para um arquivo local sem aviso.</span><span class="sxs-lookup"><span data-stu-id="bdd20-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="bdd20-114">Exemplo 2: Obter um arquivo e, em seguida, pipeline para baixar o arquivo para um arquivo local</span><span class="sxs-lookup"><span data-stu-id="bdd20-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="bdd20-115">Esse comando obtém primeiro um arquivo e, em seguida, o pipeline para baixar o arquivo para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="bdd20-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="bdd20-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdd20-116">PARAMETERS</span></span>

### <span data-ttu-id="bdd20-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdd20-117">-AsJob</span></span>
<span data-ttu-id="bdd20-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bdd20-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdd20-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="bdd20-119">-CheckMd5</span></span>
<span data-ttu-id="bdd20-120">verificar a md5sum</span><span class="sxs-lookup"><span data-stu-id="bdd20-120">check the md5sum</span></span>

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

### <span data-ttu-id="bdd20-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bdd20-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bdd20-122">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bdd20-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="bdd20-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="bdd20-123">The default value is 10.</span></span>

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

### <span data-ttu-id="bdd20-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bdd20-124">-Context</span></span>
<span data-ttu-id="bdd20-125">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="bdd20-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="bdd20-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd20-126">-DefaultProfile</span></span>
<span data-ttu-id="bdd20-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd20-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdd20-128">-Destino</span><span class="sxs-lookup"><span data-stu-id="bdd20-128">-Destination</span></span>
<span data-ttu-id="bdd20-129">Caminho de arquivo local de destino.</span><span class="sxs-lookup"><span data-stu-id="bdd20-129">Destination local file path.</span></span>

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

### <span data-ttu-id="bdd20-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="bdd20-130">-FileSystem</span></span>
<span data-ttu-id="bdd20-131">Nome do Sistema de Arquivos</span><span class="sxs-lookup"><span data-stu-id="bdd20-131">FileSystem name</span></span>

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

### <span data-ttu-id="bdd20-132">-Forçar</span><span class="sxs-lookup"><span data-stu-id="bdd20-132">-Force</span></span>
<span data-ttu-id="bdd20-133">Forçar a substituir o blob ou o arquivo existente</span><span class="sxs-lookup"><span data-stu-id="bdd20-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="bdd20-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdd20-134">-InputObject</span></span>
<span data-ttu-id="bdd20-135">Objeto de item do Azure Datalake Gen2 para download.</span><span class="sxs-lookup"><span data-stu-id="bdd20-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="bdd20-136">-Caminho</span><span class="sxs-lookup"><span data-stu-id="bdd20-136">-Path</span></span>
<span data-ttu-id="bdd20-137">O caminho no sistema de arquivos especificado que deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="bdd20-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="bdd20-138">Pode ser um arquivo ou diretório no formato "diretório/file.txt" ou "diretório1/diretório2/"</span><span class="sxs-lookup"><span data-stu-id="bdd20-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="bdd20-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bdd20-139">-Confirm</span></span>
<span data-ttu-id="bdd20-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdd20-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd20-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdd20-141">-WhatIf</span></span>
<span data-ttu-id="bdd20-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bdd20-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdd20-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdd20-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd20-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd20-144">CommonParameters</span></span>
<span data-ttu-id="bdd20-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd20-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd20-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd20-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd20-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="bdd20-147">INPUTS</span></span>

### <span data-ttu-id="bdd20-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bdd20-148">System.String</span></span>

### <span data-ttu-id="bdd20-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="bdd20-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="bdd20-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bdd20-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bdd20-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="bdd20-151">OUTPUTS</span></span>

### <span data-ttu-id="bdd20-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="bdd20-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="bdd20-153">Notas</span><span class="sxs-lookup"><span data-stu-id="bdd20-153">NOTES</span></span>

## <span data-ttu-id="bdd20-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdd20-154">RELATED LINKS</span></span>
