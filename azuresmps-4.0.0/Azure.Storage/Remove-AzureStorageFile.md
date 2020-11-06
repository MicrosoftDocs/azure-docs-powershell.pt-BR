---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24b4ddfa86027885b5094b164f24da36e9604900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425914"
---
# <span data-ttu-id="f2749-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="f2749-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="f2749-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2749-102">SYNOPSIS</span></span>
<span data-ttu-id="f2749-103">Exclui um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2749-103">Deletes a file.</span></span>

## <span data-ttu-id="f2749-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2749-104">SYNTAX</span></span>

### <span data-ttu-id="f2749-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2749-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2749-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="f2749-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2749-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="f2749-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2749-108">Arquivos</span><span class="sxs-lookup"><span data-stu-id="f2749-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2749-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2749-109">DESCRIPTION</span></span>
<span data-ttu-id="f2749-110">O cmdlet **Remove-AzureStorageFile** exclui um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2749-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="f2749-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2749-111">EXAMPLES</span></span>

### <span data-ttu-id="f2749-112">Exemplo 1: excluir um arquivo de um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="f2749-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="f2749-113">Esse comando exclui o arquivo chamado ContosoFile22 do compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f2749-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="f2749-114">Exemplo 2: obter um arquivo de um compartilhamento de arquivos usando um objeto de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="f2749-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="f2749-115">Esse comando usa o cmdlet **Get-AzureStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="f2749-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f2749-116">O comando atual exclui o arquivo chamado ContosoFile22 de ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f2749-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="f2749-117">OS</span><span class="sxs-lookup"><span data-stu-id="f2749-117">PARAMETERS</span></span>

### <span data-ttu-id="f2749-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2749-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f2749-119">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="f2749-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f2749-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f2749-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f2749-121">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f2749-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f2749-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f2749-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f2749-123">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f2749-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f2749-124">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f2749-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f2749-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="f2749-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f2749-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="f2749-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f2749-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="f2749-127">The default value is 10.</span></span>

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

### <span data-ttu-id="f2749-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f2749-128">-Context</span></span>
<span data-ttu-id="f2749-129">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2749-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f2749-130">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f2749-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f2749-131">-Diretório</span><span class="sxs-lookup"><span data-stu-id="f2749-131">-Directory</span></span>
<span data-ttu-id="f2749-132">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="f2749-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="f2749-133">Esse cmdlet Remove um arquivo na pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f2749-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2749-134">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="f2749-134">-File</span></span>
<span data-ttu-id="f2749-135">Especifica um arquivo como um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="f2749-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="f2749-136">Esse cmdlet Remove o arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f2749-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="f2749-137">Para obter um objeto **cloudfile** , use o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="f2749-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2749-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2749-138">-PassThru</span></span>
<span data-ttu-id="f2749-139">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="f2749-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f2749-140">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f2749-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f2749-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f2749-141">-Path</span></span>
<span data-ttu-id="f2749-142">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2749-142">Specifies the path of a file.</span></span>
<span data-ttu-id="f2749-143">Esse cmdlet exclui o arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f2749-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2749-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2749-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f2749-145">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="f2749-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f2749-146">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="f2749-146">-Share</span></span>
<span data-ttu-id="f2749-147">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="f2749-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="f2749-148">Esse cmdlet Remove o arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f2749-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="f2749-149">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="f2749-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="f2749-150">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f2749-150">This object contains the storage context.</span></span>
<span data-ttu-id="f2749-151">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="f2749-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="f2749-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f2749-152">-ShareName</span></span>
<span data-ttu-id="f2749-153">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f2749-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="f2749-154">Esse cmdlet Remove o arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f2749-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="f2749-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2749-155">-Confirm</span></span>
<span data-ttu-id="f2749-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2749-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2749-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2749-157">-WhatIf</span></span>
<span data-ttu-id="f2749-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2749-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2749-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2749-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2749-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2749-160">CommonParameters</span></span>
<span data-ttu-id="f2749-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2749-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2749-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2749-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2749-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2749-163">INPUTS</span></span>

## <span data-ttu-id="f2749-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2749-164">OUTPUTS</span></span>

## <span data-ttu-id="f2749-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2749-165">NOTES</span></span>

## <span data-ttu-id="f2749-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2749-166">RELATED LINKS</span></span>

[<span data-ttu-id="f2749-167">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="f2749-167">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="f2749-168">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f2749-168">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="f2749-169">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f2749-169">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
