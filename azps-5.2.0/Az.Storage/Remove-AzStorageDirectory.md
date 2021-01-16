---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260797"
---
# <span data-ttu-id="b39d3-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b39d3-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="b39d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b39d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b39d3-103">Exclui um diretório.</span><span class="sxs-lookup"><span data-stu-id="b39d3-103">Deletes a directory.</span></span>

## <span data-ttu-id="b39d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b39d3-104">SYNTAX</span></span>

### <span data-ttu-id="b39d3-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="b39d3-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b39d3-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="b39d3-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b39d3-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="b39d3-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b39d3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b39d3-108">DESCRIPTION</span></span>
<span data-ttu-id="b39d3-109">O cmdlet **Remove-AzStorageDirectory** exclui um diretório.</span><span class="sxs-lookup"><span data-stu-id="b39d3-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="b39d3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b39d3-110">EXAMPLES</span></span>

### <span data-ttu-id="b39d3-111">Exemplo 1: excluir uma pasta</span><span class="sxs-lookup"><span data-stu-id="b39d3-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="b39d3-112">Esse comando exclui a pasta denominada ContosoWorkingFolder do compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b39d3-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="b39d3-113">OS</span><span class="sxs-lookup"><span data-stu-id="b39d3-113">PARAMETERS</span></span>

### <span data-ttu-id="b39d3-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b39d3-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b39d3-115">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="b39d3-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b39d3-116">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b39d3-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b39d3-117">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b39d3-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b39d3-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b39d3-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b39d3-119">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b39d3-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b39d3-120">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b39d3-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b39d3-121">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="b39d3-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b39d3-122">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b39d3-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b39d3-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="b39d3-123">The default value is 10.</span></span>

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

### <span data-ttu-id="b39d3-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b39d3-124">-Context</span></span>
<span data-ttu-id="b39d3-125">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b39d3-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b39d3-126">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="b39d3-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b39d3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39d3-127">-DefaultProfile</span></span>
<span data-ttu-id="b39d3-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b39d3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b39d3-129">-Diretório</span><span class="sxs-lookup"><span data-stu-id="b39d3-129">-Directory</span></span>
<span data-ttu-id="b39d3-130">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="b39d3-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b39d3-131">Esse cmdlet Remove a pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b39d3-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="b39d3-132">Para obter um diretório, use o cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="b39d3-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b39d3-133">Você também pode usar o cmdlet **Get-AzStorageFile** para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="b39d3-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="b39d3-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b39d3-134">-PassThru</span></span>
<span data-ttu-id="b39d3-135">Indica que, se esse cmdlet for bem-sucedido, ele retornará um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="b39d3-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="b39d3-136">Se você especificar esse parâmetro e se o cmdlet não for bem-sucedido devido a um valor inapropriado para o parâmetro _path_ , o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b39d3-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="b39d3-137">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="b39d3-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b39d3-138">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b39d3-138">-Path</span></span>
<span data-ttu-id="b39d3-139">Especifica o caminho de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="b39d3-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="b39d3-140">Se a pasta que esse parâmetro especifica estiver vazia, esse cmdlet excluirá essa pasta.</span><span class="sxs-lookup"><span data-stu-id="b39d3-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="b39d3-141">Se a pasta não estiver vazia, esse cmdlet não fará nenhuma alteração e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b39d3-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="b39d3-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b39d3-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b39d3-143">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="b39d3-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b39d3-144">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="b39d3-144">-Share</span></span>
<span data-ttu-id="b39d3-145">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="b39d3-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b39d3-146">Esse cmdlet Remove uma pasta sob o compartilhamento de arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b39d3-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="b39d3-147">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="b39d3-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="b39d3-148">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b39d3-148">This object contains the storage context.</span></span>
<span data-ttu-id="b39d3-149">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="b39d3-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="b39d3-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b39d3-150">-ShareName</span></span>
<span data-ttu-id="b39d3-151">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b39d3-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="b39d3-152">Esse cmdlet Remove uma pasta sob o compartilhamento de arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b39d3-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="b39d3-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b39d3-153">-Confirm</span></span>
<span data-ttu-id="b39d3-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b39d3-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b39d3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b39d3-155">-WhatIf</span></span>
<span data-ttu-id="b39d3-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b39d3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b39d3-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b39d3-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b39d3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39d3-158">CommonParameters</span></span>
<span data-ttu-id="b39d3-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b39d3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39d3-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b39d3-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39d3-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b39d3-161">INPUTS</span></span>

### <span data-ttu-id="b39d3-162">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b39d3-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="b39d3-163">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b39d3-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="b39d3-164">System. String</span><span class="sxs-lookup"><span data-stu-id="b39d3-164">System.String</span></span>

### <span data-ttu-id="b39d3-165">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b39d3-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b39d3-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b39d3-166">OUTPUTS</span></span>

### <span data-ttu-id="b39d3-167">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b39d3-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="b39d3-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b39d3-168">NOTES</span></span>

## <span data-ttu-id="b39d3-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b39d3-169">RELATED LINKS</span></span>

[<span data-ttu-id="b39d3-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="b39d3-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="b39d3-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b39d3-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b39d3-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b39d3-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
