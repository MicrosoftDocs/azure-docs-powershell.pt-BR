---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: 5e2021277792bbaf52b6fcf6ffba88d71c854c7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886542"
---
# <span data-ttu-id="1fe46-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="1fe46-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="1fe46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe46-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe46-103">Exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1fe46-103">Deletes a file share.</span></span>

## <span data-ttu-id="1fe46-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1fe46-104">SYNTAX</span></span>

### <span data-ttu-id="1fe46-105">ShareName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1fe46-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fe46-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="1fe46-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fe46-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1fe46-107">DESCRIPTION</span></span>
<span data-ttu-id="1fe46-108">O cmdlet **Remove-AzStorageShare** exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1fe46-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="1fe46-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fe46-109">EXAMPLES</span></span>

### <span data-ttu-id="1fe46-110">Exemplo 1: Remover um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="1fe46-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="1fe46-111">Este comando remove o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="1fe46-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="1fe46-112">Exemplo 2: Remover um compartilhamento de arquivos e todos os instantâneos</span><span class="sxs-lookup"><span data-stu-id="1fe46-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="1fe46-113">Este comando remove o compartilhamento de arquivos chamado ContosoShare06 e todos os instantâneos.</span><span class="sxs-lookup"><span data-stu-id="1fe46-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="1fe46-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1fe46-114">PARAMETERS</span></span>

### <span data-ttu-id="1fe46-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1fe46-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1fe46-116">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1fe46-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1fe46-117">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1fe46-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1fe46-118">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1fe46-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1fe46-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1fe46-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1fe46-120">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1fe46-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1fe46-121">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1fe46-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1fe46-122">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="1fe46-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1fe46-123">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1fe46-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1fe46-124">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="1fe46-124">The default value is 10.</span></span>

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

### <span data-ttu-id="1fe46-125">-Context</span><span class="sxs-lookup"><span data-stu-id="1fe46-125">-Context</span></span>
<span data-ttu-id="1fe46-126">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe46-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1fe46-127">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="1fe46-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1fe46-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe46-128">-DefaultProfile</span></span>
<span data-ttu-id="1fe46-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe46-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe46-130">-Force</span><span class="sxs-lookup"><span data-stu-id="1fe46-130">-Force</span></span>
<span data-ttu-id="1fe46-131">Force a remover o compartilhamento com todos os instantâneos e todo o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1fe46-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="1fe46-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="1fe46-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="1fe46-133">Remover Compartilhamento de Arquivos com todos os instantâneos</span><span class="sxs-lookup"><span data-stu-id="1fe46-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="1fe46-134">-Name</span><span class="sxs-lookup"><span data-stu-id="1fe46-134">-Name</span></span>
<span data-ttu-id="1fe46-135">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1fe46-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="1fe46-136">Este cmdlet exclui o compartilhamento de arquivos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1fe46-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="1fe46-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fe46-137">-PassThru</span></span>
<span data-ttu-id="1fe46-138">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="1fe46-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1fe46-139">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1fe46-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1fe46-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1fe46-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1fe46-141">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="1fe46-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1fe46-142">-Share</span><span class="sxs-lookup"><span data-stu-id="1fe46-142">-Share</span></span>
<span data-ttu-id="1fe46-143">Especifica um **objeto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="1fe46-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1fe46-144">Este cmdlet remove o objeto especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1fe46-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="1fe46-145">Para obter um **objeto CloudFileShare,** use Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe46-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="1fe46-146">Este objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1fe46-146">This object contains the storage context.</span></span>
<span data-ttu-id="1fe46-147">Se você especificar esse parâmetro, não especifique o *parâmetro Context.*</span><span class="sxs-lookup"><span data-stu-id="1fe46-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="1fe46-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fe46-148">-Confirm</span></span>
<span data-ttu-id="1fe46-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe46-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe46-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe46-150">-WhatIf</span></span>
<span data-ttu-id="1fe46-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1fe46-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe46-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fe46-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe46-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe46-153">CommonParameters</span></span>
<span data-ttu-id="1fe46-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe46-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe46-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe46-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe46-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fe46-156">INPUTS</span></span>

### <span data-ttu-id="1fe46-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1fe46-157">System.String</span></span>

### <span data-ttu-id="1fe46-158">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="1fe46-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="1fe46-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1fe46-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1fe46-160">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1fe46-160">OUTPUTS</span></span>

### <span data-ttu-id="1fe46-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="1fe46-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="1fe46-162">NOTES</span><span class="sxs-lookup"><span data-stu-id="1fe46-162">NOTES</span></span>

## <span data-ttu-id="1fe46-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fe46-163">RELATED LINKS</span></span>

[<span data-ttu-id="1fe46-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="1fe46-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="1fe46-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1fe46-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1fe46-166">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="1fe46-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
