---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 7bca28da7b4729a414fafc5268bc4e0e02ee3c72
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776251"
---
# <span data-ttu-id="ee7cd-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ee7cd-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="ee7cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7cd-103">Obtém as propriedades de métricas para o serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ee7cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee7cd-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee7cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee7cd-105">DESCRIPTION</span></span>
<span data-ttu-id="ee7cd-106">O cmdlet **Get-AzStorageServiceMetricsProperty** Obtém as propriedades Metrics do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ee7cd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee7cd-107">EXAMPLES</span></span>

### <span data-ttu-id="ee7cd-108">Exemplo 1: obter as propriedades de métricas do serviço blob</span><span class="sxs-lookup"><span data-stu-id="ee7cd-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="ee7cd-109">Esse comando obtém as propriedades Metrics do armazenamento de BLOB para o tipo métricas de hora.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="ee7cd-110">OS</span><span class="sxs-lookup"><span data-stu-id="ee7cd-110">PARAMETERS</span></span>

### <span data-ttu-id="ee7cd-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ee7cd-111">-Context</span></span>
<span data-ttu-id="ee7cd-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ee7cd-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ee7cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee7cd-114">-DefaultProfile</span></span>
<span data-ttu-id="ee7cd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee7cd-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="ee7cd-116">-MetricsType</span></span>
<span data-ttu-id="ee7cd-117">Especifica um tipo de métrica.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-117">Specifies a metrics type.</span></span>
<span data-ttu-id="ee7cd-118">Este cmdlet obtém as propriedades de métricas do serviço de armazenamento do Azure para o tipo de métricas que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="ee7cd-119">Os valores aceitáveis para esse parâmetro são: Hour e minute.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7cd-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ee7cd-120">-ServiceType</span></span>
<span data-ttu-id="ee7cd-121">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-121">Specifies the storage service type.</span></span>
<span data-ttu-id="ee7cd-122">Esse cmdlet obtém as propriedades de métricas do tipo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="ee7cd-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ee7cd-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee7cd-124">Irregular</span><span class="sxs-lookup"><span data-stu-id="ee7cd-124">Blob</span></span> 
- <span data-ttu-id="ee7cd-125">TableName</span><span class="sxs-lookup"><span data-stu-id="ee7cd-125">Table</span></span>
- <span data-ttu-id="ee7cd-126">Coloca</span><span class="sxs-lookup"><span data-stu-id="ee7cd-126">Queue</span></span>
- <span data-ttu-id="ee7cd-127">Arquivo no momento, não há suporte para o valor do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ee7cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7cd-128">CommonParameters</span></span>
<span data-ttu-id="ee7cd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee7cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7cd-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee7cd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7cd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee7cd-131">INPUTS</span></span>

### <span data-ttu-id="ee7cd-132">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee7cd-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ee7cd-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee7cd-133">OUTPUTS</span></span>

### <span data-ttu-id="ee7cd-134">Microsoft. WindowsAz. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="ee7cd-134">Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="ee7cd-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee7cd-135">NOTES</span></span>

## <span data-ttu-id="ee7cd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee7cd-136">RELATED LINKS</span></span>

[<span data-ttu-id="ee7cd-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee7cd-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ee7cd-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ee7cd-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


