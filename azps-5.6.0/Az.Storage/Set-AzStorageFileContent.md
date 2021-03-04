---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 597728b1b327da28495574ca865a2e75a1a774a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888156"
---
# <span data-ttu-id="763f7-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="763f7-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="763f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="763f7-102">SYNOPSIS</span></span>
<span data-ttu-id="763f7-103">Carrega o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="763f7-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="763f7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="763f7-104">SYNTAX</span></span>

### <span data-ttu-id="763f7-105">ShareName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="763f7-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="763f7-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="763f7-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="763f7-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="763f7-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="763f7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="763f7-108">DESCRIPTION</span></span>
<span data-ttu-id="763f7-109">O cmdlet **Set-AzStorageFileContent** carrega o conteúdo de um arquivo em um arquivo em um compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="763f7-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="763f7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="763f7-110">EXAMPLES</span></span>

### <span data-ttu-id="763f7-111">Exemplo 1: Carregar um arquivo na pasta atual</span><span class="sxs-lookup"><span data-stu-id="763f7-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="763f7-112">Esse comando carrega um arquivo chamado DataFile37 na pasta atual como um arquivo chamado CurrentDataFile na pasta chamada ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="763f7-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="763f7-113">Exemplo 2: Carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="763f7-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="763f7-114">Este exemplo usa vários cmdlets Windows PowerShell comuns e o cmdlet atual para carregar todos os arquivos da pasta atual para a pasta raiz do contêiner ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="763f7-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="763f7-115">O primeiro comando obtém o nome da pasta atual e armazena-a na variável $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="763f7-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="763f7-116">O segundo comando usa o cmdlet **Get-AzStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, o armazena na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="763f7-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="763f7-117">O comando final obtém o conteúdo da pasta atual e passa cada um para o cmdlet Where-Object usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="763f7-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="763f7-118">Esse cmdlet filtra objetos que não são arquivos e passa os arquivos para o cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="763f7-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="763f7-119">Esse cmdlet executa um bloco de script para cada arquivo que cria o caminho apropriado para ele e usa o cmdlet atual para carregar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="763f7-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="763f7-120">O resultado tem o mesmo nome e mesma posição relativa em relação aos outros arquivos que este exemplo carrega.</span><span class="sxs-lookup"><span data-stu-id="763f7-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="763f7-121">Para obter mais informações sobre blocos de script, digite `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="763f7-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="763f7-122">Exemplo 3: carregue um arquivo local em um arquivo do Azure e mantenha as propriedades SMB de arquivo locais (Atribuições de Arquivo, Hora de Criação de Arquivo, Última Gravação de Arquivo) no arquivo do Azure.</span><span class="sxs-lookup"><span data-stu-id="763f7-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="763f7-123">Este exemplo carrega um arquivo local em um arquivo do Azure e preserva as propriedades SMB de arquivo locais (Atribuições de Arquivo, Hora de Criação de Arquivo, Última Gravação de Arquivo) no arquivo do Azure.</span><span class="sxs-lookup"><span data-stu-id="763f7-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="763f7-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="763f7-124">PARAMETERS</span></span>

### <span data-ttu-id="763f7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="763f7-125">-AsJob</span></span>
<span data-ttu-id="763f7-126">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="763f7-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="763f7-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="763f7-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="763f7-128">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="763f7-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="763f7-129">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="763f7-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="763f7-130">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="763f7-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="763f7-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="763f7-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="763f7-132">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="763f7-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="763f7-133">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="763f7-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="763f7-134">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="763f7-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="763f7-135">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="763f7-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="763f7-136">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="763f7-136">The default value is 10.</span></span>

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

