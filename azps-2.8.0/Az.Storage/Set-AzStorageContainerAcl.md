---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 2ed750f2206389a4951efacb153c287e9e80ac8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595846"
---
# <span data-ttu-id="d5d3f-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="d5d3f-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="d5d3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d3f-103">Define a permissão de acesso público para um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="d5d3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5d3f-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d5d3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="d5d3f-106">O cmdlet **set-AzStorageContainerAcl** define a permissão de acesso público para o contêiner de armazenamento especificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="d5d3f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="d5d3f-108">Exemplo 1: definir a ACL do contêiner de armazenamento do Azure por nome</span><span class="sxs-lookup"><span data-stu-id="d5d3f-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="d5d3f-109">Esse comando cria um contêiner que não tem acesso público.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="d5d3f-110">Exemplo 2: definir a ACL do contêiner de armazenamento do Azure usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d5d3f-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="d5d3f-111">Esse comando obtém todos os contêineres de armazenamento cujo nome começa com contêiner e, em seguida, passa o resultado no pipeline para definir a permissão para eles todos para o acesso ao blob.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="d5d3f-112">OS</span><span class="sxs-lookup"><span data-stu-id="d5d3f-112">PARAMETERS</span></span>

### <span data-ttu-id="d5d3f-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d5d3f-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d5d3f-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d5d3f-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d5d3f-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d5d3f-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d5d3f-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d5d3f-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d5d3f-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d5d3f-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d5d3f-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d5d3f-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d5d3f-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d5d3f-123">-Context</span></span>
<span data-ttu-id="d5d3f-124">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d5d3f-125">Você pode criá-lo usando o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d5d3f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d3f-126">-DefaultProfile</span></span>
<span data-ttu-id="d5d3f-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d3f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5d3f-128">-Name</span></span>
<span data-ttu-id="d5d3f-129">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="d5d3f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5d3f-130">-PassThru</span></span>
<span data-ttu-id="d5d3f-131">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d5d3f-132">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-132">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d3f-133">-Permissão</span><span class="sxs-lookup"><span data-stu-id="d5d3f-133">-Permission</span></span>
<span data-ttu-id="d5d3f-134">Especifica o nível de acesso público a este contêiner.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="d5d3f-135">Por padrão, o contêiner e os BLOBs nele só podem ser acessados pelo proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="d5d3f-136">Para conceder permissões de leitura de usuários anônimos a um contêiner e a seus BLOBs, você pode definir as permissões de contêiner para habilitar o acesso público.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="d5d3f-137">Usuários anônimos podem ler BLOBs em um contêiner disponível publicamente sem autenticar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="d5d3f-138">Os valores aceitáveis para esse parâmetro são:--contêiner.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="d5d3f-139">Fornece acesso de leitura completo a um contêiner e seus BLOBs.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="d5d3f-140">Os clientes podem enumerar BLOBs no contêiner por meio de solicitação anônima, mas não podem enumerar contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="d5d3f-141">--Blob.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-141">--Blob.</span></span>
<span data-ttu-id="d5d3f-142">Fornece acesso de leitura a dados de BLOB em um contêiner por meio de solicitação anônima, mas não fornece acesso a dados de contêiner.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="d5d3f-143">Os clientes não podem enumerar BLOBs no contêiner usando solicitação anônima.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="d5d3f-144">--Desativada.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-144">--Off.</span></span>
<span data-ttu-id="d5d3f-145">Restringe o acesso somente ao proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d3f-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d5d3f-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d5d3f-147">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d5d3f-148">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="d5d3f-149">Tempo limite do lado do servidor para cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="d5d3f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d3f-150">CommonParameters</span></span>
<span data-ttu-id="d5d3f-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d3f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d3f-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5d3f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d3f-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5d3f-153">INPUTS</span></span>

### <span data-ttu-id="d5d3f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d5d3f-154">System.String</span></span>

### <span data-ttu-id="d5d3f-155">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d5d3f-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d5d3f-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5d3f-156">OUTPUTS</span></span>

### <span data-ttu-id="d5d3f-157">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d5d3f-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="d5d3f-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5d3f-158">NOTES</span></span>

## <span data-ttu-id="d5d3f-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5d3f-159">RELATED LINKS</span></span>

[<span data-ttu-id="d5d3f-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d5d3f-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="d5d3f-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d5d3f-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="d5d3f-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d5d3f-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


