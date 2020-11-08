---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116343"
---
# <span data-ttu-id="3b895-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3b895-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="3b895-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b895-102">SYNOPSIS</span></span>
<span data-ttu-id="3b895-103">Obtém Propriedades de registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b895-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="3b895-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b895-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b895-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b895-105">DESCRIPTION</span></span>
<span data-ttu-id="3b895-106">O cmdlet **Get-AzStorageServiceLoggingProperty** Obtém Propriedades de log para os serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b895-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="3b895-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b895-107">EXAMPLES</span></span>

### <span data-ttu-id="3b895-108">Exemplo 1: obter propriedades de log para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="3b895-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="3b895-109">Este comando obtém Propriedades de log para armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="3b895-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="3b895-110">OS</span><span class="sxs-lookup"><span data-stu-id="3b895-110">PARAMETERS</span></span>

### <span data-ttu-id="3b895-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3b895-111">-Context</span></span>
<span data-ttu-id="3b895-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b895-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3b895-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3b895-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3b895-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b895-114">-DefaultProfile</span></span>
<span data-ttu-id="3b895-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b895-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b895-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="3b895-116">-ServiceType</span></span>
<span data-ttu-id="3b895-117">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3b895-117">Specifies the storage service type.</span></span>
<span data-ttu-id="3b895-118">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="3b895-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="3b895-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3b895-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3b895-120">Irregular</span><span class="sxs-lookup"><span data-stu-id="3b895-120">Blob</span></span> 
- <span data-ttu-id="3b895-121">TableName</span><span class="sxs-lookup"><span data-stu-id="3b895-121">Table</span></span>
- <span data-ttu-id="3b895-122">Coloca</span><span class="sxs-lookup"><span data-stu-id="3b895-122">Queue</span></span>
- <span data-ttu-id="3b895-123">Arquivo no momento, não há suporte para o valor do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3b895-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="3b895-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b895-124">CommonParameters</span></span>
<span data-ttu-id="3b895-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b895-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b895-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b895-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b895-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b895-127">INPUTS</span></span>

### <span data-ttu-id="3b895-128">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b895-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3b895-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b895-129">OUTPUTS</span></span>

### <span data-ttu-id="3b895-130">Microsoft. Azure. Storage. Shared. Protocol. Loggingproperties</span><span class="sxs-lookup"><span data-stu-id="3b895-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="3b895-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b895-131">NOTES</span></span>

## <span data-ttu-id="3b895-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b895-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b895-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b895-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3b895-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3b895-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


