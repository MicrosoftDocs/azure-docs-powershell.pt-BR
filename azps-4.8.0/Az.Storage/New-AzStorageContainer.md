---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: b056504786d641d137d5188ed529eecb0ede690f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947518"
---
# <span data-ttu-id="9921e-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9921e-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="9921e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9921e-102">SYNOPSIS</span></span>
<span data-ttu-id="9921e-103">Cria um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9921e-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="9921e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9921e-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9921e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9921e-105">DESCRIPTION</span></span>
<span data-ttu-id="9921e-106">O cmdlet **New-AzStorageContainer** cria um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9921e-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="9921e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9921e-107">EXAMPLES</span></span>

### <span data-ttu-id="9921e-108">Exemplo 1: criar um contêiner de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="9921e-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="9921e-109">Esse comando cria um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9921e-109">This command creates a storage container.</span></span>

### <span data-ttu-id="9921e-110">Exemplo 2: criar vários contêineres de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="9921e-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="9921e-111">Este exemplo cria vários contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9921e-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="9921e-112">Ele usa o método **Split** da classe **String** .net e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="9921e-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="9921e-113">OS</span><span class="sxs-lookup"><span data-stu-id="9921e-113">PARAMETERS</span></span>

### <span data-ttu-id="9921e-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9921e-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9921e-115">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="9921e-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9921e-116">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9921e-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9921e-117">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9921e-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9921e-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9921e-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9921e-119">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9921e-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9921e-120">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9921e-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9921e-121">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="9921e-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9921e-122">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9921e-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9921e-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="9921e-123">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9921e-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9921e-124">-Context</span></span>
<span data-ttu-id="9921e-125">Especifica um contexto para o novo contêiner.</span><span class="sxs-lookup"><span data-stu-id="9921e-125">Specifies a context for the new container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9921e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9921e-126">-DefaultProfile</span></span>
<span data-ttu-id="9921e-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9921e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9921e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9921e-128">-Name</span></span>
<span data-ttu-id="9921e-129">Especifica um nome para o novo contêiner.</span><span class="sxs-lookup"><span data-stu-id="9921e-129">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9921e-130">-Permissão</span><span class="sxs-lookup"><span data-stu-id="9921e-130">-Permission</span></span>
<span data-ttu-id="9921e-131">Especifica o nível de acesso público a este contêiner.</span><span class="sxs-lookup"><span data-stu-id="9921e-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="9921e-132">Por padrão, o contêiner e os BLOBs nele só podem ser acessados pelo proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9921e-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="9921e-133">Para conceder permissões de leitura de usuários anônimos a um contêiner e a seus BLOBs, você pode definir as permissões de contêiner para habilitar o acesso público.</span><span class="sxs-lookup"><span data-stu-id="9921e-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="9921e-134">Usuários anônimos podem ler BLOBs em um contêiner disponível publicamente sem autenticar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9921e-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="9921e-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9921e-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9921e-136">Contêiner.</span><span class="sxs-lookup"><span data-stu-id="9921e-136">Container.</span></span>
<span data-ttu-id="9921e-137">Fornece acesso de leitura completo a um contêiner e seus BLOBs.</span><span class="sxs-lookup"><span data-stu-id="9921e-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="9921e-138">Os clientes podem enumerar BLOBs no contêiner por meio de solicitação anônima, mas não podem enumerar contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9921e-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="9921e-139">Irregular.</span><span class="sxs-lookup"><span data-stu-id="9921e-139">Blob.</span></span>
<span data-ttu-id="9921e-140">Fornece acesso de leitura a dados blob em um contêiner por meio de solicitação anônima, mas não fornece acesso a dados do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9921e-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="9921e-141">Os clientes não podem enumerar BLOBs no contêiner usando solicitação anônima.</span><span class="sxs-lookup"><span data-stu-id="9921e-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="9921e-142">Redonda.</span><span class="sxs-lookup"><span data-stu-id="9921e-142">Off.</span></span>
<span data-ttu-id="9921e-143">Que restringe o acesso somente ao proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9921e-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9921e-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9921e-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9921e-145">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9921e-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9921e-146">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9921e-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9921e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9921e-147">CommonParameters</span></span>
<span data-ttu-id="9921e-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9921e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9921e-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9921e-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9921e-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9921e-150">INPUTS</span></span>

### <span data-ttu-id="9921e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="9921e-151">System.String</span></span>

### <span data-ttu-id="9921e-152">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9921e-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9921e-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9921e-153">OUTPUTS</span></span>

### <span data-ttu-id="9921e-154">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9921e-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="9921e-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9921e-155">NOTES</span></span>

## <span data-ttu-id="9921e-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9921e-156">RELATED LINKS</span></span>

[<span data-ttu-id="9921e-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9921e-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="9921e-158">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9921e-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="9921e-159">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="9921e-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


