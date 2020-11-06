---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: a36b1f13f08cd94339f9791512d764a872019672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431524"
---
# <span data-ttu-id="12a80-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="12a80-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="12a80-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12a80-102">SYNOPSIS</span></span>
<span data-ttu-id="12a80-103">Obtém as propriedades dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12a80-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12a80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12a80-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a80-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12a80-105">DESCRIPTION</span></span>
<span data-ttu-id="12a80-106">O cmdlet **Get-AzureStorageServiceProperty** Obtém as propriedades dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12a80-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="12a80-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12a80-107">EXAMPLES</span></span>

### <span data-ttu-id="12a80-108">Exemplo 1: obter a propriedade de serviços de armazenamento do Azure do serviço blob</span><span class="sxs-lookup"><span data-stu-id="12a80-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29
```

<span data-ttu-id="12a80-109">Esse comando obtém a propriedade DefaultServiceVersion do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="12a80-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="12a80-110">OS</span><span class="sxs-lookup"><span data-stu-id="12a80-110">PARAMETERS</span></span>

### <span data-ttu-id="12a80-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="12a80-111">-Context</span></span>
<span data-ttu-id="12a80-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12a80-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="12a80-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="12a80-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="12a80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a80-114">-DefaultProfile</span></span>
<span data-ttu-id="12a80-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12a80-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12a80-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="12a80-116">-ServiceType</span></span>
<span data-ttu-id="12a80-117">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12a80-117">Specifies the storage service type.</span></span>
<span data-ttu-id="12a80-118">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="12a80-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="12a80-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="12a80-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="12a80-120">Irregular</span><span class="sxs-lookup"><span data-stu-id="12a80-120">Blob</span></span> 
- <span data-ttu-id="12a80-121">TableName</span><span class="sxs-lookup"><span data-stu-id="12a80-121">Table</span></span>
- <span data-ttu-id="12a80-122">Coloca</span><span class="sxs-lookup"><span data-stu-id="12a80-122">Queue</span></span>
- <span data-ttu-id="12a80-123">Arquivos</span><span class="sxs-lookup"><span data-stu-id="12a80-123">File</span></span>

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

### <span data-ttu-id="12a80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a80-124">CommonParameters</span></span>
<span data-ttu-id="12a80-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a80-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a80-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a80-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12a80-127">INPUTS</span></span>

### <span data-ttu-id="12a80-128">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="12a80-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="12a80-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12a80-129">OUTPUTS</span></span>

### <span data-ttu-id="12a80-130">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="12a80-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="12a80-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12a80-131">NOTES</span></span>

## <span data-ttu-id="12a80-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12a80-132">RELATED LINKS</span></span>
