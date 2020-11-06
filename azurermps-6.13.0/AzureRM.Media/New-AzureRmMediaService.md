---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 353cccddea39d68c9eefa891e95eb06c6663d173
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428088"
---
# <span data-ttu-id="80c66-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="80c66-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="80c66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80c66-102">SYNOPSIS</span></span>
<span data-ttu-id="80c66-103">Cria um serviço de mídia se o serviço de mídia já existir, todas as suas propriedades serão atualizadas com a entrada fornecida.</span><span class="sxs-lookup"><span data-stu-id="80c66-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80c66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80c66-104">SYNTAX</span></span>

### <span data-ttu-id="80c66-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="80c66-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c66-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="80c66-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80c66-107">DESCRIPTION</span></span>
<span data-ttu-id="80c66-108">O cmdlet **New-AzureRmMediaService** cria um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="80c66-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="80c66-109">Se o serviço de mídia já existir, esse cmdlet atualizará suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="80c66-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="80c66-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80c66-110">EXAMPLES</span></span>

### <span data-ttu-id="80c66-111">Example1: criar um serviço de mídia com apenas a conta de armazenamento principal</span><span class="sxs-lookup"><span data-stu-id="80c66-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="80c66-112">Este exemplo mostra como criar um serviço de mídia para especificar apenas a conta de armazenamento principal.</span><span class="sxs-lookup"><span data-stu-id="80c66-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="80c66-113">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="80c66-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="80c66-114">Exemplo 2: criar um serviço de mídia com vários armazenamentos</span><span class="sxs-lookup"><span data-stu-id="80c66-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="80c66-115">Este exemplo mostra como criar um serviço de mídia com várias contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="80c66-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="80c66-116">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="80c66-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="80c66-117">OS</span><span class="sxs-lookup"><span data-stu-id="80c66-117">PARAMETERS</span></span>

### <span data-ttu-id="80c66-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80c66-118">-AccountName</span></span>
<span data-ttu-id="80c66-119">Especifica o nome do serviço de mídia criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c66-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c66-120">-DefaultProfile</span></span>
<span data-ttu-id="80c66-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="80c66-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-122">-Local</span><span class="sxs-lookup"><span data-stu-id="80c66-122">-Location</span></span>
<span data-ttu-id="80c66-123">Especifica a região em que esse cmdlet cria o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="80c66-123">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c66-124">-ResourceGroupName</span></span>
<span data-ttu-id="80c66-125">Especifica o nome do grupo de recursos ao qual o serviço de mídia está atribuído.</span><span class="sxs-lookup"><span data-stu-id="80c66-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="80c66-126">-StorageAccountId</span></span>
<span data-ttu-id="80c66-127">Especifica a conta de armazenamento associada à conta de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="80c66-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="80c66-128">-StorageAccounts</span></span>
<span data-ttu-id="80c66-129">Especifica uma matriz de contas de armazenamento a serem associadas ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="80c66-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="80c66-130">-Tag</span></span>
<span data-ttu-id="80c66-131">As marcas associadas à conta de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="80c66-131">The tags associated with the media service account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="80c66-132">-Confirm</span></span>
<span data-ttu-id="80c66-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c66-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c66-134">-WhatIf</span></span>
<span data-ttu-id="80c66-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80c66-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c66-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80c66-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c66-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c66-137">CommonParameters</span></span>
<span data-ttu-id="80c66-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c66-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c66-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c66-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c66-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80c66-140">INPUTS</span></span>

### <span data-ttu-id="80c66-141">System. String</span><span class="sxs-lookup"><span data-stu-id="80c66-141">System.String</span></span>

### <span data-ttu-id="80c66-142">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="80c66-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="80c66-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80c66-143">OUTPUTS</span></span>

### <span data-ttu-id="80c66-144">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="80c66-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="80c66-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80c66-145">NOTES</span></span>

## <span data-ttu-id="80c66-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80c66-146">RELATED LINKS</span></span>

[<span data-ttu-id="80c66-147">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="80c66-147">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="80c66-148">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="80c66-148">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="80c66-149">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="80c66-149">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)

