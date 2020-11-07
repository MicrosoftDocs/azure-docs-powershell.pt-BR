---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: a7554468824e85dbd922c0fac874ca9d881c13d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944534"
---
# <span data-ttu-id="35ae5-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="35ae5-101">New-AzMediaService</span></span>

## <span data-ttu-id="35ae5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="35ae5-103">Cria um serviço de mídia se o serviço de mídia já existir, todas as suas propriedades serão atualizadas com a entrada fornecida.</span><span class="sxs-lookup"><span data-stu-id="35ae5-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="35ae5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35ae5-104">SYNTAX</span></span>

### <span data-ttu-id="35ae5-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="35ae5-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35ae5-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="35ae5-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ae5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35ae5-107">DESCRIPTION</span></span>
<span data-ttu-id="35ae5-108">O cmdlet **New-AzMediaService** cria um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="35ae5-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="35ae5-109">Se o serviço de mídia já existir, esse cmdlet atualizará suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="35ae5-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="35ae5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35ae5-110">EXAMPLES</span></span>

### <span data-ttu-id="35ae5-111">Example1: criar um serviço de mídia com apenas a conta de armazenamento principal</span><span class="sxs-lookup"><span data-stu-id="35ae5-111">Example1: Create a media service with the primary storage account only</span></span>
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
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="35ae5-112">Este exemplo mostra como criar um serviço de mídia para especificar apenas a conta de armazenamento principal.</span><span class="sxs-lookup"><span data-stu-id="35ae5-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="35ae5-113">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="35ae5-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="35ae5-114">Exemplo 2: criar um serviço de mídia com vários armazenamentos</span><span class="sxs-lookup"><span data-stu-id="35ae5-114">Example 2: Create a media service with multiple storage</span></span>
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
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="35ae5-115">Este exemplo mostra como criar um serviço de mídia com várias contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="35ae5-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="35ae5-116">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="35ae5-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="35ae5-117">OS</span><span class="sxs-lookup"><span data-stu-id="35ae5-117">PARAMETERS</span></span>

### <span data-ttu-id="35ae5-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="35ae5-118">-AccountName</span></span>
<span data-ttu-id="35ae5-119">Especifica o nome do serviço de mídia criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ae5-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="35ae5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ae5-120">-DefaultProfile</span></span>
<span data-ttu-id="35ae5-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="35ae5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35ae5-122">-Local</span><span class="sxs-lookup"><span data-stu-id="35ae5-122">-Location</span></span>
<span data-ttu-id="35ae5-123">Especifica a região em que esse cmdlet cria o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="35ae5-123">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="35ae5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ae5-124">-ResourceGroupName</span></span>
<span data-ttu-id="35ae5-125">Especifica o nome do grupo de recursos ao qual o serviço de mídia está atribuído.</span><span class="sxs-lookup"><span data-stu-id="35ae5-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="35ae5-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="35ae5-126">-StorageAccountId</span></span>
<span data-ttu-id="35ae5-127">Especifica a conta de armazenamento associada à conta de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="35ae5-127">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="35ae5-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="35ae5-128">-StorageAccounts</span></span>
<span data-ttu-id="35ae5-129">Especifica uma matriz de contas de armazenamento a serem associadas ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="35ae5-129">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="35ae5-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="35ae5-130">-Tag</span></span>
<span data-ttu-id="35ae5-131">As marcas associadas à conta de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="35ae5-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="35ae5-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35ae5-132">-Confirm</span></span>
<span data-ttu-id="35ae5-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ae5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ae5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ae5-134">-WhatIf</span></span>
<span data-ttu-id="35ae5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35ae5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ae5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35ae5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ae5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ae5-137">CommonParameters</span></span>
<span data-ttu-id="35ae5-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ae5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ae5-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ae5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ae5-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35ae5-140">INPUTS</span></span>

### <span data-ttu-id="35ae5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="35ae5-141">System.String</span></span>

### <span data-ttu-id="35ae5-142">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="35ae5-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="35ae5-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35ae5-143">OUTPUTS</span></span>

### <span data-ttu-id="35ae5-144">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="35ae5-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="35ae5-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35ae5-145">NOTES</span></span>

## <span data-ttu-id="35ae5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35ae5-146">RELATED LINKS</span></span>

[<span data-ttu-id="35ae5-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="35ae5-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="35ae5-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="35ae5-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="35ae5-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="35ae5-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


