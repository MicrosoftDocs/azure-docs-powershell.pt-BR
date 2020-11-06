---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 5c3475a49c76a9a9617de02519a1f37c29059f31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441431"
---
# <span data-ttu-id="f8da6-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f8da6-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="f8da6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8da6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8da6-103">Remove o CORS para um serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f8da6-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8da6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8da6-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8da6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8da6-105">DESCRIPTION</span></span>
<span data-ttu-id="f8da6-106">O cmdlet **Remove-AzureStorageCORSRule** remove o compartilhamento de recursos entre origens (CORS) para um serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8da6-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="f8da6-107">Esse cmdlet exclui todas as regras CORS em um tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f8da6-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="f8da6-108">Os tipos de serviços de armazenamento para esse cmdlet são BLOB, tabela, fila e arquivo.</span><span class="sxs-lookup"><span data-stu-id="f8da6-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="f8da6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8da6-109">EXAMPLES</span></span>

### <span data-ttu-id="f8da6-110">Exemplo 1: remover regras CORS para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="f8da6-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="f8da6-111">Esse comando remove as regras CORS para o tipo de serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="f8da6-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="f8da6-112">OS</span><span class="sxs-lookup"><span data-stu-id="f8da6-112">PARAMETERS</span></span>

### <span data-ttu-id="f8da6-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f8da6-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f8da6-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="f8da6-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f8da6-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f8da6-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f8da6-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f8da6-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f8da6-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f8da6-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f8da6-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f8da6-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f8da6-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f8da6-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f8da6-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="f8da6-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f8da6-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="f8da6-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f8da6-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="f8da6-122">The default value is 10.</span></span>

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

### <span data-ttu-id="f8da6-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f8da6-123">-Context</span></span>
<span data-ttu-id="f8da6-124">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8da6-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f8da6-125">Para obter o contexto de armazenamento, o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f8da6-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f8da6-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f8da6-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f8da6-127">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="f8da6-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f8da6-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f8da6-128">-ServiceType</span></span>
<span data-ttu-id="f8da6-129">Especifica o tipo de serviço de armazenamento do Azure para o qual esse cmdlet Remove regras.</span><span class="sxs-lookup"><span data-stu-id="f8da6-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="f8da6-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f8da6-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f8da6-131">Irregular</span><span class="sxs-lookup"><span data-stu-id="f8da6-131">Blob</span></span> 
- <span data-ttu-id="f8da6-132">TableName</span><span class="sxs-lookup"><span data-stu-id="f8da6-132">Table</span></span> 
- <span data-ttu-id="f8da6-133">Coloca</span><span class="sxs-lookup"><span data-stu-id="f8da6-133">Queue</span></span> 
- <span data-ttu-id="f8da6-134">Arquivos</span><span class="sxs-lookup"><span data-stu-id="f8da6-134">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8da6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8da6-135">CommonParameters</span></span>
<span data-ttu-id="f8da6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8da6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8da6-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8da6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8da6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8da6-138">INPUTS</span></span>

### <span data-ttu-id="f8da6-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8da6-139">IStorageContext</span></span>

<span data-ttu-id="f8da6-140">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f8da6-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="f8da6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8da6-141">OUTPUTS</span></span>

## <span data-ttu-id="f8da6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8da6-142">NOTES</span></span>

## <span data-ttu-id="f8da6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8da6-143">RELATED LINKS</span></span>

[<span data-ttu-id="f8da6-144">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f8da6-144">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="f8da6-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f8da6-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


