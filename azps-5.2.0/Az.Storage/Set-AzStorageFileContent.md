---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260755"
---
# <span data-ttu-id="af798-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="af798-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="af798-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af798-102">SYNOPSIS</span></span>
<span data-ttu-id="af798-103">Carrega o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="af798-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="af798-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af798-104">SYNTAX</span></span>

### <span data-ttu-id="af798-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="af798-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="af798-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="af798-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="af798-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="af798-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="af798-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af798-108">DESCRIPTION</span></span>
<span data-ttu-id="af798-109">O cmdlet **set-AzStorageFileContent** carrega o conteúdo de um arquivo em um arquivo em um compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="af798-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="af798-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af798-110">EXAMPLES</span></span>

### <span data-ttu-id="af798-111">Exemplo 1: carregar um arquivo na pasta atual</span><span class="sxs-lookup"><span data-stu-id="af798-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="af798-112">Esse comando carrega um arquivo chamado DataFile37 na pasta atual como um arquivo chamado CurrentDataFile na pasta denominada ContosoWorkingFolderme.</span><span class="sxs-lookup"><span data-stu-id="af798-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="af798-113">Exemplo 2: carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="af798-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="af798-114">Este exemplo usa vários cmdlets comuns do Windows PowerShell e o cmdlet atual para carregar todos os arquivos da pasta atual para a pasta raiz do contêiner ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="af798-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="af798-115">O primeiro comando obtém o nome da pasta atual e a armazena na variável $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="af798-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="af798-116">O segundo comando usa o cmdlet **Get-AzStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, armazena-o na variável $container.</span><span class="sxs-lookup"><span data-stu-id="af798-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="af798-117">O comando final Obtém o conteúdo da pasta atual e passa cada um para o cmdlet Where-Object usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="af798-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="af798-118">Esse cmdlet filtra objetos que não são arquivos e, em seguida, passa os arquivos para o cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="af798-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="af798-119">Esse cmdlet executa um bloco de script para cada arquivo que cria o caminho apropriado para ele e, em seguida, usa o cmdlet atual para carregar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="af798-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="af798-120">O resultado tem o mesmo nome e a mesma posição relativa em relação aos outros arquivos que este exemplo carrega.</span><span class="sxs-lookup"><span data-stu-id="af798-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="af798-121">Para obter mais informações sobre blocos de script, digite `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="af798-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="af798-122">Exemplo 3: carregue um arquivo local em um arquivo do Azure e perpreserve as propriedades SMB do arquivo local (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo do Azure.</span><span class="sxs-lookup"><span data-stu-id="af798-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="af798-123">Este exemplo carrega um arquivo local em um arquivo do Azure e perservindo as propriedades SMB do arquivo local (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo do Azure.</span><span class="sxs-lookup"><span data-stu-id="af798-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="af798-124">OS</span><span class="sxs-lookup"><span data-stu-id="af798-124">PARAMETERS</span></span>

### <span data-ttu-id="af798-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af798-125">-AsJob</span></span>
<span data-ttu-id="af798-126">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="af798-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="af798-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="af798-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="af798-128">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="af798-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="af798-129">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="af798-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="af798-130">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="af798-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="af798-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="af798-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="af798-132">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="af798-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="af798-133">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="af798-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="af798-134">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="af798-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="af798-135">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="af798-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="af798-136">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="af798-136">The default value is 10.</span></span>

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

### <span data-ttu-id="af798-137">-Contexto</span><span class="sxs-lookup"><span data-stu-id="af798-137">-Context</span></span>
<span data-ttu-id="af798-138">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="af798-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="af798-139">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="af798-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="af798-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af798-140">-DefaultProfile</span></span>
<span data-ttu-id="af798-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af798-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af798-142">-Diretório</span><span class="sxs-lookup"><span data-stu-id="af798-142">-Directory</span></span>
<span data-ttu-id="af798-143">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="af798-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="af798-144">Esse cmdlet carrega o arquivo para a pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="af798-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="af798-145">Para obter um diretório, use o cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="af798-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="af798-146">Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="af798-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af798-147">-Force</span><span class="sxs-lookup"><span data-stu-id="af798-147">-Force</span></span>
<span data-ttu-id="af798-148">Indica que esse cmdlet substitui um arquivo de armazenamento do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="af798-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="af798-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af798-149">-PassThru</span></span>
<span data-ttu-id="af798-150">Indica que esse cmdlet retorna o objeto **AzureStorageFile** que ele cria ou carrega.</span><span class="sxs-lookup"><span data-stu-id="af798-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="af798-151">-Caminho</span><span class="sxs-lookup"><span data-stu-id="af798-151">-Path</span></span>
<span data-ttu-id="af798-152">Especifica o caminho de um arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="af798-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="af798-153">Esse cmdlet carrega o conteúdo para o arquivo que esse parâmetro especifica ou para um arquivo na pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="af798-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="af798-154">Se você especificar uma pasta, esse cmdlet criará um arquivo com o mesmo nome do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="af798-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="af798-155">Se você especificar um caminho para um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo nesse arquivo.</span><span class="sxs-lookup"><span data-stu-id="af798-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="af798-156">Se você especificar um arquivo que já existe e especificar o parâmetro _Force_ , esse cmdlet substituirá o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="af798-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="af798-157">Se você especificar um arquivo que já existe e não especificar _Force_, esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="af798-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="af798-158">Se você especificar um caminho para uma pasta que não existe, esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="af798-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="af798-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="af798-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="af798-160">Mantenha as propriedades SMB do arquivo de origem (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="af798-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="af798-161">Este parâmetro só está disponível no Windows.</span><span class="sxs-lookup"><span data-stu-id="af798-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="af798-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="af798-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="af798-163">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="af798-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="af798-164">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="af798-164">-Share</span></span>
<span data-ttu-id="af798-165">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="af798-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="af798-166">Esse cmdlet é carregado em um arquivo no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="af798-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="af798-167">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="af798-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="af798-168">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="af798-168">This object contains the storage context.</span></span>
<span data-ttu-id="af798-169">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="af798-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af798-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="af798-170">-ShareName</span></span>
<span data-ttu-id="af798-171">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="af798-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="af798-172">Esse cmdlet é carregado em um arquivo no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="af798-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="af798-173">-Fonte</span><span class="sxs-lookup"><span data-stu-id="af798-173">-Source</span></span>
<span data-ttu-id="af798-174">Especifica o arquivo de origem que esse cmdlet carregará.</span><span class="sxs-lookup"><span data-stu-id="af798-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="af798-175">Se você especificar um arquivo que não existe, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="af798-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af798-176">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af798-176">-Confirm</span></span>
<span data-ttu-id="af798-177">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af798-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af798-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af798-178">-WhatIf</span></span>
<span data-ttu-id="af798-179">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af798-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af798-180">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af798-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af798-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af798-181">CommonParameters</span></span>
<span data-ttu-id="af798-182">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af798-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af798-183">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af798-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af798-184">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af798-184">INPUTS</span></span>

### <span data-ttu-id="af798-185">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="af798-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="af798-186">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="af798-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="af798-187">System. String</span><span class="sxs-lookup"><span data-stu-id="af798-187">System.String</span></span>

### <span data-ttu-id="af798-188">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="af798-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="af798-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af798-189">OUTPUTS</span></span>

### <span data-ttu-id="af798-190">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="af798-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="af798-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af798-191">NOTES</span></span>

## <span data-ttu-id="af798-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af798-192">RELATED LINKS</span></span>

[<span data-ttu-id="af798-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="af798-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="af798-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="af798-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="af798-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="af798-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
