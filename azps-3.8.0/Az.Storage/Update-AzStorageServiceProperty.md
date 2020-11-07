---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942452"
---
# <span data-ttu-id="915cc-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="915cc-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="915cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="915cc-102">SYNOPSIS</span></span>
<span data-ttu-id="915cc-103">Modifica as propriedades do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="915cc-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="915cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="915cc-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="915cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="915cc-105">DESCRIPTION</span></span>
<span data-ttu-id="915cc-106">O cmdlet **Update-AzStorageServiceProperty** modifica as propriedades do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="915cc-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="915cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="915cc-107">EXAMPLES</span></span>

### <span data-ttu-id="915cc-108">Exemplo 1: definir o serviço de blob DefaultServiceVersion para 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="915cc-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="915cc-109">Este comando define o DefaultServiceVersion do serviço de blob como 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="915cc-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="915cc-110">OS</span><span class="sxs-lookup"><span data-stu-id="915cc-110">PARAMETERS</span></span>

### <span data-ttu-id="915cc-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="915cc-111">-Context</span></span>
<span data-ttu-id="915cc-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="915cc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="915cc-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="915cc-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="915cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="915cc-114">-DefaultProfile</span></span>
<span data-ttu-id="915cc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="915cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="915cc-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="915cc-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="915cc-117">DefaultServiceVersion indica a versão padrão a ser usada nas solicitações para o serviço BLOB se a versão de uma solicitação recebida não for especificada.</span><span class="sxs-lookup"><span data-stu-id="915cc-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="915cc-118">Os valores possíveis incluem a versão 2008-10-27 e todas as versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="915cc-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="915cc-119">Veja mais detalhes em https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="915cc-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="915cc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="915cc-120">-PassThru</span></span>
<span data-ttu-id="915cc-121">Display Serviceproperties</span><span class="sxs-lookup"><span data-stu-id="915cc-121">Display ServiceProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="915cc-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="915cc-122">-ServiceType</span></span>
<span data-ttu-id="915cc-123">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="915cc-123">Specifies the storage service type.</span></span>
<span data-ttu-id="915cc-124">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="915cc-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="915cc-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="915cc-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="915cc-126">Irregular</span><span class="sxs-lookup"><span data-stu-id="915cc-126">Blob</span></span> 
- <span data-ttu-id="915cc-127">TableName</span><span class="sxs-lookup"><span data-stu-id="915cc-127">Table</span></span>
- <span data-ttu-id="915cc-128">Coloca</span><span class="sxs-lookup"><span data-stu-id="915cc-128">Queue</span></span>
- <span data-ttu-id="915cc-129">Arquivos</span><span class="sxs-lookup"><span data-stu-id="915cc-129">File</span></span>

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

### <span data-ttu-id="915cc-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="915cc-130">-Confirm</span></span>
<span data-ttu-id="915cc-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="915cc-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="915cc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="915cc-132">-WhatIf</span></span>
<span data-ttu-id="915cc-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="915cc-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="915cc-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="915cc-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="915cc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915cc-135">CommonParameters</span></span>
<span data-ttu-id="915cc-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="915cc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915cc-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="915cc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915cc-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="915cc-138">INPUTS</span></span>

### <span data-ttu-id="915cc-139">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="915cc-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="915cc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="915cc-140">OUTPUTS</span></span>

### <span data-ttu-id="915cc-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="915cc-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="915cc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="915cc-142">NOTES</span></span>

## <span data-ttu-id="915cc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="915cc-143">RELATED LINKS</span></span>
