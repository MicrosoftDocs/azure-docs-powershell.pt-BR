---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
ms.openlocfilehash: 74fbb0d5336eb5c3f9f34efb5724f8a86b8868ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786596"
---
# <span data-ttu-id="41df6-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="41df6-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="41df6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41df6-102">SYNOPSIS</span></span>
<span data-ttu-id="41df6-103">Carrega o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="41df6-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41df6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41df6-104">SYNTAX</span></span>

### <span data-ttu-id="41df6-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="41df6-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41df6-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="41df6-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41df6-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="41df6-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41df6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41df6-108">DESCRIPTION</span></span>
<span data-ttu-id="41df6-109">O cmdlet **set-AzureStorageFileContent** carrega o conteúdo de um arquivo em um arquivo em um compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="41df6-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="41df6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41df6-110">EXAMPLES</span></span>

### <span data-ttu-id="41df6-111">Exemplo 1: carregar um arquivo na pasta atual</span><span class="sxs-lookup"><span data-stu-id="41df6-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="41df6-112">Esse comando carrega um arquivo chamado DataFile37 na pasta atual como um arquivo chamado CurrentDataFile na pasta denominada ContosoWorkingFolderme.</span><span class="sxs-lookup"><span data-stu-id="41df6-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="41df6-113">Exemplo 2: carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="41df6-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="41df6-114">Este exemplo usa vários cmdlets comuns do Windows PowerShell e o cmdlet atual para carregar todos os arquivos da pasta atual para a pasta raiz do contêiner ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="41df6-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="41df6-115">O primeiro comando obtém o nome da pasta atual e a armazena na variável $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="41df6-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="41df6-116">O segundo comando usa o cmdlet **Get-AzureStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, armazena-o na variável $container.</span><span class="sxs-lookup"><span data-stu-id="41df6-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="41df6-117">O comando final Obtém o conteúdo da pasta atual e passa cada um para o cmdlet Where-Object usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="41df6-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="41df6-118">Esse cmdlet filtra objetos que não são arquivos e, em seguida, passa os arquivos para o cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="41df6-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="41df6-119">Esse cmdlet executa um bloco de script para cada arquivo que cria o caminho apropriado para ele e, em seguida, usa o cmdlet atual para carregar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="41df6-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="41df6-120">O resultado tem o mesmo nome e a mesma posição relativa em relação aos outros arquivos que este exemplo carrega.</span><span class="sxs-lookup"><span data-stu-id="41df6-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="41df6-121">Para obter mais informações sobre blocos de script, digite `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="41df6-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="41df6-122">OS</span><span class="sxs-lookup"><span data-stu-id="41df6-122">PARAMETERS</span></span>

### <span data-ttu-id="41df6-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="41df6-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="41df6-124">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="41df6-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="41df6-125">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="41df6-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="41df6-126">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="41df6-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="41df6-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="41df6-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="41df6-128">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="41df6-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="41df6-129">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="41df6-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="41df6-130">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="41df6-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="41df6-131">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="41df6-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="41df6-132">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="41df6-132">The default value is 10.</span></span>

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

