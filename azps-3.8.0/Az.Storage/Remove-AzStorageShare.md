---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: 0f8ee91c01f4486dd1d306bb9d4982fcc4658c3e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942456"
---
# <span data-ttu-id="68837-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="68837-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="68837-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68837-102">SYNOPSIS</span></span>
<span data-ttu-id="68837-103">Exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="68837-103">Deletes a file share.</span></span>

## <span data-ttu-id="68837-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68837-104">SYNTAX</span></span>

### <span data-ttu-id="68837-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="68837-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68837-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="68837-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68837-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68837-107">DESCRIPTION</span></span>
<span data-ttu-id="68837-108">O cmdlet **Remove-AzStorageShare** exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="68837-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="68837-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68837-109">EXAMPLES</span></span>

### <span data-ttu-id="68837-110">Exemplo 1: remover um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="68837-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="68837-111">Esse comando Remove o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="68837-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="68837-112">Exemplo 2: remover um compartilhamento de arquivos e todos os seus instantâneos</span><span class="sxs-lookup"><span data-stu-id="68837-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="68837-113">Esse comando Remove o compartilhamento de arquivos chamado ContosoShare06 e todos os seus instantâneos.</span><span class="sxs-lookup"><span data-stu-id="68837-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="68837-114">OS</span><span class="sxs-lookup"><span data-stu-id="68837-114">PARAMETERS</span></span>

### <span data-ttu-id="68837-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="68837-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="68837-116">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="68837-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="68837-117">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="68837-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="68837-118">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="68837-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="68837-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="68837-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="68837-120">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="68837-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="68837-121">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="68837-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="68837-122">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="68837-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="68837-123">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="68837-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="68837-124">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="68837-124">The default value is 10.</span></span>

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

### <span data-ttu-id="68837-125">-Contexto</span><span class="sxs-lookup"><span data-stu-id="68837-125">-Context</span></span>
<span data-ttu-id="68837-126">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68837-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="68837-127">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="68837-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="68837-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68837-128">-DefaultProfile</span></span>
<span data-ttu-id="68837-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68837-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68837-130">-Force</span><span class="sxs-lookup"><span data-stu-id="68837-130">-Force</span></span>
<span data-ttu-id="68837-131">Force a remoção do compartilhamento com todos os seus instantâneos e todo o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="68837-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="68837-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="68837-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="68837-133">Remover o compartilhamento de arquivos com todos os seus instantâneos</span><span class="sxs-lookup"><span data-stu-id="68837-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="68837-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="68837-134">-Name</span></span>
<span data-ttu-id="68837-135">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="68837-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="68837-136">Esse cmdlet exclui o compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="68837-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68837-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68837-137">-PassThru</span></span>
<span data-ttu-id="68837-138">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="68837-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="68837-139">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="68837-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="68837-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="68837-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="68837-141">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="68837-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="68837-142">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="68837-142">-Share</span></span>
<span data-ttu-id="68837-143">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="68837-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="68837-144">Esse cmdlet Remove o objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="68837-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="68837-145">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="68837-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="68837-146">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="68837-146">This object contains the storage context.</span></span>
<span data-ttu-id="68837-147">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="68837-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="68837-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68837-148">-Confirm</span></span>
<span data-ttu-id="68837-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68837-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68837-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68837-150">-WhatIf</span></span>
<span data-ttu-id="68837-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68837-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68837-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68837-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68837-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68837-153">CommonParameters</span></span>
<span data-ttu-id="68837-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68837-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68837-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68837-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68837-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68837-156">INPUTS</span></span>

### <span data-ttu-id="68837-157">System. String</span><span class="sxs-lookup"><span data-stu-id="68837-157">System.String</span></span>

### <span data-ttu-id="68837-158">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="68837-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="68837-159">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="68837-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="68837-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68837-160">OUTPUTS</span></span>

### <span data-ttu-id="68837-161">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="68837-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="68837-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68837-162">NOTES</span></span>

## <span data-ttu-id="68837-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68837-163">RELATED LINKS</span></span>

[<span data-ttu-id="68837-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="68837-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="68837-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="68837-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="68837-166">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="68837-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
