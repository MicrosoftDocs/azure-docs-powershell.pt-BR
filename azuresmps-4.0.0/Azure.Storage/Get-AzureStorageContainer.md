---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66845678619a7777bbda9257aa208393b0fa178c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426161"
---
# <span data-ttu-id="fdba0-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fdba0-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="fdba0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdba0-102">SYNOPSIS</span></span>
<span data-ttu-id="fdba0-103">Lista os contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fdba0-103">Lists the storage containers.</span></span>

## <span data-ttu-id="fdba0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdba0-104">SYNTAX</span></span>

### <span data-ttu-id="fdba0-105">ContainerName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fdba0-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fdba0-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="fdba0-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fdba0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdba0-107">DESCRIPTION</span></span>
<span data-ttu-id="fdba0-108">O cmdlet **Get-AzureStorageContainer** lista os contêineres de armazenamento associados à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="fdba0-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="fdba0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdba0-109">EXAMPLES</span></span>

### <span data-ttu-id="fdba0-110">Exemplo 1: obter blob de armazenamento do Azure por nome</span><span class="sxs-lookup"><span data-stu-id="fdba0-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="fdba0-111">Este exemplo usa um caractere curinga para retornar uma lista de todos os contêineres com um nome que começa com container.</span><span class="sxs-lookup"><span data-stu-id="fdba0-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="fdba0-112">Exemplo 2: obter contêiner de armazenamento do Azure por prefixo do nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="fdba0-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="fdba0-113">Este exemplo usa o parâmetro *prefix* para retornar uma lista de todos os contêineres com um nome que começa com container.</span><span class="sxs-lookup"><span data-stu-id="fdba0-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="fdba0-114">OS</span><span class="sxs-lookup"><span data-stu-id="fdba0-114">PARAMETERS</span></span>

### <span data-ttu-id="fdba0-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fdba0-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fdba0-116">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="fdba0-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fdba0-117">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fdba0-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fdba0-118">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="fdba0-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fdba0-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fdba0-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fdba0-120">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fdba0-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fdba0-121">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fdba0-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fdba0-122">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="fdba0-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fdba0-123">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fdba0-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fdba0-124">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="fdba0-124">The default value is 10.</span></span>

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

### <span data-ttu-id="fdba0-125">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fdba0-125">-Context</span></span>
<span data-ttu-id="fdba0-126">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fdba0-126">Specifies the storage context.</span></span>
<span data-ttu-id="fdba0-127">Para criá-la, você pode usar o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fdba0-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fdba0-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="fdba0-128">-ContinuationToken</span></span>
<span data-ttu-id="fdba0-129">Especifica um token de continuação para a lista de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="fdba0-129">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="fdba0-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fdba0-130">-MaxCount</span></span>
<span data-ttu-id="fdba0-131">Especifica o número máximo de objetos que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="fdba0-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="fdba0-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdba0-132">-Name</span></span>
<span data-ttu-id="fdba0-133">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fdba0-133">Specifies the container name.</span></span>
<span data-ttu-id="fdba0-134">Se o nome do contêiner estiver vazio, o cmdlet lista todos os contêineres.</span><span class="sxs-lookup"><span data-stu-id="fdba0-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="fdba0-135">Caso contrário, ele lista todos os contêineres que correspondem ao nome especificado ou ao padrão de nome normal.</span><span class="sxs-lookup"><span data-stu-id="fdba0-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdba0-136">-Prefix</span><span class="sxs-lookup"><span data-stu-id="fdba0-136">-Prefix</span></span>
<span data-ttu-id="fdba0-137">Especifica um prefixo usado no nome do contêiner ou contêineres que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="fdba0-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="fdba0-138">Você pode usar isso para localizar todos os contêineres que começam com a mesma cadeia de caracteres, como "My" ou "Test".</span><span class="sxs-lookup"><span data-stu-id="fdba0-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="fdba0-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fdba0-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fdba0-140">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="fdba0-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fdba0-141">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="fdba0-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fdba0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdba0-142">CommonParameters</span></span>
<span data-ttu-id="fdba0-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdba0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdba0-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdba0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdba0-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdba0-145">INPUTS</span></span>

## <span data-ttu-id="fdba0-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdba0-146">OUTPUTS</span></span>

## <span data-ttu-id="fdba0-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdba0-147">NOTES</span></span>

## <span data-ttu-id="fdba0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdba0-148">RELATED LINKS</span></span>

[<span data-ttu-id="fdba0-149">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fdba0-149">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="fdba0-150">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fdba0-150">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="fdba0-151">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="fdba0-151">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


