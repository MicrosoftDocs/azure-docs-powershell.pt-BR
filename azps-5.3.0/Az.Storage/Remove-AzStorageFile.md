---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427709"
---
# <span data-ttu-id="b4b7c-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="b4b7c-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="b4b7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b7c-103">Exclui um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-103">Deletes a file.</span></span>

## <span data-ttu-id="b4b7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4b7c-104">SYNTAX</span></span>

### <span data-ttu-id="b4b7c-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4b7c-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4b7c-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="b4b7c-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b7c-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="b4b7c-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4b7c-108">Arquivos</span><span class="sxs-lookup"><span data-stu-id="b4b7c-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b7c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4b7c-109">DESCRIPTION</span></span>
<span data-ttu-id="b4b7c-110">O cmdlet **Remove-AzStorageFile** exclui um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="b4b7c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4b7c-111">EXAMPLES</span></span>

### <span data-ttu-id="b4b7c-112">Exemplo 1: excluir um arquivo de um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="b4b7c-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="b4b7c-113">Esse comando exclui o arquivo chamado ContosoFile22 do compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="b4b7c-114">Exemplo 2: obter um arquivo de um compartilhamento de arquivos usando um objeto de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="b4b7c-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="b4b7c-115">Esse comando usa o cmdlet **Get-AzStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4b7c-116">O comando atual exclui o arquivo chamado ContosoFile22 de ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="b4b7c-117">OS</span><span class="sxs-lookup"><span data-stu-id="b4b7c-117">PARAMETERS</span></span>

### <span data-ttu-id="b4b7c-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b4b7c-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b4b7c-119">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b4b7c-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b4b7c-121">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b4b7c-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b4b7c-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b4b7c-123">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b4b7c-124">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b4b7c-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b4b7c-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b4b7c-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-127">The default value is 10.</span></span>

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

### <span data-ttu-id="b4b7c-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b4b7c-128">-Context</span></span>
<span data-ttu-id="b4b7c-129">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b4b7c-130">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="b4b7c-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b4b7c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b7c-131">-DefaultProfile</span></span>
<span data-ttu-id="b4b7c-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4b7c-133">-Diretório</span><span class="sxs-lookup"><span data-stu-id="b4b7c-133">-Directory</span></span>
<span data-ttu-id="b4b7c-134">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="b4b7c-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b4b7c-135">Esse cmdlet Remove um arquivo na pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4b7c-136">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="b4b7c-136">-File</span></span>
<span data-ttu-id="b4b7c-137">Especifica um arquivo como um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="b4b7c-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="b4b7c-138">Esse cmdlet Remove o arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="b4b7c-139">Para obter um objeto **cloudfile** , use o cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="b4b7c-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4b7c-140">-PassThru</span></span>
<span data-ttu-id="b4b7c-141">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b4b7c-142">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b4b7c-143">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b4b7c-143">-Path</span></span>
<span data-ttu-id="b4b7c-144">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-144">Specifies the path of a file.</span></span>
<span data-ttu-id="b4b7c-145">Esse cmdlet exclui o arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b7c-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b4b7c-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b4b7c-147">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b4b7c-148">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="b4b7c-148">-Share</span></span>
<span data-ttu-id="b4b7c-149">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="b4b7c-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b4b7c-150">Esse cmdlet Remove o arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="b4b7c-151">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="b4b7c-152">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-152">This object contains the storage context.</span></span>
<span data-ttu-id="b4b7c-153">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="b4b7c-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="b4b7c-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b4b7c-154">-ShareName</span></span>
<span data-ttu-id="b4b7c-155">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="b4b7c-156">Esse cmdlet Remove o arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="b4b7c-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4b7c-157">-Confirm</span></span>
<span data-ttu-id="b4b7c-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b7c-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b7c-159">-WhatIf</span></span>
<span data-ttu-id="b4b7c-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b7c-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b7c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b7c-162">CommonParameters</span></span>
<span data-ttu-id="b4b7c-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b7c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b7c-164">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b7c-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b7c-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4b7c-165">INPUTS</span></span>

### <span data-ttu-id="b4b7c-166">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b4b7c-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="b4b7c-167">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b4b7c-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="b4b7c-168">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="b4b7c-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="b4b7c-169">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4b7c-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b4b7c-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4b7c-170">OUTPUTS</span></span>

### <span data-ttu-id="b4b7c-171">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="b4b7c-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="b4b7c-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4b7c-172">NOTES</span></span>

## <span data-ttu-id="b4b7c-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4b7c-173">RELATED LINKS</span></span>

[<span data-ttu-id="b4b7c-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="b4b7c-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="b4b7c-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="b4b7c-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="b4b7c-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4b7c-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
