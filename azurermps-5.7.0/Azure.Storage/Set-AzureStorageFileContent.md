---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 5f2aed68aea9f97b3dd66a5322d332d4666c081e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610961"
---
# <span data-ttu-id="963fc-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="963fc-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="963fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="963fc-102">SYNOPSIS</span></span>
<span data-ttu-id="963fc-103">Carrega o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="963fc-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="963fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="963fc-104">SYNTAX</span></span>

### <span data-ttu-id="963fc-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="963fc-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="963fc-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="963fc-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="963fc-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="963fc-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="963fc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="963fc-108">DESCRIPTION</span></span>
<span data-ttu-id="963fc-109">O cmdlet **set-AzureStorageFileContent** carrega o conteúdo de um arquivo em um arquivo em um compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="963fc-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="963fc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="963fc-110">EXAMPLES</span></span>

### <span data-ttu-id="963fc-111">Exemplo 1: carregar um arquivo na pasta atual</span><span class="sxs-lookup"><span data-stu-id="963fc-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="963fc-112">Esse comando carrega um arquivo chamado DataFile37 na pasta atual como um arquivo chamado CurrentDataFile na pasta denominada ContosoWorkingFolderme.</span><span class="sxs-lookup"><span data-stu-id="963fc-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="963fc-113">Exemplo 2: carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="963fc-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="963fc-114">Este exemplo usa vários cmdlets comuns do Windows PowerShell e o cmdlet atual para carregar todos os arquivos da pasta atual para a pasta raiz do contêiner ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="963fc-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="963fc-115">O primeiro comando obtém o nome da pasta atual e a armazena na variável $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="963fc-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="963fc-116">O segundo comando usa o cmdlet **Get-AzureStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, armazena-o na variável $container.</span><span class="sxs-lookup"><span data-stu-id="963fc-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="963fc-117">O comando final Obtém o conteúdo da pasta atual e passa cada um para o cmdlet Where-Object usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="963fc-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="963fc-118">Esse cmdlet filtra objetos que não são arquivos e, em seguida, passa os arquivos para o cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="963fc-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="963fc-119">Esse cmdlet executa um bloco de script para cada arquivo que cria o caminho apropriado para ele e, em seguida, usa o cmdlet atual para carregar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="963fc-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="963fc-120">O resultado tem o mesmo nome e a mesma posição relativa em relação aos outros arquivos que este exemplo carrega.</span><span class="sxs-lookup"><span data-stu-id="963fc-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="963fc-121">Para obter mais informações sobre blocos de script, digite `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="963fc-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="963fc-122">OS</span><span class="sxs-lookup"><span data-stu-id="963fc-122">PARAMETERS</span></span>

### <span data-ttu-id="963fc-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="963fc-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="963fc-124">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="963fc-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="963fc-125">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="963fc-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="963fc-126">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="963fc-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="963fc-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="963fc-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="963fc-128">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="963fc-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="963fc-129">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="963fc-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="963fc-130">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="963fc-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="963fc-131">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="963fc-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="963fc-132">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="963fc-132">The default value is 10.</span></span>

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

