---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6e7230ad6cb2bd3f58ebd3328aa20fe3c1bf2bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891964"
---
# <span data-ttu-id="44fd1-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44fd1-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="44fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="44fd1-103">Cria uma política de acesso armazenada para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44fd1-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="44fd1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44fd1-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="44fd1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="44fd1-106">O cmdlet **New-AzStorageContainerStoredAccessPolicy** cria uma política de acesso armazenada para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44fd1-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="44fd1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44fd1-107">EXAMPLES</span></span>

### <span data-ttu-id="44fd1-108">Exemplo 1: criar uma política de acesso armazenado em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44fd1-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="44fd1-109">Este comando cria uma política de acesso chamada Policy01 no contêiner de armazenamento chamado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="44fd1-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="44fd1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44fd1-110">PARAMETERS</span></span>

### <span data-ttu-id="44fd1-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="44fd1-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="44fd1-112">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="44fd1-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="44fd1-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="44fd1-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="44fd1-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="44fd1-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="44fd1-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="44fd1-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="44fd1-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="44fd1-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="44fd1-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="44fd1-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="44fd1-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="44fd1-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="44fd1-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="44fd1-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="44fd1-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="44fd1-120">The default value is 10.</span></span>

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

### <span data-ttu-id="44fd1-121">-Container</span><span class="sxs-lookup"><span data-stu-id="44fd1-121">-Container</span></span>
<span data-ttu-id="44fd1-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44fd1-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="44fd1-123">-Context</span><span class="sxs-lookup"><span data-stu-id="44fd1-123">-Context</span></span>
<span data-ttu-id="44fd1-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44fd1-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="44fd1-125">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44fd1-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="44fd1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fd1-126">-DefaultProfile</span></span>
<span data-ttu-id="44fd1-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44fd1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44fd1-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="44fd1-128">-ExpiryTime</span></span>
<span data-ttu-id="44fd1-129">Especifica o momento em que a política de acesso armazenada se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="44fd1-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fd1-130">-Permission</span><span class="sxs-lookup"><span data-stu-id="44fd1-130">-Permission</span></span>
<span data-ttu-id="44fd1-131">Especifica permissões na política de acesso armazenado para acessar o contêiner.</span><span class="sxs-lookup"><span data-stu-id="44fd1-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="44fd1-132">É importante observar que esta é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="44fd1-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fd1-133">-Policy</span><span class="sxs-lookup"><span data-stu-id="44fd1-133">-Policy</span></span>
<span data-ttu-id="44fd1-134">Especifica uma política de acesso armazenada, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="44fd1-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fd1-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="44fd1-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="44fd1-136">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="44fd1-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="44fd1-137">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="44fd1-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="44fd1-138">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="44fd1-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="44fd1-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="44fd1-139">-StartTime</span></span>
<span data-ttu-id="44fd1-140">Especifica o momento em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="44fd1-140">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fd1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fd1-141">CommonParameters</span></span>
<span data-ttu-id="44fd1-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44fd1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fd1-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44fd1-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fd1-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44fd1-144">INPUTS</span></span>

### <span data-ttu-id="44fd1-145">System.String</span><span class="sxs-lookup"><span data-stu-id="44fd1-145">System.String</span></span>

### <span data-ttu-id="44fd1-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="44fd1-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="44fd1-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44fd1-147">OUTPUTS</span></span>

### <span data-ttu-id="44fd1-148">System.String</span><span class="sxs-lookup"><span data-stu-id="44fd1-148">System.String</span></span>

## <span data-ttu-id="44fd1-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="44fd1-149">NOTES</span></span>

## <span data-ttu-id="44fd1-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44fd1-150">RELATED LINKS</span></span>

[<span data-ttu-id="44fd1-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44fd1-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="44fd1-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="44fd1-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="44fd1-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44fd1-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="44fd1-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44fd1-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


