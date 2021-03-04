---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 23aa7e6df5aae820980551db445339ade34ac779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891935"
---
# <span data-ttu-id="886d0-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="886d0-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="886d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="886d0-102">SYNOPSIS</span></span>
<span data-ttu-id="886d0-103">Define a permissão de acesso público como um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="886d0-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="886d0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="886d0-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="886d0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="886d0-105">DESCRIPTION</span></span>
<span data-ttu-id="886d0-106">O cmdlet **Set-AzStorageContainerAcl** define a permissão de acesso público para o contêiner de armazenamento especificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="886d0-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="886d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="886d0-107">EXAMPLES</span></span>

### <span data-ttu-id="886d0-108">Exemplo 1: Definir o ACL do contêiner de armazenamento do azure pelo nome</span><span class="sxs-lookup"><span data-stu-id="886d0-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="886d0-109">Este comando cria um contêiner que não tem acesso público.</span><span class="sxs-lookup"><span data-stu-id="886d0-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="886d0-110">Exemplo 2: Definir a ACL do contêiner de armazenamento do azure usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="886d0-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="886d0-111">Esse comando obtém todos os contêineres de armazenamento cujo nome começa com contêiner e, em seguida, passa o resultado no pipeline para definir a permissão para todos eles para acesso a Blob.</span><span class="sxs-lookup"><span data-stu-id="886d0-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="886d0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="886d0-112">PARAMETERS</span></span>

### <span data-ttu-id="886d0-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="886d0-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="886d0-114">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="886d0-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="886d0-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="886d0-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="886d0-116">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="886d0-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="886d0-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="886d0-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="886d0-118">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="886d0-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="886d0-119">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="886d0-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="886d0-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="886d0-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="886d0-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="886d0-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="886d0-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="886d0-122">The default value is 10.</span></span>

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

### <span data-ttu-id="886d0-123">-Context</span><span class="sxs-lookup"><span data-stu-id="886d0-123">-Context</span></span>
<span data-ttu-id="886d0-124">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="886d0-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="886d0-125">Você pode criar usando o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="886d0-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="886d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="886d0-126">-DefaultProfile</span></span>
<span data-ttu-id="886d0-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="886d0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="886d0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="886d0-128">-Name</span></span>
<span data-ttu-id="886d0-129">Especifica um nome de contêiner.</span><span class="sxs-lookup"><span data-stu-id="886d0-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="886d0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="886d0-130">-PassThru</span></span>
<span data-ttu-id="886d0-131">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="886d0-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="886d0-132">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="886d0-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="886d0-133">-Permission</span><span class="sxs-lookup"><span data-stu-id="886d0-133">-Permission</span></span>
<span data-ttu-id="886d0-134">Especifica o nível de acesso público a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="886d0-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="886d0-135">Por padrão, o contêiner e todos os blobs nele podem ser acessados apenas pelo proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="886d0-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="886d0-136">Para conceder aos usuários anônimos permissões de leitura para um contêiner e seus blobs, você pode definir as permissões de contêiner para habilitar o acesso público.</span><span class="sxs-lookup"><span data-stu-id="886d0-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="886d0-137">Os usuários anônimos podem ler blobs em um contêiner disponível publicamente sem autenticar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="886d0-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="886d0-138">Os valores aceitáveis para este parâmetro são: --Container.</span><span class="sxs-lookup"><span data-stu-id="886d0-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="886d0-139">Fornece acesso de leitura total a um contêiner e seus blobs.</span><span class="sxs-lookup"><span data-stu-id="886d0-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="886d0-140">Os clientes podem enumerar blobs no contêiner por meio de solicitação anônima, mas não podem enumerar contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="886d0-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="886d0-141">--Blob.</span><span class="sxs-lookup"><span data-stu-id="886d0-141">--Blob.</span></span>
<span data-ttu-id="886d0-142">Fornece acesso de leitura a dados blob em um contêiner por meio de solicitação anônima, mas não fornece acesso a dados de contêiner.</span><span class="sxs-lookup"><span data-stu-id="886d0-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="886d0-143">Os clientes não podem enumerar blobs no contêiner usando solicitação anônima.</span><span class="sxs-lookup"><span data-stu-id="886d0-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="886d0-144">--Off.</span><span class="sxs-lookup"><span data-stu-id="886d0-144">--Off.</span></span>
<span data-ttu-id="886d0-145">Restringe o acesso apenas ao proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="886d0-145">Restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="886d0-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="886d0-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="886d0-147">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="886d0-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="886d0-148">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="886d0-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="886d0-149">Tempo de tempo de saída do servidor para cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="886d0-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="886d0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="886d0-150">CommonParameters</span></span>
<span data-ttu-id="886d0-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="886d0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="886d0-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="886d0-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="886d0-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="886d0-153">INPUTS</span></span>

### <span data-ttu-id="886d0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="886d0-154">System.String</span></span>

### <span data-ttu-id="886d0-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="886d0-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="886d0-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="886d0-156">OUTPUTS</span></span>

### <span data-ttu-id="886d0-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="886d0-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="886d0-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="886d0-158">NOTES</span></span>

## <span data-ttu-id="886d0-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="886d0-159">RELATED LINKS</span></span>

[<span data-ttu-id="886d0-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="886d0-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="886d0-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="886d0-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="886d0-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="886d0-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


