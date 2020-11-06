---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428560"
---
# <span data-ttu-id="82b7b-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="82b7b-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="82b7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="82b7b-103">Obter ou listar versões da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="82b7b-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82b7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82b7b-104">SYNTAX</span></span>

### <span data-ttu-id="82b7b-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="82b7b-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82b7b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="82b7b-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b7b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82b7b-107">DESCRIPTION</span></span>
<span data-ttu-id="82b7b-108">Obter ou listar versões da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="82b7b-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="82b7b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82b7b-109">EXAMPLES</span></span>

### <span data-ttu-id="82b7b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="82b7b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="82b7b-111">Obtenha a versão da Galeria de imagens.</span><span class="sxs-lookup"><span data-stu-id="82b7b-111">Get the gallery image version.</span></span>

## <span data-ttu-id="82b7b-112">OS</span><span class="sxs-lookup"><span data-stu-id="82b7b-112">PARAMETERS</span></span>

### <span data-ttu-id="82b7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b7b-113">-DefaultProfile</span></span>
<span data-ttu-id="82b7b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="82b7b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b7b-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="82b7b-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="82b7b-116">Mostrar status de replicação.</span><span class="sxs-lookup"><span data-stu-id="82b7b-116">Show replication status.</span></span>

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

### <span data-ttu-id="82b7b-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="82b7b-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="82b7b-118">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="82b7b-118">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="82b7b-119">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="82b7b-119">-GalleryName</span></span>
<span data-ttu-id="82b7b-120">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="82b7b-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="82b7b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="82b7b-121">-Name</span></span>
<span data-ttu-id="82b7b-122">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="82b7b-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b7b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b7b-123">-ResourceGroupName</span></span>
<span data-ttu-id="82b7b-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="82b7b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="82b7b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82b7b-125">-ResourceId</span></span>
<span data-ttu-id="82b7b-126">A ID do recurso da versão da imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="82b7b-126">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="82b7b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b7b-127">CommonParameters</span></span>
<span data-ttu-id="82b7b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b7b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b7b-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b7b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b7b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82b7b-130">INPUTS</span></span>

### <span data-ttu-id="82b7b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="82b7b-131">System.String</span></span>

### <span data-ttu-id="82b7b-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="82b7b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="82b7b-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82b7b-133">OUTPUTS</span></span>

### <span data-ttu-id="82b7b-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="82b7b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="82b7b-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82b7b-135">NOTES</span></span>

## <span data-ttu-id="82b7b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82b7b-136">RELATED LINKS</span></span>
