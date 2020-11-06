---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3429c142ce31f8cd08786e180b6725130501ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428340"
---
# <span data-ttu-id="3320f-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3320f-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="3320f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3320f-102">SYNOPSIS</span></span>
<span data-ttu-id="3320f-103">Cria uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3320f-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3320f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3320f-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3320f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3320f-105">DESCRIPTION</span></span>
<span data-ttu-id="3320f-106">O cmdlet **New-AzureStorageContainerStoredAccessPolicy** cria uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3320f-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="3320f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3320f-107">EXAMPLES</span></span>

### <span data-ttu-id="3320f-108">Exemplo 1: criar uma política de acesso armazenada em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3320f-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="3320f-109">Esse comando cria uma política de acesso chamada Policy01 no contêiner de armazenamento denominado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="3320f-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="3320f-110">OS</span><span class="sxs-lookup"><span data-stu-id="3320f-110">PARAMETERS</span></span>

### <span data-ttu-id="3320f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3320f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3320f-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="3320f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3320f-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3320f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3320f-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="3320f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3320f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3320f-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="3320f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3320f-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="3320f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3320f-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="3320f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3320f-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="3320f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3320f-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="3320f-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="3320f-121">-Container</span></span>
<span data-ttu-id="3320f-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3320f-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3320f-123">-Context</span></span>
<span data-ttu-id="3320f-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3320f-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3320f-125">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3320f-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3320f-126">-ExpiryTime</span></span>
<span data-ttu-id="3320f-127">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="3320f-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-128">-Permissão</span><span class="sxs-lookup"><span data-stu-id="3320f-128">-Permission</span></span>
<span data-ttu-id="3320f-129">Especifica as permissões na política de acesso armazenado para acessar o contêiner.</span><span class="sxs-lookup"><span data-stu-id="3320f-129">Specifies permissions in the stored access policy to access the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-130">-Política</span><span class="sxs-lookup"><span data-stu-id="3320f-130">-Policy</span></span>
<span data-ttu-id="3320f-131">Especifica uma política de acesso armazenado, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="3320f-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3320f-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3320f-133">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="3320f-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3320f-134">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3320f-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3320f-135">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="3320f-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3320f-136">-StartTime</span></span>
<span data-ttu-id="3320f-137">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="3320f-137">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3320f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3320f-138">CommonParameters</span></span>
<span data-ttu-id="3320f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3320f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3320f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3320f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3320f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3320f-141">INPUTS</span></span>

### <span data-ttu-id="3320f-142">String</span><span class="sxs-lookup"><span data-stu-id="3320f-142">String</span></span>

<span data-ttu-id="3320f-143">O parâmetro ' container ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3320f-143">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="3320f-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3320f-144">IStorageContext</span></span>

<span data-ttu-id="3320f-145">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3320f-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="3320f-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3320f-146">OUTPUTS</span></span>

### <span data-ttu-id="3320f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3320f-147">System.String</span></span>

## <span data-ttu-id="3320f-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3320f-148">NOTES</span></span>

## <span data-ttu-id="3320f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3320f-149">RELATED LINKS</span></span>

[<span data-ttu-id="3320f-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3320f-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3320f-151">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3320f-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3320f-152">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3320f-152">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3320f-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3320f-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


