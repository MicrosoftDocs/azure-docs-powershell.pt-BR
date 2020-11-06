---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428568"
---
# <span data-ttu-id="ff022-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="ff022-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="ff022-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff022-102">SYNOPSIS</span></span>
<span data-ttu-id="ff022-103">Obter ou lista galerias.</span><span class="sxs-lookup"><span data-stu-id="ff022-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff022-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff022-104">SYNTAX</span></span>

### <span data-ttu-id="ff022-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff022-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff022-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ff022-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff022-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff022-107">DESCRIPTION</span></span>
<span data-ttu-id="ff022-108">Obter ou lista galerias.</span><span class="sxs-lookup"><span data-stu-id="ff022-108">Get or list galleries.</span></span>

## <span data-ttu-id="ff022-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff022-109">EXAMPLES</span></span>

### <span data-ttu-id="ff022-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ff022-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

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

<span data-ttu-id="ff022-111">Obter a galeria.</span><span class="sxs-lookup"><span data-stu-id="ff022-111">Get the gallery.</span></span>

## <span data-ttu-id="ff022-112">OS</span><span class="sxs-lookup"><span data-stu-id="ff022-112">PARAMETERS</span></span>

### <span data-ttu-id="ff022-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff022-113">-DefaultProfile</span></span>
<span data-ttu-id="ff022-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff022-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff022-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff022-115">-Name</span></span>
<span data-ttu-id="ff022-116">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="ff022-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff022-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff022-117">-ResourceGroupName</span></span>
<span data-ttu-id="ff022-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff022-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff022-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff022-119">-ResourceId</span></span>
<span data-ttu-id="ff022-120">A ID do recurso para a Galeria</span><span class="sxs-lookup"><span data-stu-id="ff022-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="ff022-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff022-121">CommonParameters</span></span>
<span data-ttu-id="ff022-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff022-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff022-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff022-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff022-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff022-124">INPUTS</span></span>

### <span data-ttu-id="ff022-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ff022-125">System.String</span></span>

### <span data-ttu-id="ff022-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="ff022-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="ff022-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff022-127">OUTPUTS</span></span>

### <span data-ttu-id="ff022-128">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="ff022-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="ff022-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff022-129">NOTES</span></span>

## <span data-ttu-id="ff022-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff022-130">RELATED LINKS</span></span>
