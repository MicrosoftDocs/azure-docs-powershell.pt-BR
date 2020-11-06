---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 49d966c23569080ab72d0793014fe4fa5dd71b55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427063"
---
# <span data-ttu-id="7fbb7-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7fbb7-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="7fbb7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbb7-103">Cria uma política de acesso armazenado em um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fbb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fbb7-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fbb7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fbb7-105">DESCRIPTION</span></span>
<span data-ttu-id="7fbb7-106">O cmdlet **New-AzureStorageShareStoredAccessPolicy** cria uma política de acesso armazenado em um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="7fbb7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fbb7-107">EXAMPLES</span></span>

### <span data-ttu-id="7fbb7-108">Exemplo 1: criar uma política de acesso armazenado em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="7fbb7-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="7fbb7-109">Esse comando cria uma política de acesso armazenado que tem permissão total em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="7fbb7-110">OS</span><span class="sxs-lookup"><span data-stu-id="7fbb7-110">PARAMETERS</span></span>

### <span data-ttu-id="7fbb7-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7fbb7-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7fbb7-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7fbb7-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7fbb7-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7fbb7-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7fbb7-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7fbb7-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7fbb7-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7fbb7-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7fbb7-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7fbb7-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7fbb7-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7fbb7-121">-Context</span></span>
<span data-ttu-id="7fbb7-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7fbb7-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="7fbb7-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7fbb7-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7fbb7-124">-ExpiryTime</span></span>
<span data-ttu-id="7fbb7-125">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="7fbb7-126">-Permissão</span><span class="sxs-lookup"><span data-stu-id="7fbb7-126">-Permission</span></span>
<span data-ttu-id="7fbb7-127">Especifica as permissões na política de acesso armazenado para acessar os arquivos ou o compartilhamento de armazenamento abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

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

### <span data-ttu-id="7fbb7-128">-Política</span><span class="sxs-lookup"><span data-stu-id="7fbb7-128">-Policy</span></span>
<span data-ttu-id="7fbb7-129">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-129">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="7fbb7-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7fbb7-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7fbb7-131">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7fbb7-132">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7fbb7-132">-ShareName</span></span>
<span data-ttu-id="7fbb7-133">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-133">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="7fbb7-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7fbb7-134">-StartTime</span></span>
<span data-ttu-id="7fbb7-135">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-135">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="7fbb7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbb7-136">CommonParameters</span></span>
<span data-ttu-id="7fbb7-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fbb7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbb7-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbb7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbb7-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fbb7-139">INPUTS</span></span>

### <span data-ttu-id="7fbb7-140">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fbb7-140">IStorageContext</span></span>

<span data-ttu-id="7fbb7-141">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7fbb7-141">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7fbb7-142">String</span><span class="sxs-lookup"><span data-stu-id="7fbb7-142">String</span></span>

<span data-ttu-id="7fbb7-143">O parâmetro ' ShareName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7fbb7-143">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7fbb7-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fbb7-144">OUTPUTS</span></span>

### <span data-ttu-id="7fbb7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7fbb7-145">System.String</span></span>

## <span data-ttu-id="7fbb7-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fbb7-146">NOTES</span></span>

## <span data-ttu-id="7fbb7-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fbb7-147">RELATED LINKS</span></span>

[<span data-ttu-id="7fbb7-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7fbb7-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="7fbb7-149">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fbb7-149">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7fbb7-150">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7fbb7-150">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="7fbb7-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7fbb7-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
