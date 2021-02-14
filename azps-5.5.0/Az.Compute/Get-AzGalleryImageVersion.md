---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116888"
---
# <span data-ttu-id="b50dd-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b50dd-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="b50dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b50dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b50dd-103">Obter ou listar versões de imagem.</span><span class="sxs-lookup"><span data-stu-id="b50dd-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="b50dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b50dd-104">SYNTAX</span></span>

### <span data-ttu-id="b50dd-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b50dd-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b50dd-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b50dd-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b50dd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b50dd-107">DESCRIPTION</span></span>
<span data-ttu-id="b50dd-108">Obter ou listar versões de imagem.</span><span class="sxs-lookup"><span data-stu-id="b50dd-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="b50dd-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b50dd-109">EXAMPLES</span></span>

### <span data-ttu-id="b50dd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b50dd-110">Example 1</span></span>
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

<span data-ttu-id="b50dd-111">Obter a versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="b50dd-111">Get the gallery image version.</span></span>

### <span data-ttu-id="b50dd-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b50dd-112">Example 2</span></span>
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

<span data-ttu-id="b50dd-113">Obter as versões de imagem da galeria que começam com "1".</span><span class="sxs-lookup"><span data-stu-id="b50dd-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="b50dd-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b50dd-114">Example 3</span></span>
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

<span data-ttu-id="b50dd-115">Obter todas as versões de imagens da galeria.</span><span class="sxs-lookup"><span data-stu-id="b50dd-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="b50dd-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b50dd-116">PARAMETERS</span></span>

### <span data-ttu-id="b50dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50dd-117">-DefaultProfile</span></span>
<span data-ttu-id="b50dd-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b50dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50dd-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="b50dd-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="b50dd-120">Mostrar status de replicação.</span><span class="sxs-lookup"><span data-stu-id="b50dd-120">Show replication status.</span></span>

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

### <span data-ttu-id="b50dd-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b50dd-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="b50dd-122">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="b50dd-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b50dd-123">-Nomeda Galeria</span><span class="sxs-lookup"><span data-stu-id="b50dd-123">-GalleryName</span></span>
<span data-ttu-id="b50dd-124">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="b50dd-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="b50dd-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b50dd-125">-Name</span></span>
<span data-ttu-id="b50dd-126">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="b50dd-126">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="b50dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b50dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="b50dd-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b50dd-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="b50dd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b50dd-129">-ResourceId</span></span>
<span data-ttu-id="b50dd-130">A ID do recurso para a versão de imagem da galeria</span><span class="sxs-lookup"><span data-stu-id="b50dd-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="b50dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50dd-131">CommonParameters</span></span>
<span data-ttu-id="b50dd-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b50dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50dd-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b50dd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50dd-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="b50dd-134">INPUTS</span></span>

### <span data-ttu-id="b50dd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b50dd-135">System.String</span></span>

### <span data-ttu-id="b50dd-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b50dd-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b50dd-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="b50dd-137">OUTPUTS</span></span>

### <span data-ttu-id="b50dd-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b50dd-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="b50dd-139">Notas</span><span class="sxs-lookup"><span data-stu-id="b50dd-139">NOTES</span></span>

## <span data-ttu-id="b50dd-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b50dd-140">RELATED LINKS</span></span>