### <span data-ttu-id="963fc-133">-Contexto</span><span class="sxs-lookup"><span data-stu-id="963fc-133">-Context</span></span>
<span data-ttu-id="963fc-134">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="963fc-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="963fc-135">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="963fc-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="963fc-136">-Diretório</span><span class="sxs-lookup"><span data-stu-id="963fc-136">-Directory</span></span>
<span data-ttu-id="963fc-137">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="963fc-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="963fc-138">Esse cmdlet carrega o arquivo para a pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="963fc-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="963fc-139">Para obter um diretório, use o cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="963fc-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="963fc-140">Você também pode usar o cmdlet Get-AzureStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="963fc-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="963fc-141">-Force</span><span class="sxs-lookup"><span data-stu-id="963fc-141">-Force</span></span>
<span data-ttu-id="963fc-142">Indica que esse cmdlet substitui um arquivo de armazenamento do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="963fc-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="963fc-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="963fc-143">-PassThru</span></span>
<span data-ttu-id="963fc-144">Indica que esse cmdlet retorna o objeto **AzureStorageFile** que ele cria ou carrega.</span><span class="sxs-lookup"><span data-stu-id="963fc-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="963fc-145">-Caminho</span><span class="sxs-lookup"><span data-stu-id="963fc-145">-Path</span></span>
<span data-ttu-id="963fc-146">Especifica o caminho de um arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="963fc-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="963fc-147">Esse cmdlet carrega o conteúdo para o arquivo que esse parâmetro especifica ou para um arquivo na pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="963fc-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="963fc-148">Se você especificar uma pasta, esse cmdlet criará um arquivo com o mesmo nome do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="963fc-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="963fc-149">Se você especificar um caminho para um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo nesse arquivo.</span><span class="sxs-lookup"><span data-stu-id="963fc-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="963fc-150">Se você especificar um arquivo que já existe e especificar o parâmetro _Force_ , esse cmdlet substituirá o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="963fc-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="963fc-151">Se você especificar um arquivo que já existe e não especificar _Force_ , esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="963fc-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="963fc-152">Se você especificar um caminho para uma pasta que não existe, esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="963fc-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


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

### <span data-ttu-id="963fc-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="963fc-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="963fc-154">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="963fc-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="963fc-155">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="963fc-155">-Share</span></span>
<span data-ttu-id="963fc-156">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="963fc-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="963fc-157">Esse cmdlet é carregado em um arquivo no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="963fc-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="963fc-158">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="963fc-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="963fc-159">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="963fc-159">This object contains the storage context.</span></span>
<span data-ttu-id="963fc-160">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="963fc-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="963fc-161">-ShareName</span><span class="sxs-lookup"><span data-stu-id="963fc-161">-ShareName</span></span>
<span data-ttu-id="963fc-162">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="963fc-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="963fc-163">Esse cmdlet é carregado em um arquivo no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="963fc-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="963fc-164">-Fonte</span><span class="sxs-lookup"><span data-stu-id="963fc-164">-Source</span></span>
<span data-ttu-id="963fc-165">Especifica o arquivo de origem que esse cmdlet carregará.</span><span class="sxs-lookup"><span data-stu-id="963fc-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="963fc-166">Se você especificar um arquivo que não existe, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="963fc-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="963fc-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="963fc-167">-Confirm</span></span>
<span data-ttu-id="963fc-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="963fc-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="963fc-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="963fc-169">-WhatIf</span></span>
<span data-ttu-id="963fc-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="963fc-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="963fc-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="963fc-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="963fc-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963fc-172">CommonParameters</span></span>
<span data-ttu-id="963fc-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="963fc-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963fc-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="963fc-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963fc-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="963fc-175">INPUTS</span></span>

### <span data-ttu-id="963fc-176">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="963fc-176">IStorageContext</span></span>

<span data-ttu-id="963fc-177">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="963fc-177">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="963fc-178">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="963fc-178">CloudFileDirectory</span></span>

<span data-ttu-id="963fc-179">O parâmetro ' Directory ' aceita o valor do tipo ' CloudFileDirectory ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="963fc-179">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="963fc-180">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="963fc-180">CloudFileShare</span></span>

<span data-ttu-id="963fc-181">O parâmetro ' Share ' aceita o valor do tipo ' CloudFileShare ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="963fc-181">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="963fc-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="963fc-182">OUTPUTS</span></span>

## <span data-ttu-id="963fc-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="963fc-183">NOTES</span></span>

## <span data-ttu-id="963fc-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="963fc-184">RELATED LINKS</span></span>

[<span data-ttu-id="963fc-185">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="963fc-185">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="963fc-186">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="963fc-186">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="963fc-187">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="963fc-187">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
