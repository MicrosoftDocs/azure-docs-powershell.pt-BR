---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
ms.openlocfilehash: 43a1a18675a662e30e88dd2d96f2fc901ffab8dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609465"
---
# <span data-ttu-id="9e376-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9e376-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="9e376-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e376-102">SYNOPSIS</span></span>
<span data-ttu-id="9e376-103">Exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9e376-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e376-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e376-104">SYNTAX</span></span>

### <span data-ttu-id="9e376-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e376-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e376-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="9e376-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e376-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e376-107">DESCRIPTION</span></span>
<span data-ttu-id="9e376-108">O cmdlet **Remove-AzureStorageShare** exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9e376-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="9e376-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e376-109">EXAMPLES</span></span>

### <span data-ttu-id="9e376-110">Exemplo 1: remover um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="9e376-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="9e376-111">Esse comando Remove o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9e376-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="9e376-112">Exemplo 2: remover um compartilhamento de arquivos e todos os seus instantâneos</span><span class="sxs-lookup"><span data-stu-id="9e376-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="9e376-113">Esse comando Remove o compartilhamento de arquivos chamado ContosoShare06 e todos os seus instantâneos.</span><span class="sxs-lookup"><span data-stu-id="9e376-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="9e376-114">OS</span><span class="sxs-lookup"><span data-stu-id="9e376-114">PARAMETERS</span></span>

### <span data-ttu-id="9e376-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e376-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9e376-116">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e376-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9e376-117">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9e376-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9e376-118">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9e376-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9e376-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9e376-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9e376-120">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9e376-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9e376-121">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9e376-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9e376-122">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="9e376-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9e376-123">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9e376-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9e376-124">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="9e376-124">The default value is 10.</span></span>

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

### <span data-ttu-id="9e376-125">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9e376-125">-Context</span></span>
<span data-ttu-id="9e376-126">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e376-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9e376-127">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9e376-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9e376-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e376-128">-DefaultProfile</span></span>
<span data-ttu-id="9e376-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e376-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e376-130">-Force</span><span class="sxs-lookup"><span data-stu-id="9e376-130">-Force</span></span>
<span data-ttu-id="9e376-131">Force a remoção do compartilhamento com todos os seus instantâneos e todo o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9e376-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="9e376-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="9e376-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="9e376-133">Remover o compartilhamento de arquivos com todos os seus instantâneos</span><span class="sxs-lookup"><span data-stu-id="9e376-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="9e376-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e376-134">-Name</span></span>
<span data-ttu-id="9e376-135">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9e376-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="9e376-136">Esse cmdlet exclui o compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9e376-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e376-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e376-137">-PassThru</span></span>
<span data-ttu-id="9e376-138">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="9e376-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9e376-139">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9e376-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9e376-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e376-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9e376-141">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9e376-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9e376-142">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="9e376-142">-Share</span></span>
<span data-ttu-id="9e376-143">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="9e376-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9e376-144">Esse cmdlet Remove o objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9e376-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="9e376-145">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="9e376-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="9e376-146">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9e376-146">This object contains the storage context.</span></span>
<span data-ttu-id="9e376-147">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="9e376-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9e376-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e376-148">-Confirm</span></span>
<span data-ttu-id="9e376-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e376-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e376-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e376-150">-WhatIf</span></span>
<span data-ttu-id="9e376-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e376-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e376-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e376-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e376-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e376-153">CommonParameters</span></span>
<span data-ttu-id="9e376-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e376-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e376-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e376-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e376-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e376-156">INPUTS</span></span>

### <span data-ttu-id="9e376-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9e376-157">System.String</span></span>

### <span data-ttu-id="9e376-158">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9e376-158">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="9e376-159">Parâmetros: share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e376-159">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="9e376-160">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e376-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9e376-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e376-161">OUTPUTS</span></span>

### <span data-ttu-id="9e376-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9e376-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="9e376-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e376-163">NOTES</span></span>

## <span data-ttu-id="9e376-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e376-164">RELATED LINKS</span></span>

[<span data-ttu-id="9e376-165">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9e376-165">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="9e376-166">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e376-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9e376-167">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9e376-167">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
