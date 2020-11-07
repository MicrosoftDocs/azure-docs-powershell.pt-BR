---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: dc7f579366956f8447ba64fc898e97f5c33b70f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774038"
---
# <span data-ttu-id="e5a23-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e5a23-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="e5a23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5a23-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a23-103">Modifica as propriedades do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a23-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="e5a23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5a23-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5a23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5a23-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a23-106">O cmdlet **Update-AzStorageServiceProperty** modifica as propriedades do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a23-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="e5a23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5a23-107">EXAMPLES</span></span>

### <span data-ttu-id="e5a23-108">Exemplo 1: definir o serviço de blob DefaultServiceVersion para 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="e5a23-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="e5a23-109">Este comando define o DefaultServiceVersion do serviço de blob como 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="e5a23-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="e5a23-110">OS</span><span class="sxs-lookup"><span data-stu-id="e5a23-110">PARAMETERS</span></span>

### <span data-ttu-id="e5a23-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e5a23-111">-Context</span></span>
<span data-ttu-id="e5a23-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a23-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e5a23-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e5a23-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e5a23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a23-114">-DefaultProfile</span></span>
<span data-ttu-id="e5a23-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5a23-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="e5a23-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="e5a23-117">DefaultServiceVersion indica a versão padrão a ser usada nas solicitações para o serviço BLOB se a versão de uma solicitação recebida não for especificada.</span><span class="sxs-lookup"><span data-stu-id="e5a23-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="e5a23-118">Os valores possíveis incluem a versão 2008-10-27 e todas as versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="e5a23-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="e5a23-119">Veja mais detalhes em https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="e5a23-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="e5a23-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5a23-120">-PassThru</span></span>
<span data-ttu-id="e5a23-121">Display Serviceproperties</span><span class="sxs-lookup"><span data-stu-id="e5a23-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="e5a23-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e5a23-122">-ServiceType</span></span>
<span data-ttu-id="e5a23-123">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5a23-123">Specifies the storage service type.</span></span>
<span data-ttu-id="e5a23-124">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e5a23-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="e5a23-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e5a23-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5a23-126">Irregular</span><span class="sxs-lookup"><span data-stu-id="e5a23-126">Blob</span></span> 
- <span data-ttu-id="e5a23-127">TableName</span><span class="sxs-lookup"><span data-stu-id="e5a23-127">Table</span></span>
- <span data-ttu-id="e5a23-128">Coloca</span><span class="sxs-lookup"><span data-stu-id="e5a23-128">Queue</span></span>
- <span data-ttu-id="e5a23-129">Arquivos</span><span class="sxs-lookup"><span data-stu-id="e5a23-129">File</span></span>

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

### <span data-ttu-id="e5a23-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e5a23-130">-Confirm</span></span>
<span data-ttu-id="e5a23-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a23-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a23-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a23-132">-WhatIf</span></span>
<span data-ttu-id="e5a23-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5a23-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5a23-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5a23-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a23-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a23-135">CommonParameters</span></span>
<span data-ttu-id="e5a23-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a23-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a23-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a23-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a23-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5a23-138">INPUTS</span></span>

### <span data-ttu-id="e5a23-139">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5a23-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e5a23-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5a23-140">OUTPUTS</span></span>

### <span data-ttu-id="e5a23-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="e5a23-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="e5a23-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5a23-142">NOTES</span></span>

## <span data-ttu-id="e5a23-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5a23-143">RELATED LINKS</span></span>
