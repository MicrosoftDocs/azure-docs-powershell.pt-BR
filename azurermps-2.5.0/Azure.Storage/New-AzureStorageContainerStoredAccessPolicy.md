---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 0610e4ca8bf520bc9812599747968a583641dd76
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786020"
---
# <span data-ttu-id="7305e-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7305e-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="7305e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7305e-102">SYNOPSIS</span></span>
<span data-ttu-id="7305e-103">Cria uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7305e-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7305e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7305e-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7305e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7305e-105">DESCRIPTION</span></span>
<span data-ttu-id="7305e-106">O cmdlet **New-AzureStorageContainerStoredAccessPolicy** cria uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7305e-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="7305e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7305e-107">EXAMPLES</span></span>

### <span data-ttu-id="7305e-108">Exemplo 1: criar uma política de acesso armazenada em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7305e-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="7305e-109">Esse comando cria uma política de acesso chamada Policy01 no contêiner de armazenamento denominado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="7305e-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="7305e-110">OS</span><span class="sxs-lookup"><span data-stu-id="7305e-110">PARAMETERS</span></span>

### <span data-ttu-id="7305e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7305e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7305e-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="7305e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7305e-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7305e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7305e-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7305e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7305e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7305e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7305e-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="7305e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7305e-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="7305e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7305e-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="7305e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7305e-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="7305e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7305e-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="7305e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7305e-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="7305e-121">-Container</span></span>
<span data-ttu-id="7305e-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7305e-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="7305e-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7305e-123">-Context</span></span>
<span data-ttu-id="7305e-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7305e-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7305e-125">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7305e-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7305e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7305e-126">-DefaultProfile</span></span>
<span data-ttu-id="7305e-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7305e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7305e-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7305e-128">-ExpiryTime</span></span>
<span data-ttu-id="7305e-129">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="7305e-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="7305e-130">-Permissão</span><span class="sxs-lookup"><span data-stu-id="7305e-130">-Permission</span></span>
<span data-ttu-id="7305e-131">Especifica as permissões na política de acesso armazenado para acessar o contêiner.</span><span class="sxs-lookup"><span data-stu-id="7305e-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="7305e-132">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="7305e-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7305e-133">-Política</span><span class="sxs-lookup"><span data-stu-id="7305e-133">-Policy</span></span>
<span data-ttu-id="7305e-134">Especifica uma política de acesso armazenado, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="7305e-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="7305e-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7305e-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7305e-136">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="7305e-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7305e-137">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7305e-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7305e-138">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7305e-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7305e-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7305e-139">-StartTime</span></span>
<span data-ttu-id="7305e-140">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="7305e-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="7305e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7305e-141">CommonParameters</span></span>
<span data-ttu-id="7305e-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7305e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7305e-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7305e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7305e-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7305e-144">INPUTS</span></span>

### <span data-ttu-id="7305e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7305e-145">System.String</span></span>

### <span data-ttu-id="7305e-146">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7305e-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7305e-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7305e-147">OUTPUTS</span></span>

### <span data-ttu-id="7305e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7305e-148">System.String</span></span>

## <span data-ttu-id="7305e-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7305e-149">NOTES</span></span>

## <span data-ttu-id="7305e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7305e-150">RELATED LINKS</span></span>

[<span data-ttu-id="7305e-151">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7305e-151">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="7305e-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7305e-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7305e-153">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7305e-153">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="7305e-154">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7305e-154">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


