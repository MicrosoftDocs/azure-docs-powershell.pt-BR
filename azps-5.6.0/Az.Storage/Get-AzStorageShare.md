---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: 88655ed408242794c6f23a7b170dc007a11ced50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892282"
---
# <span data-ttu-id="c2b69-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c2b69-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="c2b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b69-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b69-103">Obtém uma lista de compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c2b69-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="c2b69-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c2b69-104">SYNTAX</span></span>

### <span data-ttu-id="c2b69-105">MatchingPrefix (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c2b69-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2b69-106">Específico</span><span class="sxs-lookup"><span data-stu-id="c2b69-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c2b69-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c2b69-107">DESCRIPTION</span></span>
<span data-ttu-id="c2b69-108">O cmdlet **Get-AzStorageShare** obtém uma lista de compartilhamentos de arquivos para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c2b69-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="c2b69-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2b69-109">EXAMPLES</span></span>

### <span data-ttu-id="c2b69-110">Exemplo 1: Obter um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="c2b69-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="c2b69-111">Este comando obtém o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c2b69-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="c2b69-112">Exemplo 2: Obter todos os compartilhamentos de arquivos que começam com uma cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="c2b69-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="c2b69-113">Este comando obtém todos os compartilhamentos de arquivos que têm nomes que começam com Contoso.</span><span class="sxs-lookup"><span data-stu-id="c2b69-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="c2b69-114">Exemplo 3: Obter todos os compartilhamentos de arquivos em um contexto especificado</span><span class="sxs-lookup"><span data-stu-id="c2b69-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="c2b69-115">O primeiro comando usa o cmdlet **New-AzStorageContext** para criar um contexto usando o parâmetro *Local* e armazena esse objeto de contexto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="c2b69-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="c2b69-116">O segundo comando obtém os compartilhamentos de arquivo do objeto de contexto armazenados $Context.</span><span class="sxs-lookup"><span data-stu-id="c2b69-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="c2b69-117">Exemplo 4: obter um instantâneo de compartilhamento de arquivos com o nome de compartilhamento específico e o InstantâneoTime</span><span class="sxs-lookup"><span data-stu-id="c2b69-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="c2b69-118">Este comando obtém um instantâneo de compartilhamento de arquivos com nome de compartilhamento específico e InstantâneoTime.</span><span class="sxs-lookup"><span data-stu-id="c2b69-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="c2b69-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c2b69-119">PARAMETERS</span></span>

### <span data-ttu-id="c2b69-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c2b69-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c2b69-121">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c2b69-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c2b69-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c2b69-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c2b69-123">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c2b69-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c2b69-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c2b69-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c2b69-125">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c2b69-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c2b69-126">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c2b69-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c2b69-127">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="c2b69-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c2b69-128">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c2b69-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c2b69-129">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c2b69-129">The default value is 10.</span></span>

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

### <span data-ttu-id="c2b69-130">-Context</span><span class="sxs-lookup"><span data-stu-id="c2b69-130">-Context</span></span>
<span data-ttu-id="c2b69-131">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b69-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c2b69-132">Para obter um contexto, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="c2b69-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c2b69-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b69-133">-DefaultProfile</span></span>
<span data-ttu-id="c2b69-134">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b69-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b69-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c2b69-135">-Name</span></span>
<span data-ttu-id="c2b69-136">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c2b69-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="c2b69-137">Este cmdlet obtém o compartilhamento de arquivos especificado por esse parâmetro ou nada se você especificar o nome de um compartilhamento de arquivos que não existe.</span><span class="sxs-lookup"><span data-stu-id="c2b69-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="c2b69-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="c2b69-138">-Prefix</span></span>
<span data-ttu-id="c2b69-139">Especifica o prefixo para compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c2b69-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="c2b69-140">Este cmdlet obtém compartilhamentos de arquivos que corresponderem ao prefixo especificado por esse parâmetro ou nenhum compartilhamento de arquivos se nenhum compartilhamento de arquivos corresponder ao prefixo especificado.</span><span class="sxs-lookup"><span data-stu-id="c2b69-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="c2b69-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c2b69-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c2b69-142">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c2b69-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c2b69-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c2b69-143">-SnapshotTime</span></span>
<span data-ttu-id="c2b69-144">InstantâneoTime do instantâneo de compartilhamento de arquivos a ser recebido.</span><span class="sxs-lookup"><span data-stu-id="c2b69-144">SnapshotTime of the file share snapshot to be received.</span></span>

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

### <span data-ttu-id="c2b69-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b69-145">CommonParameters</span></span>
<span data-ttu-id="c2b69-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b69-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b69-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b69-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b69-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2b69-148">INPUTS</span></span>

### <span data-ttu-id="c2b69-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2b69-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2b69-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c2b69-150">OUTPUTS</span></span>

### <span data-ttu-id="c2b69-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="c2b69-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="c2b69-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="c2b69-152">NOTES</span></span>

## <span data-ttu-id="c2b69-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2b69-153">RELATED LINKS</span></span>

[<span data-ttu-id="c2b69-154">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c2b69-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="c2b69-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c2b69-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
