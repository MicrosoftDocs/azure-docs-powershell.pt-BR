---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 174353aacbfe939294f654a4f5f61548bfc672dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441445"
---
# <span data-ttu-id="43f0d-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43f0d-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="43f0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="43f0d-103">Obtém a política de acesso armazenado ou políticas para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="43f0d-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43f0d-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="43f0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="43f0d-106">O cmdlet **Get-AzureStorageContainerStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="43f0d-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="43f0d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43f0d-107">EXAMPLES</span></span>

### <span data-ttu-id="43f0d-108">Exemplo 1: obter uma política de acesso armazenado em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="43f0d-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="43f0d-109">Esse comando obtém a política de acesso chamada Policy22 no contêiner de armazenamento chamado Container07.</span><span class="sxs-lookup"><span data-stu-id="43f0d-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="43f0d-110">Exemplo 2: obter todas as políticas de acesso armazenadas em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="43f0d-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="43f0d-111">Esse comando obtém todas as políticas de acesso no contêiner de armazenamento chamado Container07.</span><span class="sxs-lookup"><span data-stu-id="43f0d-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="43f0d-112">OS</span><span class="sxs-lookup"><span data-stu-id="43f0d-112">PARAMETERS</span></span>

### <span data-ttu-id="43f0d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="43f0d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="43f0d-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="43f0d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="43f0d-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="43f0d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="43f0d-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="43f0d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="43f0d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="43f0d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="43f0d-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="43f0d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="43f0d-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="43f0d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="43f0d-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="43f0d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="43f0d-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="43f0d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="43f0d-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="43f0d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="43f0d-123">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="43f0d-123">-Container</span></span>
<span data-ttu-id="43f0d-124">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="43f0d-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43f0d-125">-Contexto</span><span class="sxs-lookup"><span data-stu-id="43f0d-125">-Context</span></span>
<span data-ttu-id="43f0d-126">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="43f0d-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="43f0d-127">-Política</span><span class="sxs-lookup"><span data-stu-id="43f0d-127">-Policy</span></span>
<span data-ttu-id="43f0d-128">Especifica a política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="43f0d-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f0d-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="43f0d-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="43f0d-130">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="43f0d-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="43f0d-131">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="43f0d-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="43f0d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f0d-132">CommonParameters</span></span>
<span data-ttu-id="43f0d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f0d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f0d-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f0d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f0d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43f0d-135">INPUTS</span></span>

### <span data-ttu-id="43f0d-136">String</span><span class="sxs-lookup"><span data-stu-id="43f0d-136">String</span></span>

<span data-ttu-id="43f0d-137">O parâmetro ' container ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="43f0d-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="43f0d-138">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="43f0d-138">IStorageContext</span></span>

<span data-ttu-id="43f0d-139">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="43f0d-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="43f0d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43f0d-140">OUTPUTS</span></span>

### <span data-ttu-id="43f0d-141">Microsoft. WindowsAzure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="43f0d-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="43f0d-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43f0d-142">NOTES</span></span>

## <span data-ttu-id="43f0d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43f0d-143">RELATED LINKS</span></span>

[<span data-ttu-id="43f0d-144">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43f0d-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="43f0d-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43f0d-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="43f0d-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43f0d-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


