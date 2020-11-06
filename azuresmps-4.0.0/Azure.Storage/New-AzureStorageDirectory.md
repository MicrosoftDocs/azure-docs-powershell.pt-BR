---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bd97057cfafc48b3f1edd8539e7808056599117
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425981"
---
# <span data-ttu-id="c958c-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c958c-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="c958c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c958c-102">SYNOPSIS</span></span>
<span data-ttu-id="c958c-103">Cria um diretório.</span><span class="sxs-lookup"><span data-stu-id="c958c-103">Creates a directory.</span></span>

## <span data-ttu-id="c958c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c958c-104">SYNTAX</span></span>

### <span data-ttu-id="c958c-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="c958c-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c958c-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="c958c-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c958c-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="c958c-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c958c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c958c-108">DESCRIPTION</span></span>
<span data-ttu-id="c958c-109">O cmdlet **New-AzureStorageDirectory** cria um diretório.</span><span class="sxs-lookup"><span data-stu-id="c958c-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="c958c-110">Esse cmdlet retorna um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="c958c-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="c958c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c958c-111">EXAMPLES</span></span>

### <span data-ttu-id="c958c-112">Exemplo 1: criar uma pasta em um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="c958c-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="c958c-113">Esse comando cria uma pasta chamada ContosoWorkingFolder no compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c958c-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="c958c-114">Exemplo 2: criar uma pasta em um compartilhamento de arquivos especificada em um objeto de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="c958c-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="c958c-115">Esse comando usa o cmdlet **Get-AzureStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, passa-o para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c958c-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c958c-116">O cmdlet atual cria a pasta chamada ContosoWorkingFolder em ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c958c-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="c958c-117">OS</span><span class="sxs-lookup"><span data-stu-id="c958c-117">PARAMETERS</span></span>

### <span data-ttu-id="c958c-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c958c-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c958c-119">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c958c-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c958c-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c958c-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c958c-121">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c958c-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c958c-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c958c-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c958c-123">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c958c-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c958c-124">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c958c-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c958c-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="c958c-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c958c-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c958c-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c958c-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c958c-127">The default value is 10.</span></span>

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

### <span data-ttu-id="c958c-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c958c-128">-Context</span></span>
<span data-ttu-id="c958c-129">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c958c-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c958c-130">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c958c-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c958c-131">-Diretório</span><span class="sxs-lookup"><span data-stu-id="c958c-131">-Directory</span></span>
<span data-ttu-id="c958c-132">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="c958c-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="c958c-133">Esse cmdlet cria a pasta no local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c958c-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="c958c-134">Para obter um diretório, use o cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="c958c-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="c958c-135">Você também pode usar o cmdlet Get-AzureStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="c958c-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="c958c-136">-Caminho</span><span class="sxs-lookup"><span data-stu-id="c958c-136">-Path</span></span>
<span data-ttu-id="c958c-137">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="c958c-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="c958c-138">Esse cmdlet cria uma pasta para o caminho especificado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c958c-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c958c-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c958c-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c958c-140">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c958c-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c958c-141">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="c958c-141">-Share</span></span>
<span data-ttu-id="c958c-142">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="c958c-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c958c-143">Esse cmdlet cria uma pasta no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c958c-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="c958c-144">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="c958c-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="c958c-145">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c958c-145">This object contains the storage context.</span></span>
<span data-ttu-id="c958c-146">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="c958c-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="c958c-147">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c958c-147">-ShareName</span></span>
<span data-ttu-id="c958c-148">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c958c-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="c958c-149">Esse cmdlet cria uma pasta no compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c958c-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="c958c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c958c-150">CommonParameters</span></span>
<span data-ttu-id="c958c-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c958c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c958c-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c958c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c958c-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c958c-153">INPUTS</span></span>

## <span data-ttu-id="c958c-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c958c-154">OUTPUTS</span></span>

## <span data-ttu-id="c958c-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c958c-155">NOTES</span></span>

## <span data-ttu-id="c958c-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c958c-156">RELATED LINKS</span></span>

[<span data-ttu-id="c958c-157">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c958c-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c958c-158">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c958c-158">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="c958c-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c958c-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c958c-160">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c958c-160">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="c958c-161">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c958c-161">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
