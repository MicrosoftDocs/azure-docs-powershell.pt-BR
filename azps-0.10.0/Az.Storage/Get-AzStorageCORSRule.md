---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: c32e58f2e6b8c146d1b5a01f252f1341092f86d5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776270"
---
# <span data-ttu-id="bf297-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bf297-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="bf297-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf297-102">SYNOPSIS</span></span>
<span data-ttu-id="bf297-103">Obtém regras CORS para um tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bf297-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="bf297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf297-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bf297-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf297-105">DESCRIPTION</span></span>
<span data-ttu-id="bf297-106">O cmdlet **Get-AzStorageCORSRule** Obtém regras de compartilhamento de recursos entre origens (CORS) para um tipo de serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf297-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="bf297-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf297-107">EXAMPLES</span></span>

### <span data-ttu-id="bf297-108">Exemplo 1: obter regras CORS do serviço blob</span><span class="sxs-lookup"><span data-stu-id="bf297-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="bf297-109">Este comando obtém as regras CORS para o tipo de serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="bf297-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="bf297-110">OS</span><span class="sxs-lookup"><span data-stu-id="bf297-110">PARAMETERS</span></span>

### <span data-ttu-id="bf297-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf297-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bf297-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="bf297-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bf297-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="bf297-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bf297-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="bf297-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bf297-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bf297-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bf297-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bf297-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bf297-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bf297-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bf297-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="bf297-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bf297-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="bf297-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bf297-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="bf297-120">The default value is 10.</span></span>

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

### <span data-ttu-id="bf297-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bf297-121">-Context</span></span>
<span data-ttu-id="bf297-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf297-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="bf297-123">Para obter um contexto, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bf297-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bf297-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf297-124">-DefaultProfile</span></span>
<span data-ttu-id="bf297-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf297-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf297-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf297-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bf297-127">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="bf297-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bf297-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bf297-128">-ServiceType</span></span>
<span data-ttu-id="bf297-129">Especifica o tipo de serviço de armazenamento do Azure para o qual este cmdlet obtém regras CORS.</span><span class="sxs-lookup"><span data-stu-id="bf297-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="bf297-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bf297-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf297-131">Irregular</span><span class="sxs-lookup"><span data-stu-id="bf297-131">Blob</span></span> 
- <span data-ttu-id="bf297-132">TableName</span><span class="sxs-lookup"><span data-stu-id="bf297-132">Table</span></span> 
- <span data-ttu-id="bf297-133">Coloca</span><span class="sxs-lookup"><span data-stu-id="bf297-133">Queue</span></span> 
- <span data-ttu-id="bf297-134">Arquivos</span><span class="sxs-lookup"><span data-stu-id="bf297-134">File</span></span>

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

### <span data-ttu-id="bf297-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf297-135">CommonParameters</span></span>
<span data-ttu-id="bf297-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf297-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf297-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf297-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf297-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf297-138">INPUTS</span></span>

### <span data-ttu-id="bf297-139">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf297-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bf297-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf297-140">OUTPUTS</span></span>

### <span data-ttu-id="bf297-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="bf297-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="bf297-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf297-142">NOTES</span></span>

## <span data-ttu-id="bf297-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf297-143">RELATED LINKS</span></span>

[<span data-ttu-id="bf297-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bf297-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="bf297-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bf297-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)

