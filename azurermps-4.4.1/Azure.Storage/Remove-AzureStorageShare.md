---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 66662899694f7b1fb93dd109e1dccefee5e00182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440262"
---
# <span data-ttu-id="e1ee5-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e1ee5-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="e1ee5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ee5-103">Exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ee5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1ee5-104">SYNTAX</span></span>

### <span data-ttu-id="e1ee5-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="e1ee5-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ee5-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="e1ee5-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1ee5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1ee5-107">DESCRIPTION</span></span>
<span data-ttu-id="e1ee5-108">O cmdlet **Remove-AzureStorageShare** exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="e1ee5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1ee5-109">EXAMPLES</span></span>

### <span data-ttu-id="e1ee5-110">Exemplo 1: remover um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="e1ee5-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="e1ee5-111">Esse comando Remove o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="e1ee5-112">OS</span><span class="sxs-lookup"><span data-stu-id="e1ee5-112">PARAMETERS</span></span>

### <span data-ttu-id="e1ee5-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1ee5-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e1ee5-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e1ee5-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e1ee5-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e1ee5-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e1ee5-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e1ee5-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e1ee5-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e1ee5-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e1ee5-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e1ee5-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e1ee5-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e1ee5-123">-Context</span></span>
<span data-ttu-id="e1ee5-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e1ee5-125">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ee5-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e1ee5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e1ee5-126">-Force</span></span>
<span data-ttu-id="e1ee5-127">Forçar a remoção do compartilhamento e todo o conteúdo dele</span><span class="sxs-lookup"><span data-stu-id="e1ee5-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="e1ee5-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1ee5-128">-Name</span></span>
<span data-ttu-id="e1ee5-129">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="e1ee5-130">Esse cmdlet exclui o compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ee5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1ee5-131">-PassThru</span></span>
<span data-ttu-id="e1ee5-132">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e1ee5-133">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e1ee5-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1ee5-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e1ee5-135">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e1ee5-136">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="e1ee5-136">-Share</span></span>
<span data-ttu-id="e1ee5-137">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="e1ee5-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="e1ee5-138">Esse cmdlet Remove o objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="e1ee5-139">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="e1ee5-140">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-140">This object contains the storage context.</span></span>
<span data-ttu-id="e1ee5-141">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="e1ee5-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="e1ee5-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1ee5-142">-Confirm</span></span>
<span data-ttu-id="e1ee5-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ee5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ee5-144">-WhatIf</span></span>
<span data-ttu-id="e1ee5-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ee5-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ee5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ee5-147">CommonParameters</span></span>
<span data-ttu-id="e1ee5-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ee5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ee5-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ee5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ee5-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1ee5-150">INPUTS</span></span>

### <span data-ttu-id="e1ee5-151">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1ee5-151">IStorageContext</span></span>

<span data-ttu-id="e1ee5-152">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e1ee5-152">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e1ee5-153">String</span><span class="sxs-lookup"><span data-stu-id="e1ee5-153">String</span></span>

<span data-ttu-id="e1ee5-154">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e1ee5-154">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e1ee5-155">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e1ee5-155">CloudFileShare</span></span>

<span data-ttu-id="e1ee5-156">O parâmetro ' Share ' aceita o valor do tipo ' CloudFileShare ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e1ee5-156">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="e1ee5-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1ee5-157">OUTPUTS</span></span>

## <span data-ttu-id="e1ee5-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1ee5-158">NOTES</span></span>

## <span data-ttu-id="e1ee5-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1ee5-159">RELATED LINKS</span></span>

[<span data-ttu-id="e1ee5-160">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e1ee5-160">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="e1ee5-161">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1ee5-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e1ee5-162">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e1ee5-162">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
