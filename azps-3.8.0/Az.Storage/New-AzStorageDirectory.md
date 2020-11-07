---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: daf7493ba21673359a11a9cdc4efaa068f629c03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777386"
---
# <span data-ttu-id="74d91-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="74d91-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="74d91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74d91-102">SYNOPSIS</span></span>
<span data-ttu-id="74d91-103">Cria um diretório.</span><span class="sxs-lookup"><span data-stu-id="74d91-103">Creates a directory.</span></span>

## <span data-ttu-id="74d91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74d91-104">SYNTAX</span></span>

### <span data-ttu-id="74d91-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="74d91-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="74d91-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="74d91-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="74d91-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="74d91-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="74d91-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74d91-108">DESCRIPTION</span></span>
<span data-ttu-id="74d91-109">O cmdlet **New-AzStorageDirectory** cria um diretório.</span><span class="sxs-lookup"><span data-stu-id="74d91-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="74d91-110">Esse cmdlet retorna um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="74d91-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="74d91-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74d91-111">EXAMPLES</span></span>

### <span data-ttu-id="74d91-112">Exemplo 1: criar uma pasta em um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="74d91-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="74d91-113">Esse comando cria uma pasta chamada ContosoWorkingFolder no compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="74d91-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="74d91-114">Exemplo 2: criar uma pasta em um compartilhamento de arquivos especificada em um objeto de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="74d91-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="74d91-115">Esse comando usa o cmdlet **Get-AzStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, passa-o para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="74d91-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="74d91-116">O cmdlet atual cria a pasta chamada ContosoWorkingFolder em ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="74d91-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="74d91-117">OS</span><span class="sxs-lookup"><span data-stu-id="74d91-117">PARAMETERS</span></span>

### <span data-ttu-id="74d91-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="74d91-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="74d91-119">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="74d91-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="74d91-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="74d91-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="74d91-121">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="74d91-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="74d91-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="74d91-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="74d91-123">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="74d91-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="74d91-124">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="74d91-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="74d91-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="74d91-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="74d91-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="74d91-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="74d91-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="74d91-127">The default value is 10.</span></span>

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

### <span data-ttu-id="74d91-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="74d91-128">-Context</span></span>
<span data-ttu-id="74d91-129">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="74d91-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="74d91-130">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="74d91-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="74d91-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d91-131">-DefaultProfile</span></span>
<span data-ttu-id="74d91-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74d91-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d91-133">-Diretório</span><span class="sxs-lookup"><span data-stu-id="74d91-133">-Directory</span></span>
<span data-ttu-id="74d91-134">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="74d91-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="74d91-135">Esse cmdlet cria a pasta no local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="74d91-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="74d91-136">Para obter um diretório, use o cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="74d91-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="74d91-137">Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="74d91-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d91-138">-Caminho</span><span class="sxs-lookup"><span data-stu-id="74d91-138">-Path</span></span>
<span data-ttu-id="74d91-139">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="74d91-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="74d91-140">Esse cmdlet cria uma pasta para o caminho especificado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74d91-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d91-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="74d91-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="74d91-142">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="74d91-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="74d91-143">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="74d91-143">-Share</span></span>
<span data-ttu-id="74d91-144">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="74d91-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="74d91-145">Esse cmdlet cria uma pasta no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="74d91-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="74d91-146">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="74d91-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="74d91-147">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74d91-147">This object contains the storage context.</span></span>
<span data-ttu-id="74d91-148">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="74d91-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d91-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="74d91-149">-ShareName</span></span>
<span data-ttu-id="74d91-150">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="74d91-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="74d91-151">Esse cmdlet cria uma pasta no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="74d91-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="74d91-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d91-152">CommonParameters</span></span>
<span data-ttu-id="74d91-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d91-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d91-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d91-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d91-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74d91-155">INPUTS</span></span>

### <span data-ttu-id="74d91-156">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="74d91-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="74d91-157">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="74d91-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="74d91-158">System. String</span><span class="sxs-lookup"><span data-stu-id="74d91-158">System.String</span></span>

### <span data-ttu-id="74d91-159">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="74d91-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="74d91-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74d91-160">OUTPUTS</span></span>

### <span data-ttu-id="74d91-161">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="74d91-161">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="74d91-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74d91-162">NOTES</span></span>

## <span data-ttu-id="74d91-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74d91-163">RELATED LINKS</span></span>

[<span data-ttu-id="74d91-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="74d91-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="74d91-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="74d91-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="74d91-166">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="74d91-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="74d91-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="74d91-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="74d91-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="74d91-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
