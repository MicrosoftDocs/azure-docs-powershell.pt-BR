---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: d800c8deed7a56c50175fcb6607c8c53b8f9dce5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776249"
---
# <span data-ttu-id="a13ff-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a13ff-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="a13ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a13ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a13ff-103">Obtém uma lista de compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a13ff-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="a13ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a13ff-104">SYNTAX</span></span>

### <span data-ttu-id="a13ff-105">MatchingPrefix (padrão)</span><span class="sxs-lookup"><span data-stu-id="a13ff-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a13ff-106">Especifica</span><span class="sxs-lookup"><span data-stu-id="a13ff-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a13ff-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a13ff-107">DESCRIPTION</span></span>
<span data-ttu-id="a13ff-108">O cmdlet **Get-AzStorageShare** Obtém uma lista de compartilhamentos de arquivos para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a13ff-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="a13ff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a13ff-109">EXAMPLES</span></span>

### <span data-ttu-id="a13ff-110">Exemplo 1: obter um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="a13ff-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="a13ff-111">Esse comando obtém o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a13ff-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="a13ff-112">Exemplo 2: obter todos os compartilhamentos de arquivos que começam com uma cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a13ff-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="a13ff-113">Esse comando obtém todos os compartilhamentos de arquivos que têm nomes que começam com contoso.</span><span class="sxs-lookup"><span data-stu-id="a13ff-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="a13ff-114">Exemplo 3: obter todos os compartilhamentos de arquivos em um contexto especificado</span><span class="sxs-lookup"><span data-stu-id="a13ff-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="a13ff-115">O primeiro comando usa o cmdlet **New-AzStorageContext** para criar um contexto usando o parâmetro *local* e, em seguida, armazena esse objeto Context na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="a13ff-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="a13ff-116">O segundo comando obtém os compartilhamentos de arquivos para o objeto de contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="a13ff-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="a13ff-117">Exemplo 4: obter um instantâneo de compartilhamento de arquivos com um nome de compartilhamento específico e Instantâneotime</span><span class="sxs-lookup"><span data-stu-id="a13ff-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="a13ff-118">Esse comando obtém um instantâneo do compartilhamento de arquivos com um nome de compartilhamento específico e Instantâneotime.</span><span class="sxs-lookup"><span data-stu-id="a13ff-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="a13ff-119">OS</span><span class="sxs-lookup"><span data-stu-id="a13ff-119">PARAMETERS</span></span>

### <span data-ttu-id="a13ff-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a13ff-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a13ff-121">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="a13ff-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a13ff-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a13ff-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a13ff-123">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a13ff-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a13ff-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a13ff-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a13ff-125">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a13ff-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a13ff-126">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a13ff-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a13ff-127">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="a13ff-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a13ff-128">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a13ff-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a13ff-129">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a13ff-129">The default value is 10.</span></span>

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

### <span data-ttu-id="a13ff-130">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a13ff-130">-Context</span></span>
<span data-ttu-id="a13ff-131">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a13ff-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a13ff-132">Para obter um contexto, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="a13ff-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a13ff-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a13ff-133">-DefaultProfile</span></span>
<span data-ttu-id="a13ff-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a13ff-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a13ff-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="a13ff-135">-Name</span></span>
<span data-ttu-id="a13ff-136">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a13ff-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="a13ff-137">Esse cmdlet obtém o compartilhamento de arquivo que esse parâmetro especifica ou nada se você especificar o nome de um compartilhamento de arquivos que não existe.</span><span class="sxs-lookup"><span data-stu-id="a13ff-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="a13ff-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="a13ff-138">-Prefix</span></span>
<span data-ttu-id="a13ff-139">Especifica o prefixo dos compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a13ff-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="a13ff-140">Esse cmdlet obtém os compartilhamentos de arquivos que correspondem ao prefixo que esse parâmetro especifica, ou nenhum compartilhamento de arquivos se nenhum compartilhamento de arquivos corresponder ao prefixo especificado.</span><span class="sxs-lookup"><span data-stu-id="a13ff-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="a13ff-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a13ff-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a13ff-142">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a13ff-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a13ff-143">-Instantâneotime</span><span class="sxs-lookup"><span data-stu-id="a13ff-143">-SnapshotTime</span></span>
<span data-ttu-id="a13ff-144">Instantâneotime do instantâneo de compartilhamento de arquivos a ser recebido.</span><span class="sxs-lookup"><span data-stu-id="a13ff-144">SnapshotTime of the file share snapshot to be received.</span></span>

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

### <span data-ttu-id="a13ff-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a13ff-145">CommonParameters</span></span>
<span data-ttu-id="a13ff-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a13ff-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a13ff-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a13ff-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a13ff-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a13ff-148">INPUTS</span></span>

### <span data-ttu-id="a13ff-149">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a13ff-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a13ff-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a13ff-150">OUTPUTS</span></span>

### <span data-ttu-id="a13ff-151">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a13ff-151">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="a13ff-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a13ff-152">NOTES</span></span>

## <span data-ttu-id="a13ff-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a13ff-153">RELATED LINKS</span></span>

[<span data-ttu-id="a13ff-154">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a13ff-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="a13ff-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a13ff-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)