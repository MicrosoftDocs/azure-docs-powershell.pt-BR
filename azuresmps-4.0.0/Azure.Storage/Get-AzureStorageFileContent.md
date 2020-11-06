---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
ms.openlocfilehash: c945838d7d237fb37610d3763525b0ecac838fbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426156"
---
# <span data-ttu-id="5e85d-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5e85d-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="5e85d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e85d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e85d-103">Baixa o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="5e85d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e85d-104">SYNTAX</span></span>

### <span data-ttu-id="5e85d-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e85d-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e85d-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="5e85d-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e85d-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="5e85d-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e85d-108">Arquivos</span><span class="sxs-lookup"><span data-stu-id="5e85d-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e85d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e85d-109">DESCRIPTION</span></span>
<span data-ttu-id="5e85d-110">O cmdlet **Get-AzureStorageFileContent** faz o download do conteúdo de um arquivo e, em seguida, o salva em um destino que você especificar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="5e85d-111">Esse cmdlet não retorna o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="5e85d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e85d-112">EXAMPLES</span></span>

### <span data-ttu-id="5e85d-113">Exemplo 1: baixar um arquivo de uma pasta</span><span class="sxs-lookup"><span data-stu-id="5e85d-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="5e85d-114">Esse comando baixa um arquivo chamado CurrentDataFile na pasta ContosoWorkingFolder do compartilhamento de arquivos ContosoShare06 para a pasta atual.</span><span class="sxs-lookup"><span data-stu-id="5e85d-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

## <span data-ttu-id="5e85d-115">OS</span><span class="sxs-lookup"><span data-stu-id="5e85d-115">PARAMETERS</span></span>

### <span data-ttu-id="5e85d-116">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="5e85d-116">-CheckMd5</span></span>
<span data-ttu-id="5e85d-117">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-117">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5e85d-118">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-118">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5e85d-119">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-119">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="5e85d-120">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e85d-120">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5e85d-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5e85d-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5e85d-122">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-122">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5e85d-123">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-123">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5e85d-124">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-124">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="5e85d-125">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e85d-125">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5e85d-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5e85d-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5e85d-127">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-127">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5e85d-128">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-128">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5e85d-129">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-129">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="5e85d-130">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e85d-130">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5e85d-131">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5e85d-131">-Context</span></span>
<span data-ttu-id="5e85d-132">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-132">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5e85d-133">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-133">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5e85d-134">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-134">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="5e85d-135">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e85d-135">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e85d-136">-Destino</span><span class="sxs-lookup"><span data-stu-id="5e85d-136">-Destination</span></span>
<span data-ttu-id="5e85d-137">Especifica o caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="5e85d-137">Specifies the destination path.</span></span>
<span data-ttu-id="5e85d-138">Esse cmdlet baixa o conteúdo do arquivo para o local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5e85d-138">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="5e85d-139">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-139">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5e85d-140">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-140">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5e85d-141">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-141">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="5e85d-142">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e85d-142">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e85d-143">-Diretório</span><span class="sxs-lookup"><span data-stu-id="5e85d-143">-Directory</span></span>
<span data-ttu-id="5e85d-144">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="5e85d-144">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="5e85d-145">Esse cmdlet obtém conteúdo para um arquivo na pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5e85d-145">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="5e85d-146">Para obter um diretório, use o cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="5e85d-146">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="5e85d-147">Você também pode usar o cmdlet Get-AzureStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="5e85d-147">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e85d-148">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="5e85d-148">-File</span></span>
<span data-ttu-id="5e85d-149">Especifica um arquivo como um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="5e85d-149">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="5e85d-150">Esse cmdlet obtém o arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5e85d-150">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="5e85d-151">Para obter um objeto **cloudfile** , use o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="5e85d-151">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e85d-152">-Force</span><span class="sxs-lookup"><span data-stu-id="5e85d-152">-Force</span></span>
<span data-ttu-id="5e85d-153">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-153">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5e85d-154">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-154">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5e85d-155">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-155">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="5e85d-156">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e85d-156">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5e85d-157">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e85d-157">-PassThru</span></span>
<span data-ttu-id="5e85d-158">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-158">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5e85d-159">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-159">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5e85d-160">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-160">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="5e85d-161">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e85d-161">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5e85d-162">-Caminho</span><span class="sxs-lookup"><span data-stu-id="5e85d-162">-Path</span></span>
<span data-ttu-id="5e85d-163">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-163">Specifies the path of a file.</span></span>
<span data-ttu-id="5e85d-164">Esse cmdlet obtém o conteúdo do arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5e85d-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="5e85d-165">Se o arquivo não existir, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5e85d-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e85d-166">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5e85d-166">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5e85d-167">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-167">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5e85d-168">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e85d-168">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5e85d-169">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5e85d-169">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="5e85d-170">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e85d-170">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5e85d-171">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="5e85d-171">-Share</span></span>
<span data-ttu-id="5e85d-172">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="5e85d-172">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="5e85d-173">Esse cmdlet baixa o conteúdo do arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5e85d-173">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="5e85d-174">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="5e85d-174">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="5e85d-175">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5e85d-175">This object contains the storage context.</span></span>
<span data-ttu-id="5e85d-176">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="5e85d-176">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e85d-177">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5e85d-177">-ShareName</span></span>
<span data-ttu-id="5e85d-178">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5e85d-178">Specifies the name of the file share.</span></span>
<span data-ttu-id="5e85d-179">Esse cmdlet baixa o conteúdo do arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5e85d-179">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e85d-180">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e85d-180">-Confirm</span></span>
<span data-ttu-id="5e85d-181">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e85d-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e85d-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e85d-182">-WhatIf</span></span>
<span data-ttu-id="5e85d-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e85d-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e85d-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e85d-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e85d-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e85d-185">CommonParameters</span></span>
<span data-ttu-id="5e85d-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e85d-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e85d-187">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e85d-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e85d-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e85d-188">INPUTS</span></span>

## <span data-ttu-id="5e85d-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e85d-189">OUTPUTS</span></span>

## <span data-ttu-id="5e85d-190">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e85d-190">NOTES</span></span>

## <span data-ttu-id="5e85d-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e85d-191">RELATED LINKS</span></span>

[<span data-ttu-id="5e85d-192">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="5e85d-192">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="5e85d-193">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5e85d-193">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


