---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602084"
---
# <span data-ttu-id="7999f-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7999f-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="7999f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7999f-102">SYNOPSIS</span></span>
<span data-ttu-id="7999f-103">Obtém Propriedades de registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7999f-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7999f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7999f-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="7999f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7999f-105">DESCRIPTION</span></span>
<span data-ttu-id="7999f-106">O cmdlet **Get-AzureStorageServiceLoggingProperty** Obtém Propriedades de log para os serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7999f-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="7999f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7999f-107">EXAMPLES</span></span>

### <span data-ttu-id="7999f-108">Exemplo 1: obter propriedades de log para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="7999f-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="7999f-109">Este comando obtém Propriedades de log para armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="7999f-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="7999f-110">OS</span><span class="sxs-lookup"><span data-stu-id="7999f-110">PARAMETERS</span></span>

### <span data-ttu-id="7999f-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7999f-111">-Context</span></span>
<span data-ttu-id="7999f-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7999f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7999f-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7999f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7999f-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="7999f-114">-ServiceType</span></span>
<span data-ttu-id="7999f-115">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7999f-115">Specifies the storage service type.</span></span>
<span data-ttu-id="7999f-116">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7999f-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="7999f-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7999f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7999f-118">Irregular</span><span class="sxs-lookup"><span data-stu-id="7999f-118">Blob</span></span> 
- <span data-ttu-id="7999f-119">TableName</span><span class="sxs-lookup"><span data-stu-id="7999f-119">Table</span></span>
- <span data-ttu-id="7999f-120">Coloca</span><span class="sxs-lookup"><span data-stu-id="7999f-120">Queue</span></span>
- <span data-ttu-id="7999f-121">Arquivos</span><span class="sxs-lookup"><span data-stu-id="7999f-121">File</span></span>

<span data-ttu-id="7999f-122">Não há suporte para o valor do arquivo no momento.</span><span class="sxs-lookup"><span data-stu-id="7999f-122">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7999f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7999f-123">CommonParameters</span></span>
<span data-ttu-id="7999f-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7999f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7999f-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7999f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7999f-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7999f-126">INPUTS</span></span>

### <span data-ttu-id="7999f-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7999f-127">IStorageContext</span></span>

<span data-ttu-id="7999f-128">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7999f-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="7999f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7999f-129">OUTPUTS</span></span>

### <span data-ttu-id="7999f-130">Microsoft. WindowsAzure. Storage. Shared. Protocol. Loggingproperties</span><span class="sxs-lookup"><span data-stu-id="7999f-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="7999f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7999f-131">NOTES</span></span>

## <span data-ttu-id="7999f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7999f-132">RELATED LINKS</span></span>

[<span data-ttu-id="7999f-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7999f-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7999f-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7999f-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


