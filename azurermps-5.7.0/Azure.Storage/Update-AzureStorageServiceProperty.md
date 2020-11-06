---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: 7036f12b4ab47043b69fe4164ac567f4355a51ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432989"
---
# <span data-ttu-id="350de-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="350de-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="350de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="350de-102">SYNOPSIS</span></span>
<span data-ttu-id="350de-103">Modifica as propriedades do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="350de-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="350de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="350de-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="350de-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="350de-105">DESCRIPTION</span></span>
<span data-ttu-id="350de-106">O cmdlet **Update-AzureStorageServiceProperty** modifica as propriedades do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="350de-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="350de-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="350de-107">EXAMPLES</span></span>

### <span data-ttu-id="350de-108">Exemplo 1: definir o serviço de blob DefaultServiceVersion para 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="350de-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="350de-109">Este comando define o DefaultServiceVersion do serviço de blob como 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="350de-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="350de-110">OS</span><span class="sxs-lookup"><span data-stu-id="350de-110">PARAMETERS</span></span>

### <span data-ttu-id="350de-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="350de-111">-Context</span></span>
<span data-ttu-id="350de-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="350de-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="350de-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="350de-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="350de-114">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="350de-114">-DefaultServiceVersion</span></span>
<span data-ttu-id="350de-115">DefaultServiceVersion indica a versão padrão a ser usada nas solicitações para o serviço BLOB se a versão de uma solicitação recebida não for especificada.</span><span class="sxs-lookup"><span data-stu-id="350de-115">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="350de-116">Os valores possíveis incluem a versão 2008-10-27 e todas as versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="350de-116">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="350de-117">Veja mais detalhes em https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="350de-117">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="350de-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="350de-118">-PassThru</span></span>
<span data-ttu-id="350de-119">Display Serviceproperties</span><span class="sxs-lookup"><span data-stu-id="350de-119">Display ServiceProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="350de-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="350de-120">-ServiceType</span></span>
<span data-ttu-id="350de-121">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="350de-121">Specifies the storage service type.</span></span>
<span data-ttu-id="350de-122">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="350de-122">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="350de-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="350de-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="350de-124">Irregular</span><span class="sxs-lookup"><span data-stu-id="350de-124">Blob</span></span> 
- <span data-ttu-id="350de-125">TableName</span><span class="sxs-lookup"><span data-stu-id="350de-125">Table</span></span>
- <span data-ttu-id="350de-126">Coloca</span><span class="sxs-lookup"><span data-stu-id="350de-126">Queue</span></span>
- <span data-ttu-id="350de-127">Arquivos</span><span class="sxs-lookup"><span data-stu-id="350de-127">File</span></span>

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

### <span data-ttu-id="350de-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="350de-128">-Confirm</span></span>
<span data-ttu-id="350de-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="350de-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="350de-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="350de-130">-WhatIf</span></span>
<span data-ttu-id="350de-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="350de-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="350de-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="350de-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="350de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350de-133">CommonParameters</span></span>
<span data-ttu-id="350de-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="350de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350de-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="350de-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350de-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="350de-136">INPUTS</span></span>

### <span data-ttu-id="350de-137">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="350de-137">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="350de-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="350de-138">OUTPUTS</span></span>

### <span data-ttu-id="350de-139">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="350de-139">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="350de-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="350de-140">NOTES</span></span>

## <span data-ttu-id="350de-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="350de-141">RELATED LINKS</span></span>

