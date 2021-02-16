---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116327"
---
# <span data-ttu-id="c81c3-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c81c3-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="c81c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c81c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c81c3-103">Cria um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c81c3-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="c81c3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c81c3-104">SYNTAX</span></span>

### <span data-ttu-id="c81c3-105">Nomedo Contêiner (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c81c3-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c81c3-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="c81c3-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c81c3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c81c3-107">DESCRIPTION</span></span>
<span data-ttu-id="c81c3-108">O **cmdlet New-AzStorageContainer** cria um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c81c3-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="c81c3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c81c3-109">EXAMPLES</span></span>

### <span data-ttu-id="c81c3-110">Exemplo 1: Criar um contêiner de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="c81c3-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="c81c3-111">Esse comando cria um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c81c3-111">This command creates a storage container.</span></span>

### <span data-ttu-id="c81c3-112">Exemplo 2: Criar vários contêineres de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="c81c3-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="c81c3-113">Este exemplo cria vários contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c81c3-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="c81c3-114">Ele usa o **método** Dividir da classe cadeia de caracteres **.NET** e passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="c81c3-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="c81c3-115">Exemplo 3: Criar um contêiner de armazenamento do Azure com Escopo de Criptografia</span><span class="sxs-lookup"><span data-stu-id="c81c3-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="c81c3-116">Esse comando cria um contêiner de armazenamento, com Escopo de Criptografia padrão como myencryptscope e upload de blob de prevert com escopo de criptografia diferente para esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="c81c3-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="c81c3-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c81c3-117">PARAMETERS</span></span>

### <span data-ttu-id="c81c3-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c81c3-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c81c3-119">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c81c3-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c81c3-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c81c3-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c81c3-121">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c81c3-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c81c3-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c81c3-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c81c3-123">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c81c3-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c81c3-124">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c81c3-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c81c3-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="c81c3-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c81c3-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c81c3-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c81c3-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c81c3-127">The default value is 10.</span></span>

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

### <span data-ttu-id="c81c3-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c81c3-128">-Context</span></span>
<span data-ttu-id="c81c3-129">Especifica um contexto para o novo contêiner.</span><span class="sxs-lookup"><span data-stu-id="c81c3-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="c81c3-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="c81c3-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="c81c3-131">Padrão do contêiner para usar escopo de criptografia especificado para todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="c81c3-131">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="c81c3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81c3-132">-DefaultProfile</span></span>
<span data-ttu-id="c81c3-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c81c3-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c81c3-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="c81c3-134">-Name</span></span>
<span data-ttu-id="c81c3-135">Especifica um nome para o novo contêiner.</span><span class="sxs-lookup"><span data-stu-id="c81c3-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="c81c3-136">-Permissão</span><span class="sxs-lookup"><span data-stu-id="c81c3-136">-Permission</span></span>
<span data-ttu-id="c81c3-137">Especifica o nível de acesso público a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="c81c3-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="c81c3-138">Por padrão, o contêiner e todos os blobs nele podem ser acessados apenas pelo proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c81c3-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="c81c3-139">Para conceder permissões de leitura a usuários anônimos para um contêiner e seus blobs, você pode definir as permissões de contêiner para habilitar o acesso público.</span><span class="sxs-lookup"><span data-stu-id="c81c3-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="c81c3-140">Os usuários anônimos podem ler blobs em um contêiner disponível publicamente sem autenticar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c81c3-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="c81c3-141">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c81c3-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c81c3-142">Recipiente.</span><span class="sxs-lookup"><span data-stu-id="c81c3-142">Container.</span></span>
<span data-ttu-id="c81c3-143">Fornece acesso de leitura total a um contêiner e a seus blobs.</span><span class="sxs-lookup"><span data-stu-id="c81c3-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="c81c3-144">Os clientes podem enumerar blobs no contêiner por meio de solicitação anônima, mas não podem enumerar contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c81c3-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="c81c3-145">Blob.</span><span class="sxs-lookup"><span data-stu-id="c81c3-145">Blob.</span></span>
<span data-ttu-id="c81c3-146">Fornece acesso de leitura a dados de blob em todo o contêiner por meio de solicitação anônima, mas não fornece acesso aos dados do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c81c3-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="c81c3-147">Os clientes não podem enumerar blobs no contêiner usando solicitação anônima.</span><span class="sxs-lookup"><span data-stu-id="c81c3-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="c81c3-148">Desligado.</span><span class="sxs-lookup"><span data-stu-id="c81c3-148">Off.</span></span>
<span data-ttu-id="c81c3-149">O que restringe o acesso apenas ao proprietário da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c81c3-149">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="c81c3-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="c81c3-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="c81c3-151">Bloquear a substituição do escopo de criptografia do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="c81c3-151">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="c81c3-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c81c3-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c81c3-153">Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c81c3-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c81c3-154">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c81c3-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c81c3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81c3-155">CommonParameters</span></span>
<span data-ttu-id="c81c3-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81c3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81c3-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c81c3-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81c3-158">Entradas</span><span class="sxs-lookup"><span data-stu-id="c81c3-158">INPUTS</span></span>

### <span data-ttu-id="c81c3-159">System.String</span><span class="sxs-lookup"><span data-stu-id="c81c3-159">System.String</span></span>

### <span data-ttu-id="c81c3-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c81c3-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c81c3-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="c81c3-161">OUTPUTS</span></span>

### <span data-ttu-id="c81c3-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c81c3-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="c81c3-163">Notas</span><span class="sxs-lookup"><span data-stu-id="c81c3-163">NOTES</span></span>

## <span data-ttu-id="c81c3-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c81c3-164">RELATED LINKS</span></span>

[<span data-ttu-id="c81c3-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c81c3-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="c81c3-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c81c3-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="c81c3-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="c81c3-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


