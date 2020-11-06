---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425916"
---
# <span data-ttu-id="a6c4e-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a6c4e-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="a6c4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c4e-103">Exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-103">Deletes a file share.</span></span>

## <span data-ttu-id="a6c4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6c4e-104">SYNTAX</span></span>

### <span data-ttu-id="a6c4e-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6c4e-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c4e-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="a6c4e-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c4e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6c4e-107">DESCRIPTION</span></span>
<span data-ttu-id="a6c4e-108">O cmdlet **Remove-AzureStorageShare** exclui um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="a6c4e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6c4e-109">EXAMPLES</span></span>

### <span data-ttu-id="a6c4e-110">Exemplo 1: remover um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="a6c4e-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="a6c4e-111">Esse comando Remove o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="a6c4e-112">OS</span><span class="sxs-lookup"><span data-stu-id="a6c4e-112">PARAMETERS</span></span>

### <span data-ttu-id="a6c4e-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6c4e-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a6c4e-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a6c4e-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a6c4e-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a6c4e-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a6c4e-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a6c4e-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a6c4e-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a6c4e-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a6c4e-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a6c4e-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-122">The default value is 10.</span></span>

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

### <span data-ttu-id="a6c4e-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a6c4e-123">-Context</span></span>
<span data-ttu-id="a6c4e-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a6c4e-125">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="a6c4e-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a6c4e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a6c4e-126">-Force</span></span>
<span data-ttu-id="a6c4e-127">Forçar a remoção do compartilhamento e todo o conteúdo dele</span><span class="sxs-lookup"><span data-stu-id="a6c4e-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="a6c4e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6c4e-128">-Name</span></span>
<span data-ttu-id="a6c4e-129">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="a6c4e-130">Esse cmdlet exclui o compartilhamento de arquivos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6c4e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6c4e-131">-PassThru</span></span>
<span data-ttu-id="a6c4e-132">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a6c4e-133">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a6c4e-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6c4e-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a6c4e-135">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a6c4e-136">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="a6c4e-136">-Share</span></span>
<span data-ttu-id="a6c4e-137">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="a6c4e-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a6c4e-138">Esse cmdlet Remove o objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="a6c4e-139">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="a6c4e-140">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-140">This object contains the storage context.</span></span>
<span data-ttu-id="a6c4e-141">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="a6c4e-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="a6c4e-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6c4e-142">-Confirm</span></span>
<span data-ttu-id="a6c4e-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c4e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c4e-144">-WhatIf</span></span>
<span data-ttu-id="a6c4e-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c4e-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c4e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c4e-147">CommonParameters</span></span>
<span data-ttu-id="a6c4e-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c4e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c4e-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c4e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c4e-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6c4e-150">INPUTS</span></span>

## <span data-ttu-id="a6c4e-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6c4e-151">OUTPUTS</span></span>

## <span data-ttu-id="a6c4e-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6c4e-152">NOTES</span></span>

## <span data-ttu-id="a6c4e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6c4e-153">RELATED LINKS</span></span>

[<span data-ttu-id="a6c4e-154">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a6c4e-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="a6c4e-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6c4e-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a6c4e-156">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a6c4e-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
