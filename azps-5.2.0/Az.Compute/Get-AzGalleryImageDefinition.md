---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: c6c689ce2c9ccda71150f221bdea4ae5dd2a20fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258168"
---
# <span data-ttu-id="0bdc4-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="0bdc4-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="0bdc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="0bdc4-103">Obter ou listar definições de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="0bdc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bdc4-104">SYNTAX</span></span>

### <span data-ttu-id="0bdc4-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="0bdc4-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bdc4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0bdc4-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bdc4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bdc4-107">DESCRIPTION</span></span>
<span data-ttu-id="0bdc4-108">Obter ou listar definições de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="0bdc4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bdc4-109">EXAMPLES</span></span>

### <span data-ttu-id="0bdc4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0bdc4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="0bdc4-111">Obter a definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="0bdc4-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0bdc4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="0bdc4-113">Obtenha a definição de imagem da galeria que começa com "imagem".</span><span class="sxs-lookup"><span data-stu-id="0bdc4-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="0bdc4-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0bdc4-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="0bdc4-115">Obtenha as definições de imagem da galeria no gallery1.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="0bdc4-116">OS</span><span class="sxs-lookup"><span data-stu-id="0bdc4-116">PARAMETERS</span></span>

### <span data-ttu-id="0bdc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bdc4-117">-DefaultProfile</span></span>
<span data-ttu-id="0bdc4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bdc4-119">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="0bdc4-119">-GalleryName</span></span>
<span data-ttu-id="0bdc4-120">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="0bdc4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bdc4-121">-Name</span></span>
<span data-ttu-id="0bdc4-122">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0bdc4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bdc4-123">-ResourceGroupName</span></span>
<span data-ttu-id="0bdc4-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="0bdc4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bdc4-125">-ResourceId</span></span>
<span data-ttu-id="0bdc4-126">A ID do recurso da definição de imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="0bdc4-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="0bdc4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bdc4-127">CommonParameters</span></span>
<span data-ttu-id="0bdc4-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bdc4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bdc4-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bdc4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bdc4-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bdc4-130">INPUTS</span></span>

### <span data-ttu-id="0bdc4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0bdc4-131">System.String</span></span>

## <span data-ttu-id="0bdc4-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bdc4-132">OUTPUTS</span></span>

### <span data-ttu-id="0bdc4-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="0bdc4-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="0bdc4-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bdc4-134">NOTES</span></span>

## <span data-ttu-id="0bdc4-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bdc4-135">RELATED LINKS</span></span>
