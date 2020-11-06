---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: 56410e48bedbe7af616ffd1dcada4e99f1668cdc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598648"
---
# <span data-ttu-id="4cda7-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4cda7-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="4cda7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cda7-102">SYNOPSIS</span></span>
<span data-ttu-id="4cda7-103">Obtém uma lista de compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cda7-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="4cda7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cda7-104">SYNTAX</span></span>

### <span data-ttu-id="4cda7-105">MatchingPrefix (padrão)</span><span class="sxs-lookup"><span data-stu-id="4cda7-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cda7-106">Especifica</span><span class="sxs-lookup"><span data-stu-id="4cda7-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4cda7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cda7-107">DESCRIPTION</span></span>
<span data-ttu-id="4cda7-108">O cmdlet **Get-AzStorageShare** Obtém uma lista de compartilhamentos de arquivos para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4cda7-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="4cda7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cda7-109">EXAMPLES</span></span>

### <span data-ttu-id="4cda7-110">Exemplo 1: obter um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="4cda7-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4cda7-111">Esse comando obtém o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="4cda7-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="4cda7-112">Exemplo 2: obter todos os compartilhamentos de arquivos que começam com uma cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="4cda7-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="4cda7-113">Esse comando obtém todos os compartilhamentos de arquivos que têm nomes que começam com contoso.</span><span class="sxs-lookup"><span data-stu-id="4cda7-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="4cda7-114">Exemplo 3: obter todos os compartilhamentos de arquivos em um contexto especificado</span><span class="sxs-lookup"><span data-stu-id="4cda7-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="4cda7-115">O primeiro comando usa o cmdlet **New-AzStorageContext** para criar um contexto usando o parâmetro *local* e, em seguida, armazena esse objeto Context na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="4cda7-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="4cda7-116">O segundo comando obtém os compartilhamentos de arquivos para o objeto de contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="4cda7-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="4cda7-117">Exemplo 4: obter um instantâneo de compartilhamento de arquivos com um nome de compartilhamento específico e Instantâneotime</span><span class="sxs-lookup"><span data-stu-id="4cda7-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="4cda7-118">Esse comando obtém um instantâneo do compartilhamento de arquivos com um nome de compartilhamento específico e Instantâneotime.</span><span class="sxs-lookup"><span data-stu-id="4cda7-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="4cda7-119">OS</span><span class="sxs-lookup"><span data-stu-id="4cda7-119">PARAMETERS</span></span>

### <span data-ttu-id="4cda7-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cda7-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4cda7-121">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="4cda7-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4cda7-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4cda7-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4cda7-123">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="4cda7-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4cda7-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4cda7-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4cda7-125">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4cda7-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4cda7-126">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4cda7-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4cda7-127">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="4cda7-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4cda7-128">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4cda7-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4cda7-129">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="4cda7-129">The default value is 10.</span></span>

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

### <span data-ttu-id="4cda7-130">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4cda7-130">-Context</span></span>
<span data-ttu-id="4cda7-131">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cda7-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4cda7-132">Para obter um contexto, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="4cda7-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4cda7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cda7-133">-DefaultProfile</span></span>
<span data-ttu-id="4cda7-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cda7-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cda7-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cda7-135">-Name</span></span>
<span data-ttu-id="4cda7-136">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cda7-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="4cda7-137">Esse cmdlet obtém o compartilhamento de arquivo que esse parâmetro especifica ou nada se você especificar o nome de um compartilhamento de arquivos que não existe.</span><span class="sxs-lookup"><span data-stu-id="4cda7-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="4cda7-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4cda7-138">-Prefix</span></span>
<span data-ttu-id="4cda7-139">Especifica o prefixo dos compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cda7-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="4cda7-140">Esse cmdlet obtém os compartilhamentos de arquivos que correspondem ao prefixo que esse parâmetro especifica, ou nenhum compartilhamento de arquivos se nenhum compartilhamento de arquivos corresponder ao prefixo especificado.</span><span class="sxs-lookup"><span data-stu-id="4cda7-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="4cda7-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cda7-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4cda7-142">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="4cda7-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4cda7-143">-Instantâneotime</span><span class="sxs-lookup"><span data-stu-id="4cda7-143">-SnapshotTime</span></span>
<span data-ttu-id="4cda7-144">Instantâneotime do instantâneo de compartilhamento de arquivos a ser recebido.</span><span class="sxs-lookup"><span data-stu-id="4cda7-144">SnapshotTime of the file share snapshot to be received.</span></span>

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

### <span data-ttu-id="4cda7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cda7-145">CommonParameters</span></span>
<span data-ttu-id="4cda7-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cda7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cda7-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cda7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cda7-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cda7-148">INPUTS</span></span>

### <span data-ttu-id="4cda7-149">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cda7-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4cda7-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cda7-150">OUTPUTS</span></span>

### <span data-ttu-id="4cda7-151">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4cda7-151">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="4cda7-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cda7-152">NOTES</span></span>

## <span data-ttu-id="4cda7-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cda7-153">RELATED LINKS</span></span>

[<span data-ttu-id="4cda7-154">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4cda7-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="4cda7-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4cda7-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