### <span data-ttu-id="41df6-133">-Contexto</span><span class="sxs-lookup"><span data-stu-id="41df6-133">-Context</span></span>
<span data-ttu-id="41df6-134">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="41df6-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="41df6-135">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="41df6-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="41df6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41df6-136">-DefaultProfile</span></span>
<span data-ttu-id="41df6-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41df6-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41df6-138">-Diretório</span><span class="sxs-lookup"><span data-stu-id="41df6-138">-Directory</span></span>
<span data-ttu-id="41df6-139">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="41df6-139">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="41df6-140">Esse cmdlet carrega o arquivo para a pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41df6-140">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="41df6-141">Para obter um diretório, use o cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="41df6-141">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="41df6-142">Você também pode usar o cmdlet Get-AzureStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="41df6-142">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="41df6-143">-Force</span><span class="sxs-lookup"><span data-stu-id="41df6-143">-Force</span></span>
<span data-ttu-id="41df6-144">Indica que esse cmdlet substitui um arquivo de armazenamento do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="41df6-144">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="41df6-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41df6-145">-PassThru</span></span>
<span data-ttu-id="41df6-146">Indica que esse cmdlet retorna o objeto **AzureStorageFile** que ele cria ou carrega.</span><span class="sxs-lookup"><span data-stu-id="41df6-146">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="41df6-147">-Caminho</span><span class="sxs-lookup"><span data-stu-id="41df6-147">-Path</span></span>
<span data-ttu-id="41df6-148">Especifica o caminho de um arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="41df6-148">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="41df6-149">Esse cmdlet carrega o conteúdo para o arquivo que esse parâmetro especifica ou para um arquivo na pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41df6-149">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="41df6-150">Se você especificar uma pasta, esse cmdlet criará um arquivo com o mesmo nome do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="41df6-150">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="41df6-151">Se você especificar um caminho para um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo nesse arquivo.</span><span class="sxs-lookup"><span data-stu-id="41df6-151">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="41df6-152">Se você especificar um arquivo que já existe e especificar o parâmetro _Force_ , esse cmdlet substituirá o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="41df6-152">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="41df6-153">Se você especificar um arquivo que já existe e não especificar _Force_ , esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="41df6-153">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="41df6-154">Se você especificar um caminho para uma pasta que não existe, esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="41df6-154">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="41df6-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="41df6-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="41df6-156">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="41df6-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="41df6-157">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="41df6-157">-Share</span></span>
<span data-ttu-id="41df6-158">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="41df6-158">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="41df6-159">Esse cmdlet é carregado em um arquivo no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41df6-159">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="41df6-160">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="41df6-160">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="41df6-161">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="41df6-161">This object contains the storage context.</span></span>
<span data-ttu-id="41df6-162">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="41df6-162">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="41df6-163">-ShareName</span><span class="sxs-lookup"><span data-stu-id="41df6-163">-ShareName</span></span>
<span data-ttu-id="41df6-164">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="41df6-164">Specifies the name of the file share.</span></span>
<span data-ttu-id="41df6-165">Esse cmdlet é carregado em um arquivo no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41df6-165">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="41df6-166">-Fonte</span><span class="sxs-lookup"><span data-stu-id="41df6-166">-Source</span></span>
<span data-ttu-id="41df6-167">Especifica o arquivo de origem que esse cmdlet carregará.</span><span class="sxs-lookup"><span data-stu-id="41df6-167">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="41df6-168">Se você especificar um arquivo que não existe, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="41df6-168">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="41df6-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41df6-169">-Confirm</span></span>
<span data-ttu-id="41df6-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41df6-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41df6-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41df6-171">-WhatIf</span></span>
<span data-ttu-id="41df6-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41df6-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41df6-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41df6-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41df6-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41df6-174">CommonParameters</span></span>
<span data-ttu-id="41df6-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41df6-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41df6-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41df6-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41df6-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41df6-177">INPUTS</span></span>

### <span data-ttu-id="41df6-178">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="41df6-178">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="41df6-179">Parâmetros: share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41df6-179">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="41df6-180">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="41df6-180">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="41df6-181">Parâmetros: diretório (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41df6-181">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="41df6-182">System. String</span><span class="sxs-lookup"><span data-stu-id="41df6-182">System.String</span></span>

### <span data-ttu-id="41df6-183">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="41df6-183">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="41df6-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41df6-184">OUTPUTS</span></span>

### <span data-ttu-id="41df6-185">Microsoft. WindowsAzure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="41df6-185">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="41df6-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41df6-186">NOTES</span></span>

## <span data-ttu-id="41df6-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41df6-187">RELATED LINKS</span></span>

[<span data-ttu-id="41df6-188">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="41df6-188">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="41df6-189">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="41df6-189">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="41df6-190">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="41df6-190">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
