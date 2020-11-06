---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75e94fe8270287410902b215ec4e33ac9cd51624
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426154"
---
# <span data-ttu-id="1fca2-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="1fca2-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="1fca2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fca2-102">SYNOPSIS</span></span>
<span data-ttu-id="1fca2-103">Obtém o estado de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="1fca2-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="1fca2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fca2-104">SYNTAX</span></span>

### <span data-ttu-id="1fca2-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="1fca2-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1fca2-106">Arquivos</span><span class="sxs-lookup"><span data-stu-id="1fca2-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1fca2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fca2-107">DESCRIPTION</span></span>
<span data-ttu-id="1fca2-108">O cmdlet **Get-AzureStorageFileCopyState** Obtém o estado de uma operação de cópia de arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fca2-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="1fca2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fca2-109">EXAMPLES</span></span>

### <span data-ttu-id="1fca2-110">Exemplo 1: obter o estado de cópia por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="1fca2-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="1fca2-111">Esse comando obtém o estado da operação de cópia para um arquivo que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="1fca2-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="1fca2-112">OS</span><span class="sxs-lookup"><span data-stu-id="1fca2-112">PARAMETERS</span></span>

### <span data-ttu-id="1fca2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1fca2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1fca2-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1fca2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1fca2-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1fca2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1fca2-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1fca2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1fca2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1fca2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1fca2-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1fca2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1fca2-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1fca2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1fca2-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="1fca2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1fca2-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1fca2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1fca2-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="1fca2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="1fca2-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1fca2-123">-Context</span></span>
<span data-ttu-id="1fca2-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fca2-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1fca2-125">Para obter um contexto, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="1fca2-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1fca2-126">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="1fca2-126">-File</span></span>
<span data-ttu-id="1fca2-127">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="1fca2-127">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="1fca2-128">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="1fca2-128">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="1fca2-129">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1fca2-129">-FilePath</span></span>
<span data-ttu-id="1fca2-130">Especifica o caminho do arquivo relativo a um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fca2-130">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="1fca2-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1fca2-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1fca2-132">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="1fca2-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1fca2-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1fca2-133">-ShareName</span></span>
<span data-ttu-id="1fca2-134">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1fca2-134">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="1fca2-135">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="1fca2-135">-WaitForComplete</span></span>
<span data-ttu-id="1fca2-136">Indica que esse cmdlet aguarda a conclusão da cópia.</span><span class="sxs-lookup"><span data-stu-id="1fca2-136">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="1fca2-137">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1fca2-137">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="1fca2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fca2-138">CommonParameters</span></span>
<span data-ttu-id="1fca2-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fca2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fca2-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fca2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fca2-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fca2-141">INPUTS</span></span>

## <span data-ttu-id="1fca2-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fca2-142">OUTPUTS</span></span>

## <span data-ttu-id="1fca2-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fca2-143">NOTES</span></span>

## <span data-ttu-id="1fca2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fca2-144">RELATED LINKS</span></span>

[<span data-ttu-id="1fca2-145">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1fca2-145">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="1fca2-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1fca2-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1fca2-147">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1fca2-147">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="1fca2-148">Parar-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1fca2-148">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
