---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: 31a8d6cbb205b451233bdc72793fb45443350fdd
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93611155"
---
# <span data-ttu-id="4cbb2-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4cbb2-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="4cbb2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cbb2-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbb2-103">Obtém uma lista de compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cbb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cbb2-104">SYNTAX</span></span>

### <span data-ttu-id="4cbb2-105">MatchingPrefix (padrão)</span><span class="sxs-lookup"><span data-stu-id="4cbb2-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cbb2-106">Especifica</span><span class="sxs-lookup"><span data-stu-id="4cbb2-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4cbb2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cbb2-107">DESCRIPTION</span></span>
<span data-ttu-id="4cbb2-108">O cmdlet **Get-AzureStorageShare** Obtém uma lista de compartilhamentos de arquivos para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="4cbb2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cbb2-109">EXAMPLES</span></span>

### <span data-ttu-id="4cbb2-110">Exemplo 1: obter um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="4cbb2-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4cbb2-111">Esse comando obtém o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="4cbb2-112">Exemplo 2: obter todos os compartilhamentos de arquivos que começam com uma cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="4cbb2-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="4cbb2-113">Esse comando obtém todos os compartilhamentos de arquivos que têm nomes que começam com contoso.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="4cbb2-114">Exemplo 3: obter todos os compartilhamentos de arquivos em um contexto especificado</span><span class="sxs-lookup"><span data-stu-id="4cbb2-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="4cbb2-115">O primeiro comando usa o cmdlet **New-AzureStorageContext** para criar um contexto usando o parâmetro *local* e, em seguida, armazena esse objeto Context na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="4cbb2-116">O segundo comando obtém os compartilhamentos de arquivos para o objeto de contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="4cbb2-117">Exemplo 4: obter um instantâneo de compartilhamento de arquivos com um nome de compartilhamento específico e Instantâneotime</span><span class="sxs-lookup"><span data-stu-id="4cbb2-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="4cbb2-118">Esse comando obtém um instantâneo do compartilhamento de arquivos com um nome de compartilhamento específico e Instantâneotime.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="4cbb2-119">OS</span><span class="sxs-lookup"><span data-stu-id="4cbb2-119">PARAMETERS</span></span>

### <span data-ttu-id="4cbb2-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cbb2-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4cbb2-121">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4cbb2-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4cbb2-123">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4cbb2-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4cbb2-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4cbb2-125">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4cbb2-126">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4cbb2-127">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4cbb2-128">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4cbb2-129">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-129">The default value is 10.</span></span>

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

### <span data-ttu-id="4cbb2-130">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4cbb2-130">-Context</span></span>
<span data-ttu-id="4cbb2-131">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4cbb2-132">Para obter um contexto, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="4cbb2-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4cbb2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbb2-133">-DefaultProfile</span></span>
<span data-ttu-id="4cbb2-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cbb2-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cbb2-135">-Name</span></span>
<span data-ttu-id="4cbb2-136">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="4cbb2-137">Esse cmdlet obtém o compartilhamento de arquivo que esse parâmetro especifica ou nada se você especificar o nome de um compartilhamento de arquivos que não existe.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbb2-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4cbb2-138">-Prefix</span></span>
<span data-ttu-id="4cbb2-139">Especifica o prefixo dos compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="4cbb2-140">Esse cmdlet obtém os compartilhamentos de arquivos que correspondem ao prefixo que esse parâmetro especifica, ou nenhum compartilhamento de arquivos se nenhum compartilhamento de arquivos corresponder ao prefixo especificado.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbb2-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cbb2-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4cbb2-142">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4cbb2-143">-Instantâneotime</span><span class="sxs-lookup"><span data-stu-id="4cbb2-143">-SnapshotTime</span></span>
<span data-ttu-id="4cbb2-144">Instantâneotime do instantâneo de compartilhamento de arquivos a ser recebido.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbb2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbb2-145">CommonParameters</span></span>
<span data-ttu-id="4cbb2-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbb2-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbb2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbb2-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cbb2-148">INPUTS</span></span>

### <span data-ttu-id="4cbb2-149">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cbb2-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4cbb2-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cbb2-150">OUTPUTS</span></span>

### <span data-ttu-id="4cbb2-151">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4cbb2-151">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="4cbb2-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cbb2-152">NOTES</span></span>

## <span data-ttu-id="4cbb2-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cbb2-153">RELATED LINKS</span></span>

[<span data-ttu-id="4cbb2-154">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4cbb2-154">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="4cbb2-155">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4cbb2-155">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
