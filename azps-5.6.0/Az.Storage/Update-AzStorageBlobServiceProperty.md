---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 46fff0df9eddc417f823aa7b0243824befb974e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888046"
---
# <span data-ttu-id="1d8a6-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1d8a6-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="1d8a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8a6-103">Modifica as propriedades de serviço do serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="1d8a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1d8a6-104">SYNTAX</span></span>

### <span data-ttu-id="1d8a6-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1d8a6-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8a6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1d8a6-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8a6-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="1d8a6-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d8a6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1d8a6-108">DESCRIPTION</span></span>
<span data-ttu-id="1d8a6-109">O cmdlet **Update-AzStorageBlobServiceProperty** modifica as propriedades de serviço do serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="1d8a6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d8a6-110">EXAMPLES</span></span>

### <span data-ttu-id="1d8a6-111">Exemplo 1: Definir o serviço Blob DefaultServiceVersion como 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="1d8a6-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="1d8a6-112">Este comando define DefaultServiceVersion of Blob Service como 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="1d8a6-113">Exemplo 2: Habilitar Changefeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1d8a6-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="1d8a6-114">Este comando habilita o serviço Changefeed on Blob de um suporte de feed de alteração de conta de armazenamento no Armazenamento de Blob do Azure funciona escutando uma conta de armazenamento GPv2 ou Blob para qualquer evento de criação, modificação ou exclusão de nível de blob.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="1d8a6-115">Em seguida, ele faz um log ordenado de eventos para os blobs armazenados no contêiner $blobchangefeed dentro da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="1d8a6-116">As alterações serializadas são persistentes como um arquivo Avro apache e podem ser processadas de forma assíncrona e incremental.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="1d8a6-117">Exemplo 3: Habilitar o versioning no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1d8a6-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="1d8a6-118">Este comando habilita o controle de versão no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1d8a6-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="1d8a6-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1d8a6-119">PARAMETERS</span></span>

### <span data-ttu-id="1d8a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8a6-120">-DefaultProfile</span></span>
<span data-ttu-id="1d8a6-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8a6-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="1d8a6-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="1d8a6-123">Versão padrão do serviço a ser definida</span><span class="sxs-lookup"><span data-stu-id="1d8a6-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="1d8a6-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="1d8a6-124">-EnableChangeFeed</span></span>
<span data-ttu-id="1d8a6-125">Habilitar o registro em log alterar feed para a conta de armazenamento definindo como $true, desabilite o registro em log alterar feed definindo como $false.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8a6-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="1d8a6-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="1d8a6-127">Obtém ou define o versioning é habilitado se definido como true.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8a6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8a6-128">-ResourceGroupName</span></span>
<span data-ttu-id="1d8a6-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8a6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d8a6-130">-ResourceId</span></span>
<span data-ttu-id="1d8a6-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8a6-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d8a6-132">-StorageAccount</span></span>
<span data-ttu-id="1d8a6-133">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1d8a6-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8a6-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1d8a6-134">-StorageAccountName</span></span>
<span data-ttu-id="1d8a6-135">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d8a6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d8a6-136">-Confirm</span></span>
<span data-ttu-id="1d8a6-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d8a6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8a6-138">-WhatIf</span></span>
<span data-ttu-id="1d8a6-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8a6-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d8a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8a6-141">CommonParameters</span></span>
<span data-ttu-id="1d8a6-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d8a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8a6-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d8a6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8a6-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d8a6-144">INPUTS</span></span>

### <span data-ttu-id="1d8a6-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d8a6-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1d8a6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1d8a6-146">System.String</span></span>

## <span data-ttu-id="1d8a6-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1d8a6-147">OUTPUTS</span></span>

### <span data-ttu-id="1d8a6-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="1d8a6-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="1d8a6-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="1d8a6-149">NOTES</span></span>

## <span data-ttu-id="1d8a6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d8a6-150">RELATED LINKS</span></span>
