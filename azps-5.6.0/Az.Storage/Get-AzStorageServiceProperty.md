---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: eff94aac5ac9a1a71a12f31be81a1eb4c89bf73b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889059"
---
# <span data-ttu-id="b83d1-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b83d1-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="b83d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b83d1-102">SYNOPSIS</span></span>
<span data-ttu-id="b83d1-103">Obtém propriedades para os serviços de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b83d1-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="b83d1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b83d1-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b83d1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b83d1-105">DESCRIPTION</span></span>
<span data-ttu-id="b83d1-106">O cmdlet **Get-AzStorageServiceProperty** obtém as propriedades dos serviços de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b83d1-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="b83d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b83d1-107">EXAMPLES</span></span>

### <span data-ttu-id="b83d1-108">Exemplo 1: Obter a propriedade serviços de Armazenamento do Azure do serviço Blob</span><span class="sxs-lookup"><span data-stu-id="b83d1-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="b83d1-109">Este comando obtém a propriedade DefaultServiceVersion do serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="b83d1-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="b83d1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b83d1-110">PARAMETERS</span></span>

### <span data-ttu-id="b83d1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b83d1-111">-Context</span></span>
<span data-ttu-id="b83d1-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b83d1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b83d1-113">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b83d1-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b83d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83d1-114">-DefaultProfile</span></span>
<span data-ttu-id="b83d1-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b83d1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b83d1-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b83d1-116">-ServiceType</span></span>
<span data-ttu-id="b83d1-117">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b83d1-117">Specifies the storage service type.</span></span>
<span data-ttu-id="b83d1-118">Este cmdlet obtém as propriedades de registro em log para o tipo de serviço especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b83d1-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="b83d1-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b83d1-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b83d1-120">Blob</span><span class="sxs-lookup"><span data-stu-id="b83d1-120">Blob</span></span> 
- <span data-ttu-id="b83d1-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="b83d1-121">Table</span></span>
- <span data-ttu-id="b83d1-122">Fila</span><span class="sxs-lookup"><span data-stu-id="b83d1-122">Queue</span></span>
- <span data-ttu-id="b83d1-123">Arquivo</span><span class="sxs-lookup"><span data-stu-id="b83d1-123">File</span></span>

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

### <span data-ttu-id="b83d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83d1-124">CommonParameters</span></span>
<span data-ttu-id="b83d1-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b83d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83d1-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b83d1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83d1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b83d1-127">INPUTS</span></span>

### <span data-ttu-id="b83d1-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b83d1-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b83d1-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b83d1-129">OUTPUTS</span></span>

### <span data-ttu-id="b83d1-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="b83d1-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="b83d1-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="b83d1-131">NOTES</span></span>

## <span data-ttu-id="b83d1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b83d1-132">RELATED LINKS</span></span>
