---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 85e91ded08fb3d4a8f026f463de58ff0b0cd7e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432698"
---
# <span data-ttu-id="fc361-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="fc361-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="fc361-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc361-102">SYNOPSIS</span></span>
<span data-ttu-id="fc361-103">Obtém o estado de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="fc361-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc361-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc361-104">SYNTAX</span></span>

### <span data-ttu-id="fc361-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="fc361-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fc361-106">Arquivos</span><span class="sxs-lookup"><span data-stu-id="fc361-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fc361-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc361-107">DESCRIPTION</span></span>
<span data-ttu-id="fc361-108">O cmdlet **Get-AzureStorageFileCopyState** Obtém o estado de uma operação de cópia de arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc361-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="fc361-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc361-109">EXAMPLES</span></span>

### <span data-ttu-id="fc361-110">Exemplo 1: obter o estado de cópia por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="fc361-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="fc361-111">Esse comando obtém o estado da operação de cópia para um arquivo que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="fc361-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="fc361-112">OS</span><span class="sxs-lookup"><span data-stu-id="fc361-112">PARAMETERS</span></span>

### <span data-ttu-id="fc361-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fc361-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fc361-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc361-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fc361-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fc361-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fc361-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="fc361-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fc361-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fc361-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fc361-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fc361-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fc361-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fc361-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fc361-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="fc361-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fc361-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fc361-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fc361-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="fc361-122">The default value is 10.</span></span>

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

### <span data-ttu-id="fc361-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fc361-123">-Context</span></span>
<span data-ttu-id="fc361-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc361-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="fc361-125">Para obter um contexto, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="fc361-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="fc361-126">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="fc361-126">-File</span></span>
<span data-ttu-id="fc361-127">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="fc361-127">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="fc361-128">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="fc361-128">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="fc361-129">-FilePath</span><span class="sxs-lookup"><span data-stu-id="fc361-129">-FilePath</span></span>
<span data-ttu-id="fc361-130">Especifica o caminho do arquivo relativo a um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc361-130">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="fc361-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fc361-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fc361-132">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="fc361-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fc361-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fc361-133">-ShareName</span></span>
<span data-ttu-id="fc361-134">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="fc361-134">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="fc361-135">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="fc361-135">-WaitForComplete</span></span>
<span data-ttu-id="fc361-136">Indica que esse cmdlet aguarda a conclusão da cópia.</span><span class="sxs-lookup"><span data-stu-id="fc361-136">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="fc361-137">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="fc361-137">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="fc361-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc361-138">CommonParameters</span></span>
<span data-ttu-id="fc361-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc361-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc361-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc361-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc361-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc361-141">INPUTS</span></span>

### <span data-ttu-id="fc361-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fc361-142">IStorageContext</span></span>

<span data-ttu-id="fc361-143">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fc361-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="fc361-144">Cloudfile</span><span class="sxs-lookup"><span data-stu-id="fc361-144">CloudFile</span></span>

<span data-ttu-id="fc361-145">O parâmetro ' file ' aceita o valor do tipo ' Cloudfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fc361-145">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="fc361-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc361-146">OUTPUTS</span></span>

## <span data-ttu-id="fc361-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc361-147">NOTES</span></span>

## <span data-ttu-id="fc361-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc361-148">RELATED LINKS</span></span>

[<span data-ttu-id="fc361-149">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="fc361-149">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="fc361-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fc361-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fc361-151">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fc361-151">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="fc361-152">Parar-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fc361-152">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
