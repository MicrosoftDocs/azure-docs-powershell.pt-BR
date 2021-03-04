---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: e61171faba3661ad1d518641655ad87f06771ae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891250"
---
# <span data-ttu-id="b8679-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="b8679-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="b8679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8679-102">SYNOPSIS</span></span>
<span data-ttu-id="b8679-103">Lista diretórios e arquivos para um caminho.</span><span class="sxs-lookup"><span data-stu-id="b8679-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="b8679-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8679-104">SYNTAX</span></span>

### <span data-ttu-id="b8679-105">ShareName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b8679-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b8679-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="b8679-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8679-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="b8679-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8679-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8679-108">DESCRIPTION</span></span>
<span data-ttu-id="b8679-109">O cmdlet **Get-AzStorageFile** lista diretórios e arquivos para o compartilhamento ou diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="b8679-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="b8679-110">*Especifique o parâmetro Path* para obter uma instância de um diretório ou arquivo no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="b8679-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="b8679-111">Este cmdlet retorna **objetos AzureStorageFile** e **AzureStorageDirectory.**</span><span class="sxs-lookup"><span data-stu-id="b8679-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="b8679-112">Você pode usar a **propriedade IsDirectory** para distinguir entre pastas e arquivos.</span><span class="sxs-lookup"><span data-stu-id="b8679-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="b8679-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8679-113">EXAMPLES</span></span>

### <span data-ttu-id="b8679-114">Exemplo 1: Listar diretórios em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="b8679-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="b8679-115">Este comando lista apenas os diretórios no compartilhamento ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b8679-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="b8679-116">Ele primeiro recupera arquivos e diretórios,  os passa para o operador de onde usando o operador de pipeline e descarta todos os objetos cujo tipo não seja "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="b8679-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="b8679-117">Exemplo 2: Listar um Diretório de Arquivos</span><span class="sxs-lookup"><span data-stu-id="b8679-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="b8679-118">Este comando lista os arquivos e pastas no diretório ContosoWorkingFolder no compartilhamento ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b8679-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="b8679-119">Ele primeiro obtém a instância do diretório e, em seguida, a canalização para o cmdlet **Get-AzStorageFile** para listar o diretório.</span><span class="sxs-lookup"><span data-stu-id="b8679-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="b8679-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8679-120">PARAMETERS</span></span>

### <span data-ttu-id="b8679-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8679-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8679-122">Especifica o intervalo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8679-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8679-123">Se a chamada anterior falhar dentro do intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b8679-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8679-124">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b8679-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8679-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8679-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8679-126">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b8679-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8679-127">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b8679-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8679-128">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="b8679-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8679-129">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b8679-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8679-130">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="b8679-130">The default value is 10.</span></span>

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

### <span data-ttu-id="b8679-131">-Context</span><span class="sxs-lookup"><span data-stu-id="b8679-131">-Context</span></span>
<span data-ttu-id="b8679-132">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8679-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="b8679-133">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8679-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b8679-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8679-134">-DefaultProfile</span></span>
<span data-ttu-id="b8679-135">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8679-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8679-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="b8679-136">-Directory</span></span>
<span data-ttu-id="b8679-137">Especifica uma pasta como um **objeto CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="b8679-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b8679-138">Este cmdlet obtém a pasta especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b8679-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="b8679-139">Para obter um diretório, use o New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8679-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b8679-140">Você também pode usar o cmdlet **Get-AzStorageFile** para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="b8679-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="b8679-141">-Path</span><span class="sxs-lookup"><span data-stu-id="b8679-141">-Path</span></span>
<span data-ttu-id="b8679-142">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="b8679-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="b8679-143">Se você omitir o parâmetro *Path,* **Get-AzStorageFile** lista os diretórios e arquivos no compartilhamento de arquivos ou diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="b8679-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="b8679-144">Se você incluir o *parâmetro Path,* **Get-AzStorageFile** retornará uma instância de um diretório ou arquivo no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="b8679-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="b8679-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8679-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8679-146">Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="b8679-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="b8679-147">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de Armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b8679-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="b8679-148">-Share</span><span class="sxs-lookup"><span data-stu-id="b8679-148">-Share</span></span>
<span data-ttu-id="b8679-149">Especifica um **objeto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="b8679-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b8679-150">Este cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b8679-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="b8679-151">Para obter um **objeto CloudFileShare,** use Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8679-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="b8679-152">Este objeto contém o contexto armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b8679-152">This object contains the Storage context.</span></span>
<span data-ttu-id="b8679-153">Se você especificar esse parâmetro, não especifique o *parâmetro Context.*</span><span class="sxs-lookup"><span data-stu-id="b8679-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="b8679-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b8679-154">-ShareName</span></span>
<span data-ttu-id="b8679-155">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b8679-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="b8679-156">Este cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b8679-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8679-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8679-157">CommonParameters</span></span>
<span data-ttu-id="b8679-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8679-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8679-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8679-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8679-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8679-160">INPUTS</span></span>

### <span data-ttu-id="b8679-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b8679-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="b8679-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b8679-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="b8679-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8679-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b8679-164">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8679-164">OUTPUTS</span></span>

### <span data-ttu-id="b8679-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="b8679-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="b8679-166">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8679-166">NOTES</span></span>

## <span data-ttu-id="b8679-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8679-167">RELATED LINKS</span></span>

[<span data-ttu-id="b8679-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b8679-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="b8679-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b8679-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="b8679-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b8679-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="b8679-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="b8679-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="b8679-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b8679-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


