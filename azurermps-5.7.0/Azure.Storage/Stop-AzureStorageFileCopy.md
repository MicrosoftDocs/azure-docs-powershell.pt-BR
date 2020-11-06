---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
ms.openlocfilehash: ea9902b9bf678ad8f914104022a5ce5a7d04eb07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432139"
---
# <span data-ttu-id="e15b0-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e15b0-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="e15b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e15b0-102">SYNOPSIS</span></span>
<span data-ttu-id="e15b0-103">Interrompe uma operação de cópia para o arquivo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="e15b0-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e15b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e15b0-104">SYNTAX</span></span>

### <span data-ttu-id="e15b0-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="e15b0-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e15b0-106">Arquivos</span><span class="sxs-lookup"><span data-stu-id="e15b0-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e15b0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e15b0-107">DESCRIPTION</span></span>
<span data-ttu-id="e15b0-108">O cmdlet **Stop-AzureStorageFileCopy** interrompe a cópia de um arquivo para um arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="e15b0-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="e15b0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e15b0-109">EXAMPLES</span></span>

### <span data-ttu-id="e15b0-110">Exemplo 1: parar uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="e15b0-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="e15b0-111">Esse comando para de copiar um arquivo com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="e15b0-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="e15b0-112">OS</span><span class="sxs-lookup"><span data-stu-id="e15b0-112">PARAMETERS</span></span>

### <span data-ttu-id="e15b0-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e15b0-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e15b0-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="e15b0-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e15b0-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e15b0-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e15b0-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="e15b0-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e15b0-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e15b0-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e15b0-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e15b0-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e15b0-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e15b0-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e15b0-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="e15b0-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e15b0-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e15b0-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e15b0-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="e15b0-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e15b0-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e15b0-123">-Context</span></span>
<span data-ttu-id="e15b0-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e15b0-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e15b0-125">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e15b0-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e15b0-126">-Copyid</span><span class="sxs-lookup"><span data-stu-id="e15b0-126">-CopyId</span></span>
<span data-ttu-id="e15b0-127">Especifica a ID da operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="e15b0-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e15b0-128">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="e15b0-128">-File</span></span>
<span data-ttu-id="e15b0-129">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="e15b0-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e15b0-130">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="e15b0-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e15b0-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e15b0-131">-FilePath</span></span>
<span data-ttu-id="e15b0-132">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e15b0-132">Specifies the path of a file.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e15b0-133">-Force</span><span class="sxs-lookup"><span data-stu-id="e15b0-133">-Force</span></span>
<span data-ttu-id="e15b0-134">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e15b0-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e15b0-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e15b0-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e15b0-136">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e15b0-136">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e15b0-137">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e15b0-137">-ShareName</span></span>
<span data-ttu-id="e15b0-138">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e15b0-138">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="e15b0-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e15b0-139">-Confirm</span></span>
<span data-ttu-id="e15b0-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e15b0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e15b0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e15b0-141">-WhatIf</span></span>
<span data-ttu-id="e15b0-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e15b0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e15b0-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e15b0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e15b0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e15b0-144">CommonParameters</span></span>
<span data-ttu-id="e15b0-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e15b0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e15b0-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e15b0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e15b0-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e15b0-147">INPUTS</span></span>

### <span data-ttu-id="e15b0-148">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e15b0-148">IStorageContext</span></span>

<span data-ttu-id="e15b0-149">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e15b0-149">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e15b0-150">Cloudfile</span><span class="sxs-lookup"><span data-stu-id="e15b0-150">CloudFile</span></span>

<span data-ttu-id="e15b0-151">O parâmetro ' file ' aceita o valor do tipo ' Cloudfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e15b0-151">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="e15b0-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e15b0-152">OUTPUTS</span></span>

## <span data-ttu-id="e15b0-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e15b0-153">NOTES</span></span>

## <span data-ttu-id="e15b0-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e15b0-154">RELATED LINKS</span></span>

[<span data-ttu-id="e15b0-155">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e15b0-155">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="e15b0-156">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="e15b0-156">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="e15b0-157">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e15b0-157">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e15b0-158">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e15b0-158">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)