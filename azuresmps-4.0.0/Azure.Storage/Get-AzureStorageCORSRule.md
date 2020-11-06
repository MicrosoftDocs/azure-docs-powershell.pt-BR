---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c65daf144708340649b9f7b1566c5e5f2dd81e45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426163"
---
# <span data-ttu-id="efe02-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="efe02-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="efe02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efe02-102">SYNOPSIS</span></span>
<span data-ttu-id="efe02-103">Obtém regras CORS para um tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="efe02-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="efe02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efe02-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="efe02-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="efe02-105">DESCRIPTION</span></span>
<span data-ttu-id="efe02-106">O cmdlet **Get-AzureStorageCORSRule** Obtém regras de compartilhamento de recursos entre origens (CORS) para um tipo de serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="efe02-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="efe02-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efe02-107">EXAMPLES</span></span>

### <span data-ttu-id="efe02-108">Exemplo 1: obter regras CORS do serviço blob</span><span class="sxs-lookup"><span data-stu-id="efe02-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="efe02-109">Este comando obtém as regras CORS para o tipo de serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="efe02-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="efe02-110">OS</span><span class="sxs-lookup"><span data-stu-id="efe02-110">PARAMETERS</span></span>

### <span data-ttu-id="efe02-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="efe02-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="efe02-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="efe02-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="efe02-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="efe02-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="efe02-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="efe02-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="efe02-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="efe02-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="efe02-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="efe02-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="efe02-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="efe02-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="efe02-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="efe02-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="efe02-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="efe02-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="efe02-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="efe02-120">The default value is 10.</span></span>

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

### <span data-ttu-id="efe02-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="efe02-121">-Context</span></span>
<span data-ttu-id="efe02-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="efe02-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="efe02-123">Para obter um contexto, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="efe02-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="efe02-124">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="efe02-124">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="efe02-125">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="efe02-125">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="efe02-126">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="efe02-126">-ServiceType</span></span>
<span data-ttu-id="efe02-127">Especifica o tipo de serviço de armazenamento do Azure para o qual este cmdlet obtém regras CORS.</span><span class="sxs-lookup"><span data-stu-id="efe02-127">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="efe02-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="efe02-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="efe02-129">Irregular</span><span class="sxs-lookup"><span data-stu-id="efe02-129">Blob</span></span> 
- <span data-ttu-id="efe02-130">TableName</span><span class="sxs-lookup"><span data-stu-id="efe02-130">Table</span></span> 
- <span data-ttu-id="efe02-131">Coloca</span><span class="sxs-lookup"><span data-stu-id="efe02-131">Queue</span></span> 
- <span data-ttu-id="efe02-132">Arquivos</span><span class="sxs-lookup"><span data-stu-id="efe02-132">File</span></span>

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

### <span data-ttu-id="efe02-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe02-133">CommonParameters</span></span>
<span data-ttu-id="efe02-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe02-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe02-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe02-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe02-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efe02-136">INPUTS</span></span>

## <span data-ttu-id="efe02-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efe02-137">OUTPUTS</span></span>

###  
<span data-ttu-id="efe02-138">Esse cmdlet retorna uma matriz de objetos **PSCORSRule** que representam as regras CORS atualmente em um serviço.</span><span class="sxs-lookup"><span data-stu-id="efe02-138">This cmdlet returns an array of **PSCORSRule** objects which represent the CORS rules currently on a service.</span></span>

## <span data-ttu-id="efe02-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efe02-139">NOTES</span></span>

## <span data-ttu-id="efe02-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efe02-140">RELATED LINKS</span></span>

[<span data-ttu-id="efe02-141">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="efe02-141">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="efe02-142">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="efe02-142">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


