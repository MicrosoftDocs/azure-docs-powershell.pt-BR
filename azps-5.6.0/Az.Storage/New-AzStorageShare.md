---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 492ad3713bafa692d0ddf969540b8cab89fc05a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891947"
---
# <span data-ttu-id="c7d3a-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c7d3a-101">New-AzStorageShare</span></span>

## <span data-ttu-id="c7d3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d3a-103">Cria um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-103">Creates a file share.</span></span>

## <span data-ttu-id="c7d3a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c7d3a-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7d3a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c7d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d3a-106">O cmdlet **New-AzStorageShare** cria um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="c7d3a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7d3a-107">EXAMPLES</span></span>

### <span data-ttu-id="c7d3a-108">Exemplo 1: Criar um compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="c7d3a-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="c7d3a-109">Este comando cria um compartilhamento de arquivos chamado ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="c7d3a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c7d3a-110">PARAMETERS</span></span>

### <span data-ttu-id="c7d3a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7d3a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c7d3a-112">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c7d3a-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c7d3a-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c7d3a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c7d3a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c7d3a-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c7d3a-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c7d3a-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c7d3a-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c7d3a-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c7d3a-121">-Context</span><span class="sxs-lookup"><span data-stu-id="c7d3a-121">-Context</span></span>
<span data-ttu-id="c7d3a-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c7d3a-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="c7d3a-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c7d3a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d3a-124">-DefaultProfile</span></span>
<span data-ttu-id="c7d3a-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7d3a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c7d3a-126">-Name</span></span>
<span data-ttu-id="c7d3a-127">Especifica o nome de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="c7d3a-128">Este cmdlet cria um compartilhamento de arquivos que tem o nome especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="c7d3a-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7d3a-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c7d3a-130">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c7d3a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d3a-131">CommonParameters</span></span>
<span data-ttu-id="c7d3a-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d3a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d3a-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d3a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d3a-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7d3a-134">INPUTS</span></span>

### <span data-ttu-id="c7d3a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c7d3a-135">System.String</span></span>

### <span data-ttu-id="c7d3a-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7d3a-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7d3a-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c7d3a-137">OUTPUTS</span></span>

### <span data-ttu-id="c7d3a-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="c7d3a-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="c7d3a-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="c7d3a-139">NOTES</span></span>

## <span data-ttu-id="c7d3a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7d3a-140">RELATED LINKS</span></span>

[<span data-ttu-id="c7d3a-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c7d3a-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c7d3a-142">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7d3a-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c7d3a-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c7d3a-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
