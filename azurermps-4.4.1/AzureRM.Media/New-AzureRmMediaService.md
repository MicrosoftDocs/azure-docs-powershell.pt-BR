---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 86f1667c1383f226d47afed2a842af6386dad81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609642"
---
# <span data-ttu-id="e1907-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="e1907-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="e1907-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1907-102">SYNOPSIS</span></span>
<span data-ttu-id="e1907-103">Cria um serviço de mídia se o serviço de mídia já existir, todas as suas propriedades serão atualizadas com a entrada fornecida.</span><span class="sxs-lookup"><span data-stu-id="e1907-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1907-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1907-104">SYNTAX</span></span>

### <span data-ttu-id="e1907-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="e1907-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1907-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="e1907-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1907-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1907-107">DESCRIPTION</span></span>
<span data-ttu-id="e1907-108">O cmdlet **New-AzureRmMediaService** cria um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1907-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="e1907-109">Se o serviço de mídia já existir, esse cmdlet atualizará suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e1907-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="e1907-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1907-110">EXAMPLES</span></span>

### <span data-ttu-id="e1907-111">Example1: criar um serviço de mídia com apenas a conta de armazenamento principal</span><span class="sxs-lookup"><span data-stu-id="e1907-111">Example1: Create a media service with the primary storage account only</span></span>
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

<span data-ttu-id="e1907-112">Este exemplo mostra como criar um serviço de mídia para especificar apenas a conta de armazenamento principal.</span><span class="sxs-lookup"><span data-stu-id="e1907-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="e1907-113">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e1907-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="e1907-114">Exemplo 2: criar um serviço de mídia com vários armazenamentos</span><span class="sxs-lookup"><span data-stu-id="e1907-114">Example 2: Create a media service with multiple storage</span></span>
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

<span data-ttu-id="e1907-115">Este exemplo mostra como criar um serviço de mídia com várias contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e1907-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="e1907-116">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e1907-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="e1907-117">OS</span><span class="sxs-lookup"><span data-stu-id="e1907-117">PARAMETERS</span></span>

### <span data-ttu-id="e1907-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e1907-118">-AccountName</span></span>
<span data-ttu-id="e1907-119">Especifica o nome do serviço de mídia criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1907-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e1907-120">-Local</span><span class="sxs-lookup"><span data-stu-id="e1907-120">-Location</span></span>
<span data-ttu-id="e1907-121">Especifica a região em que esse cmdlet cria o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1907-121">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="e1907-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1907-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1907-123">Especifica o nome do grupo de recursos ao qual o serviço de mídia está atribuído.</span><span class="sxs-lookup"><span data-stu-id="e1907-123">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="e1907-124">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e1907-124">-StorageAccountId</span></span>
<span data-ttu-id="e1907-125">Especifica a conta de armazenamento associada à conta de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1907-125">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="e1907-126">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e1907-126">-StorageAccounts</span></span>
<span data-ttu-id="e1907-127">Especifica uma matriz de contas de armazenamento a serem associadas ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1907-127">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="e1907-128">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e1907-128">-Tags</span></span>
<span data-ttu-id="e1907-129">Especifica as marcas do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1907-129">Specifies tags for the media service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1907-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1907-130">-Confirm</span></span>
<span data-ttu-id="e1907-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1907-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1907-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1907-132">-WhatIf</span></span>
<span data-ttu-id="e1907-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1907-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1907-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1907-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1907-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1907-135">-DefaultProfile</span></span>
<span data-ttu-id="e1907-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1907-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1907-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1907-137">CommonParameters</span></span>
<span data-ttu-id="e1907-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1907-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1907-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1907-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1907-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1907-140">INPUTS</span></span>

## <span data-ttu-id="e1907-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1907-141">OUTPUTS</span></span>

### <span data-ttu-id="e1907-142">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="e1907-142">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="e1907-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1907-143">NOTES</span></span>

## <span data-ttu-id="e1907-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1907-144">RELATED LINKS</span></span>

[<span data-ttu-id="e1907-145">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="e1907-145">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="e1907-146">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="e1907-146">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="e1907-147">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="e1907-147">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


