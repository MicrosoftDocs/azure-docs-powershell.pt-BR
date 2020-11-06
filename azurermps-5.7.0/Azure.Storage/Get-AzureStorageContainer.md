---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
ms.openlocfilehash: 45368a3abe428c65604d4ba103cf793972e50ea1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430593"
---
# <span data-ttu-id="87597-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="87597-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="87597-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87597-102">SYNOPSIS</span></span>
<span data-ttu-id="87597-103">Lista os contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="87597-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87597-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87597-104">SYNTAX</span></span>

### <span data-ttu-id="87597-105">ContainerName (padrão)</span><span class="sxs-lookup"><span data-stu-id="87597-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="87597-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="87597-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="87597-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87597-107">DESCRIPTION</span></span>
<span data-ttu-id="87597-108">O cmdlet **Get-AzureStorageContainer** lista os contêineres de armazenamento associados à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="87597-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="87597-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87597-109">EXAMPLES</span></span>

### <span data-ttu-id="87597-110">Exemplo 1: obter blob de armazenamento do Azure por nome</span><span class="sxs-lookup"><span data-stu-id="87597-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="87597-111">Este exemplo usa um caractere curinga para retornar uma lista de todos os contêineres com um nome que começa com container.</span><span class="sxs-lookup"><span data-stu-id="87597-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="87597-112">Exemplo 2: obter contêiner de armazenamento do Azure por prefixo do nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="87597-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="87597-113">Este exemplo usa o parâmetro *prefix* para retornar uma lista de todos os contêineres com um nome que começa com container.</span><span class="sxs-lookup"><span data-stu-id="87597-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="87597-114">OS</span><span class="sxs-lookup"><span data-stu-id="87597-114">PARAMETERS</span></span>

### <span data-ttu-id="87597-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="87597-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="87597-116">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="87597-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="87597-117">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="87597-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="87597-118">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="87597-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="87597-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="87597-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="87597-120">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="87597-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="87597-121">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="87597-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="87597-122">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="87597-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="87597-123">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="87597-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="87597-124">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="87597-124">The default value is 10.</span></span>

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

### <span data-ttu-id="87597-125">-Contexto</span><span class="sxs-lookup"><span data-stu-id="87597-125">-Context</span></span>
<span data-ttu-id="87597-126">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="87597-126">Specifies the storage context.</span></span>
<span data-ttu-id="87597-127">Para criá-la, você pode usar o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="87597-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="87597-128">O cmdlet falhará quando você usar um contexto de armazenamento criado a partir do token SAS porque o cmdlet consultará as permissões de contêiner que exigem permissão de chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="87597-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="87597-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="87597-129">-ContinuationToken</span></span>
<span data-ttu-id="87597-130">Especifica um token de continuação para a lista de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="87597-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87597-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="87597-131">-MaxCount</span></span>
<span data-ttu-id="87597-132">Especifica o número máximo de objetos que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="87597-132">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="87597-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="87597-133">-Name</span></span>
<span data-ttu-id="87597-134">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="87597-134">Specifies the container name.</span></span>
<span data-ttu-id="87597-135">Se o nome do contêiner estiver vazio, o cmdlet lista todos os contêineres.</span><span class="sxs-lookup"><span data-stu-id="87597-135">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="87597-136">Caso contrário, ele lista todos os contêineres que correspondem ao nome especificado ou ao padrão de nome normal.</span><span class="sxs-lookup"><span data-stu-id="87597-136">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="87597-137">-Prefix</span><span class="sxs-lookup"><span data-stu-id="87597-137">-Prefix</span></span>
<span data-ttu-id="87597-138">Especifica um prefixo usado no nome do contêiner ou contêineres que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="87597-138">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="87597-139">Você pode usar isso para localizar todos os contêineres que começam com a mesma cadeia de caracteres, como "My" ou "Test".</span><span class="sxs-lookup"><span data-stu-id="87597-139">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87597-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="87597-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="87597-141">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="87597-141">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="87597-142">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="87597-142">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="87597-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87597-143">CommonParameters</span></span>
<span data-ttu-id="87597-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87597-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87597-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87597-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87597-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87597-146">INPUTS</span></span>

### <span data-ttu-id="87597-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="87597-147">IStorageContext</span></span>

<span data-ttu-id="87597-148">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="87597-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="87597-149">String</span><span class="sxs-lookup"><span data-stu-id="87597-149">String</span></span>

<span data-ttu-id="87597-150">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="87597-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="87597-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87597-151">OUTPUTS</span></span>

### <span data-ttu-id="87597-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="87597-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="87597-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87597-153">NOTES</span></span>

## <span data-ttu-id="87597-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87597-154">RELATED LINKS</span></span>

[<span data-ttu-id="87597-155">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="87597-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="87597-156">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="87597-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="87597-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="87597-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


