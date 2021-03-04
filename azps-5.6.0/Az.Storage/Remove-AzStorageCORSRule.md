---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: 9c6213fb619297ca5e2c49883f42a5d875d940e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889599"
---
# <span data-ttu-id="eff07-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="eff07-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="eff07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eff07-102">SYNOPSIS</span></span>
<span data-ttu-id="eff07-103">Remove o CORS para um serviço de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eff07-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="eff07-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eff07-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="eff07-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eff07-105">DESCRIPTION</span></span>
<span data-ttu-id="eff07-106">O cmdlet **Remove-AzStorageCORSRule** remove o CORS (Compartilhamento de Recursos entre Origens) para um serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="eff07-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="eff07-107">Este cmdlet exclui todas as regras do CORS em um tipo de serviço de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eff07-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="eff07-108">Os tipos de serviços de armazenamento para este cmdlet são Blob, Table, Queue e File.</span><span class="sxs-lookup"><span data-stu-id="eff07-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="eff07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eff07-109">EXAMPLES</span></span>

### <span data-ttu-id="eff07-110">Exemplo 1: Remover regras do CORS para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="eff07-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="eff07-111">Este comando remove as regras do CORS para o tipo de serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="eff07-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="eff07-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eff07-112">PARAMETERS</span></span>

### <span data-ttu-id="eff07-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eff07-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eff07-114">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="eff07-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eff07-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="eff07-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eff07-116">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="eff07-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eff07-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eff07-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eff07-118">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="eff07-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eff07-119">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="eff07-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eff07-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="eff07-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eff07-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="eff07-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eff07-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="eff07-122">The default value is 10.</span></span>

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

### <span data-ttu-id="eff07-123">-Context</span><span class="sxs-lookup"><span data-stu-id="eff07-123">-Context</span></span>
<span data-ttu-id="eff07-124">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="eff07-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="eff07-125">Para obter o contexto de armazenamento, o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eff07-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="eff07-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff07-126">-DefaultProfile</span></span>
<span data-ttu-id="eff07-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eff07-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eff07-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eff07-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eff07-129">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="eff07-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="eff07-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="eff07-130">-ServiceType</span></span>
<span data-ttu-id="eff07-131">Especifica o tipo de serviço de Armazenamento do Azure para o qual este cmdlet remove regras.</span><span class="sxs-lookup"><span data-stu-id="eff07-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="eff07-132">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="eff07-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eff07-133">Blob</span><span class="sxs-lookup"><span data-stu-id="eff07-133">Blob</span></span> 
- <span data-ttu-id="eff07-134">Tabela</span><span class="sxs-lookup"><span data-stu-id="eff07-134">Table</span></span> 
- <span data-ttu-id="eff07-135">Fila</span><span class="sxs-lookup"><span data-stu-id="eff07-135">Queue</span></span> 
- <span data-ttu-id="eff07-136">Arquivo</span><span class="sxs-lookup"><span data-stu-id="eff07-136">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff07-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff07-137">CommonParameters</span></span>
<span data-ttu-id="eff07-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff07-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff07-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff07-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff07-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eff07-140">INPUTS</span></span>

### <span data-ttu-id="eff07-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eff07-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eff07-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eff07-142">OUTPUTS</span></span>

### <span data-ttu-id="eff07-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="eff07-143">System.Void</span></span>

## <span data-ttu-id="eff07-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="eff07-144">NOTES</span></span>

## <span data-ttu-id="eff07-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eff07-145">RELATED LINKS</span></span>

[<span data-ttu-id="eff07-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="eff07-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="eff07-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="eff07-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


