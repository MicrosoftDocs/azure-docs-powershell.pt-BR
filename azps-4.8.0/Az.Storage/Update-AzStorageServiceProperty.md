---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110758"
---
# <span data-ttu-id="ca298-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ca298-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="ca298-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca298-102">SYNOPSIS</span></span>
<span data-ttu-id="ca298-103">Modifica as propriedades do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca298-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ca298-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca298-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca298-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca298-105">DESCRIPTION</span></span>
<span data-ttu-id="ca298-106">O cmdlet **Update-AzStorageServiceProperty** modifica as propriedades do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca298-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ca298-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca298-107">EXAMPLES</span></span>

### <span data-ttu-id="ca298-108">Exemplo 1: definir o serviço de blob DefaultServiceVersion para 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="ca298-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="ca298-109">Este comando define o DefaultServiceVersion do serviço de blob como 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="ca298-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="ca298-110">OS</span><span class="sxs-lookup"><span data-stu-id="ca298-110">PARAMETERS</span></span>

### <span data-ttu-id="ca298-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ca298-111">-Context</span></span>
<span data-ttu-id="ca298-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca298-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ca298-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ca298-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ca298-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca298-114">-DefaultProfile</span></span>
<span data-ttu-id="ca298-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca298-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca298-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="ca298-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="ca298-117">DefaultServiceVersion indica a versão padrão a ser usada nas solicitações para o serviço BLOB se a versão de uma solicitação recebida não for especificada.</span><span class="sxs-lookup"><span data-stu-id="ca298-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="ca298-118">Os valores possíveis incluem a versão 2008-10-27 e todas as versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="ca298-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="ca298-119">Veja mais detalhes em https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="ca298-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="ca298-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca298-120">-PassThru</span></span>
<span data-ttu-id="ca298-121">Display Serviceproperties</span><span class="sxs-lookup"><span data-stu-id="ca298-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="ca298-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ca298-122">-ServiceType</span></span>
<span data-ttu-id="ca298-123">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ca298-123">Specifies the storage service type.</span></span>
<span data-ttu-id="ca298-124">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca298-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ca298-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ca298-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca298-126">Irregular</span><span class="sxs-lookup"><span data-stu-id="ca298-126">Blob</span></span> 
- <span data-ttu-id="ca298-127">TableName</span><span class="sxs-lookup"><span data-stu-id="ca298-127">Table</span></span>
- <span data-ttu-id="ca298-128">Coloca</span><span class="sxs-lookup"><span data-stu-id="ca298-128">Queue</span></span>
- <span data-ttu-id="ca298-129">Arquivos</span><span class="sxs-lookup"><span data-stu-id="ca298-129">File</span></span>

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

### <span data-ttu-id="ca298-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca298-130">-Confirm</span></span>
<span data-ttu-id="ca298-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca298-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca298-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca298-132">-WhatIf</span></span>
<span data-ttu-id="ca298-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca298-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca298-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca298-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca298-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca298-135">CommonParameters</span></span>
<span data-ttu-id="ca298-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca298-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca298-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca298-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca298-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca298-138">INPUTS</span></span>

### <span data-ttu-id="ca298-139">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca298-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca298-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca298-140">OUTPUTS</span></span>

### <span data-ttu-id="ca298-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="ca298-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="ca298-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca298-142">NOTES</span></span>

## <span data-ttu-id="ca298-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca298-143">RELATED LINKS</span></span>
