---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 15aefebea30e829371c57c3c1cd575a604b81eaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889077"
---
# <span data-ttu-id="bd9d4-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bd9d4-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="bd9d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9d4-103">Lista os contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-103">Lists the storage containers.</span></span>

## <span data-ttu-id="bd9d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bd9d4-104">SYNTAX</span></span>

### <span data-ttu-id="bd9d4-105">ContainerName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bd9d4-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bd9d4-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="bd9d4-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bd9d4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bd9d4-107">DESCRIPTION</span></span>
<span data-ttu-id="bd9d4-108">O cmdlet **Get-AzStorageContainer** lista os contêineres de armazenamento associados à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="bd9d4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd9d4-109">EXAMPLES</span></span>

### <span data-ttu-id="bd9d4-110">Exemplo 1: Obter blob de armazenamento do Azure pelo nome</span><span class="sxs-lookup"><span data-stu-id="bd9d4-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="bd9d4-111">Este exemplo usa um caractere curinga para retornar uma lista de todos os contêineres com um nome que começa com contêiner.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="bd9d4-112">Exemplo 2: Obter contêiner de armazenamento do Azure pelo prefixo de nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="bd9d4-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="bd9d4-113">Este exemplo usa o *parâmetro Prefix* para retornar uma lista de todos os contêineres com um nome que começa com contêiner.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="bd9d4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bd9d4-114">PARAMETERS</span></span>

### <span data-ttu-id="bd9d4-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bd9d4-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bd9d4-116">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bd9d4-117">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bd9d4-118">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bd9d4-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bd9d4-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bd9d4-120">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bd9d4-121">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bd9d4-122">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bd9d4-123">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bd9d4-124">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-124">The default value is 10.</span></span>

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

### <span data-ttu-id="bd9d4-125">-Context</span><span class="sxs-lookup"><span data-stu-id="bd9d4-125">-Context</span></span>
<span data-ttu-id="bd9d4-126">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-126">Specifies the storage context.</span></span>
<span data-ttu-id="bd9d4-127">Para criar, você pode usar o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="bd9d4-128">As permissões de contêiner não serão recuperadas quando você usar um contexto de armazenamento criado a partir do Token SAS, pois as permissões do contêiner de consulta exigem a permissão da chave de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="bd9d4-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="bd9d4-129">-ContinuationToken</span></span>
<span data-ttu-id="bd9d4-130">Especifica um token de continuação para a lista de blob.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9d4-131">-DefaultProfile</span></span>
<span data-ttu-id="bd9d4-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd9d4-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bd9d4-133">-MaxCount</span></span>
<span data-ttu-id="bd9d4-134">Especifica o número máximo de objetos que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="bd9d4-135">-Name</span><span class="sxs-lookup"><span data-stu-id="bd9d4-135">-Name</span></span>
<span data-ttu-id="bd9d4-136">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-136">Specifies the container name.</span></span>
<span data-ttu-id="bd9d4-137">Se o nome do contêiner estiver vazio, o cmdlet lista todos os contêineres.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="bd9d4-138">Caso contrário, lista todos os contêineres que corresponderem ao nome especificado ou ao padrão de nome regular.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d4-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="bd9d4-139">-Prefix</span></span>
<span data-ttu-id="bd9d4-140">Especifica um prefixo usado no nome do contêiner ou contêineres que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="bd9d4-141">Você pode usar isso para encontrar todos os contêineres que começam com a mesma cadeia de caracteres, como "my" ou "test".</span><span class="sxs-lookup"><span data-stu-id="bd9d4-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d4-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bd9d4-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bd9d4-143">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="bd9d4-144">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="bd9d4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9d4-145">CommonParameters</span></span>
<span data-ttu-id="bd9d4-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd9d4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9d4-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd9d4-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9d4-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd9d4-148">INPUTS</span></span>

### <span data-ttu-id="bd9d4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="bd9d4-149">System.String</span></span>

### <span data-ttu-id="bd9d4-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bd9d4-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bd9d4-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bd9d4-151">OUTPUTS</span></span>

### <span data-ttu-id="bd9d4-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bd9d4-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="bd9d4-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="bd9d4-153">NOTES</span></span>

## <span data-ttu-id="bd9d4-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd9d4-154">RELATED LINKS</span></span>

[<span data-ttu-id="bd9d4-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bd9d4-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="bd9d4-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bd9d4-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="bd9d4-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="bd9d4-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


