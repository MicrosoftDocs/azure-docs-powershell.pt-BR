---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110759"
---
# <span data-ttu-id="32b89-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="32b89-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="32b89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32b89-102">SYNOPSIS</span></span>
<span data-ttu-id="32b89-103">Modifica as propriedades do serviço do serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="32b89-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="32b89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32b89-104">SYNTAX</span></span>

### <span data-ttu-id="32b89-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="32b89-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b89-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="32b89-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b89-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="32b89-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32b89-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32b89-108">DESCRIPTION</span></span>
<span data-ttu-id="32b89-109">O cmdlet **Update-AzStorageBlobServiceProperty** modifica as propriedades do serviço do serviço de blob do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="32b89-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="32b89-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32b89-110">EXAMPLES</span></span>

### <span data-ttu-id="32b89-111">Exemplo 1: definir o serviço de blob DefaultServiceVersion para 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="32b89-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
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

<span data-ttu-id="32b89-112">Esse comando define o DefaultServiceVersion do serviço de BLOB para 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="32b89-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="32b89-113">Exemplo 2: habilitar o changefeed no serviço blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="32b89-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
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

<span data-ttu-id="32b89-114">Esse comando habilita o changefeed no serviço blob de um feed de alteração de conta de armazenamento no Azure Blob Storage funciona ouvindo uma conta de armazenamento de GPv2 ou BLOB para qualquer evento de criação, modificação ou exclusão em nível de BLOB.</span><span class="sxs-lookup"><span data-stu-id="32b89-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="32b89-115">Em seguida, ele emite um log ordenado de eventos para os BLOBs armazenados no contêiner $blobchangefeed dentro da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="32b89-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="32b89-116">As alterações serializadas são mantidas como um arquivo Apache Avro e podem ser processadas de forma assíncrona e incremental.</span><span class="sxs-lookup"><span data-stu-id="32b89-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="32b89-117">Exemplo 3: habilitar o controle de versão no serviço blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="32b89-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
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

<span data-ttu-id="32b89-118">Este comando habilita o controle de versão no serviço blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="32b89-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="32b89-119">OS</span><span class="sxs-lookup"><span data-stu-id="32b89-119">PARAMETERS</span></span>

### <span data-ttu-id="32b89-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b89-120">-DefaultProfile</span></span>
<span data-ttu-id="32b89-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32b89-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b89-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="32b89-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="32b89-123">Versão de serviço padrão a ser definida</span><span class="sxs-lookup"><span data-stu-id="32b89-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="32b89-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="32b89-124">-EnableChangeFeed</span></span>
<span data-ttu-id="32b89-125">Habilitar o registro em log do feed de alterações para a conta de armazenamento definida como $true, desabilite a configuração do log de feed definido como $false.</span><span class="sxs-lookup"><span data-stu-id="32b89-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

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

### <span data-ttu-id="32b89-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="32b89-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="32b89-127">Obtém ou define o controle de versão está habilitado se definido como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="32b89-127">Gets or sets versioning is enabled if set to true.</span></span>

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

### <span data-ttu-id="32b89-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b89-128">-ResourceGroupName</span></span>
<span data-ttu-id="32b89-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32b89-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="32b89-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32b89-130">-ResourceId</span></span>
<span data-ttu-id="32b89-131">Insira uma ID de recurso da conta de armazenamento ou uma ID do recurso de propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="32b89-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="32b89-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="32b89-132">-StorageAccount</span></span>
<span data-ttu-id="32b89-133">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="32b89-133">Storage account object</span></span>

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

### <span data-ttu-id="32b89-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="32b89-134">-StorageAccountName</span></span>
<span data-ttu-id="32b89-135">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="32b89-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="32b89-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32b89-136">-Confirm</span></span>
<span data-ttu-id="32b89-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32b89-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b89-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b89-138">-WhatIf</span></span>
<span data-ttu-id="32b89-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32b89-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b89-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32b89-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b89-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b89-141">CommonParameters</span></span>
<span data-ttu-id="32b89-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b89-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b89-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b89-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b89-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32b89-144">INPUTS</span></span>

### <span data-ttu-id="32b89-145">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="32b89-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="32b89-146">System. String</span><span class="sxs-lookup"><span data-stu-id="32b89-146">System.String</span></span>

## <span data-ttu-id="32b89-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32b89-147">OUTPUTS</span></span>

### <span data-ttu-id="32b89-148">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="32b89-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="32b89-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32b89-149">NOTES</span></span>

## <span data-ttu-id="32b89-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32b89-150">RELATED LINKS</span></span>
