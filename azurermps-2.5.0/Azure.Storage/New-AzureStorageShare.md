---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageshare
schema: 2.0.0
ms.openlocfilehash: 55ee72941f49954bcc56f9558bc7ffb444ae9e6b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786008"
---
# <span data-ttu-id="e6aa3-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e6aa3-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="e6aa3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="e6aa3-103">Cria um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6aa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6aa3-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6aa3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="e6aa3-106">O cmdlet **New-AzureStorageShare** cria um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="e6aa3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="e6aa3-108">Exemplo 1: criar um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="e6aa3-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="e6aa3-109">Esse comando cria um compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="e6aa3-110">OS</span><span class="sxs-lookup"><span data-stu-id="e6aa3-110">PARAMETERS</span></span>

### <span data-ttu-id="e6aa3-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e6aa3-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e6aa3-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e6aa3-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e6aa3-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e6aa3-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e6aa3-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e6aa3-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e6aa3-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e6aa3-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e6aa3-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e6aa3-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e6aa3-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e6aa3-121">-Context</span></span>
<span data-ttu-id="e6aa3-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e6aa3-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e6aa3-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e6aa3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6aa3-124">-DefaultProfile</span></span>
<span data-ttu-id="e6aa3-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6aa3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6aa3-126">-Name</span></span>
<span data-ttu-id="e6aa3-127">Especifica o nome de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="e6aa3-128">Esse cmdlet cria um compartilhamento de arquivos que tem o nome que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6aa3-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e6aa3-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e6aa3-130">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e6aa3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6aa3-131">CommonParameters</span></span>
<span data-ttu-id="e6aa3-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6aa3-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6aa3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6aa3-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6aa3-134">INPUTS</span></span>

### <span data-ttu-id="e6aa3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e6aa3-135">System.String</span></span>

### <span data-ttu-id="e6aa3-136">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e6aa3-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e6aa3-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6aa3-137">OUTPUTS</span></span>

### <span data-ttu-id="e6aa3-138">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e6aa3-138">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="e6aa3-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6aa3-139">NOTES</span></span>

## <span data-ttu-id="e6aa3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6aa3-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6aa3-141">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e6aa3-141">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="e6aa3-142">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e6aa3-142">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e6aa3-143">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e6aa3-143">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
