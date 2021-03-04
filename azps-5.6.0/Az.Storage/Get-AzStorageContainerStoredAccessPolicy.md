---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 7d3d16632e2afb503bf659058643244fd8578d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886396"
---
# <span data-ttu-id="969f2-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="969f2-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="969f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="969f2-102">SYNOPSIS</span></span>
<span data-ttu-id="969f2-103">Obtém a política ou políticas de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="969f2-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="969f2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="969f2-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="969f2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="969f2-105">DESCRIPTION</span></span>
<span data-ttu-id="969f2-106">O cmdlet **Get-AzStorageContainerStoredAccessPolicy** lista a política de acesso armazenada ou as políticas de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="969f2-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="969f2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="969f2-107">EXAMPLES</span></span>

### <span data-ttu-id="969f2-108">Exemplo 1: Obter uma política de acesso armazenado em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="969f2-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="969f2-109">Este comando obtém a política de acesso chamada Policy22 no contêiner de armazenamento chamado Container07.</span><span class="sxs-lookup"><span data-stu-id="969f2-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="969f2-110">Exemplo 2: Obter todas as políticas de acesso armazenadas em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="969f2-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="969f2-111">Este comando obtém todas as políticas de acesso no contêiner de armazenamento chamado Container07.</span><span class="sxs-lookup"><span data-stu-id="969f2-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="969f2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="969f2-112">PARAMETERS</span></span>

### <span data-ttu-id="969f2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="969f2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="969f2-114">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="969f2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="969f2-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="969f2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="969f2-116">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="969f2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="969f2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="969f2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="969f2-118">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="969f2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="969f2-119">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="969f2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="969f2-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="969f2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="969f2-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="969f2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="969f2-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="969f2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="969f2-123">-Container</span><span class="sxs-lookup"><span data-stu-id="969f2-123">-Container</span></span>
<span data-ttu-id="969f2-124">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="969f2-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="969f2-125">-Context</span><span class="sxs-lookup"><span data-stu-id="969f2-125">-Context</span></span>
<span data-ttu-id="969f2-126">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="969f2-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="969f2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969f2-127">-DefaultProfile</span></span>
<span data-ttu-id="969f2-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="969f2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="969f2-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="969f2-129">-Policy</span></span>
<span data-ttu-id="969f2-130">Especifica a política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="969f2-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969f2-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="969f2-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="969f2-132">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="969f2-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="969f2-133">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="969f2-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="969f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969f2-134">CommonParameters</span></span>
<span data-ttu-id="969f2-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969f2-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969f2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969f2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="969f2-137">INPUTS</span></span>

### <span data-ttu-id="969f2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="969f2-138">System.String</span></span>

### <span data-ttu-id="969f2-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="969f2-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="969f2-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="969f2-140">OUTPUTS</span></span>

### <span data-ttu-id="969f2-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="969f2-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="969f2-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="969f2-142">NOTES</span></span>

## <span data-ttu-id="969f2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="969f2-143">RELATED LINKS</span></span>

[<span data-ttu-id="969f2-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="969f2-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="969f2-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="969f2-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="969f2-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="969f2-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


