---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426158"
---
# <span data-ttu-id="1b108-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1b108-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="1b108-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b108-102">SYNOPSIS</span></span>
<span data-ttu-id="1b108-103">Lista os diretórios e arquivos de um caminho.</span><span class="sxs-lookup"><span data-stu-id="1b108-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="1b108-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b108-104">SYNTAX</span></span>

### <span data-ttu-id="1b108-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b108-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b108-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="1b108-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1b108-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="1b108-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1b108-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b108-108">DESCRIPTION</span></span>
<span data-ttu-id="1b108-109">O cmdlet **Get-AzureStorageFile** lista os diretórios e arquivos do compartilhamento ou do diretório que você especificar.</span><span class="sxs-lookup"><span data-stu-id="1b108-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="1b108-110">Especifique o parâmetro *path* para obter uma instância de um diretório ou arquivo no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="1b108-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="1b108-111">Esse cmdlet retorna objetos **AzureStorageFile** e **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="1b108-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="1b108-112">Você pode usar a propriedade **IsDirectory** para distinguir entre pastas e arquivos.</span><span class="sxs-lookup"><span data-stu-id="1b108-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="1b108-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b108-113">EXAMPLES</span></span>

### <span data-ttu-id="1b108-114">Exemplo 1: listar diretórios em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="1b108-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="1b108-115">Esse comando lista apenas as pastas no compartilhamento ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="1b108-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="1b108-116">Ele primeiro recupera arquivos e diretórios, passa-os para o operador **Where** usando o operador pipeline e, em seguida, descarta todos os objetos cujo tipo não é "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="1b108-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="1b108-117">Exemplo 2: listar um diretório de arquivos</span><span class="sxs-lookup"><span data-stu-id="1b108-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="1b108-118">Esse comando lista os arquivos e pastas no diretório ContosoWorkingFolder sob o compartilhamento ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="1b108-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="1b108-119">Primeiro, ele obtém a instância do diretório e, em seguida, a canaliza para o cmdlet **Get-AzureStorageFile** para listar o diretório.</span><span class="sxs-lookup"><span data-stu-id="1b108-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="1b108-120">OS</span><span class="sxs-lookup"><span data-stu-id="1b108-120">PARAMETERS</span></span>

### <span data-ttu-id="1b108-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1b108-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1b108-122">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1b108-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1b108-123">Se a chamada anterior falhar dentro do intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1b108-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1b108-124">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1b108-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1b108-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1b108-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1b108-126">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1b108-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1b108-127">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1b108-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1b108-128">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="1b108-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1b108-129">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1b108-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1b108-130">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="1b108-130">The default value is 10.</span></span>

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

### <span data-ttu-id="1b108-131">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1b108-131">-Context</span></span>
<span data-ttu-id="1b108-132">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b108-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1b108-133">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b108-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1b108-134">-Diretório</span><span class="sxs-lookup"><span data-stu-id="1b108-134">-Directory</span></span>
<span data-ttu-id="1b108-135">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="1b108-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="1b108-136">Esse cmdlet obtém a pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b108-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="1b108-137">Para obter um diretório, use o cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="1b108-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="1b108-138">Você também pode usar o cmdlet **Get-AzureStorageFile** para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="1b108-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="1b108-139">-Caminho</span><span class="sxs-lookup"><span data-stu-id="1b108-139">-Path</span></span>
<span data-ttu-id="1b108-140">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1b108-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="1b108-141">Se você omitir o parâmetro *Path* , **Get-AzureStorageFile** lista as pastas e arquivos no compartilhamento de arquivos ou diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="1b108-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="1b108-142">Se você incluir o parâmetro *Path* , **Get-AzureStorageFile** retornará uma instância de um diretório ou arquivo no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="1b108-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b108-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1b108-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1b108-144">Especifica o intervalo de tempo limite do lado do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="1b108-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="1b108-145">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1b108-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="1b108-146">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="1b108-146">-Share</span></span>
<span data-ttu-id="1b108-147">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="1b108-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1b108-148">Esse cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b108-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="1b108-149">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="1b108-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="1b108-150">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1b108-150">This object contains the Storage context.</span></span>
<span data-ttu-id="1b108-151">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="1b108-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="1b108-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1b108-152">-ShareName</span></span>
<span data-ttu-id="1b108-153">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1b108-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="1b108-154">Esse cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b108-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b108-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b108-155">CommonParameters</span></span>
<span data-ttu-id="1b108-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b108-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b108-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b108-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b108-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b108-158">INPUTS</span></span>

## <span data-ttu-id="1b108-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b108-159">OUTPUTS</span></span>

## <span data-ttu-id="1b108-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b108-160">NOTES</span></span>

## <span data-ttu-id="1b108-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b108-161">RELATED LINKS</span></span>

[<span data-ttu-id="1b108-162">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1b108-162">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="1b108-163">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="1b108-163">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="1b108-164">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="1b108-164">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="1b108-165">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1b108-165">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="1b108-166">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1b108-166">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


