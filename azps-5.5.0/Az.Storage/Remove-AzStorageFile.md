---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115642"
---
# <span data-ttu-id="a0eaa-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="a0eaa-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="a0eaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="a0eaa-103">Exclui um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-103">Deletes a file.</span></span>

## <span data-ttu-id="a0eaa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0eaa-104">SYNTAX</span></span>

### <span data-ttu-id="a0eaa-105">ShareName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a0eaa-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0eaa-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="a0eaa-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0eaa-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="a0eaa-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0eaa-108">Arquivo</span><span class="sxs-lookup"><span data-stu-id="a0eaa-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0eaa-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0eaa-109">DESCRIPTION</span></span>
<span data-ttu-id="a0eaa-110">O **cmdlet Remove-AzStorageFile** exclui um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="a0eaa-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a0eaa-111">EXAMPLES</span></span>

### <span data-ttu-id="a0eaa-112">Exemplo 1: Excluir um arquivo de um compartilhamento de arquivo</span><span class="sxs-lookup"><span data-stu-id="a0eaa-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="a0eaa-113">Esse comando exclui o arquivo chamado ContosoFile22 do compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="a0eaa-114">Exemplo 2: Obter um arquivo de um compartilhamento de arquivo usando um objeto de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="a0eaa-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="a0eaa-115">Esse comando usa o cmdlet **Get-AzStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e passa esse objeto para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a0eaa-116">O comando atual exclui o arquivo chamado ContosoFile22 da ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="a0eaa-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0eaa-117">PARAMETERS</span></span>

### <span data-ttu-id="a0eaa-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0eaa-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a0eaa-119">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a0eaa-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a0eaa-121">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a0eaa-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a0eaa-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a0eaa-123">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a0eaa-124">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a0eaa-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a0eaa-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a0eaa-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-127">The default value is 10.</span></span>

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

### <span data-ttu-id="a0eaa-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a0eaa-128">-Context</span></span>
<span data-ttu-id="a0eaa-129">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a0eaa-130">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="a0eaa-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a0eaa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0eaa-131">-DefaultProfile</span></span>
<span data-ttu-id="a0eaa-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0eaa-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="a0eaa-133">-Directory</span></span>
<span data-ttu-id="a0eaa-134">Especifica uma pasta como um objeto **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="a0eaa-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="a0eaa-135">Este cmdlet remove um arquivo na pasta especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0eaa-136">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="a0eaa-136">-File</span></span>
<span data-ttu-id="a0eaa-137">Especifica um arquivo como um objeto **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="a0eaa-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="a0eaa-138">Este cmdlet remove o arquivo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="a0eaa-139">Para obter um **objeto CloudFile,** use o cmdlet Get-AzStorageFile nuvem.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="a0eaa-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0eaa-140">-PassThru</span></span>
<span data-ttu-id="a0eaa-141">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a0eaa-142">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a0eaa-143">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a0eaa-143">-Path</span></span>
<span data-ttu-id="a0eaa-144">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-144">Specifies the path of a file.</span></span>
<span data-ttu-id="a0eaa-145">Este cmdlet exclui o arquivo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0eaa-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0eaa-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a0eaa-147">Especifica a duração do período de tempo de tempo para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a0eaa-148">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="a0eaa-148">-Share</span></span>
<span data-ttu-id="a0eaa-149">Especifica um **objeto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="a0eaa-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a0eaa-150">Este cmdlet remove o arquivo no compartilhamento especificado por este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="a0eaa-151">Para obter um **objeto CloudFileShare,** use o cmdlet Get-AzStorageShare nuvem.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="a0eaa-152">Este objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-152">This object contains the storage context.</span></span>
<span data-ttu-id="a0eaa-153">Se você especificar esse parâmetro, não especifique o *parâmetro De* contexto.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="a0eaa-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a0eaa-154">-ShareName</span></span>
<span data-ttu-id="a0eaa-155">Especifica o nome do compartilhamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="a0eaa-156">Este cmdlet remove o arquivo no compartilhamento especificado por este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="a0eaa-157">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a0eaa-157">-Confirm</span></span>
<span data-ttu-id="a0eaa-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0eaa-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0eaa-159">-WhatIf</span></span>
<span data-ttu-id="a0eaa-160">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0eaa-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0eaa-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0eaa-162">CommonParameters</span></span>
<span data-ttu-id="a0eaa-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0eaa-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0eaa-164">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0eaa-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0eaa-165">Entradas</span><span class="sxs-lookup"><span data-stu-id="a0eaa-165">INPUTS</span></span>

### <span data-ttu-id="a0eaa-166">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a0eaa-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="a0eaa-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a0eaa-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="a0eaa-168">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="a0eaa-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="a0eaa-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0eaa-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a0eaa-170">Saídas</span><span class="sxs-lookup"><span data-stu-id="a0eaa-170">OUTPUTS</span></span>

### <span data-ttu-id="a0eaa-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="a0eaa-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="a0eaa-172">Notas</span><span class="sxs-lookup"><span data-stu-id="a0eaa-172">NOTES</span></span>

## <span data-ttu-id="a0eaa-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0eaa-173">RELATED LINKS</span></span>

[<span data-ttu-id="a0eaa-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="a0eaa-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="a0eaa-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a0eaa-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="a0eaa-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0eaa-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
