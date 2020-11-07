---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954545"
---
# <span data-ttu-id="94176-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="94176-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="94176-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94176-102">SYNOPSIS</span></span>
<span data-ttu-id="94176-103">Lista os diretórios e arquivos de um caminho.</span><span class="sxs-lookup"><span data-stu-id="94176-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="94176-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94176-104">SYNTAX</span></span>

### <span data-ttu-id="94176-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="94176-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="94176-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="94176-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="94176-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="94176-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="94176-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94176-108">DESCRIPTION</span></span>
<span data-ttu-id="94176-109">O cmdlet **Get-AzStorageFile** lista os diretórios e arquivos do compartilhamento ou do diretório que você especificar.</span><span class="sxs-lookup"><span data-stu-id="94176-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="94176-110">Especifique o parâmetro *path* para obter uma instância de um diretório ou arquivo no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="94176-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="94176-111">Esse cmdlet retorna objetos **AzureStorageFile** e **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="94176-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="94176-112">Você pode usar a propriedade **IsDirectory** para distinguir entre pastas e arquivos.</span><span class="sxs-lookup"><span data-stu-id="94176-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="94176-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94176-113">EXAMPLES</span></span>

### <span data-ttu-id="94176-114">Exemplo 1: listar diretórios em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="94176-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="94176-115">Esse comando lista apenas as pastas no compartilhamento ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="94176-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="94176-116">Ele primeiro recupera arquivos e diretórios, passa-os para o operador **Where** usando o operador pipeline e, em seguida, descarta todos os objetos cujo tipo não é "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="94176-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="94176-117">Exemplo 2: listar um diretório de arquivos</span><span class="sxs-lookup"><span data-stu-id="94176-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="94176-118">Esse comando lista os arquivos e pastas no diretório ContosoWorkingFolder sob o compartilhamento ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="94176-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="94176-119">Primeiro, ele obtém a instância do diretório e, em seguida, a canaliza para o cmdlet **Get-AzStorageFile** para listar o diretório.</span><span class="sxs-lookup"><span data-stu-id="94176-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="94176-120">OS</span><span class="sxs-lookup"><span data-stu-id="94176-120">PARAMETERS</span></span>

### <span data-ttu-id="94176-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="94176-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="94176-122">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="94176-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="94176-123">Se a chamada anterior falhar dentro do intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="94176-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="94176-124">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="94176-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="94176-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="94176-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="94176-126">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="94176-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="94176-127">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="94176-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="94176-128">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="94176-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="94176-129">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="94176-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="94176-130">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="94176-130">The default value is 10.</span></span>

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

### <span data-ttu-id="94176-131">-Contexto</span><span class="sxs-lookup"><span data-stu-id="94176-131">-Context</span></span>
<span data-ttu-id="94176-132">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="94176-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="94176-133">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="94176-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="94176-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94176-134">-DefaultProfile</span></span>
<span data-ttu-id="94176-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94176-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94176-136">-Diretório</span><span class="sxs-lookup"><span data-stu-id="94176-136">-Directory</span></span>
<span data-ttu-id="94176-137">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="94176-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="94176-138">Esse cmdlet obtém a pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="94176-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="94176-139">Para obter um diretório, use o cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="94176-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="94176-140">Você também pode usar o cmdlet **Get-AzStorageFile** para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="94176-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="94176-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="94176-141">-Path</span></span>
<span data-ttu-id="94176-142">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="94176-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="94176-143">Se você omitir o parâmetro *Path* , **Get-AzStorageFile** lista as pastas e arquivos no compartilhamento de arquivos ou diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="94176-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="94176-144">Se você incluir o parâmetro *Path* , **Get-AzStorageFile** retornará uma instância de um diretório ou arquivo no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="94176-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94176-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="94176-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="94176-146">Especifica o intervalo de tempo limite do lado do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="94176-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="94176-147">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="94176-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="94176-148">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="94176-148">-Share</span></span>
<span data-ttu-id="94176-149">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="94176-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="94176-150">Esse cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="94176-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="94176-151">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="94176-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="94176-152">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94176-152">This object contains the Storage context.</span></span>
<span data-ttu-id="94176-153">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="94176-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="94176-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="94176-154">-ShareName</span></span>
<span data-ttu-id="94176-155">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="94176-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="94176-156">Esse cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="94176-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="94176-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94176-157">CommonParameters</span></span>
<span data-ttu-id="94176-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94176-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94176-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94176-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94176-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94176-160">INPUTS</span></span>

### <span data-ttu-id="94176-161">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="94176-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="94176-162">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="94176-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="94176-163">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="94176-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="94176-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94176-164">OUTPUTS</span></span>

### <span data-ttu-id="94176-165">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="94176-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="94176-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94176-166">NOTES</span></span>

## <span data-ttu-id="94176-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94176-167">RELATED LINKS</span></span>

[<span data-ttu-id="94176-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="94176-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="94176-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="94176-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="94176-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="94176-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="94176-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="94176-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="94176-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="94176-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


