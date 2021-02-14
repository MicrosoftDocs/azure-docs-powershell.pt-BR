---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111161"
---
# <span data-ttu-id="9f598-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="9f598-101">Get-AzGallery</span></span>

## <span data-ttu-id="9f598-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f598-102">SYNOPSIS</span></span>
<span data-ttu-id="9f598-103">Obter ou listar galerias.</span><span class="sxs-lookup"><span data-stu-id="9f598-103">Get or list galleries.</span></span>

## <span data-ttu-id="9f598-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f598-104">SYNTAX</span></span>

### <span data-ttu-id="9f598-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f598-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f598-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9f598-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f598-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f598-107">DESCRIPTION</span></span>
<span data-ttu-id="9f598-108">Obter ou listar galerias.</span><span class="sxs-lookup"><span data-stu-id="9f598-108">Get or list galleries.</span></span>

## <span data-ttu-id="9f598-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f598-109">EXAMPLES</span></span>

### <span data-ttu-id="9f598-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f598-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="9f598-111">Obter a galeria "galeria1"</span><span class="sxs-lookup"><span data-stu-id="9f598-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="9f598-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9f598-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="9f598-113">Obter todas as galerias no rg1.</span><span class="sxs-lookup"><span data-stu-id="9f598-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="9f598-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9f598-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="9f598-115">Obter todas as galerias em assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f598-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="9f598-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="9f598-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="9f598-117">Obter todas as galerias em assinatura que comecem com "galeria".</span><span class="sxs-lookup"><span data-stu-id="9f598-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="9f598-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f598-118">PARAMETERS</span></span>

### <span data-ttu-id="9f598-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f598-119">-DefaultProfile</span></span>
<span data-ttu-id="9f598-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f598-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f598-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f598-121">-Name</span></span>
<span data-ttu-id="9f598-122">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="9f598-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9f598-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f598-123">-ResourceGroupName</span></span>
<span data-ttu-id="9f598-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f598-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9f598-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f598-125">-ResourceId</span></span>
<span data-ttu-id="9f598-126">A ID do recurso para Galeria</span><span class="sxs-lookup"><span data-stu-id="9f598-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="9f598-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f598-127">CommonParameters</span></span>
<span data-ttu-id="9f598-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f598-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f598-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f598-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f598-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f598-130">INPUTS</span></span>

### <span data-ttu-id="9f598-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9f598-131">System.String</span></span>

## <span data-ttu-id="9f598-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f598-132">OUTPUTS</span></span>

### <span data-ttu-id="9f598-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="9f598-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="9f598-134">Notas</span><span class="sxs-lookup"><span data-stu-id="9f598-134">NOTES</span></span>

## <span data-ttu-id="9f598-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f598-135">RELATED LINKS</span></span>
