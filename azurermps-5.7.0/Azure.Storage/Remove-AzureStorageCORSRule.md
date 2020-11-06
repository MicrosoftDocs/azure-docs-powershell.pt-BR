---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
ms.openlocfilehash: 873cee6ce1f724fb925ae743133ecfb9a1a5210a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429006"
---
# <span data-ttu-id="fe674-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fe674-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="fe674-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe674-102">SYNOPSIS</span></span>
<span data-ttu-id="fe674-103">Remove o CORS para um serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fe674-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe674-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe674-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe674-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe674-105">DESCRIPTION</span></span>
<span data-ttu-id="fe674-106">O cmdlet **Remove-AzureStorageCORSRule** remove o compartilhamento de recursos entre origens (CORS) para um serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe674-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="fe674-107">Esse cmdlet exclui todas as regras CORS em um tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fe674-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="fe674-108">Os tipos de serviços de armazenamento para esse cmdlet são BLOB, tabela, fila e arquivo.</span><span class="sxs-lookup"><span data-stu-id="fe674-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="fe674-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe674-109">EXAMPLES</span></span>

### <span data-ttu-id="fe674-110">Exemplo 1: remover regras CORS para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="fe674-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="fe674-111">Esse comando remove as regras CORS para o tipo de serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="fe674-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="fe674-112">OS</span><span class="sxs-lookup"><span data-stu-id="fe674-112">PARAMETERS</span></span>

### <span data-ttu-id="fe674-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fe674-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fe674-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="fe674-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fe674-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fe674-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fe674-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="fe674-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fe674-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fe674-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fe674-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fe674-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fe674-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fe674-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fe674-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="fe674-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fe674-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fe674-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fe674-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="fe674-122">The default value is 10.</span></span>

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

### <span data-ttu-id="fe674-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fe674-123">-Context</span></span>
<span data-ttu-id="fe674-124">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe674-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="fe674-125">Para obter o contexto de armazenamento, o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fe674-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fe674-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fe674-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fe674-127">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="fe674-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fe674-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fe674-128">-ServiceType</span></span>
<span data-ttu-id="fe674-129">Especifica o tipo de serviço de armazenamento do Azure para o qual esse cmdlet Remove regras.</span><span class="sxs-lookup"><span data-stu-id="fe674-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="fe674-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fe674-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe674-131">Irregular</span><span class="sxs-lookup"><span data-stu-id="fe674-131">Blob</span></span> 
- <span data-ttu-id="fe674-132">TableName</span><span class="sxs-lookup"><span data-stu-id="fe674-132">Table</span></span> 
- <span data-ttu-id="fe674-133">Coloca</span><span class="sxs-lookup"><span data-stu-id="fe674-133">Queue</span></span> 
- <span data-ttu-id="fe674-134">Arquivos</span><span class="sxs-lookup"><span data-stu-id="fe674-134">File</span></span>

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

### <span data-ttu-id="fe674-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe674-135">CommonParameters</span></span>
<span data-ttu-id="fe674-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe674-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe674-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe674-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe674-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe674-138">INPUTS</span></span>

### <span data-ttu-id="fe674-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe674-139">IStorageContext</span></span>

<span data-ttu-id="fe674-140">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fe674-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="fe674-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe674-141">OUTPUTS</span></span>

## <span data-ttu-id="fe674-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe674-142">NOTES</span></span>

## <span data-ttu-id="fe674-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe674-143">RELATED LINKS</span></span>

[<span data-ttu-id="fe674-144">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fe674-144">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="fe674-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fe674-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


