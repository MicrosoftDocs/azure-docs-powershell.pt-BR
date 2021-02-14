---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110870"
---
# <span data-ttu-id="38d9a-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="38d9a-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="38d9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="38d9a-103">Obtém propriedades de registro em log para os serviços de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="38d9a-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="38d9a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38d9a-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38d9a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="38d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="38d9a-106">O cmdlet **Get-AzStorageServiceLoggingProperty** obtém propriedades de log para os serviços de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="38d9a-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="38d9a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="38d9a-108">Exemplo 1: Obter propriedades de registro em log para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="38d9a-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="38d9a-109">Esse comando obtém propriedades de registro em log para armazenamento de blob.</span><span class="sxs-lookup"><span data-stu-id="38d9a-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="38d9a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38d9a-110">PARAMETERS</span></span>

### <span data-ttu-id="38d9a-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="38d9a-111">-Context</span></span>
<span data-ttu-id="38d9a-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="38d9a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="38d9a-113">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38d9a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="38d9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d9a-114">-DefaultProfile</span></span>
<span data-ttu-id="38d9a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38d9a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d9a-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="38d9a-116">-ServiceType</span></span>
<span data-ttu-id="38d9a-117">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="38d9a-117">Specifies the storage service type.</span></span>
<span data-ttu-id="38d9a-118">Este cmdlet obtém as propriedades de registro em log para o tipo de serviço especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="38d9a-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="38d9a-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="38d9a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38d9a-120">Blob</span><span class="sxs-lookup"><span data-stu-id="38d9a-120">Blob</span></span> 
- <span data-ttu-id="38d9a-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="38d9a-121">Table</span></span>
- <span data-ttu-id="38d9a-122">Fila</span><span class="sxs-lookup"><span data-stu-id="38d9a-122">Queue</span></span>
- <span data-ttu-id="38d9a-123">Arquivo O valor do Arquivo não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="38d9a-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="38d9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d9a-124">CommonParameters</span></span>
<span data-ttu-id="38d9a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d9a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d9a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d9a-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="38d9a-127">INPUTS</span></span>

### <span data-ttu-id="38d9a-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="38d9a-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="38d9a-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="38d9a-129">OUTPUTS</span></span>

### <span data-ttu-id="38d9a-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="38d9a-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="38d9a-131">Notas</span><span class="sxs-lookup"><span data-stu-id="38d9a-131">NOTES</span></span>

## <span data-ttu-id="38d9a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38d9a-132">RELATED LINKS</span></span>

[<span data-ttu-id="38d9a-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="38d9a-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="38d9a-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="38d9a-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


