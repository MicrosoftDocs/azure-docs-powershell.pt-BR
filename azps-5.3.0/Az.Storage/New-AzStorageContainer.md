---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98264627"
---
# <span data-ttu-id="61c57-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="61c57-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="61c57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61c57-102">SYNOPSIS</span></span>
<span data-ttu-id="61c57-103">Cria um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="61c57-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="61c57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61c57-104">SYNTAX</span></span>

### <span data-ttu-id="61c57-105">ContainerName (padrão)</span><span class="sxs-lookup"><span data-stu-id="61c57-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="61c57-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="61c57-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="61c57-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61c57-107">DESCRIPTION</span></span>
<span data-ttu-id="61c57-108">O cmdlet **New-AzStorageContainer** cria um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="61c57-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="61c57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61c57-109">EXAMPLES</span></span>

### <span data-ttu-id="61c57-110">Exemplo 1: criar um contêiner de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="61c57-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="61c57-111">Esse comando cria um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61c57-111">This command creates a storage container.</span></span>

### <span data-ttu-id="61c57-112">Exemplo 2: criar vários contêineres de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="61c57-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="61c57-113">Este exemplo cria vários contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61c57-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="61c57-114">Ele usa o método **Split** da classe **String** .net e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="61c57-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="61c57-115">Exemplo 3: criar um contêiner de armazenamento do Azure com escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="61c57-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="61c57-116">Esse comando cria um contêiner de armazenamento, com o escopo de criptografia padrão como myencryptscope, e o carregamento de BLOBs prevertidos com diferentes escopos de criptografia para esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="61c57-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="61c57-117">OS</span><span class="sxs-lookup"><span data-stu-id="61c57-117">PARAMETERS</span></span>

### <span data-ttu-id="61c57-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61c57-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="61c57-119">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="61c57-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="61c57-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="61c57-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="61c57-121">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="61c57-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="61c57-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="61c57-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="61c57-123">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="61c57-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="61c57-124">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="61c57-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="61c57-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="61c57-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="61c57-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="61c57-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="61c57-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="61c57-127">The default value is 10.</span></span>

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

### <span data-ttu-id="61c57-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="61c57-128">-Context</span></span>
<span data-ttu-id="61c57-129">Especifica um contexto para o novo contêiner.</span><span class="sxs-lookup"><span data-stu-id="61c57-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="61c57-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="61c57-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="61c57-131">Use o contêiner padrão para usar o escopo de criptografia especificado para todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="61c57-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c57-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c57-132">-DefaultProfile</span></span>
<span data-ttu-id="61c57-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61c57-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61c57-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="61c57-134">-Name</span></span>
<span data-ttu-id="61c57-135">Especifica um nome para o novo contêiner.</span><span class="sxs-lookup"><span data-stu-id="61c57-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="61c57-136">-Permissão</span><span class="sxs-lookup"><span data-stu-id="61c57-136">-Permission</span></span>
<span data-ttu-id="61c57-137">Especifica o nível de acesso público a este contêiner.</span><span class="sxs-lookup"><span data-stu-id="61c57-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="61c57-138">Por padrão, o contêiner e os BLOBs nele só podem ser acessados pelo proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61c57-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="61c57-139">Para conceder permissões de leitura de usuários anônimos a um contêiner e a seus BLOBs, você pode definir as permissões de contêiner para habilitar o acesso público.</span><span class="sxs-lookup"><span data-stu-id="61c57-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="61c57-140">Usuários anônimos podem ler BLOBs em um contêiner disponível publicamente sem autenticar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="61c57-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="61c57-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="61c57-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="61c57-142">Contêiner.</span><span class="sxs-lookup"><span data-stu-id="61c57-142">Container.</span></span>
<span data-ttu-id="61c57-143">Fornece acesso de leitura completo a um contêiner e seus BLOBs.</span><span class="sxs-lookup"><span data-stu-id="61c57-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="61c57-144">Os clientes podem enumerar BLOBs no contêiner por meio de solicitação anônima, mas não podem enumerar contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61c57-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="61c57-145">Irregular.</span><span class="sxs-lookup"><span data-stu-id="61c57-145">Blob.</span></span>
<span data-ttu-id="61c57-146">Fornece acesso de leitura a dados blob em um contêiner por meio de solicitação anônima, mas não fornece acesso a dados do contêiner.</span><span class="sxs-lookup"><span data-stu-id="61c57-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="61c57-147">Os clientes não podem enumerar BLOBs no contêiner usando solicitação anônima.</span><span class="sxs-lookup"><span data-stu-id="61c57-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="61c57-148">Redonda.</span><span class="sxs-lookup"><span data-stu-id="61c57-148">Off.</span></span>
<span data-ttu-id="61c57-149">Que restringe o acesso somente ao proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61c57-149">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="61c57-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="61c57-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="61c57-151">Bloquear a substituição do escopo de criptografia do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="61c57-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c57-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61c57-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="61c57-153">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="61c57-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="61c57-154">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="61c57-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="61c57-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c57-155">CommonParameters</span></span>
<span data-ttu-id="61c57-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c57-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c57-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c57-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c57-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61c57-158">INPUTS</span></span>

### <span data-ttu-id="61c57-159">System. String</span><span class="sxs-lookup"><span data-stu-id="61c57-159">System.String</span></span>

### <span data-ttu-id="61c57-160">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="61c57-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="61c57-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61c57-161">OUTPUTS</span></span>

### <span data-ttu-id="61c57-162">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="61c57-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="61c57-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61c57-163">NOTES</span></span>

## <span data-ttu-id="61c57-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61c57-164">RELATED LINKS</span></span>

[<span data-ttu-id="61c57-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="61c57-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="61c57-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="61c57-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="61c57-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="61c57-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


