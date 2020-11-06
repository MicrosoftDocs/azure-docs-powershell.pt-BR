---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6df60027ff2c25a8f2c1c948d04213cfc6d6158e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427359"
---
# <span data-ttu-id="44e60-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="44e60-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="44e60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44e60-102">SYNOPSIS</span></span>
<span data-ttu-id="44e60-103">Exclui um diretório.</span><span class="sxs-lookup"><span data-stu-id="44e60-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44e60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44e60-104">SYNTAX</span></span>

### <span data-ttu-id="44e60-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="44e60-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44e60-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="44e60-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44e60-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="44e60-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44e60-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44e60-108">DESCRIPTION</span></span>
<span data-ttu-id="44e60-109">O cmdlet **Remove-AzureStorageDirectory** exclui um diretório.</span><span class="sxs-lookup"><span data-stu-id="44e60-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="44e60-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44e60-110">EXAMPLES</span></span>

### <span data-ttu-id="44e60-111">Exemplo 1: excluir uma pasta</span><span class="sxs-lookup"><span data-stu-id="44e60-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="44e60-112">Esse comando exclui a pasta denominada ContosoWorkingFolder do compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="44e60-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="44e60-113">OS</span><span class="sxs-lookup"><span data-stu-id="44e60-113">PARAMETERS</span></span>

### <span data-ttu-id="44e60-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="44e60-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="44e60-115">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="44e60-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="44e60-116">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="44e60-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="44e60-117">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="44e60-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="44e60-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="44e60-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="44e60-119">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="44e60-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="44e60-120">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="44e60-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="44e60-121">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="44e60-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="44e60-122">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="44e60-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="44e60-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="44e60-123">The default value is 10.</span></span>

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

### <span data-ttu-id="44e60-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="44e60-124">-Context</span></span>
<span data-ttu-id="44e60-125">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44e60-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="44e60-126">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="44e60-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="44e60-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e60-127">-DefaultProfile</span></span>
<span data-ttu-id="44e60-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44e60-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44e60-129">-Diretório</span><span class="sxs-lookup"><span data-stu-id="44e60-129">-Directory</span></span>
<span data-ttu-id="44e60-130">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="44e60-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="44e60-131">Esse cmdlet Remove a pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="44e60-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="44e60-132">Para obter um diretório, use o cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="44e60-132">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="44e60-133">Você também pode usar o cmdlet **Get-AzureStorageFile** para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="44e60-133">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="44e60-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44e60-134">-PassThru</span></span>
<span data-ttu-id="44e60-135">Indica que, se esse cmdlet for bem-sucedido, ele retornará um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="44e60-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="44e60-136">Se você especificar esse parâmetro e se o cmdlet não for bem-sucedido devido a um valor inapropriado para o parâmetro _path_ , o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="44e60-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="44e60-137">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="44e60-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="44e60-138">-Caminho</span><span class="sxs-lookup"><span data-stu-id="44e60-138">-Path</span></span>
<span data-ttu-id="44e60-139">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="44e60-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="44e60-140">Se a pasta que esse parâmetro especifica estiver vazia, esse cmdlet excluirá essa pasta.</span><span class="sxs-lookup"><span data-stu-id="44e60-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="44e60-141">Se a pasta não estiver vazia, esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="44e60-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e60-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="44e60-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="44e60-143">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="44e60-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="44e60-144">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="44e60-144">-Share</span></span>
<span data-ttu-id="44e60-145">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="44e60-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="44e60-146">Esse cmdlet Remove uma pasta sob o compartilhamento de arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="44e60-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="44e60-147">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="44e60-147">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="44e60-148">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44e60-148">This object contains the storage context.</span></span>
<span data-ttu-id="44e60-149">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="44e60-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="44e60-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="44e60-150">-ShareName</span></span>
<span data-ttu-id="44e60-151">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="44e60-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="44e60-152">Esse cmdlet Remove uma pasta sob o compartilhamento de arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="44e60-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="44e60-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44e60-153">-Confirm</span></span>
<span data-ttu-id="44e60-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44e60-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44e60-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44e60-155">-WhatIf</span></span>
<span data-ttu-id="44e60-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44e60-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44e60-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44e60-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44e60-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e60-158">CommonParameters</span></span>
<span data-ttu-id="44e60-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44e60-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e60-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44e60-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e60-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44e60-161">INPUTS</span></span>

### <span data-ttu-id="44e60-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="44e60-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="44e60-163">Parâmetros: share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="44e60-163">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="44e60-164">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="44e60-164">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="44e60-165">Parâmetros: diretório (ByValue)</span><span class="sxs-lookup"><span data-stu-id="44e60-165">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="44e60-166">System. String</span><span class="sxs-lookup"><span data-stu-id="44e60-166">System.String</span></span>

### <span data-ttu-id="44e60-167">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="44e60-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="44e60-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44e60-168">OUTPUTS</span></span>

### <span data-ttu-id="44e60-169">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="44e60-169">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="44e60-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44e60-170">NOTES</span></span>

## <span data-ttu-id="44e60-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44e60-171">RELATED LINKS</span></span>

[<span data-ttu-id="44e60-172">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="44e60-172">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="44e60-173">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="44e60-173">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="44e60-174">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="44e60-174">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
