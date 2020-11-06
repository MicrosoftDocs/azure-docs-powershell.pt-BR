---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426146"
---
# <span data-ttu-id="99e9c-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="99e9c-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="99e9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="99e9c-103">Obtém as propriedades de métricas para o serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="99e9c-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="99e9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99e9c-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="99e9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="99e9c-106">O cmdlet **Get-AzureStorageServiceMetricsProperty** Obtém as propriedades Metrics do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="99e9c-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="99e9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99e9c-107">EXAMPLES</span></span>

### <span data-ttu-id="99e9c-108">Exemplo 1: obter as propriedades de métricas do serviço blob</span><span class="sxs-lookup"><span data-stu-id="99e9c-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="99e9c-109">Esse comando obtém as propriedades Metrics do armazenamento de BLOB para o tipo métricas de hora.</span><span class="sxs-lookup"><span data-stu-id="99e9c-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="99e9c-110">OS</span><span class="sxs-lookup"><span data-stu-id="99e9c-110">PARAMETERS</span></span>

### <span data-ttu-id="99e9c-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="99e9c-111">-Context</span></span>
<span data-ttu-id="99e9c-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="99e9c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="99e9c-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="99e9c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="99e9c-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="99e9c-114">-MetricsType</span></span>
<span data-ttu-id="99e9c-115">Especifica um tipo de métrica.</span><span class="sxs-lookup"><span data-stu-id="99e9c-115">Specifies a metrics type.</span></span>
<span data-ttu-id="99e9c-116">Este cmdlet obtém as propriedades de métricas do serviço de armazenamento do Azure para o tipo de métricas que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="99e9c-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="99e9c-117">Os valores aceitáveis para esse parâmetro são: Hour e minute.</span><span class="sxs-lookup"><span data-stu-id="99e9c-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="99e9c-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="99e9c-118">-ServiceType</span></span>
<span data-ttu-id="99e9c-119">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="99e9c-119">Specifies the storage service type.</span></span>
<span data-ttu-id="99e9c-120">Esse cmdlet obtém as propriedades de métricas do tipo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="99e9c-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="99e9c-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="99e9c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="99e9c-122">Irregular</span><span class="sxs-lookup"><span data-stu-id="99e9c-122">Blob</span></span> 
- <span data-ttu-id="99e9c-123">TableName</span><span class="sxs-lookup"><span data-stu-id="99e9c-123">Table</span></span>
- <span data-ttu-id="99e9c-124">Coloca</span><span class="sxs-lookup"><span data-stu-id="99e9c-124">Queue</span></span>
- <span data-ttu-id="99e9c-125">Arquivos</span><span class="sxs-lookup"><span data-stu-id="99e9c-125">File</span></span> 

<span data-ttu-id="99e9c-126">Não há suporte para o valor do arquivo no momento.</span><span class="sxs-lookup"><span data-stu-id="99e9c-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="99e9c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e9c-127">CommonParameters</span></span>
<span data-ttu-id="99e9c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e9c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e9c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e9c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e9c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99e9c-130">INPUTS</span></span>

## <span data-ttu-id="99e9c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99e9c-131">OUTPUTS</span></span>

## <span data-ttu-id="99e9c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99e9c-132">NOTES</span></span>

## <span data-ttu-id="99e9c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99e9c-133">RELATED LINKS</span></span>

[<span data-ttu-id="99e9c-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="99e9c-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="99e9c-135">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="99e9c-135">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


