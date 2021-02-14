---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111269"
---
# <span data-ttu-id="6d33f-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6d33f-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="6d33f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d33f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d33f-103">Lista os contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d33f-103">Lists the storage containers.</span></span>

## <span data-ttu-id="6d33f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d33f-104">SYNTAX</span></span>

### <span data-ttu-id="6d33f-105">Nomedo Contêiner (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d33f-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6d33f-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="6d33f-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6d33f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d33f-107">DESCRIPTION</span></span>
<span data-ttu-id="6d33f-108">O **cmdlet Get-AzStorageContainer** lista os contêineres de armazenamento associados à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="6d33f-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="6d33f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d33f-109">EXAMPLES</span></span>

### <span data-ttu-id="6d33f-110">Exemplo 1: Obter o blob de Armazenamento do Azure por nome</span><span class="sxs-lookup"><span data-stu-id="6d33f-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="6d33f-111">Este exemplo usa um caractere curinga para retornar uma lista de todos os contêineres com um nome que começa com contêiner.</span><span class="sxs-lookup"><span data-stu-id="6d33f-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="6d33f-112">Exemplo 2: Obter contêiner de armazenamento do Azure por prefixo de nome de contêiner</span><span class="sxs-lookup"><span data-stu-id="6d33f-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="6d33f-113">Este exemplo usa o parâmetro *Prefixo* para retornar uma lista de todos os contêineres com um nome que começa com contêiner.</span><span class="sxs-lookup"><span data-stu-id="6d33f-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="6d33f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d33f-114">PARAMETERS</span></span>

### <span data-ttu-id="6d33f-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6d33f-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6d33f-116">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="6d33f-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6d33f-117">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6d33f-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6d33f-118">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se elapse, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6d33f-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6d33f-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6d33f-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6d33f-120">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="6d33f-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6d33f-121">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="6d33f-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6d33f-122">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="6d33f-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6d33f-123">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="6d33f-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6d33f-124">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="6d33f-124">The default value is 10.</span></span>

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

### <span data-ttu-id="6d33f-125">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6d33f-125">-Context</span></span>
<span data-ttu-id="6d33f-126">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d33f-126">Specifies the storage context.</span></span>
<span data-ttu-id="6d33f-127">Para criar, você pode usar o cmdlet New-AzStorageContext dados.</span><span class="sxs-lookup"><span data-stu-id="6d33f-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="6d33f-128">As permissões de contêiner não serão recuperadas quando você usar um contexto de armazenamento criado a partir do Token SAS, pois as permissões de contêiner de consulta exigem permissão de chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d33f-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="6d33f-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="6d33f-129">-ContinuationToken</span></span>
<span data-ttu-id="6d33f-130">Especifica um token de continuação para a lista de blob.</span><span class="sxs-lookup"><span data-stu-id="6d33f-130">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="6d33f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d33f-131">-DefaultProfile</span></span>
<span data-ttu-id="6d33f-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d33f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d33f-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6d33f-133">-MaxCount</span></span>
<span data-ttu-id="6d33f-134">Especifica o número máximo de objetos que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="6d33f-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="6d33f-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d33f-135">-Name</span></span>
<span data-ttu-id="6d33f-136">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="6d33f-136">Specifies the container name.</span></span>
<span data-ttu-id="6d33f-137">Se o nome do contêiner estiver vazio, o cmdlet lista todos os contêineres.</span><span class="sxs-lookup"><span data-stu-id="6d33f-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="6d33f-138">Caso contrário, ele lista todos os contêineres que corresponderem ao nome especificado ou ao padrão de nome normal.</span><span class="sxs-lookup"><span data-stu-id="6d33f-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="6d33f-139">-Prefixo</span><span class="sxs-lookup"><span data-stu-id="6d33f-139">-Prefix</span></span>
<span data-ttu-id="6d33f-140">Especifica um prefixo usado no nome do contêiner ou contêineres que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="6d33f-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="6d33f-141">Você pode usá-lo para encontrar todos os contêineres que começam com a mesma cadeia de caracteres, como "meu" ou "teste".</span><span class="sxs-lookup"><span data-stu-id="6d33f-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="6d33f-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6d33f-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6d33f-143">Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="6d33f-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6d33f-144">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6d33f-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6d33f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d33f-145">CommonParameters</span></span>
<span data-ttu-id="6d33f-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d33f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d33f-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d33f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d33f-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="6d33f-148">INPUTS</span></span>

### <span data-ttu-id="6d33f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="6d33f-149">System.String</span></span>

### <span data-ttu-id="6d33f-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d33f-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6d33f-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="6d33f-151">OUTPUTS</span></span>

### <span data-ttu-id="6d33f-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6d33f-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="6d33f-153">Notas</span><span class="sxs-lookup"><span data-stu-id="6d33f-153">NOTES</span></span>

## <span data-ttu-id="6d33f-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d33f-154">RELATED LINKS</span></span>

[<span data-ttu-id="6d33f-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6d33f-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="6d33f-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6d33f-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="6d33f-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="6d33f-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


