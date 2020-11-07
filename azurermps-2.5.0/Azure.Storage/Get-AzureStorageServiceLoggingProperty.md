---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: f43386ff1eca223e8ff0e1e8ea7a07d1d8e25d0d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785391"
---
# <span data-ttu-id="e35fe-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e35fe-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="e35fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e35fe-102">SYNOPSIS</span></span>
<span data-ttu-id="e35fe-103">Obtém Propriedades de registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fe-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e35fe-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e35fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e35fe-105">DESCRIPTION</span></span>
<span data-ttu-id="e35fe-106">O cmdlet **Get-AzureStorageServiceLoggingProperty** Obtém Propriedades de log para os serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fe-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="e35fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e35fe-107">EXAMPLES</span></span>

### <span data-ttu-id="e35fe-108">Exemplo 1: obter propriedades de log para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="e35fe-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="e35fe-109">Este comando obtém Propriedades de log para armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="e35fe-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="e35fe-110">OS</span><span class="sxs-lookup"><span data-stu-id="e35fe-110">PARAMETERS</span></span>

### <span data-ttu-id="e35fe-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e35fe-111">-Context</span></span>
<span data-ttu-id="e35fe-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fe-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e35fe-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e35fe-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e35fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35fe-114">-DefaultProfile</span></span>
<span data-ttu-id="e35fe-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e35fe-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e35fe-116">-ServiceType</span></span>
<span data-ttu-id="e35fe-117">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e35fe-117">Specifies the storage service type.</span></span>
<span data-ttu-id="e35fe-118">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e35fe-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="e35fe-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e35fe-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e35fe-120">Irregular</span><span class="sxs-lookup"><span data-stu-id="e35fe-120">Blob</span></span> 
- <span data-ttu-id="e35fe-121">TableName</span><span class="sxs-lookup"><span data-stu-id="e35fe-121">Table</span></span>
- <span data-ttu-id="e35fe-122">Coloca</span><span class="sxs-lookup"><span data-stu-id="e35fe-122">Queue</span></span>
- <span data-ttu-id="e35fe-123">Arquivo no momento, não há suporte para o valor do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e35fe-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="e35fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35fe-124">CommonParameters</span></span>
<span data-ttu-id="e35fe-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35fe-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35fe-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e35fe-127">INPUTS</span></span>

### <span data-ttu-id="e35fe-128">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e35fe-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e35fe-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e35fe-129">OUTPUTS</span></span>

### <span data-ttu-id="e35fe-130">Microsoft. WindowsAzure. Storage. Shared. Protocol. Loggingproperties</span><span class="sxs-lookup"><span data-stu-id="e35fe-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="e35fe-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e35fe-131">NOTES</span></span>

## <span data-ttu-id="e35fe-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e35fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="e35fe-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e35fe-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e35fe-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e35fe-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


