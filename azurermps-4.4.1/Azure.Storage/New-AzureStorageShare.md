---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a1be5816427ac1aa91b9daa98701abaec044c20f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441434"
---
# <span data-ttu-id="8749a-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="8749a-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="8749a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8749a-102">SYNOPSIS</span></span>
<span data-ttu-id="8749a-103">Cria um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8749a-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8749a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8749a-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8749a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8749a-105">DESCRIPTION</span></span>
<span data-ttu-id="8749a-106">O cmdlet **New-AzureStorageShare** cria um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8749a-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="8749a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8749a-107">EXAMPLES</span></span>

### <span data-ttu-id="8749a-108">Exemplo 1: criar um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="8749a-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="8749a-109">Esse comando cria um compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="8749a-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="8749a-110">OS</span><span class="sxs-lookup"><span data-stu-id="8749a-110">PARAMETERS</span></span>

### <span data-ttu-id="8749a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8749a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8749a-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="8749a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8749a-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8749a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8749a-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="8749a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8749a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8749a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8749a-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8749a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8749a-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8749a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8749a-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="8749a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8749a-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8749a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8749a-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="8749a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8749a-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8749a-121">-Context</span></span>
<span data-ttu-id="8749a-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8749a-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8749a-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="8749a-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8749a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8749a-124">-Name</span></span>
<span data-ttu-id="8749a-125">Especifica o nome de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8749a-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="8749a-126">Esse cmdlet cria um compartilhamento de arquivos que tem o nome que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8749a-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8749a-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8749a-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8749a-128">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="8749a-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8749a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8749a-129">CommonParameters</span></span>
<span data-ttu-id="8749a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8749a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8749a-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8749a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8749a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8749a-132">INPUTS</span></span>

### <span data-ttu-id="8749a-133">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8749a-133">IStorageContext</span></span>

<span data-ttu-id="8749a-134">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8749a-134">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8749a-135">String</span><span class="sxs-lookup"><span data-stu-id="8749a-135">String</span></span>

<span data-ttu-id="8749a-136">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8749a-136">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8749a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8749a-137">OUTPUTS</span></span>

## <span data-ttu-id="8749a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8749a-138">NOTES</span></span>

## <span data-ttu-id="8749a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8749a-139">RELATED LINKS</span></span>

[<span data-ttu-id="8749a-140">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="8749a-140">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="8749a-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8749a-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8749a-142">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="8749a-142">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
