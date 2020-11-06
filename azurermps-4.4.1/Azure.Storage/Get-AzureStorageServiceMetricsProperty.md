---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f3930216e93f13004d7d2e8b149867cf511e3708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427074"
---
# <span data-ttu-id="743c9-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="743c9-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="743c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="743c9-102">SYNOPSIS</span></span>
<span data-ttu-id="743c9-103">Obtém as propriedades de métricas para o serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="743c9-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="743c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="743c9-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="743c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="743c9-105">DESCRIPTION</span></span>
<span data-ttu-id="743c9-106">O cmdlet **Get-AzureStorageServiceMetricsProperty** Obtém as propriedades Metrics do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="743c9-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="743c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="743c9-107">EXAMPLES</span></span>

### <span data-ttu-id="743c9-108">Exemplo 1: obter as propriedades de métricas do serviço blob</span><span class="sxs-lookup"><span data-stu-id="743c9-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="743c9-109">Esse comando obtém as propriedades Metrics do armazenamento de BLOB para o tipo métricas de hora.</span><span class="sxs-lookup"><span data-stu-id="743c9-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="743c9-110">OS</span><span class="sxs-lookup"><span data-stu-id="743c9-110">PARAMETERS</span></span>

### <span data-ttu-id="743c9-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="743c9-111">-Context</span></span>
<span data-ttu-id="743c9-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="743c9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="743c9-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="743c9-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="743c9-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="743c9-114">-MetricsType</span></span>
<span data-ttu-id="743c9-115">Especifica um tipo de métrica.</span><span class="sxs-lookup"><span data-stu-id="743c9-115">Specifies a metrics type.</span></span>
<span data-ttu-id="743c9-116">Este cmdlet obtém as propriedades de métricas do serviço de armazenamento do Azure para o tipo de métricas que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="743c9-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="743c9-117">Os valores aceitáveis para esse parâmetro são: Hour e minute.</span><span class="sxs-lookup"><span data-stu-id="743c9-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743c9-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="743c9-118">-ServiceType</span></span>
<span data-ttu-id="743c9-119">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="743c9-119">Specifies the storage service type.</span></span>
<span data-ttu-id="743c9-120">Esse cmdlet obtém as propriedades de métricas do tipo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="743c9-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="743c9-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="743c9-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="743c9-122">Irregular</span><span class="sxs-lookup"><span data-stu-id="743c9-122">Blob</span></span> 
- <span data-ttu-id="743c9-123">TableName</span><span class="sxs-lookup"><span data-stu-id="743c9-123">Table</span></span>
- <span data-ttu-id="743c9-124">Coloca</span><span class="sxs-lookup"><span data-stu-id="743c9-124">Queue</span></span>
- <span data-ttu-id="743c9-125">Arquivos</span><span class="sxs-lookup"><span data-stu-id="743c9-125">File</span></span> 

<span data-ttu-id="743c9-126">Não há suporte para o valor do arquivo no momento.</span><span class="sxs-lookup"><span data-stu-id="743c9-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="743c9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743c9-127">CommonParameters</span></span>
<span data-ttu-id="743c9-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743c9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743c9-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743c9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743c9-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="743c9-130">INPUTS</span></span>

### <span data-ttu-id="743c9-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="743c9-131">IStorageContext</span></span>

<span data-ttu-id="743c9-132">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="743c9-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="743c9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="743c9-133">OUTPUTS</span></span>

### <span data-ttu-id="743c9-134">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="743c9-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="743c9-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="743c9-135">NOTES</span></span>

## <span data-ttu-id="743c9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="743c9-136">RELATED LINKS</span></span>

[<span data-ttu-id="743c9-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="743c9-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="743c9-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="743c9-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


