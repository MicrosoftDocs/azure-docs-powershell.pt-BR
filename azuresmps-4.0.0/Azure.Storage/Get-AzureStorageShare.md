---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426142"
---
# <span data-ttu-id="f1982-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1982-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="f1982-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1982-102">SYNOPSIS</span></span>
<span data-ttu-id="f1982-103">Obtém uma lista de compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f1982-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="f1982-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1982-104">SYNTAX</span></span>

### <span data-ttu-id="f1982-105">MatchingPrefix (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1982-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f1982-106">Especifica</span><span class="sxs-lookup"><span data-stu-id="f1982-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f1982-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1982-107">DESCRIPTION</span></span>
<span data-ttu-id="f1982-108">O cmdlet **Get-AzureStorageShare** Obtém uma lista de compartilhamentos de arquivos para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1982-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="f1982-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1982-109">EXAMPLES</span></span>

### <span data-ttu-id="f1982-110">Exemplo 1: obter um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="f1982-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="f1982-111">Esse comando obtém o compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f1982-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="f1982-112">Exemplo 2: obter todos os compartilhamentos de arquivos que começam com uma cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="f1982-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="f1982-113">Esse comando obtém todos os compartilhamentos de arquivos que têm nomes que começam com contoso.</span><span class="sxs-lookup"><span data-stu-id="f1982-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="f1982-114">Exemplo 3: obter todos os compartilhamentos de arquivos em um contexto especificado</span><span class="sxs-lookup"><span data-stu-id="f1982-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="f1982-115">O primeiro comando usa o cmdlet **New-AzureStorageContext** para criar um contexto usando o parâmetro *local* e, em seguida, armazena esse objeto Context na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="f1982-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="f1982-116">O segundo comando obtém os compartilhamentos de arquivos para o objeto de contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="f1982-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="f1982-117">OS</span><span class="sxs-lookup"><span data-stu-id="f1982-117">PARAMETERS</span></span>

### <span data-ttu-id="f1982-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f1982-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f1982-119">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="f1982-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f1982-120">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f1982-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f1982-121">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f1982-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f1982-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f1982-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f1982-123">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f1982-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f1982-124">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f1982-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f1982-125">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="f1982-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f1982-126">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="f1982-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f1982-127">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="f1982-127">The default value is 10.</span></span>

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

### <span data-ttu-id="f1982-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f1982-128">-Context</span></span>
<span data-ttu-id="f1982-129">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1982-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f1982-130">Para obter um contexto, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f1982-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f1982-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1982-131">-Name</span></span>
<span data-ttu-id="f1982-132">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f1982-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="f1982-133">Esse cmdlet obtém o compartilhamento de arquivo que esse parâmetro especifica ou nada se você especificar o nome de um compartilhamento de arquivos que não existe.</span><span class="sxs-lookup"><span data-stu-id="f1982-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1982-134">-Prefix</span><span class="sxs-lookup"><span data-stu-id="f1982-134">-Prefix</span></span>
<span data-ttu-id="f1982-135">Especifica o prefixo dos compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f1982-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="f1982-136">Esse cmdlet obtém os compartilhamentos de arquivos que correspondem ao prefixo que esse parâmetro especifica, ou nenhum compartilhamento de arquivos se nenhum compartilhamento de arquivos corresponder ao prefixo especificado.</span><span class="sxs-lookup"><span data-stu-id="f1982-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1982-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f1982-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f1982-138">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="f1982-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f1982-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1982-139">CommonParameters</span></span>
<span data-ttu-id="f1982-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1982-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1982-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1982-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1982-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1982-142">INPUTS</span></span>

## <span data-ttu-id="f1982-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1982-143">OUTPUTS</span></span>

## <span data-ttu-id="f1982-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1982-144">NOTES</span></span>

## <span data-ttu-id="f1982-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1982-145">RELATED LINKS</span></span>

[<span data-ttu-id="f1982-146">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1982-146">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="f1982-147">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1982-147">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
