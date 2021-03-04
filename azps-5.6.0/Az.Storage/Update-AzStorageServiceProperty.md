---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: 952f66bfffef4d8f7636098a8280cd26b6fc7f5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888037"
---
# <span data-ttu-id="dc3b3-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dc3b3-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="dc3b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3b3-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3b3-103">Modifica as propriedades do serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="dc3b3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dc3b3-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc3b3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dc3b3-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3b3-106">O cmdlet **Update-AzStorageServiceProperty** modifica as propriedades do serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="dc3b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc3b3-107">EXAMPLES</span></span>

### <span data-ttu-id="dc3b3-108">Exemplo 1: Definir DefaultServiceVersion do serviço blob como 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="dc3b3-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="dc3b3-109">Este comando Definir o DefaultServiceVersion do Serviço blob como 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="dc3b3-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="dc3b3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dc3b3-110">PARAMETERS</span></span>

### <span data-ttu-id="dc3b3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="dc3b3-111">-Context</span></span>
<span data-ttu-id="dc3b3-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dc3b3-113">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="dc3b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3b3-114">-DefaultProfile</span></span>
<span data-ttu-id="dc3b3-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc3b3-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="dc3b3-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="dc3b3-117">DefaultServiceVersion indica a versão padrão a ser usada para solicitações ao serviço Blob se a versão de uma solicitação de entrada não for especificada.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="dc3b3-118">Os valores possíveis incluem a versão 2008-10-27 e todas as versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="dc3b3-119">Confira mais detalhes em https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="dc3b3-119">See more details in https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="dc3b3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc3b3-120">-PassThru</span></span>
<span data-ttu-id="dc3b3-121">Exibir ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="dc3b3-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="dc3b3-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="dc3b3-122">-ServiceType</span></span>
<span data-ttu-id="dc3b3-123">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-123">Specifies the storage service type.</span></span>
<span data-ttu-id="dc3b3-124">Este cmdlet obtém as propriedades de registro em log para o tipo de serviço especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="dc3b3-125">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dc3b3-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dc3b3-126">Blob</span><span class="sxs-lookup"><span data-stu-id="dc3b3-126">Blob</span></span> 
- <span data-ttu-id="dc3b3-127">Tabela</span><span class="sxs-lookup"><span data-stu-id="dc3b3-127">Table</span></span>
- <span data-ttu-id="dc3b3-128">Fila</span><span class="sxs-lookup"><span data-stu-id="dc3b3-128">Queue</span></span>
- <span data-ttu-id="dc3b3-129">Arquivo</span><span class="sxs-lookup"><span data-stu-id="dc3b3-129">File</span></span>

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

### <span data-ttu-id="dc3b3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc3b3-130">-Confirm</span></span>
<span data-ttu-id="dc3b3-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc3b3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc3b3-132">-WhatIf</span></span>
<span data-ttu-id="dc3b3-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc3b3-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc3b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3b3-135">CommonParameters</span></span>
<span data-ttu-id="dc3b3-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3b3-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3b3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3b3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc3b3-138">INPUTS</span></span>

### <span data-ttu-id="dc3b3-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dc3b3-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dc3b3-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dc3b3-140">OUTPUTS</span></span>

### <span data-ttu-id="dc3b3-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="dc3b3-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="dc3b3-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="dc3b3-142">NOTES</span></span>

## <span data-ttu-id="dc3b3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc3b3-143">RELATED LINKS</span></span>
