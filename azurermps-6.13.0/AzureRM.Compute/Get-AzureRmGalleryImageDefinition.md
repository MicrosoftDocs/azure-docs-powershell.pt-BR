---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428561"
---
# <span data-ttu-id="ce1ca-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ce1ca-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="ce1ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1ca-103">Obter ou listar definições de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="ce1ca-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce1ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce1ca-104">SYNTAX</span></span>

### <span data-ttu-id="ce1ca-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce1ca-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce1ca-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ce1ca-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce1ca-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce1ca-107">DESCRIPTION</span></span>
<span data-ttu-id="ce1ca-108">Obter ou listar definições de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="ce1ca-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="ce1ca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce1ca-109">EXAMPLES</span></span>

### <span data-ttu-id="ce1ca-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce1ca-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="ce1ca-111">Obter a definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="ce1ca-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="ce1ca-112">OS</span><span class="sxs-lookup"><span data-stu-id="ce1ca-112">PARAMETERS</span></span>

### <span data-ttu-id="ce1ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ca-113">-DefaultProfile</span></span>
<span data-ttu-id="ce1ca-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce1ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce1ca-115">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="ce1ca-115">-GalleryName</span></span>
<span data-ttu-id="ce1ca-116">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="ce1ca-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="ce1ca-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce1ca-117">-Name</span></span>
<span data-ttu-id="ce1ca-118">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="ce1ca-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce1ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce1ca-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce1ca-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce1ca-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce1ca-121">-ResourceId</span></span>
<span data-ttu-id="ce1ca-122">A ID do recurso da definição de imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="ce1ca-122">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="ce1ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1ca-123">CommonParameters</span></span>
<span data-ttu-id="ce1ca-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce1ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1ca-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce1ca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1ca-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce1ca-126">INPUTS</span></span>

### <span data-ttu-id="ce1ca-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ce1ca-127">System.String</span></span>

## <span data-ttu-id="ce1ca-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce1ca-128">OUTPUTS</span></span>

### <span data-ttu-id="ce1ca-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="ce1ca-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="ce1ca-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce1ca-130">NOTES</span></span>

## <span data-ttu-id="ce1ca-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce1ca-131">RELATED LINKS</span></span>
