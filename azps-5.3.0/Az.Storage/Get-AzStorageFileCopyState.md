---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426706"
---
# <span data-ttu-id="cdb11-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="cdb11-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="cdb11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdb11-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb11-103">Obtém o estado de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="cdb11-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="cdb11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdb11-104">SYNTAX</span></span>

### <span data-ttu-id="cdb11-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="cdb11-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cdb11-106">Arquivos</span><span class="sxs-lookup"><span data-stu-id="cdb11-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdb11-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdb11-107">DESCRIPTION</span></span>
<span data-ttu-id="cdb11-108">O cmdlet **Get-AzStorageFileCopyState** Obtém o estado de uma operação de cópia de arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb11-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="cdb11-109">Ele deve ser executado no arquivo de destino da cópia.</span><span class="sxs-lookup"><span data-stu-id="cdb11-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="cdb11-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdb11-110">EXAMPLES</span></span>

### <span data-ttu-id="cdb11-111">Exemplo 1: obter o estado de cópia por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="cdb11-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="cdb11-112">Esse comando obtém o estado da operação de cópia para um arquivo que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="cdb11-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="cdb11-113">Exemplo 2: Iniciar cópia e pipeline para obter o status da cópia</span><span class="sxs-lookup"><span data-stu-id="cdb11-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="cdb11-114">O primeiro comando começa a copiar o arquivo "contosofile" para "contosofile_copy" e gera o objeto de arquivo destiantion.</span><span class="sxs-lookup"><span data-stu-id="cdb11-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="cdb11-115">O segundo pipeline de comando do objeto de arquivo destiantion para Get-AzStorageFileCopyState, para obter o estado de cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cdb11-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="cdb11-116">OS</span><span class="sxs-lookup"><span data-stu-id="cdb11-116">PARAMETERS</span></span>

### <span data-ttu-id="cdb11-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cdb11-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cdb11-118">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="cdb11-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cdb11-119">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="cdb11-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cdb11-120">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cdb11-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cdb11-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cdb11-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cdb11-122">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cdb11-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cdb11-123">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cdb11-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cdb11-124">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="cdb11-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cdb11-125">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cdb11-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cdb11-126">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="cdb11-126">The default value is 10.</span></span>

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

### <span data-ttu-id="cdb11-127">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cdb11-127">-Context</span></span>
<span data-ttu-id="cdb11-128">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb11-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="cdb11-129">Para obter um contexto, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="cdb11-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cdb11-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb11-130">-DefaultProfile</span></span>
<span data-ttu-id="cdb11-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb11-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb11-132">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="cdb11-132">-File</span></span>
<span data-ttu-id="cdb11-133">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="cdb11-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="cdb11-134">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="cdb11-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb11-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="cdb11-135">-FilePath</span></span>
<span data-ttu-id="cdb11-136">Especifica o caminho do arquivo relativo a um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb11-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb11-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cdb11-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cdb11-138">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="cdb11-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cdb11-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cdb11-139">-ShareName</span></span>
<span data-ttu-id="cdb11-140">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="cdb11-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="cdb11-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="cdb11-141">-WaitForComplete</span></span>
<span data-ttu-id="cdb11-142">Indica que esse cmdlet aguarda a conclusão da cópia.</span><span class="sxs-lookup"><span data-stu-id="cdb11-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="cdb11-143">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cdb11-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="cdb11-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb11-144">CommonParameters</span></span>
<span data-ttu-id="cdb11-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb11-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb11-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb11-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb11-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdb11-147">INPUTS</span></span>

### <span data-ttu-id="cdb11-148">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="cdb11-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="cdb11-149">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cdb11-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cdb11-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdb11-150">OUTPUTS</span></span>

### <span data-ttu-id="cdb11-151">Microsoft. Azure. Storage. File. CopyState</span><span class="sxs-lookup"><span data-stu-id="cdb11-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="cdb11-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdb11-152">NOTES</span></span>

## <span data-ttu-id="cdb11-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdb11-153">RELATED LINKS</span></span>

[<span data-ttu-id="cdb11-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cdb11-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="cdb11-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cdb11-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="cdb11-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cdb11-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="cdb11-157">Parar-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cdb11-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
