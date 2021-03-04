---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 4d956dfd49e541751003d28c31285722616ab640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891244"
---
# <span data-ttu-id="545a2-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="545a2-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="545a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545a2-102">SYNOPSIS</span></span>
<span data-ttu-id="545a2-103">Obtém propriedades de registro em log para serviços de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="545a2-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="545a2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="545a2-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="545a2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="545a2-105">DESCRIPTION</span></span>
<span data-ttu-id="545a2-106">O cmdlet **Get-AzStorageServiceLoggingProperty** obtém propriedades de registro em log para os serviços de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="545a2-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="545a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="545a2-107">EXAMPLES</span></span>

### <span data-ttu-id="545a2-108">Exemplo 1: obter propriedades de registro em log para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="545a2-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="545a2-109">Este comando obtém propriedades de registro em log para armazenamento de blob.</span><span class="sxs-lookup"><span data-stu-id="545a2-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="545a2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="545a2-110">PARAMETERS</span></span>

### <span data-ttu-id="545a2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="545a2-111">-Context</span></span>
<span data-ttu-id="545a2-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="545a2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="545a2-113">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="545a2-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="545a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545a2-114">-DefaultProfile</span></span>
<span data-ttu-id="545a2-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="545a2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="545a2-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="545a2-116">-ServiceType</span></span>
<span data-ttu-id="545a2-117">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="545a2-117">Specifies the storage service type.</span></span>
<span data-ttu-id="545a2-118">Este cmdlet obtém as propriedades de registro em log para o tipo de serviço especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="545a2-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="545a2-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="545a2-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="545a2-120">Blob</span><span class="sxs-lookup"><span data-stu-id="545a2-120">Blob</span></span> 
- <span data-ttu-id="545a2-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="545a2-121">Table</span></span>
- <span data-ttu-id="545a2-122">Fila</span><span class="sxs-lookup"><span data-stu-id="545a2-122">Queue</span></span>
- <span data-ttu-id="545a2-123">Arquivo O valor de File não é suportado no momento.</span><span class="sxs-lookup"><span data-stu-id="545a2-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="545a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545a2-124">CommonParameters</span></span>
<span data-ttu-id="545a2-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="545a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545a2-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="545a2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545a2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="545a2-127">INPUTS</span></span>

### <span data-ttu-id="545a2-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="545a2-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="545a2-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="545a2-129">OUTPUTS</span></span>

### <span data-ttu-id="545a2-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="545a2-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="545a2-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="545a2-131">NOTES</span></span>

## <span data-ttu-id="545a2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="545a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="545a2-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="545a2-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="545a2-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="545a2-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