### <span data-ttu-id="763f7-137">-Context</span><span class="sxs-lookup"><span data-stu-id="763f7-137">-Context</span></span>
<span data-ttu-id="763f7-138">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="763f7-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="763f7-139">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="763f7-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="763f7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763f7-140">-DefaultProfile</span></span>
<span data-ttu-id="763f7-141">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="763f7-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="763f7-142">-Directory</span><span class="sxs-lookup"><span data-stu-id="763f7-142">-Directory</span></span>
<span data-ttu-id="763f7-143">Especifica uma pasta como um **objeto CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="763f7-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="763f7-144">Este cmdlet carrega o arquivo na pasta especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="763f7-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="763f7-145">Para obter um diretório, use o New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="763f7-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="763f7-146">Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="763f7-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="763f7-147">-Force</span><span class="sxs-lookup"><span data-stu-id="763f7-147">-Force</span></span>
<span data-ttu-id="763f7-148">Indica que esse cmdlet substitui um arquivo de armazenamento do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="763f7-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="763f7-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="763f7-149">-PassThru</span></span>
<span data-ttu-id="763f7-150">Indica que esse cmdlet retorna o **objeto AzureStorageFile** que ele cria ou carrega.</span><span class="sxs-lookup"><span data-stu-id="763f7-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="763f7-151">-Path</span><span class="sxs-lookup"><span data-stu-id="763f7-151">-Path</span></span>
<span data-ttu-id="763f7-152">Especifica o caminho de um arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="763f7-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="763f7-153">Este cmdlet carrega conteúdo no arquivo especificado por esse parâmetro ou em um arquivo na pasta especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="763f7-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="763f7-154">Se você especificar uma pasta, esse cmdlet criará um arquivo com o mesmo nome do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="763f7-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="763f7-155">Se você especificar um caminho de um arquivo que não existe, esse cmdlet criará esse arquivo e salvará o conteúdo nesse arquivo.</span><span class="sxs-lookup"><span data-stu-id="763f7-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="763f7-156">Se você especificar um arquivo que já existe e especificar o parâmetro _Force,_ esse cmdlet substituirá o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="763f7-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="763f7-157">Se você especificar um arquivo que já existe e não especificar _Force,_ esse cmdlet não fará alterações e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="763f7-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="763f7-158">Se você especificar um caminho de uma pasta que não existe, esse cmdlet não fará alterações e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="763f7-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="763f7-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="763f7-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="763f7-160">Mantenha as propriedades SMB de arquivo de origem (Atribuições de Arquivo, Hora da Criação de Arquivo, Hora da Última Gravação do Arquivo) no Arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="763f7-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="763f7-161">Esse parâmetro só está disponível no Windows.</span><span class="sxs-lookup"><span data-stu-id="763f7-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="763f7-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="763f7-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="763f7-163">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="763f7-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="763f7-164">-Share</span><span class="sxs-lookup"><span data-stu-id="763f7-164">-Share</span></span>
<span data-ttu-id="763f7-165">Especifica um **objeto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="763f7-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="763f7-166">Este cmdlet é carregado em um arquivo no compartilhamento de arquivos especificado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="763f7-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="763f7-167">Para obter um **objeto CloudFileShare,** use Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="763f7-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="763f7-168">Este objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="763f7-168">This object contains the storage context.</span></span>
<span data-ttu-id="763f7-169">Se você especificar esse parâmetro, não especifique o *parâmetro Context.*</span><span class="sxs-lookup"><span data-stu-id="763f7-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="763f7-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="763f7-170">-ShareName</span></span>
<span data-ttu-id="763f7-171">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="763f7-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="763f7-172">Este cmdlet é carregado em um arquivo no compartilhamento de arquivos especificado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="763f7-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="763f7-173">-Source</span><span class="sxs-lookup"><span data-stu-id="763f7-173">-Source</span></span>
<span data-ttu-id="763f7-174">Especifica o arquivo de origem que esse cmdlet carrega.</span><span class="sxs-lookup"><span data-stu-id="763f7-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="763f7-175">Se você especificar um arquivo que não existe, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="763f7-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="763f7-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="763f7-176">-Confirm</span></span>
<span data-ttu-id="763f7-177">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="763f7-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="763f7-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="763f7-178">-WhatIf</span></span>
<span data-ttu-id="763f7-179">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="763f7-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="763f7-180">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="763f7-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="763f7-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763f7-181">CommonParameters</span></span>
<span data-ttu-id="763f7-182">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="763f7-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763f7-183">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="763f7-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763f7-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="763f7-184">INPUTS</span></span>

### <span data-ttu-id="763f7-185">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="763f7-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="763f7-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="763f7-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="763f7-187">System.String</span><span class="sxs-lookup"><span data-stu-id="763f7-187">System.String</span></span>

### <span data-ttu-id="763f7-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="763f7-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="763f7-189">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="763f7-189">OUTPUTS</span></span>

### <span data-ttu-id="763f7-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="763f7-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="763f7-191">NOTES</span><span class="sxs-lookup"><span data-stu-id="763f7-191">NOTES</span></span>

## <span data-ttu-id="763f7-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="763f7-192">RELATED LINKS</span></span>

[<span data-ttu-id="763f7-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="763f7-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="763f7-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="763f7-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="763f7-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="763f7-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
