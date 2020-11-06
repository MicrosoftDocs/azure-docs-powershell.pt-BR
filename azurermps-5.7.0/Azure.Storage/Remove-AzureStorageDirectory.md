---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6e5866fd053b4d6f777bd0ca84790eed737e6125
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602662"
---
# <span data-ttu-id="b8323-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b8323-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="b8323-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8323-102">SYNOPSIS</span></span>
<span data-ttu-id="b8323-103">Exclui um diretório.</span><span class="sxs-lookup"><span data-stu-id="b8323-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8323-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8323-104">SYNTAX</span></span>

### <span data-ttu-id="b8323-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8323-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8323-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="b8323-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8323-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="b8323-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8323-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8323-108">DESCRIPTION</span></span>
<span data-ttu-id="b8323-109">O cmdlet **Remove-AzureStorageDirectory** exclui um diretório.</span><span class="sxs-lookup"><span data-stu-id="b8323-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="b8323-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8323-110">EXAMPLES</span></span>

### <span data-ttu-id="b8323-111">Exemplo 1: excluir uma pasta</span><span class="sxs-lookup"><span data-stu-id="b8323-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="b8323-112">Esse comando exclui a pasta denominada ContosoWorkingFolder do compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b8323-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="b8323-113">OS</span><span class="sxs-lookup"><span data-stu-id="b8323-113">PARAMETERS</span></span>

### <span data-ttu-id="b8323-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8323-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8323-115">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8323-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8323-116">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b8323-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8323-117">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b8323-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8323-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8323-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8323-119">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b8323-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8323-120">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b8323-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8323-121">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="b8323-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8323-122">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b8323-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8323-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="b8323-123">The default value is 10.</span></span>

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

### <span data-ttu-id="b8323-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b8323-124">-Context</span></span>
<span data-ttu-id="b8323-125">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8323-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b8323-126">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="b8323-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b8323-127">-Diretório</span><span class="sxs-lookup"><span data-stu-id="b8323-127">-Directory</span></span>
<span data-ttu-id="b8323-128">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="b8323-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b8323-129">Esse cmdlet Remove a pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b8323-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="b8323-130">Para obter um diretório, use o cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="b8323-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b8323-131">Você também pode usar o cmdlet **Get-AzureStorageFile** para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="b8323-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="b8323-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8323-132">-PassThru</span></span>
<span data-ttu-id="b8323-133">Indica que, se esse cmdlet for bem-sucedido, ele retornará um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="b8323-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="b8323-134">Se você especificar esse parâmetro e se o cmdlet não for bem-sucedido devido a um valor inapropriado para o parâmetro _path_ , o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b8323-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="b8323-135">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="b8323-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b8323-136">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b8323-136">-Path</span></span>
<span data-ttu-id="b8323-137">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="b8323-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="b8323-138">Se a pasta que esse parâmetro especifica estiver vazia, esse cmdlet excluirá essa pasta.</span><span class="sxs-lookup"><span data-stu-id="b8323-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="b8323-139">Se a pasta não estiver vazia, esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b8323-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8323-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8323-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8323-141">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="b8323-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b8323-142">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="b8323-142">-Share</span></span>
<span data-ttu-id="b8323-143">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="b8323-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b8323-144">Esse cmdlet Remove uma pasta sob o compartilhamento de arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b8323-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="b8323-145">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="b8323-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="b8323-146">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b8323-146">This object contains the storage context.</span></span>
<span data-ttu-id="b8323-147">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="b8323-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="b8323-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b8323-148">-ShareName</span></span>
<span data-ttu-id="b8323-149">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b8323-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="b8323-150">Esse cmdlet Remove uma pasta sob o compartilhamento de arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b8323-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8323-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8323-151">-Confirm</span></span>
<span data-ttu-id="b8323-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8323-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8323-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8323-153">-WhatIf</span></span>
<span data-ttu-id="b8323-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8323-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8323-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8323-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8323-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8323-156">CommonParameters</span></span>
<span data-ttu-id="b8323-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8323-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8323-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8323-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8323-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8323-159">INPUTS</span></span>

### <span data-ttu-id="b8323-160">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8323-160">IStorageContext</span></span>

<span data-ttu-id="b8323-161">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b8323-161">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b8323-162">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b8323-162">CloudFileDirectory</span></span>

<span data-ttu-id="b8323-163">O parâmetro ' Directory ' aceita o valor do tipo ' CloudFileDirectory ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="b8323-163">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="b8323-164">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b8323-164">CloudFileShare</span></span>

<span data-ttu-id="b8323-165">O parâmetro ' Share ' aceita o valor do tipo ' CloudFileShare ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="b8323-165">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="b8323-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8323-166">OUTPUTS</span></span>

## <span data-ttu-id="b8323-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8323-167">NOTES</span></span>

## <span data-ttu-id="b8323-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8323-168">RELATED LINKS</span></span>

[<span data-ttu-id="b8323-169">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b8323-169">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="b8323-170">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8323-170">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b8323-171">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b8323-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
