---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
ms.openlocfilehash: c3451552d919b33b7dd2dcf72b8b9982f50e8b88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602818"
---
# <span data-ttu-id="9c682-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="9c682-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="9c682-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c682-102">SYNOPSIS</span></span>
<span data-ttu-id="9c682-103">Define a permissão de acesso público para um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c682-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c682-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c682-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9c682-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c682-105">DESCRIPTION</span></span>
<span data-ttu-id="9c682-106">O cmdlet **set-AzureStorageContainerAcl** define a permissão de acesso público para o contêiner de armazenamento especificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="9c682-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="9c682-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c682-107">EXAMPLES</span></span>

### <span data-ttu-id="9c682-108">Exemplo 1: definir a ACL do contêiner de armazenamento do Azure por nome</span><span class="sxs-lookup"><span data-stu-id="9c682-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="9c682-109">Esse comando cria um contêiner que não tem acesso público.</span><span class="sxs-lookup"><span data-stu-id="9c682-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="9c682-110">Exemplo 2: definir a ACL do contêiner de armazenamento do Azure usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="9c682-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="9c682-111">Esse comando obtém todos os contêineres de armazenamento cujo nome começa com contêiner e, em seguida, passa o resultado no pipeline para definir a permissão para eles todos para o acesso ao blob.</span><span class="sxs-lookup"><span data-stu-id="9c682-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="9c682-112">OS</span><span class="sxs-lookup"><span data-stu-id="9c682-112">PARAMETERS</span></span>

### <span data-ttu-id="9c682-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c682-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9c682-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="9c682-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9c682-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c682-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9c682-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9c682-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9c682-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9c682-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9c682-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9c682-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9c682-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9c682-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9c682-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="9c682-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9c682-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9c682-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9c682-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="9c682-122">The default value is 10.</span></span>

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

### <span data-ttu-id="9c682-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9c682-123">-Context</span></span>
<span data-ttu-id="9c682-124">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c682-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9c682-125">Você pode criá-lo usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9c682-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9c682-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c682-126">-DefaultProfile</span></span>
<span data-ttu-id="9c682-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c682-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c682-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c682-128">-Name</span></span>
<span data-ttu-id="9c682-129">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="9c682-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="9c682-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c682-130">-PassThru</span></span>
<span data-ttu-id="9c682-131">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9c682-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c682-132">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9c682-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c682-133">-Permissão</span><span class="sxs-lookup"><span data-stu-id="9c682-133">-Permission</span></span>
<span data-ttu-id="9c682-134">Especifica o nível de acesso público a este contêiner.</span><span class="sxs-lookup"><span data-stu-id="9c682-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="9c682-135">Por padrão, o contêiner e os BLOBs nele só podem ser acessados pelo proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c682-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="9c682-136">Para conceder permissões de leitura de usuários anônimos a um contêiner e a seus BLOBs, você pode definir as permissões de contêiner para habilitar o acesso público.</span><span class="sxs-lookup"><span data-stu-id="9c682-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="9c682-137">Usuários anônimos podem ler BLOBs em um contêiner disponível publicamente sem autenticar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c682-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="9c682-138">Os valores aceitáveis para esse parâmetro são:--contêiner.</span><span class="sxs-lookup"><span data-stu-id="9c682-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="9c682-139">Fornece acesso de leitura completo a um contêiner e seus BLOBs.</span><span class="sxs-lookup"><span data-stu-id="9c682-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="9c682-140">Os clientes podem enumerar BLOBs no contêiner por meio de solicitação anônima, mas não podem enumerar contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c682-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="9c682-141">--Blob.</span><span class="sxs-lookup"><span data-stu-id="9c682-141">--Blob.</span></span>
<span data-ttu-id="9c682-142">Fornece acesso de leitura a dados de BLOB em um contêiner por meio de solicitação anônima, mas não fornece acesso a dados de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9c682-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="9c682-143">Os clientes não podem enumerar BLOBs no contêiner usando solicitação anônima.</span><span class="sxs-lookup"><span data-stu-id="9c682-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="9c682-144">--Desativada.</span><span class="sxs-lookup"><span data-stu-id="9c682-144">--Off.</span></span>
<span data-ttu-id="9c682-145">Restringe o acesso somente ao proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c682-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c682-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c682-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9c682-147">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c682-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9c682-148">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9c682-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="9c682-149">Tempo limite do lado do servidor para cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c682-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="9c682-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c682-150">CommonParameters</span></span>
<span data-ttu-id="9c682-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c682-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c682-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c682-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c682-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c682-153">INPUTS</span></span>

### <span data-ttu-id="9c682-154">System. String</span><span class="sxs-lookup"><span data-stu-id="9c682-154">System.String</span></span>

### <span data-ttu-id="9c682-155">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9c682-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9c682-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c682-156">OUTPUTS</span></span>

### <span data-ttu-id="9c682-157">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9c682-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="9c682-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c682-158">NOTES</span></span>

## <span data-ttu-id="9c682-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c682-159">RELATED LINKS</span></span>

[<span data-ttu-id="9c682-160">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9c682-160">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="9c682-161">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9c682-161">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="9c682-162">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9c682-162">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


