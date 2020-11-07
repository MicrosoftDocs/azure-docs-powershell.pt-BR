---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
ms.openlocfilehash: 0a474171b7659346a1d921f98920a9befc85eea8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786016"
---
# <span data-ttu-id="075f2-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="075f2-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="075f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="075f2-102">SYNOPSIS</span></span>
<span data-ttu-id="075f2-103">Cria um diretório.</span><span class="sxs-lookup"><span data-stu-id="075f2-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="075f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="075f2-104">SYNTAX</span></span>

### <span data-ttu-id="075f2-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="075f2-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="075f2-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="075f2-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="075f2-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="075f2-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="075f2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="075f2-108">DESCRIPTION</span></span>
<span data-ttu-id="075f2-109">O cmdlet **New-AzureStorageDirectory** cria um diretório.</span><span class="sxs-lookup"><span data-stu-id="075f2-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="075f2-110">Esse cmdlet retorna um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="075f2-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="075f2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="075f2-111">EXAMPLES</span></span>

### <span data-ttu-id="075f2-112">Exemplo 1: criar uma pasta em um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="075f2-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="075f2-113">Esse comando cria uma pasta chamada ContosoWorkingFolder no compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="075f2-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="075f2-114">Exemplo 2: criar uma pasta em um compartilhamento de arquivos especificada em um objeto de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="075f2-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="075f2-115">Esse comando usa o cmdlet **Get-AzureStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, passa-o para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="075f2-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="075f2-116">O cmdlet atual cria a pasta chamada ContosoWorkingFolder em ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="075f2-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="075f2-117">OS</span><span class="sxs-lookup"><span data-stu-id="075f2-117">PARAMETERS</span></span>

### <span data-ttu-id="075f2-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="075f2-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="075f2-119">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="075f2-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="075f2-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="075f2-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="075f2-121">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="075f2-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="075f2-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="075f2-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="075f2-123">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="075f2-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="075f2-124">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="075f2-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="075f2-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="075f2-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="075f2-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="075f2-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="075f2-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="075f2-127">The default value is 10.</span></span>

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

### <span data-ttu-id="075f2-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="075f2-128">-Context</span></span>
<span data-ttu-id="075f2-129">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="075f2-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="075f2-130">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="075f2-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="075f2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075f2-131">-DefaultProfile</span></span>
<span data-ttu-id="075f2-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="075f2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="075f2-133">-Diretório</span><span class="sxs-lookup"><span data-stu-id="075f2-133">-Directory</span></span>
<span data-ttu-id="075f2-134">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="075f2-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="075f2-135">Esse cmdlet cria a pasta no local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="075f2-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="075f2-136">Para obter um diretório, use o cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="075f2-136">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="075f2-137">Você também pode usar o cmdlet Get-AzureStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="075f2-137">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="075f2-138">-Caminho</span><span class="sxs-lookup"><span data-stu-id="075f2-138">-Path</span></span>
<span data-ttu-id="075f2-139">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="075f2-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="075f2-140">Esse cmdlet cria uma pasta para o caminho especificado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="075f2-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="075f2-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="075f2-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="075f2-142">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="075f2-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="075f2-143">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="075f2-143">-Share</span></span>
<span data-ttu-id="075f2-144">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="075f2-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="075f2-145">Esse cmdlet cria uma pasta no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="075f2-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="075f2-146">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="075f2-146">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="075f2-147">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="075f2-147">This object contains the storage context.</span></span>
<span data-ttu-id="075f2-148">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="075f2-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="075f2-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="075f2-149">-ShareName</span></span>
<span data-ttu-id="075f2-150">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="075f2-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="075f2-151">Esse cmdlet cria uma pasta no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="075f2-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="075f2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075f2-152">CommonParameters</span></span>
<span data-ttu-id="075f2-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="075f2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075f2-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="075f2-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075f2-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="075f2-155">INPUTS</span></span>

### <span data-ttu-id="075f2-156">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="075f2-156">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="075f2-157">Parâmetros: share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="075f2-157">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="075f2-158">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="075f2-158">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="075f2-159">Parâmetros: diretório (ByValue)</span><span class="sxs-lookup"><span data-stu-id="075f2-159">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="075f2-160">System. String</span><span class="sxs-lookup"><span data-stu-id="075f2-160">System.String</span></span>

### <span data-ttu-id="075f2-161">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="075f2-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="075f2-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="075f2-162">OUTPUTS</span></span>

### <span data-ttu-id="075f2-163">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="075f2-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="075f2-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="075f2-164">NOTES</span></span>

## <span data-ttu-id="075f2-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="075f2-165">RELATED LINKS</span></span>

[<span data-ttu-id="075f2-166">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="075f2-166">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="075f2-167">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="075f2-167">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="075f2-168">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="075f2-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="075f2-169">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="075f2-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="075f2-170">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="075f2-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
