---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: 6b7944f96eb3ccc67322593d9056b39e83ee9010
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776250"
---
# <span data-ttu-id="10630-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="10630-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="10630-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10630-102">SYNOPSIS</span></span>
<span data-ttu-id="10630-103">Obtém as propriedades dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="10630-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="10630-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10630-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10630-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10630-105">DESCRIPTION</span></span>
<span data-ttu-id="10630-106">O cmdlet **Get-AzStorageServiceProperty** Obtém as propriedades dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="10630-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="10630-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10630-107">EXAMPLES</span></span>

### <span data-ttu-id="10630-108">Exemplo 1: obter a propriedade de serviços de armazenamento do Azure do serviço blob</span><span class="sxs-lookup"><span data-stu-id="10630-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="10630-109">Esse comando obtém a propriedade DefaultServiceVersion do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="10630-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="10630-110">OS</span><span class="sxs-lookup"><span data-stu-id="10630-110">PARAMETERS</span></span>

### <span data-ttu-id="10630-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="10630-111">-Context</span></span>
<span data-ttu-id="10630-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="10630-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="10630-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="10630-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="10630-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10630-114">-DefaultProfile</span></span>
<span data-ttu-id="10630-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10630-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10630-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="10630-116">-ServiceType</span></span>
<span data-ttu-id="10630-117">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10630-117">Specifies the storage service type.</span></span>
<span data-ttu-id="10630-118">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="10630-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="10630-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="10630-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10630-120">Irregular</span><span class="sxs-lookup"><span data-stu-id="10630-120">Blob</span></span> 
- <span data-ttu-id="10630-121">TableName</span><span class="sxs-lookup"><span data-stu-id="10630-121">Table</span></span>
- <span data-ttu-id="10630-122">Coloca</span><span class="sxs-lookup"><span data-stu-id="10630-122">Queue</span></span>
- <span data-ttu-id="10630-123">Arquivos</span><span class="sxs-lookup"><span data-stu-id="10630-123">File</span></span>

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

### <span data-ttu-id="10630-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10630-124">CommonParameters</span></span>
<span data-ttu-id="10630-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10630-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10630-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10630-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10630-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10630-127">INPUTS</span></span>

### <span data-ttu-id="10630-128">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="10630-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="10630-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10630-129">OUTPUTS</span></span>

### <span data-ttu-id="10630-130">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="10630-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="10630-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10630-131">NOTES</span></span>

## <span data-ttu-id="10630-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10630-132">RELATED LINKS</span></span>
