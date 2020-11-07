---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: cd09679117a964cc28e24d28f4097d511304a9a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771223"
---
# <span data-ttu-id="2639a-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2639a-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="2639a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2639a-102">SYNOPSIS</span></span>
<span data-ttu-id="2639a-103">Obter ou listar versões da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="2639a-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="2639a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2639a-104">SYNTAX</span></span>

### <span data-ttu-id="2639a-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="2639a-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2639a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2639a-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2639a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2639a-107">DESCRIPTION</span></span>
<span data-ttu-id="2639a-108">Obter ou listar versões da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="2639a-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="2639a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2639a-109">EXAMPLES</span></span>

### <span data-ttu-id="2639a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2639a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1 -GalleryImageVersionName 1.0.0

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

<span data-ttu-id="2639a-111">Obtenha a versão da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="2639a-111">Get the gallery image version.</span></span>

### <span data-ttu-id="2639a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2639a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1 -GalleryImageVersionName 1*

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

<span data-ttu-id="2639a-113">Obtenha as versões de imagem da galeria que começam com "1".</span><span class="sxs-lookup"><span data-stu-id="2639a-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="2639a-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2639a-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1

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

<span data-ttu-id="2639a-115">Obter todas as versões de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="2639a-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="2639a-116">OS</span><span class="sxs-lookup"><span data-stu-id="2639a-116">PARAMETERS</span></span>

### <span data-ttu-id="2639a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2639a-117">-DefaultProfile</span></span>
<span data-ttu-id="2639a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2639a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2639a-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="2639a-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="2639a-120">Mostrar status de replicação.</span><span class="sxs-lookup"><span data-stu-id="2639a-120">Show replication status.</span></span>

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

### <span data-ttu-id="2639a-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2639a-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="2639a-122">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="2639a-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="2639a-123">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="2639a-123">-GalleryName</span></span>
<span data-ttu-id="2639a-124">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="2639a-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="2639a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2639a-125">-Name</span></span>
<span data-ttu-id="2639a-126">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="2639a-126">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="2639a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2639a-127">-ResourceGroupName</span></span>
<span data-ttu-id="2639a-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2639a-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="2639a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2639a-129">-ResourceId</span></span>
<span data-ttu-id="2639a-130">A ID do recurso da versão da imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="2639a-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="2639a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2639a-131">CommonParameters</span></span>
<span data-ttu-id="2639a-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2639a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2639a-133">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2639a-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2639a-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2639a-134">INPUTS</span></span>

### <span data-ttu-id="2639a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2639a-135">System.String</span></span>

### <span data-ttu-id="2639a-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2639a-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2639a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2639a-137">OUTPUTS</span></span>

### <span data-ttu-id="2639a-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2639a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="2639a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2639a-139">NOTES</span></span>

## <span data-ttu-id="2639a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2639a-140">RELATED LINKS</span></span>
