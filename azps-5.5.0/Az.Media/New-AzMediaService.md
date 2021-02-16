---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: a7554468824e85dbd922c0fac874ca9d881c13d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113568"
---
# <span data-ttu-id="9b872-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9b872-101">New-AzMediaService</span></span>

## <span data-ttu-id="9b872-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b872-102">SYNOPSIS</span></span>
<span data-ttu-id="9b872-103">Cria um serviço de mídia se o serviço de mídia já existir, todas as suas propriedades são atualizadas com a entrada fornecida.</span><span class="sxs-lookup"><span data-stu-id="9b872-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="9b872-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b872-104">SYNTAX</span></span>

### <span data-ttu-id="9b872-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="9b872-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b872-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="9b872-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b872-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b872-107">DESCRIPTION</span></span>
<span data-ttu-id="9b872-108">O **cmdlet New-AzMediaService** cria um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="9b872-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="9b872-109">Se o serviço de mídia já existir, esse cmdlet atualizará suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9b872-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="9b872-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9b872-110">EXAMPLES</span></span>

### <span data-ttu-id="9b872-111">Exemplo1: Criar um serviço de mídia apenas com a conta de armazenamento principal</span><span class="sxs-lookup"><span data-stu-id="9b872-111">Example1: Create a media service with the primary storage account only</span></span>
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

<span data-ttu-id="9b872-112">Este exemplo mostra como criar um serviço de mídia especificando apenas a conta de armazenamento principal.</span><span class="sxs-lookup"><span data-stu-id="9b872-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="9b872-113">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9b872-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="9b872-114">Exemplo 2: Criar um serviço de mídia com vários armazenamentos</span><span class="sxs-lookup"><span data-stu-id="9b872-114">Example 2: Create a media service with multiple storage</span></span>
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

<span data-ttu-id="9b872-115">Este exemplo mostra como criar um serviço de mídia com várias contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9b872-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="9b872-116">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9b872-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="9b872-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b872-117">PARAMETERS</span></span>

### <span data-ttu-id="9b872-118">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="9b872-118">-AccountName</span></span>
<span data-ttu-id="9b872-119">Especifica o nome do serviço de mídia que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="9b872-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9b872-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b872-120">-DefaultProfile</span></span>
<span data-ttu-id="9b872-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9b872-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b872-122">-Local</span><span class="sxs-lookup"><span data-stu-id="9b872-122">-Location</span></span>
<span data-ttu-id="9b872-123">Especifica a região em que este cmdlet cria o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="9b872-123">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="9b872-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b872-124">-ResourceGroupName</span></span>
<span data-ttu-id="9b872-125">Especifica o nome do grupo de recursos ao que o serviço de mídia está atribuído.</span><span class="sxs-lookup"><span data-stu-id="9b872-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="9b872-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9b872-126">-StorageAccountId</span></span>
<span data-ttu-id="9b872-127">Especifica a conta de armazenamento associada à conta de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="9b872-127">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="9b872-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="9b872-128">-StorageAccounts</span></span>
<span data-ttu-id="9b872-129">Especifica uma matriz de contas de armazenamento para associar ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="9b872-129">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="9b872-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b872-130">-Tag</span></span>
<span data-ttu-id="9b872-131">As marcas associadas à conta de serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="9b872-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="9b872-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9b872-132">-Confirm</span></span>
<span data-ttu-id="9b872-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b872-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b872-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b872-134">-WhatIf</span></span>
<span data-ttu-id="9b872-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9b872-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b872-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b872-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b872-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b872-137">CommonParameters</span></span>
<span data-ttu-id="9b872-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b872-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b872-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b872-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b872-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="9b872-140">INPUTS</span></span>

### <span data-ttu-id="9b872-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9b872-141">System.String</span></span>

### <span data-ttu-id="9b872-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="9b872-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="9b872-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="9b872-143">OUTPUTS</span></span>

### <span data-ttu-id="9b872-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="9b872-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="9b872-145">Notas</span><span class="sxs-lookup"><span data-stu-id="9b872-145">NOTES</span></span>

## <span data-ttu-id="9b872-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b872-146">RELATED LINKS</span></span>

[<span data-ttu-id="9b872-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9b872-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="9b872-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9b872-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="9b872-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9b872-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


