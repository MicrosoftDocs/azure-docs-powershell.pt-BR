---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426135"
---
# <span data-ttu-id="fce78-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fce78-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="fce78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fce78-102">SYNOPSIS</span></span>
<span data-ttu-id="fce78-103">Cria um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fce78-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="fce78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fce78-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fce78-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fce78-105">DESCRIPTION</span></span>
<span data-ttu-id="fce78-106">O cmdlet **New-AzureStorageContainer** cria um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fce78-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="fce78-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fce78-107">EXAMPLES</span></span>

### <span data-ttu-id="fce78-108">Exemplo 1: criar um contêiner de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="fce78-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="fce78-109">Esse comando cria um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fce78-109">This command creates a storage container.</span></span>

### <span data-ttu-id="fce78-110">Exemplo 2: criar vários contêineres de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="fce78-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="fce78-111">Este exemplo cria vários contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fce78-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="fce78-112">Ele usa o método **Split** da classe **String** .net e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="fce78-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="fce78-113">OS</span><span class="sxs-lookup"><span data-stu-id="fce78-113">PARAMETERS</span></span>

### <span data-ttu-id="fce78-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fce78-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fce78-115">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="fce78-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fce78-116">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fce78-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fce78-117">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="fce78-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fce78-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fce78-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fce78-119">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fce78-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fce78-120">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fce78-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fce78-121">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="fce78-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fce78-122">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fce78-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fce78-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="fce78-123">The default value is 10.</span></span>

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

### <span data-ttu-id="fce78-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fce78-124">-Context</span></span>
<span data-ttu-id="fce78-125">Especifica um contexto para o novo contêiner.</span><span class="sxs-lookup"><span data-stu-id="fce78-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="fce78-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="fce78-126">-Name</span></span>
<span data-ttu-id="fce78-127">Especifica um nome para o novo contêiner.</span><span class="sxs-lookup"><span data-stu-id="fce78-127">Specifies a name for the new container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fce78-128">-Permissão</span><span class="sxs-lookup"><span data-stu-id="fce78-128">-Permission</span></span>
<span data-ttu-id="fce78-129">Especifica o nível de acesso público a este contêiner.</span><span class="sxs-lookup"><span data-stu-id="fce78-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="fce78-130">Por padrão, o contêiner e os BLOBs nele só podem ser acessados pelo proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fce78-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="fce78-131">Para conceder permissões de leitura de usuários anônimos a um contêiner e a seus BLOBs, você pode definir as permissões de contêiner para habilitar o acesso público.</span><span class="sxs-lookup"><span data-stu-id="fce78-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="fce78-132">Usuários anônimos podem ler BLOBs em um contêiner disponível publicamente sem autenticar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fce78-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="fce78-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fce78-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fce78-134">Contêiner.</span><span class="sxs-lookup"><span data-stu-id="fce78-134">Container.</span></span>
<span data-ttu-id="fce78-135">Fornece acesso de leitura completo a um contêiner e seus BLOBs.</span><span class="sxs-lookup"><span data-stu-id="fce78-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="fce78-136">Os clientes podem enumerar BLOBs no contêiner por meio de solicitação anônima, mas não podem enumerar contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fce78-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="fce78-137">Irregular.</span><span class="sxs-lookup"><span data-stu-id="fce78-137">Blob.</span></span>
<span data-ttu-id="fce78-138">Fornece acesso de leitura a dados blob em um contêiner por meio de solicitação anônima, mas não fornece acesso a dados do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fce78-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="fce78-139">Os clientes não podem enumerar BLOBs no contêiner usando solicitação anônima.</span><span class="sxs-lookup"><span data-stu-id="fce78-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="fce78-140">Redonda.</span><span class="sxs-lookup"><span data-stu-id="fce78-140">Off.</span></span>
<span data-ttu-id="fce78-141">Que restringe o acesso somente ao proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fce78-141">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce78-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fce78-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fce78-143">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="fce78-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fce78-144">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="fce78-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fce78-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce78-145">CommonParameters</span></span>
<span data-ttu-id="fce78-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce78-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce78-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce78-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce78-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fce78-148">INPUTS</span></span>

## <span data-ttu-id="fce78-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fce78-149">OUTPUTS</span></span>

## <span data-ttu-id="fce78-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fce78-150">NOTES</span></span>

## <span data-ttu-id="fce78-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fce78-151">RELATED LINKS</span></span>

[<span data-ttu-id="fce78-152">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fce78-152">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="fce78-153">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fce78-153">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="fce78-154">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="fce78-154">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)

