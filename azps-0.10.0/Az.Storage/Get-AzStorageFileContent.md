---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776263"
---
# <span data-ttu-id="63f51-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="63f51-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="63f51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63f51-102">SYNOPSIS</span></span>
<span data-ttu-id="63f51-103">Baixa o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="63f51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63f51-104">SYNTAX</span></span>

### <span data-ttu-id="63f51-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="63f51-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63f51-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="63f51-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63f51-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="63f51-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63f51-108">Arquivos</span><span class="sxs-lookup"><span data-stu-id="63f51-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63f51-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63f51-109">DESCRIPTION</span></span>
<span data-ttu-id="63f51-110">O cmdlet **Get-AzStorageFileContent** faz o download do conteúdo de um arquivo e, em seguida, o salva em um destino que você especificar.</span><span class="sxs-lookup"><span data-stu-id="63f51-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="63f51-111">Esse cmdlet não retorna o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="63f51-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63f51-112">EXAMPLES</span></span>

### <span data-ttu-id="63f51-113">Exemplo 1: baixar um arquivo de uma pasta</span><span class="sxs-lookup"><span data-stu-id="63f51-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="63f51-114">Esse comando baixa um arquivo chamado CurrentDataFile na pasta ContosoWorkingFolder do compartilhamento de arquivos ContosoShare06 para a pasta atual.</span><span class="sxs-lookup"><span data-stu-id="63f51-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="63f51-115">Exemplo 2: baixar os arquivos em compartilhamento de arquivo de exemplo</span><span class="sxs-lookup"><span data-stu-id="63f51-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="63f51-116">Este exemplo baixa os arquivos em um exemplo de compartilhamento de arquivo</span><span class="sxs-lookup"><span data-stu-id="63f51-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="63f51-117">OS</span><span class="sxs-lookup"><span data-stu-id="63f51-117">PARAMETERS</span></span>

### <span data-ttu-id="63f51-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="63f51-118">-CheckMd5</span></span>
<span data-ttu-id="63f51-119">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="63f51-120">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="63f51-121">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="63f51-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="63f51-122">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="63f51-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="63f51-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="63f51-124">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="63f51-125">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="63f51-126">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="63f51-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="63f51-127">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="63f51-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="63f51-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="63f51-129">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="63f51-130">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="63f51-131">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="63f51-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="63f51-132">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="63f51-133">-Contexto</span><span class="sxs-lookup"><span data-stu-id="63f51-133">-Context</span></span>
<span data-ttu-id="63f51-134">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="63f51-135">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="63f51-136">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="63f51-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="63f51-137">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f51-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f51-138">-DefaultProfile</span></span>
<span data-ttu-id="63f51-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f51-140">-Destino</span><span class="sxs-lookup"><span data-stu-id="63f51-140">-Destination</span></span>
<span data-ttu-id="63f51-141">Especifica o caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="63f51-141">Specifies the destination path.</span></span>
<span data-ttu-id="63f51-142">Esse cmdlet baixa o conteúdo do arquivo para o local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="63f51-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="63f51-143">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="63f51-144">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="63f51-145">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="63f51-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="63f51-146">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f51-147">-Diretório</span><span class="sxs-lookup"><span data-stu-id="63f51-147">-Directory</span></span>
<span data-ttu-id="63f51-148">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="63f51-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="63f51-149">Esse cmdlet obtém conteúdo para um arquivo na pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="63f51-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="63f51-150">Para obter um diretório, use o cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="63f51-150">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="63f51-151">Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="63f51-151">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f51-152">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="63f51-152">-File</span></span>
<span data-ttu-id="63f51-153">Especifica um arquivo como um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="63f51-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="63f51-154">Esse cmdlet obtém o arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="63f51-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="63f51-155">Para obter um objeto **cloudfile** , use o cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="63f51-155">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f51-156">-Force</span><span class="sxs-lookup"><span data-stu-id="63f51-156">-Force</span></span>
<span data-ttu-id="63f51-157">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="63f51-158">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="63f51-159">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="63f51-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="63f51-160">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="63f51-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63f51-161">-PassThru</span></span>
<span data-ttu-id="63f51-162">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="63f51-163">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="63f51-164">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="63f51-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="63f51-165">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="63f51-166">-Caminho</span><span class="sxs-lookup"><span data-stu-id="63f51-166">-Path</span></span>
<span data-ttu-id="63f51-167">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-167">Specifies the path of a file.</span></span>
<span data-ttu-id="63f51-168">Esse cmdlet obtém o conteúdo do arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="63f51-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="63f51-169">Se o arquivo não existir, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="63f51-169">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f51-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="63f51-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="63f51-171">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="63f51-172">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f51-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="63f51-173">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="63f51-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="63f51-174">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63f51-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="63f51-175">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="63f51-175">-Share</span></span>
<span data-ttu-id="63f51-176">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="63f51-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="63f51-177">Esse cmdlet baixa o conteúdo do arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="63f51-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="63f51-178">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="63f51-178">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="63f51-179">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="63f51-179">This object contains the storage context.</span></span>
<span data-ttu-id="63f51-180">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="63f51-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f51-181">-ShareName</span><span class="sxs-lookup"><span data-stu-id="63f51-181">-ShareName</span></span>
<span data-ttu-id="63f51-182">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="63f51-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="63f51-183">Esse cmdlet baixa o conteúdo do arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="63f51-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f51-184">-Confirme</span><span class="sxs-lookup"><span data-stu-id="63f51-184">-Confirm</span></span>
<span data-ttu-id="63f51-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f51-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f51-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f51-186">-WhatIf</span></span>
<span data-ttu-id="63f51-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63f51-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f51-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63f51-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f51-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f51-189">CommonParameters</span></span>
<span data-ttu-id="63f51-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f51-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f51-191">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63f51-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f51-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63f51-192">INPUTS</span></span>

### <span data-ttu-id="63f51-193">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="63f51-193">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="63f51-194">Parâmetros: share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63f51-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="63f51-195">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="63f51-195">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="63f51-196">Parâmetros: diretório (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63f51-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="63f51-197">Microsoft. WindowsAz. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="63f51-197">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="63f51-198">Parâmetros: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63f51-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="63f51-199">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="63f51-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="63f51-200">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63f51-200">OUTPUTS</span></span>

### <span data-ttu-id="63f51-201">Microsoft. WindowsAz. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="63f51-201">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="63f51-202">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63f51-202">NOTES</span></span>

## <span data-ttu-id="63f51-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63f51-203">RELATED LINKS</span></span>

[<span data-ttu-id="63f51-204">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="63f51-204">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="63f51-205">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="63f51-205">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


