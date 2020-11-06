---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8a7dc4210996a233d07559f10067f71bc944ae29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427068"
---
# <span data-ttu-id="06c0d-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06c0d-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="06c0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="06c0d-103">Obtém políticas de acesso armazenadas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="06c0d-103">Gets stored access policies for a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06c0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06c0d-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="06c0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="06c0d-106">O cmdlet **Get-AzureStorageShareStoredAccessPolicy** tem políticas de acesso armazenadas para um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="06c0d-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="06c0d-107">Para obter uma política específica, especifique-a por nome.</span><span class="sxs-lookup"><span data-stu-id="06c0d-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="06c0d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06c0d-108">EXAMPLES</span></span>

### <span data-ttu-id="06c0d-109">Exemplo 1: obter uma política de acesso armazenado em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="06c0d-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="06c0d-110">Este comando obtém uma política de acesso armazenado chamada GeneralPolicy em ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="06c0d-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="06c0d-111">Exemplo 2: obter todas as políticas de acesso armazenadas no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="06c0d-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="06c0d-112">Esse comando obtém todas as políticas de acesso armazenadas no ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="06c0d-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="06c0d-113">OS</span><span class="sxs-lookup"><span data-stu-id="06c0d-113">PARAMETERS</span></span>

### <span data-ttu-id="06c0d-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="06c0d-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="06c0d-115">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="06c0d-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="06c0d-116">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="06c0d-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="06c0d-117">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="06c0d-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="06c0d-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="06c0d-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="06c0d-119">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="06c0d-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="06c0d-120">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="06c0d-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="06c0d-121">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="06c0d-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="06c0d-122">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="06c0d-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="06c0d-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="06c0d-123">The default value is 10.</span></span>

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

### <span data-ttu-id="06c0d-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="06c0d-124">-Context</span></span>
<span data-ttu-id="06c0d-125">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="06c0d-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="06c0d-126">Para obter um contexto, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="06c0d-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="06c0d-127">-Política</span><span class="sxs-lookup"><span data-stu-id="06c0d-127">-Policy</span></span>
<span data-ttu-id="06c0d-128">Especifica o nome da política de acesso armazenado que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="06c0d-128">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c0d-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="06c0d-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="06c0d-130">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="06c0d-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="06c0d-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="06c0d-131">-ShareName</span></span>
<span data-ttu-id="06c0d-132">Especifica o nome do compartilhamento de armazenamento para o qual este cmdlet obtém políticas.</span><span class="sxs-lookup"><span data-stu-id="06c0d-132">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="06c0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c0d-133">CommonParameters</span></span>
<span data-ttu-id="06c0d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06c0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c0d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c0d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c0d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06c0d-136">INPUTS</span></span>

### <span data-ttu-id="06c0d-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="06c0d-137">IStorageContext</span></span>

<span data-ttu-id="06c0d-138">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="06c0d-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="06c0d-139">String</span><span class="sxs-lookup"><span data-stu-id="06c0d-139">String</span></span>

<span data-ttu-id="06c0d-140">O parâmetro ' ShareName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="06c0d-140">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="06c0d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06c0d-141">OUTPUTS</span></span>

### <span data-ttu-id="06c0d-142">Microsoft. WindowsAzure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="06c0d-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="06c0d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06c0d-143">NOTES</span></span>

## <span data-ttu-id="06c0d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06c0d-144">RELATED LINKS</span></span>

[<span data-ttu-id="06c0d-145">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="06c0d-145">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="06c0d-146">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06c0d-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="06c0d-147">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06c0d-147">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="06c0d-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06c0d-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
