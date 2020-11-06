---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 7afcca86721488e7c19658ba1c48d4296f69d9b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598604"
---
# <span data-ttu-id="8eb51-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8eb51-101">New-AzStorageShare</span></span>

## <span data-ttu-id="8eb51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eb51-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb51-103">Cria um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8eb51-103">Creates a file share.</span></span>

## <span data-ttu-id="8eb51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8eb51-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="8eb51-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8eb51-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb51-106">O cmdlet **New-AzStorageShare** cria um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8eb51-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="8eb51-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8eb51-107">EXAMPLES</span></span>

### <span data-ttu-id="8eb51-108">Exemplo 1: criar um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="8eb51-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="8eb51-109">Esse comando cria um compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="8eb51-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="8eb51-110">OS</span><span class="sxs-lookup"><span data-stu-id="8eb51-110">PARAMETERS</span></span>

### <span data-ttu-id="8eb51-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8eb51-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8eb51-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="8eb51-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8eb51-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8eb51-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8eb51-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="8eb51-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8eb51-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8eb51-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8eb51-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8eb51-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8eb51-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8eb51-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8eb51-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="8eb51-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8eb51-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8eb51-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8eb51-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="8eb51-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8eb51-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8eb51-121">-Context</span></span>
<span data-ttu-id="8eb51-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8eb51-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8eb51-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="8eb51-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8eb51-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb51-124">-DefaultProfile</span></span>
<span data-ttu-id="8eb51-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8eb51-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eb51-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8eb51-126">-Name</span></span>
<span data-ttu-id="8eb51-127">Especifica o nome de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8eb51-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="8eb51-128">Esse cmdlet cria um compartilhamento de arquivos que tem o nome que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8eb51-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="8eb51-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8eb51-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8eb51-130">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="8eb51-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8eb51-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb51-131">CommonParameters</span></span>
<span data-ttu-id="8eb51-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb51-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb51-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb51-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb51-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8eb51-134">INPUTS</span></span>

### <span data-ttu-id="8eb51-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8eb51-135">System.String</span></span>

### <span data-ttu-id="8eb51-136">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8eb51-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8eb51-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8eb51-137">OUTPUTS</span></span>

### <span data-ttu-id="8eb51-138">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="8eb51-138">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="8eb51-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8eb51-139">NOTES</span></span>

## <span data-ttu-id="8eb51-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eb51-140">RELATED LINKS</span></span>

[<span data-ttu-id="8eb51-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8eb51-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="8eb51-142">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8eb51-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8eb51-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8eb51-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
