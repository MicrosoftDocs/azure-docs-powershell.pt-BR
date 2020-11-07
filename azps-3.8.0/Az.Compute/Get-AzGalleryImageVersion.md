---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943688"
---
# <span data-ttu-id="63253-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="63253-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="63253-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63253-102">SYNOPSIS</span></span>
<span data-ttu-id="63253-103">Obter ou listar versões da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="63253-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="63253-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63253-104">SYNTAX</span></span>

### <span data-ttu-id="63253-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="63253-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63253-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="63253-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63253-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63253-107">DESCRIPTION</span></span>
<span data-ttu-id="63253-108">Obter ou listar versões da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="63253-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="63253-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63253-109">EXAMPLES</span></span>

### <span data-ttu-id="63253-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63253-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="63253-111">Obtenha a versão da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="63253-111">Get the gallery image version.</span></span>

### <span data-ttu-id="63253-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="63253-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="63253-113">Obtenha as versões de imagem da galeria que começam com "1".</span><span class="sxs-lookup"><span data-stu-id="63253-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="63253-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="63253-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="63253-115">Obter todas as versões de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="63253-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="63253-116">OS</span><span class="sxs-lookup"><span data-stu-id="63253-116">PARAMETERS</span></span>

### <span data-ttu-id="63253-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63253-117">-DefaultProfile</span></span>
<span data-ttu-id="63253-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63253-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63253-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="63253-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="63253-120">Mostrar status de replicação.</span><span class="sxs-lookup"><span data-stu-id="63253-120">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63253-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="63253-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="63253-122">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="63253-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63253-123">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="63253-123">-GalleryName</span></span>
<span data-ttu-id="63253-124">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="63253-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63253-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="63253-125">-Name</span></span>
<span data-ttu-id="63253-126">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="63253-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="63253-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63253-127">-ResourceGroupName</span></span>
<span data-ttu-id="63253-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="63253-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63253-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63253-129">-ResourceId</span></span>
<span data-ttu-id="63253-130">A ID do recurso da versão da imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="63253-130">The resource ID for the gallery image version</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63253-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63253-131">CommonParameters</span></span>
<span data-ttu-id="63253-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63253-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63253-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63253-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63253-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63253-134">INPUTS</span></span>

### <span data-ttu-id="63253-135">System. String</span><span class="sxs-lookup"><span data-stu-id="63253-135">System.String</span></span>

### <span data-ttu-id="63253-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63253-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63253-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63253-137">OUTPUTS</span></span>

### <span data-ttu-id="63253-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="63253-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="63253-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63253-139">NOTES</span></span>

## <span data-ttu-id="63253-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63253-140">RELATED LINKS</span></span>
